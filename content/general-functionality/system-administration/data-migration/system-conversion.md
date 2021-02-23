---
title: "System Conversion"
date: 2020-02-27T21:31:21.718Z
url: "general-functionality/system-administration/data-migration/system-conversion.html"
author: Alan Quandt
version: 54
id: 12BfxOgwAp35VUX7a-OHkI2NB6mjuLK1ocGaJMTL0_jE
source: https://drive.google.com/open?id=12BfxOgwAp35VUX7a-OHkI2NB6mjuLK1ocGaJMTL0_jE
menu:
    main:
        name: "System Conversion"
        identifier: "12BfxOgwAp35VUX7a-OHkI2NB6mjuLK1ocGaJMTL0_jE"
        parent: "1uT8WLYj42KO6Q0YgNCoxLH8RikMH_C6IBQjUmhLSaWU"
        weight: 5080
---
{{% system-name %}} Conversion is a tool for converting legacy databases into a variety of components:

* Non-discrete Summary Documents
* Discrete Observations
* Discrete Respirator Fit Test Data
* Discrete Pulmonary Function Test (PFT) Data
* Discrete Audiograms
* Encounters

There are a few stages involved in the conversion:

* MIE obtains a snapshot of the Legacy Data in a MySQL dump or CSV format from the client — [Data Migration File Format Standard](data-migration-file-format-standard.html) <strong><em>(see this page for data file requirements).</em></strong>
* Legacy Data is loaded to development MySQL database using MIE's pysqlimport tool.
* Generate <em>Data Mapping Spreadsheet</em> (Google Spreadsheet exportable to Excel/CSV for client use).
* Perform data mapping and define WebChart components.
* Define metadata for WebChart components.
* Export data mapping and convert data using MIE's legacy data conversion tool.

This guide focuses on the Data Mapping Spreadsheet and how to define components to create in WebChart.

The Data Mapping Spreadsheet is a Google Spreadsheet generated from the legacy database. The following worksheets appear in the spreadsheet:

* Data Mapping: a full list of every table and every field along with details about the data type, contents, and usage. The Data Mapping worksheet contains columns for mapping legacy fields to WebChart components and defining discrete data.
* Module Summary: used in conjunction with Data Mapping to define various metadata for the summary documents and discrete components. Examples of metadata include patient ID, user ID, doc type, location, and many other pieces of data that would apply to all of the items in a summary document or discrete component.



### Data Mapping Worksheet

* Columns A-C, R-Y: details about legacy database.
    * <strong>A. Legacy DB</strong>: The name of the legacy database.
    * <strong>B. Legacy Table</strong>: The name of the legacy table.
    * <strong>C. Legacy Column</strong>: The name of the legacy column.
    * <strong>S. DB Field Type</strong>: The MySQL data type that was created by analyzing the legacy data using MIE's pysqlimport tool or mysqldump data from the legacy database.
    * <strong>T. DB Null</strong>: An indicator for whether or not the column has NULL values.
    * <strong>U. DB Key</strong>: The names of keys in which the legacy column is included.
    * <strong>V. DB Default</strong>: Default value from the legacy system if mysqldump was provided.
    * <strong>W. DB Count</strong>: The number of rows that have data in a given column.
    * <strong>X. DB Usage</strong>: Percentage of times the column is used (V/X).
    * <strong>Y. DB Total Rows</strong>: Total number of rows in a legacy table.
    * <strong>Z. Sample Data</strong>: (Optionally) sample data from the legacy data sorted by cardinality  text if the column name is not sufficient.
* <strong>Column D: Comments</strong>: Take notes here; this column is not used by the MIE legacy data conversion tool.
* <strong>Column E: Description</strong>: Description of the legacy field, used for Documents as an alternate
* <strong>Column F: Module</strong>: Handle used to refer to a WebChart component to be created. This must match a line in Module Summary to be created.
* <strong>Column G: Order</strong>: Defines the order of component items.



### Module Summary Worksheet



#### Columns

* <strong>Column A: Module</strong>: Name of module used in Data Mapping.
* <strong>Column B: Component</strong>: Name of WebChart component. e.g. Summary Document, Observation, PFT, Fit Test, Audiogram.
* <strong>Columns C, D</strong>: Order of processing for module, component.
* <strong>Columns E-G</strong>: Reserved for developer use.
* <strong>Columns J-P</strong>: Define component metadata. See next section for documentation of options.



#### Metadata options

These are a set of functions that can dynamically define component metadata per row or have a static value defined. Whether these functions are used depends on the component.

**TODO:** Insert table here.

* get_pat_id -
* get_user_id -
* get_interface_name -
* get_ext_id - Apply an external ID to a component.
* get_subject -
* get_location -
* get_encounter_id - Link component to an Encounter.



#### Updating

When entering data into the Google Spreadsheet, a menu item is available (WebChart Conversion>Update Module) to assist with completing the needed Module Summary lines. Click this at any point to update the module lines in this tab.

![](../../../external_files/ae911aa02ddbe9d93e45ab0a1a3f95e2.png)



## Migration Mapping

Components require two parts to complete. First are the **Data Mapping** rows that share the same value for Column E, **Module**. Second, the component needs a matching line (Column A, **Module**) in the **Module Summary** that defines the rest of the metadata.



### Encounters

An encounter documents a visit with a patient, and is also known as a patient visit. An encounter is a template of specific items to be addressed, in part or completely, during a patient appointment. This is a tool used for recording information collected during a patient appointment and, in turn, the data collected will be stored and also incorporated in the final desired outcome: the visit report/note.

All aspects of the visit are covered in the encounter, such as the appointment type and time (apt_id), and when the patient checked in and out (pat_location table). Medications, allergies, and related documents are included or linked to an encounter with the encounters_link table.

Data Mapping:

* Column F, Module: <em>My Encounter Module</em>
* Column K, Encounter Options
    * visit_type
    * primary_diagnosis
    * diagnosis2
    * diagnosis3
    * diagnosis4
    * service_code
    * priority
    * serv_date
    * discharge_date
    * accident_date
    * accident_code
    * accident_location
    * injury_code
    * comment (can be defined for multiple fields)
    * chief_complaint
    * stage
    * due_date

Module Summary:

* Column A, Module: <em>My Encounter Module</em>
* Column B, Component: <strong>Encounter</strong>
* Column C, Module Order: Order module is processed. Encounters are processed before any other components, so this is the order among encounters.
* Columns J-P: metadata fields
    * get_pat_id
    * get_user_id
    * get_interface_name
    * get_ext_id
    * get_location



#### Example

The following table **encounters** is used for the Encounter example.

![](../../../external_files/a005bc896fed96daaed0f1c1965bb653.png)

Notice:

* The <strong>Data Mapping</strong> tab is selected.
* The table <strong>encounters</strong> and it's columns have been located.
* <strong>Sample Encounter</strong> has been entered for the <strong>Module</strong> column for each row of the table.

Based on the *Encounter Options* listed above, determine the mapping to legacy columns and complete the column **Encounter Options**.

![](../../../external_files/ab76d739f594fadc45e6336851efc030.png)

Now that the **Data Mapping** tab has been filled, update the **Module Summary**.

![](../../../external_files/21423f078b847828956731c87add1ac8.png)

Click on the **Module Summary** tab to see a row automatically created for the **Sample Encounter** module.

![](../../../external_files/d0f08e933bcc9fa9a0c272c445f4d75d.png)

Notice:

* The <strong>Module Summary</strong> tab is selected.
* The module row has minimal information and will need to be completed.

The completed row:

![](../../../external_files/49e69d718534a2e8676659b724b048a5.png)

Notice:

* The "Module Summary" tab is still selected.
* To create an Encounter, "Component" enter "ENCOUNTER" or "encounter". Case does not matter.
* The supported metadata fields have been defined.
    * get_pat_id - Looks for the patient in WebChart.
        * partition=MIE - Look in the MIE partition for the patient.
        * db_cols=mrnumber - In the "encounters" table, the column "mrnumber" matches a Medical Record Number.
    * get_user_id - Looks for the Performing Doctor of the encounter.
        * default=0 - Use a default ID of 0 (no user).
    * get_interface_name - An identifier for the source of this data.
        * default=sample_conversion - Use sample_conversion for the interface name.
    * get_ext_id - Define an external identifier (identifies the individual record in the source data).
        * db_cols=id - In the "encounters" table, the column "id" is used for an external identifier.
    * get_location - Define the location where the encounter took place.
        * default=OFFICE - Use OFFICE for the location code for all encounters created.

The example Encounters (Visits>Encounters) were crafted to be created for the patient William Hart.

![](../../../external_files/0f672bc161c0305fcfee19442fb64ef3.png)

The newly generated Encounters:

![](../../../external_files/67bbbb6ca9c6dfa9063aa0d00f312ce2.png)



### Summary Documents

A Document is defined as a piece of electronic matter that that serves as an official record in WebChart. A Document has a "document ID" and has the following properties:

* Persistence
* Stewardship
* Potential for authentication
* Context
* Human readability

Documents store a wide variety of information pertaining to patient charts in WebChart. This includes patient photographs, insurance cards, physician or nurse notes, imaging studies, past medical histories, physician tasks for a patient, CCDs and CDAs, email correspondence about a patient, injections, and many other forms of data. Aside from encounters, incidents, observations, and other types of discrete chart data, documents represent the primary mode of storing information on a chart. The doc_type column identifies the category of the document, such as those previously mentioned.

There are several doc_types that are included as part of the default installation of WebChart, but they may be added and deleted to customize the system using the DocType Editor in WebChart. The storage_type identifies what kind of file is represented by the document. Examples of storage types include plain text documents, HTML files, PDF files, JPEG images, injections, audiograms, PFTs, and many others. Storage types are stored in the storage_types table. Each document in the documents table has a foreign key called storage_type, but these storage types may not be edited or customized in WebChart. Using the doc_type and storage_type of a document in the documents table, one can tell what sort of document it is and see how the document is stored and what other tables may be related to the document.

Data Mapping:

* Column E, Module: My Document Module
* Column D, Description: Used for left column value
* Column F, Order: Order item appears on document
* Column G, Document Options: Additional options for the document.
    * service_date: The document's date of service.
    * skiprowifempty: Do not display the element if no value is stored.
* Column H, Element Type: Controls the display of an item on a document.
    * KeyValue: Displays the description and database value in 2 columns.
    * KeyDate: Same as KeyValue except this is for dates. This is planned to be merged into KeyValue.
    * Narrative: An extended area at the bottom of the document suitable for displaying extended text entries such as paragraphs. All fields specified will be combined into this area.
* Column I, Element Format: Display this field in a custom format. KeyDates accept formats like "%Y/%m/%d"[[1]](https://miewiki.med-web.com/wiki/index.php/WebChart_Conversion#cite_note-0), while KeyValues accept formats like "Hello {0}, {1}!"[[2]](https://miewiki.med-web.com/wiki/index.php/WebChart_Conversion#cite_note-1). String formatting uses an index (starting at 0) to refer to the Legacy Columns. 0 is the first, 1 is the second, and so on.

Module Summary:

* Column A, Module: <em>My Document Module</em>
* Column B, Component: <strong>Summary Document</strong>
* Column C, Module Order: Order module is processed.
* Column H, Doc Type: Document Type code.
* Column Q, Template: Used to provide a custom template. <strong>Not currently in use.</strong>
* Columns J-P: Metadata fields.
    * get_pat_id
    * get_user_id
    * get_subject
    * get_location
    * get_ext_id
    * get_interface_name



#### Example

The following table **documents** is used for the Summary Documents example.

![](../../../external_files/fc87a814baafa78e5d4dfc408f0fde02.png)

Notice:

* The <strong>Data Mapping</strong> tab is selected.
* The table <strong>documents</strong> and it's columns have been located.
* <strong>Sample Summary Document</strong> has been entered for the <strong>Module</strong> column for each row of the table.

Based on the *Document Options* and *Element Types* listed above, determine the mapping to legacy columns and complete the columns. The **Description** and **Order** has also been filled to demonstrate their effect on the created document.

![](../../../external_files/5a08877fbb84479d6c404d36bba93d57.png)

Now that the **Data Mapping** tab has been filled, update the **Module Summary**.

![](../../../external_files/79c11c68a49bdf6dbf1371b824c7cbcd.png)

Click on the **Module Summary** tab to see a row automatically created for the **Sample Summary Document** module.

![](../../../external_files/c0aeb223531366fe72b085ae503aba3f.png)

Notice:

* The <strong>Module Summary</strong> tab is selected.
* The module row has minimal information and will need to be completed.

The completed row:

![](../../../external_files/c3bbbd372149a6dd792a1886c719affe.png)

Notice:

* The <strong>Module Summary</strong> tab is <em>still</em> selected.
* To create a Summary Document, enter "SUMMARY DOCUMENT" or "summary document" in "Component". Case does not matter.
* The supported metadata fields have been defined.
    * Doc Type
        * WCDOCNOT - Create a Doctor Note document type.
    * get_pat_id - Looks for the patient in WebChart.
        * partition=MIE - Look in the MIE partition for the patient.
        * db_cols=mrnumber - In the "documents" table, the column "mrnumber" matches a Medical Record Number.
    * get_user_id - Defines the author of the document.
        * default=0 - Use a default ID of 0 (no user).
    * get_interface_name - An identifier for the source of this data.
        * default=sample_conversion - Use sample_conversion for the interface name.
    * get_ext_id - Define an external identifier (identifies the individual record in the source data).
        * db_cols=id - In the "documents" table, the column "id" is used for an external identifier.
    * get_location - Define the location where the document was created.
        * default=OFFICE - Use OFFICE for the location code for all documents created.

The example Summary Documents (Document Summary) were crafted to be created for the patient William Hart.

![](../../../external_files/323127dd3ac9977c978372a823c7afb5.png)

The newly generated Summary Documents:

![](../../../external_files/daadf788aa84592fe5b914d96d8611c4.png)

Here is an example Summary Document. Descriptions appear on the left column, while database values appear on the right. At the bottom containing comments is the *narrative*. Both sections are sorted according to the order specified in the **Data Mapping**.

![](../../../external_files/f0a5e1ddc5455e87cf3a62638ce37896.png)



### Observations

An observation in WebChart is a means of storing repeated historic data, such as vital signs, lab results, measurements, and other discrete data. Any discrete data can be stored as an observation, but some is stored on other custom tables, such as audiograms, demographics information, injections, medications, prescriptions, and allergies. The data in these other custom tables may also be stored as observations. A number of related tables define, store, and group observations in WebChart so that they can be collected and displayed in a patient's chart, including: observation_codes, obs_forms, observation_ranges, observations_current, translate, observation_codes_list, and lab_requests.

The observations table stores discreet data related to an observation code (obs_code). The data defines where an observation appears in a WebChart system by relating the observation code to a patient (pat_id), the user who entered the observation (observer_id), when it was recorded (observed_datetime) and when it was revised (revision_number). Details in the observations table can override details stored on the observation_codes table, such as range, name, and units (obs_range, obs_name, obs_units).

Observations are linked to users through the user ID (user_id). The users table stores information on providers and WebChart users.

The translate table is used throughout WebChart for translations of all kinds, but is used specifically with observations to map an interface's own observation code to an obs_code in WebChart.

Multiple observations can be created for a single module. Each observation is a module **component**, and uses the **handle**, **obs_name**, or **obs_code** to match the Data Mapping to Module Summary.

Data Mapping:

* Column E, Module: <em>My Observations Module</em>
* Column K, Observation Options: Reserved for future use. Likely to combine L-N and also store handle here.
    * handle - Used to match Data Mapping row to Module Summary row. Use this when creating multiple observations with the same code in a single module.
    * observed - Specify the legacy column that contains the observed datetime.
* Column L, get_obs_name: The source of the observation code name.
    * name - Provide the obs_name.
    * code - Provide the obs_code.
    * description - Description column is the obs_name.
    * value - <strong>Future use</strong>, the field value is the obs_name.
* Column M, get_obs_result: Reserved for future use. When using value with get_obs_name, this will decide the obs_result. If blank, use field value as obs_result.
* Column N, get_obs_test_comments: A list of fields to combine and use as the observation comment.

Module Summary (one line per Observation):

* Column A, Module: <em>My Observations Module</em>
* Column B, Component: <strong>Observation:</strong> handle, obs_name, or obs_code
* Column C, Module Order: Order module is processed.
* Column D, Component Order: Order component/observation is processed.
* Columns J-P: Metadata fields.
    * get_pat_id
    * get_user_id
    * get_ext_id
    * get_interface_name



#### Example

The following table **observations** is used for the Observations example.

![](../../../external_files/182ad10ed0eea70a0a3aa89e27f50aa5.png)

Notice:

* The <strong>Data Mapping</strong> tab is selected.
* The table <strong>observations</strong> and it's columns have been located.
* <strong>Sample Observations</strong> has been entered for the Module column for each row of the table.

Based on the Observation Options, get_obs_name, and get_obs_test_comments options listed above, determine the mapping to legacy columns and complete the columns.

![](../../../external_files/bf3f79909052c0b58fb0980cbec583c1.png)

Three observations have been identified here. All are using the value of "test_date" for the observed date. They are also using the values of "comments1-4" for the observation comments.

* obs_name BODY HEIGHT - The observation code is specified by name.
* obs_code 2053 - The observation code is listed directly.
* obs_name BMI - The observation code is specified by name. An optional handle of "body mass index" has been applied (to be used on the Module Summary).

Now that the **Data Mapping** tab has been filled, update the **Module Summary**.

![](../../../external_files/5ec3991bfe9d3da02a26ff7edcd22566.png)

Click on the **Module Summary** tab to see a row automatically created for each **Sample Observations** component.

![](../../../external_files/016268210bb6a3f444cfa5aa03e766fd.png)

Notice:

* The <strong>Module Summary</strong> tab is selected.
* The module rows have minimal information and will need to be completed.

The completed rows:

![](../../../external_files/1cf92feb86b38b7fce986519edb28d2f.png)

Notice:

* The Module Summary tab is still selected.
* To create an Observation, this must match "OBSERVATION:" or "observation:". Case does not matter. Following this must come the handle, obs_code, or obs_name specified in the Data Mapping tab.
* The supported metadata fields have been defined.
    * get_pat_id - Looks for the patient in WebChart.
        * partition=MIE - Look in the MIE partition for the patient.
        * db_cols=mrnumber - In the "observations" table, the column "mrnumber" matches a Medical Record Number.
    * get_user_id - Looks for the Entered By user.
        * default=0 - Use a default ID of 0 (no user).
    * get_interface_name - An identifier for the source of this data.
        * default=sample_conversion - Use sample_conversion for the interface name.
    * get_ext_id - Define an external identifier (identifies the individual record in the source data).
        * db_cols=id - In the "observations" table, the column "id" is used for an external identifier.

The example Observations (Medical Record>Observations/Flowsheets) were crafted to be created for the patient William Hart.

![](../../../external_files/c8b7410bd6b50044ca643ff7993584b8.png)

To see the results:

* Select a date range that is limited to the results you need.
* For the example, which contains vitals, select the <strong>Vitals</strong> flowsheet. Depending on the observations you select, you may need to view them on a custom or different flowsheet.  ![](../../../external_files/91d062cada2a45ae4ae5cbb8f27bd37a.png)

The newly generated Observations:

![](../../../external_files/3d2aa7dd7247131d0880f8a2b4ee758c.png)



### Respirator Fit Test

Respirator fit details are stored on a custom table. The patient_respiratordetails table is a record of all respirator masks a patient/employee is tested on for use. This table records fit tests for a single patient and links to the patients table through the patient ID (pat_id).

Data Mapping:

* Column E, Module: <em>My Fit Test Module</em>
* Column F, Order: Order comment is combined.
* Column Q, Fit Test Options
    * MaskType
    * Size
    * LastFitTestDate
    * LastFitExpires
    * LastFitPassFail
    * LastFitFinalFitFactor
    * comment (can be defined for multiple fields)

Module Summary:

* Column A, Module: <em>My Fit Test Module</em>
* Column B, Component: <strong>Fit Test</strong>
* Column C, Module Order: Order module is processed.
* Columns J-P: Metadata fields.
    * get_pat_id



#### Example

The following table **fit_test** is used for the Respirator Fit Test example.

![](../../../external_files/3dca2a631e96a19ed19a9c7095460b8e.png)

Notice:

* The <strong>Data Mapping</strong> tab is selected.
* The table <strong>fit_test</strong> and its columns have been located.
* <strong>Sample Fit Test</strong> has been entered for the <strong>Module</strong> column for each row of the table.

Based on the *Fit Test Options* listed above, determine the mapping to legacy columns and complete the columns. The **Order** has also been filled to demonstrate its effect on the comments.

![](../../../external_files/e04646aec64d979482c41c2b153c39a3.png)

Now that the **Data Mapping** tab has been filled, update the **Module Summary**.

![](../../../external_files/036e01c8135b4898516cb95b526a9bd2.png)

Click on the **Module Summary** tab to see a row automatically created for the **Sample Fit Test** module.

![](../../../external_files/2c41cc92153aa90f4069f61cc120e3a2.png)

Notice:

* The <strong>Module Summary</strong> tab is selected.
* The module row has minimal information and will need to be completed.

The completed row:

![](../../../external_files/c05ef02f19f44fa4176d4c268050b8ae.png)

Notice:

* The <strong>Module Summary</strong> tab is <em>still</em> selected.
* To create a Respirator Fit Test, enter "FIT TEST" or "fit test" in "Component". Case does not matter.
* The supported metadata fields have been defined.
    * get_pat_id - Looks for the patient in WebChart.
        * partition=MIE - Look in the MIE partition for the patient.
        * db_cols=mrnumber - In the "fit_test" table, the column "mrnumber" matches a Medical Record Number.

The example Respirator Fit Tests (Test Results>Respirator Info) were crafted to be created for the patient William Hart.

![](../../../external_files/549c21173691bab404f620321a94af09.png)

The newly generated Respirator Fit Tests:

![](../../../external_files/0e98df61f54a162cc297647764438f81.png)



### Pulmonary Function Tests

Pulmonary function test (PFT) data is stored in a custom table. The pft table records details for PFT/spirometry for a patient. PFTs are linked to a patient through the documents table, using the foreign key doc_id, which contains the patient ID (pat_id). Additional information on the patient's height and weight is recorded on the pft table to compare to predicted results. Revisions to PFTs are recorded on the pft_revisions table.

Data Mapping:

* Column E, Module: <em>My PFT Module</em>
* Column O, PFT Options
    * test_datetime
    * calibration_date
    * maneuver_datetime
    * test_age
    * test_height
    * test_weight
    * calibration_result
    * prediction_method
    * spirometer
    * test_reason
    * temperature
    * humidity
    * pressure
    * session_effort
    * position
    * fvc
    * fvc_predicted
    * fvc_abnormal
    * fev1
    * fev1_predicted
    * fev1_abnormal
    * fev1_fvc
    * fev1_fvc_predicted
    * fev1_fvc_abnormal
    * fef25_75
    * fef25_75_predicted
    * fef25_75_abnormal
    * pef
    * pef_predicted
    * pef_abnormal
    * manual
    * peak_1
    * peak_2
    * peak_3
    * fev6
    * fef25
    * fef50
    * fef75
    * fvc_lln
    * fev1_lln
    * fev6_lln
    * fev1_fvc_lln
    * fef25_75_lln
    * pef_lln
    * expiratory_time
    * pef_time
    * reference_correction
    * interpretation
    * btps_factor
    * curve
    * summary
    * best_maneuver
    * comment (can be defined for multiple fields)

Module Summary:

* Column A, Module: <em>My PFT Module</em>
* Column B, Component: <strong>PFT</strong>
* Column C, Module Order: Order module is processed.
* Columns J-P: Metadata fields.
    * get_pat_id
    * get_user_id
    * get_interface_name
    * get_ext_id
    * get_subject
    * get_location



#### Example

The following table **pft** is used for the PFT example.

![](../../../external_files/33318a60cd1003ac9e496513631b4415.png)

Notice:

* The <strong>Data Mapping</strong> tab is selected.
* The table <strong>pft</strong> and it's columns have been located.
* <strong>Sample PFT</strong> has been entered for the <strong>Module</strong> column for each row of the table.

Based on the PFT Options listed above, determine the mapping to legacy columns and complete the column **PFT Options**.

![](../../../external_files/1209572cb2e39b9bd988481f5f745f55.png)

Now that the **Data Mapping** tab has been filled, update the **Module Summary**.

![](../../../external_files/39364926ddfbd4158366591aacdedb2c.png)

Click on the **Module Summary** tab to see a row automatically created for the **Sample PFT** module.

![](../../../external_files/8ef581716a78b4c6af35af594c3f2fb8.png)

Notice:

* The <strong>Module Summary</strong> tab is selected.
* The module row has minimal information and will need to be completed.

The completed row:



Notice:

* The <strong>Module Summary</strong> tab is <em>still</em> selected.
* To create a Pulmonary Function Test, enter "PFT" or "pft" in "Component". Case does not matter.
* The supported metadata fields have been defined.
    * get_pat_id - Looks for the patient in WebChart.
        * partition=MIE - Look in the MIE partition for the patient.
        * db_cols=mrnumber - In the "pft" table, the column "mrnumber" matches a Medical Record Number.
    * get_user_id - Looks for the Performing User of the Pulmonary Function Test.
        * default=0 - Use a default ID of 0 (no user).
    * get_interface_name - An identifier for the source of this data.
        * default=sample_conversion - Use sample_conversion for the interface name.
    * get_ext_id - Define an external identifier (identifies the individual record in the source data).
        * db_cols=id - In the "pft" table, the column "id" is used for an external identifier.
    * get_location - Define the location where the test took place.
        * default=OFFICE - Use OFFICE for the location code for all tests created.

The example PFTs (Test Results>PFT) were crafted to be created for the patient William Hart.

![](../../../external_files/8c99faa7353b6efaccacf18938566616.png)

The newly generated PFTs:

![](../../../external_files/3cf9217cf19e74ba6a1717aee7639c22.png)



### Audiometric Data

The audio table stores discrete data for occupational audiogram tests. Audio tests are linked to a patient through the documents table, using the foreign key doc_id, which contains the patient ID (pat_id). Like many of the other testing-related tables, the documents generated by data from the audio table contain a number of specific tests and baselines aggregated into a single document or view. Revisions to audio data are recorded on the audio_revisions table.

Data Mapping:

* Column E, Module: <em>My Audiogram Module</em>
* Column O, Audiogram Options
    * test_datetime
    * left05
    * left1
    * left2
    * left3
    * left4
    * left6
    * left8
    * right05
    * right1
    * right2
    * right3
    * right4
    * right6
    * right8
    * manual=[left05 - left8 or right05 - right8] (can be defined for multiple fields)
    * hcp
    * left_sts=[value of ‘Yes'] (can be defined for multiple fields)
    * right_sts=[value of ‘Yes'] (can be defined for multiple fields)
    * osha_recordable=[value of ‘Yes'] (can be defined for multiple fields)
    * left_baseline=[value of ‘Yes'] (can be defined for multiple fields)
    * right_baseline=[value of ‘Yes'] (can be defined for multiple fields)
    * test_reason
    * comment (can be defined for multiple fields)
    * outside provider
    * outside_location
    * audio_model
    * audio_serial
    * calibration_date

Module Summary:

* Column A, Module: <em>My Audiogram Module</em>
* Column B, Component: <strong>Audiogram</strong>
* Column C, Module Order: Order module is processed.
* Columns J-P: Metadata fields.
    * get_pat_id
    * get_user_id
    * get_interface_name
    * get_ext_id
    * get_subject
    * get_location



#### Example

The following table **audio** is used for the Audiograms example.

![](../../../external_files/ba5d2c6b0e0eed8763ce84581ad53828.png)

Notice:

* The <strong>Data Mapping</strong> tab is selected.
* The table <strong>audio</strong> and it's columns have been located.
* <strong>Sample Audiogram</strong> has been entered for the <strong>Module</strong> column for each row of the table.

Based on the *Audio Options* listed above, determine the mapping to legacy columns and complete the columns. The **Order** has also been filled to demonstrate its effect on the comments.

![](../../../external_files/221568b3bd1353c51f33e415a8d5f905.png)

Now that the **Data Mapping** tab has been filled, update the **Module Summary**.

![](../../../external_files/57de71f41cb445d45899331e9d51e919.png)

Click on the **Module Summary** tab to see a row automatically created for the **Sample Audiogram** module.

![](../../../external_files/e53826de4e5b937a897b942c81e7ccc8.png)

Notice:

* The <strong>Module Summary</strong> tab is selected.
* The module row has minimal information and will need to be completed.

The completed row:

![](../../../external_files/928c87caa26246145926fed1246f63e5.png)

Notice:

* The <strong>Module Summary</strong> tab is <em>still</em> selected.
* To create an Audiogram, enter "AUDIOGRAM" or "audiogram" in "Component". Case does not matter.
* The supported metadata fields have been defined.
    * get_pat_id - Looks for the patient in WebChart.
        * partition=MIE - Look in the MIE partition for the patient.
        * db_cols=mrnumber - In the "audio" table, the column "mrnumber" matches a Medical Record Number.
    * get_user_id - Looks for the Performing User of the test.
        * default=0 - Use a default ID of 0 (no user).
    * get_interface_name - An identifier for the source of this data.
        * default=sample_conversion - Use sample_conversion for the interface name.
    * get_ext_id - Define an external identifier (identifies the individual record in the source data).
        * db_cols=id - In the "audio" table, the column "id" is used for an external identifier.
    * get_subject - Define a subject for the Audiogram document.
        * default=Sample Audiogram - Use "Sample Audiogram" as the subject for all tests created.
    * get_location - Define the location where the test took place.
        * default=OFFICE - Use OFFICE for the location code for all tests created.

The example Audiograms (Test Results>Audio) were crafted to be created for the patient William Hart.

![](../../../external_files/31af0739fb815ba549ff8882214ed8a4.png)

The newly generated Audiograms:

![](../../../external_files/e3210e9c167edea294b9c71373fb3a06.png)



## References

* [↑](https://miewiki.med-web.com/wiki/index.php/WebChart_Conversion#cite_ref-0)[https://docs.python.org/2/library/datetime.html#strftime-and-strptime-behavior](https://docs.python.org/2/library/datetime.html#strftime-and-strptime-behavior)
* [↑](https://miewiki.med-web.com/wiki/index.php/WebChart_Conversion#cite_ref-1)[https://docs.python.org/2/library/string.html#format-string-syntax](https://docs.python.org/2/library/string.html#format-string-syntax)



## Related Pages

* [Data Migration Overview](data-migration-overview.html)
* [Data Requirements](data-migration-file-format-standard.html)
---
title: "Review Session - System Configuration"
date: 2020-02-27T21:24:23.063Z
url: "rapid-deployment/review-sessions/review-session-system-configuration.html"
author: Alan Quandt
version: 30
id: 1_A3KojfmcZzSPe0Pb6anfAlAaUidbATZLddF5NyQjrM
source: https://drive.google.com/open?id=1_A3KojfmcZzSPe0Pb6anfAlAaUidbATZLddF5NyQjrM
menu:
    main:
        name: "Review Session - System Configuration"
        identifier: "1_A3KojfmcZzSPe0Pb6anfAlAaUidbATZLddF5NyQjrM"
        parent: "1Ws2Vhysc7vAiQXeVws2C92oE2Y10i-BYITqCos59cWM"
        weight: 5990
---
## Agenda

* <strong>System Configuration Demonstration</strong>
* <strong>System Configurations</strong>
    * <strong>Corporate Branding</strong>
    * <strong>Add/Update Locations</strong>
    * <strong>Add Users</strong>
        * <strong>Set Relationships</strong>
        * <strong>Provider Setup</strong>
            * <strong>Provider Signature Image</strong>
    * <strong>Chart Types</strong>
    * <strong>Chart Tabs</strong>
    * <strong>Document Types</strong>
    * <strong>Load Employer Organizations (if needed)</strong>
    * <strong>Provider Management (if needed)</strong>
    * <strong>CPT Codes (if needed)</strong>
        * <strong>Picklists</strong>
        * <strong>Modifiers</strong>
    * <strong>Fee Schedules (if needed)</strong>
    * <strong>Insurance Plans (if needed)</strong>
        * <strong>Precertifications</strong>
    * <strong>Cron/Scheduled Jobs</strong>
    * <strong>My Settings</strong>
* <strong>Resources</strong>

## Overview

System configurations are any necessary arrangements or modifications for automated scheduled jobs, business rules (e.g., triggers for email notifications of appointment reminders, immunization reminders, surveillance appointments, etc.), as well as for the standard, out-of-the-box features and functionality. Examples include, but are not limited to, clinical decision support, or scripted rules, standard email templates, questionnaires, office visit templates/encounters, and Word templates. All billable, or additional configuration requests, will be scoped, quoted, and reviewed with the client for authorization, prior to completion.

## System Configurations

To begin addressing the requirements for effective use of the {{% system-name %}} system, navigate to the **Administrator Welcome** section of the **Quick View**, and click the [Admin Get Started link](https://system/?f=layout&s=pat&module=MASTER&name=AdministratorPortlets&tabmodule=+). Here, users are presented with various areas of the system that require initial setup and consideration for configuration.

![](../../external_files/cd9886becf6b512352ed9dc55faa4d3f.png)

![](../../external_files/26c40ac20a6ba29755e9792b3b9db575.png)

### Corporate Branding

From the **Corporate Branding** section, clients may browse to local files of their required logo, for both document letterheads and the system/portal logo(s). Click **Upload** after the appropriate files have been selected, and the system will store the files and display them, accordingly.

![](../../external_files/762537fba8147fb0b8796a7936763718.png)

### Add/Update Locations

Adding and updating locations can be done using the **Update Office Location** section. Clients click the [here](https://system/?f=chart&s=leditor&opp=Edit&oldcode=OFFICE) link to edit the primary location of the business. Once this is updated, simply click the **Modify** button, and the page will refresh the **Locations Manager**, where additional locations can be added, as needed. This editor may also be accessed by navigating to the **Control Panel** and selecting the [Locations Manager tab](https://system/?f=chart&s=leditor&tabmodule=admin&tabselect=Locations+Manager).

![](../../external_files/0d0a63ed23f4d0204187f1af647c54cd.png)

![](../../external_files/a8c41703fdcb187aa9d4a3a03b2b1c06.png)

Though all fields are not necessary, it is best practice to be as detailed as possible. Default required fields are:

* Code
* Description
* Address 1
* City, State, Zip
* Country and Time Zone
* Phone/Fax Number(s)
* Outside Location (No)
* Active (Yes)

Once the primary location has been updated, additional internal or external locations may be added, as needed. To add a new location, simply click the [Add Location link](https://system/?f=chart&s=leditor&tabmodule=admin&tabselect=Locations+Manager&opp=Add) in the upper-right corner of the page.

### Add Users

Users and providers utilizing the {{% system-name %}} system can be added manually, much like how locations are added. The manual method, however, is typically used in WebChart systems. In Enterprise Health systems, the workflow tends to *use charts* for every patient and user. In these cases, the Enterprise Health system may already be set to create a user when a chart is registered manually (or via an HR interface), by way of the *Enable PUR Routine* system setting, where the correct relationships can then be established between the chart and user, for portal functionality and other modules, as needed. If the *Enable PUR Routine* system setting is enabled, users would never add additional users manually, using the steps below. Users would need registered as a *chart* in the system first, then their user profile (that gets autocreated via this enabled system setting functionality) may be edited and updated from the [Access Control tab](https://system/?f=admin&t=security&tabmodule=admin&tabselect=Access+Control) of the **Control Panel**. From here, after locating the user, simply click the **Edit** link in the *Options* column, and update all necessary information.

Though there are several methods for adding a new user manually, the simplest is to navigate to the [Quick View](https://system/?func=omniscope) sidemenu. Within the **Administrator Welcome** portlet, there is an [Admin Get Started link](https://system/?f=layout&s=pat&module=MASTER&name=AdministratorPortlets&tabmodule=+) available. After clicking the link, the **Add User** section will be available, where the [here](https://system/?f=admin&s=pat&t=security&opp=auser) hyperlink can be used to begin manually entering a new user.

![](../../external_files/e4500264b4e91c21b28a04aefcb12613.png)

Enter all of the necessary information, as it relates to the user profile being created.

![](../../external_files/1d094147d5c3572e8a1e2ed2c9aa3548.png)

{{% info %}}

Every user in the system must have an associated chart in order to access the portal.

{{% /info %}}


#### Set Relationships

Relationships can be established between charts/users within the {{% system-name %}} system. This feature is typically used for linking supervisors to employees, but there are many possible relationships that could be defined, as needed. Relationships are typically automated through an HR interface; however, to manually set a relationship, the client may use either the **Demographics** chart tab or [Access Control](https://system/?f=admin&t=security&tabmodule=admin&tabselect=Access+Control). From the **Edit User** screen, click the **Edit Patients Linked to User** in the upper-right of the page.

{{% info %}}

In this context, the term *Patients* refers to any available chart in the {{% system-name %}} system, including employee charts.

{{% /info %}}


![](../../external_files/51765597cb458074c1ca5357ebc4d0af.png)
The **Patients Linked to User** page will load. Begin typing the last name of the patient to be linked to the user, and select the name from the autocomplete. In order to gain access to the portal, the patient and user accounts require the role of **No More Clipboard User**. A supervisor should be linked with the **Supervisor** role.

![](../../external_files/9ef1ee8806bc77c4d833a41762fc5c90.png)

#### Provider Setup

Setting up providers in the {{% system-name %}} system is not much different than adding a standard user. However, if the provider intends to prescribe medication, there are additional requirements needed, such as the provider's NPI and DEA, along with the completed [verification](https://docs.google.com/document/d/1CofebAnz02InLwE8PxHVRFBfvRbzoSjBajFEk9RjaJ0) documentation. Again, if the system is set up to *use charts*, then a provider chart must be created first, which will then create the user profile for the provider.

##### Provider Signature Image

In order to provide a "wet" signature on documentation, each provider will need to perform a signature capture to load into the system. This signature capture image displays on visit encounter notes, Word templates, and prescriptions. Using the verification form, above, providers should sign their name with a fine-point, felt-tip black pen, and a Deployment Consultant will then load in the signature images.

### Chart Types

Chart Types are an important concept in {{% system-name %}} . Chart Types are used to differentiate between *types* of records in the system, allowing for different chart tabs, as needed. These should only be managed by a Deployment Consultant. To view chart types, navigate to the **Chart Types** tab in the Control Panel.

![](../../external_files/31bf258eece778e8f7ab9def64c6669b.png)

### Chart Tabs

Chart tabs, too, are very important in the {{% system-name %}} system. Chart tabs hold the various contents of a chart type, or specific record. One aspect of chart tabs is to designate the types of documents to be available or used from a given chart tab. Though their color can be modified, and they can be added, removed, or renamed, as needed, they should only be managed by a Deployment Consultant. To view the default chart tabs, navigate to the **Chart Tabs** tab in the Control Panel.

![](../../external_files/9cedeaf862c28030f440075cfa027d0c.png)

### Document Types

Document types are a foundational element of the {{% system-name %}} system. Document types establish the type of document, so that {{% system-name %}} understands what to do with the content, or data. Each document type gets mapped so that specific documents can display in one or more designated areas, or chart tabs. These are set up by default and should only be managed by the Deployment Consultant, from the [Document Types tab](https://system/?f=chart&s=dteditor&t=Document+Types&tabmodule=admin&tabselect=Document+Types) of the Control Panel, if necessary.

![](../../external_files/30efbbf0407821593a67c091ae34bd30.png)

### Load Employer Organizations

Depending on the needs of the business, Employer Organizations can be added and set up to provide access to any portal(s). Each location would be set up as a separate Employer Organization, if separate portals are required. These may be added by clients from the [Employer Organizations sidemenu](https://system/?f=layout&module=EO&name=Maintenance&tabmodule=+), as needed. Additionally, if clients are interested in the Industrial Hygiene module, Employer Organizations will be used for tracking and monitoring needs, by location. They allow clients to track orders, referrals, and due list items by location, as well.

### Provider Management

The ability to add a Provider Organization is a feature designed to assist with provider management and to establish, or build provider directories. The provider directory is accessible when creating an order, where it pulls the provider name, address, and phone number onto the order form. This allows referring by provider. Provider Organizations may be added by clients from the [Provider Management sidemenu](https://system/?f=layout&module=MASTER&name=EPM_Maintenance&tabmodule=+).

![](../../external_files/38b435ff4eb800a4a7adc0c1fbcc9a7f.png)

### CPT Codes

To assist with streamlining billing and charges, a CPT editor is available for managing CPT codes, picklists, and modifiers. To access the editor, navigate to the [CPT Codes tab](https://system/?f=encounter&s=cpt_manage&tabmodule=admin&t=CPT+Codes&tabmodule=admin&tabselect=CPT+Codes) of the **Control Panel**.

![](../../external_files/be75ffe0b2ee1bcb8a46474301192959.png)

To begin adding CPT codes and their associated descriptions to the {{% system-name %}} system, simply click the [Add CPT code link](https://system/?f=encounter&s=cpt_manage&tabmodule=admin&tabmodule=admin&tabselect=CPT+Codes&opp=add_cpt), in the upper-right corner of the page.

![](../../external_files/5333a613be571205601530b3e1b7065b.png)

Duplicate CPT codes cannot be added to the system. An error message will appear, if attempted.

#### Picklists

Once all CPT codes and descriptions have been entered, picklists can be created. Picklists provide a means to limit the number of available CPT codes by encounter type, or what's more is the ability to group CPT codes according to their function (e.g., Immunization CPT codes can be grouped into an individual picklist). Depending on the business needs, *all* picklists can be shown in the Billing and Charges section of encounters, by default; or certain picklists can be set to display in any encounter, as needed.

![](../../external_files/4a5da9d5e4d8fd1d3a4420eb21f14bfa.png)

To begin building picklists, click the [Add Picklist link](https://system/?f=encounter&s=cpt_manage&tabmodule=admin&tabmodule=admin&tabselect=CPT+Codes&view=picklist&opp=add_list) from the CPT Codes editor. This will open the CPT Picklist editor. Enter the name of the picklist in the **Name** field (must be unique). This field is limited to 30 characters. Next, enter the CPT codes needed to display within this picklist. The order in which they are entered is the way in which they display. When finished, click the **Save** button. Alternatively, clicking the **Save & Alphabetize** button will change the way the CPT codes display within the picklist, making them display alphabetically by description, rather than in the order in which they were entered.

{{% tip %}}

Additional codes may be added to the picklist, anytime. Simply click the **Edit** link in the *Options* column, to reopen the picklist and add additional CPT codes.

{{% /tip %}}


#### Modifiers

Modifiers can also be managed from the CPT Codes chart tab of the Control Panel. To edit or update the modifiers list, simply click the [Manage Modifiers link](https://system/?f=encounter&s=cpt_manage&tabmodule=admin&tabmodule=admin&tabselect=CPT+Codes&view=modifier) in the upper-right corner. This allows the modifier picklist to be managed, controlling what is seen for descriptions and selections. Also, clients with an established billing interface will be able to send CPT codes and modifiers to their PM system, as needed.

Modifiers display in the **Billing and Charges** section of encounters, after a CPT code has been added. Modifiers are labeled **M1**, **M2**, **M3**, and **M4** to signify the order of the modifiers going onto a claim. When a modifier button (i.e., M1, M2, etc.) is selected, a pop-up window will appear, where users can select a modifier to attach to the CPT code. After selecting the appropriate modifier, click **Ok**.

### Fee Schedules

Fee schedules are used to manage pricing for provided services, dependent upon a specified insurance plan and the billing code(s) submitted. In order to utilize fee schedules, CPT codes and picklists must be previously entered into the system. Fee schedules cannot be managed without the proper security permissions, including those needed to add or change fee schedules in insurance plans. Ensure the appropriate users have the proper security role with **Manage Fee Schedule** and **Manage Insurance Plans** set to *Yes*; or simply customize the security settings of a designated user, as needed. Once set, begin managing fee schedules by navigating to the [Fee Schedule](https://system/?f=admin&s=fee_schedule&tabmodule=admin&tabselect=Fee+Schedule) tab of the **Control Panel**.

### Insurance Plans

Adding and updating insurance to a chart is quick and easy with {{% system-name %}} . While in the individual's chart, navigate to the **Admin** chart tab, and select **Demographics** from the menu. Scroll to the bottom of the page, to the **Insurance Summary** section. To begin entering insurance information, click the **Add Insurance** link. The page will refresh and display the *Add Insurance Policy* screen, where the insurance policy and pre-certification information may be added to the patient's chart.

![](../../external_files/dd78e3cc4c243897476ecceeaf0c0c1e.png).

![](../../external_files/c0fad081eb2569cc161656ffba398865.png)

When adding an insurance plan to a chart, it is important the insurance plan is available within {{% system-name %}} . To view and manage available insurance plans within the system, navigate to the [Insurance Plans tab](https://system/?f=chart&s=insplan&tabmodule=admin&t=Insurance+Plans&tabmodule=admin&tabselect=Insurance+Plans) of the **Control Panel**. Here, administrators may add and update available insurance plans, as needed. The plans that are added will be available for selection from the *Insurance Plan* autocomplete, found when adding a policy to the patient's chart.

#### Pre-Certifications

When adding an insurance policy to a chart, the ability to enter precertification details is available, as well. For example, a patient needing physical therapy may be precertified for 10 visits, spanning October through December. This can be documented in the chart when adding or editing the insurance in the Demographics chart tab.

If there are any precertification details entered in for a patient's insurance, the specified precertification information will appear in the Checkin module, as well as when the patient is being checked in. This information also displays when the insurance name is hovered over in the appointment details in the Scheduler.

### Cron/Scheduled Jobs

As a means to automate varying types of system maintenance and necessary workflows, {{% system-name %}} often has recurring scheduled, or cron, jobs that are set to run periodically, on set dates, times, or intervals. It is important that any necessary scheduled/cron jobs are established and set up, prior to any Go-Live dates. Speak with your Deployment Consultant for more information on established cron jobs and how they are used and customized.

### My Settings

Users have the ability to manage specific settings for themselves, for others, or system-wide, depending on their specific security permissions. Users may navigate to [My Settings](https://system/?f=admin&tabmodule=admin&tabselect=My+Settings) in the **Control Panel**, to begin editing these options. For information on each of the preferences, check out the [My Settings](../../general-functionality/system-administration/security/my-settings.html) and [Security Role Settings](../../general-functionality/system-administration/security/security-role-settings.html) help documentation.

![](../../external_files/d1c96d43a0e13dc251d54993679643fe.png)

Some of the most commonly changed user preferences are:

* <strong>WebChart</strong>:
    * <strong>User Interface</strong>:
        * <strong>Default Location</strong> - This sets the user's default location.
        * <strong>Use Popups</strong> - This setting determines, when clicking a link or tab, if a new window will open (Yes) or the user will be taken away from the current screen (No).
        * <strong>Default Page</strong> - Select a sidemenu option as the landing page, upon login (e.g., Default to the Quick View or E-Chart page).
    * <strong>User Searching Default</strong>:
        * <strong>Search By</strong> - To set the default search option, select either Name, MR#, DOB, or SSN, depending on the user's preference for chart lookups. This is usually set to Name by default.
    * <strong>International Settings</strong>:
        * <strong>Language</strong> - To specify a language for translations, begin typing the language name in the field. Contact the Deployment Consultant for information on making the system available in another language.
        * <strong>English Translations on Hover</strong> - For multilingual systems, selecting <em>Show</em> will display English translations when hovering over translated items.
        * <strong>Date Format</strong> - The system default is MM-DD-YYYY. Changing the default will refresh any date (i.e., dates of birth, document dates, revision dates, etc.) with the selected format. The separator for dates is standardized to use the hyphen ( - ).
        * <strong>Preferred Unit System</strong> - Regardless of the selection, users can still enter observations and vitals with either unit system. This preference sets dropdowns and selections to the specified unit system.
* <strong>E-Chart</strong>
    * <strong>Faxing</strong>:
        * <strong>Default CoverSheet</strong> - Select the default fax coversheet. The user can always select a different coversheet from the fax module, if necessary.
    * <strong>Defaults</strong>:
        * <strong>Number of Recent Patients</strong> - Pick the preferred number of patients to display in the recent patient list. This defaults to twenty (20).
        * <strong>Starting Folder</strong> - This preference sets the default chart tab when going into a chart. Select the preferred starting folder (chart tab).
        * <strong>Print Definition</strong> - Determines the default print definition when printing or faxing from Print Chart links.
    * <strong>Esign</strong>:
        * <strong>Number of Documents in Multi-Sign</strong> - Defaulted to 20, users may designate the number of documents pulled up for review when performing a Multi-Review from the E-Sign Pending queue. Choose from increments of 10.
    * <strong>Encounters</strong>:
        * <strong>Default Visit Type</strong> - This preference sets the default visit type when clicking Add Encounter links.
* <strong>Scheduler</strong>
    * <strong>Defaults</strong>:
        * <strong>Duration</strong> - Changes the appointment increments found in the Scheduler.
        * <strong>Start Time</strong> - Use this option to specify the preferred start time for all schedules.
        * <strong>End Time</strong> - Use this option to specify the preferred end time for all schedules.
* <strong>EMR</strong>:
    * <strong>Billing</strong>:
        * <strong>CPT Picklist</strong> - When the system is set up to use CPT codes, this user preference allows users to select a default CPT picklist to display.
* <strong>Orders</strong>:
    * <strong>Defaults</strong>:
        * <strong>Ordering Physician</strong> - Begin typing the first or last name of the preferred default ordering physician. Select the appropriate name from the autocomplete. The selected physician will default to the Ordering Physician field in order requests. The autocomplete pulls from the Physicians department and shows active and login-disabled users, in case there are ordering physicians that do not log into the system.
        * <strong>Location</strong> - Choose the preferred default location for order requests. When adding an order, the default location is triggered by this setting.
        * <strong>Default Order Set</strong> - Select the preferred default Order Set name. This specifies the Order Set that will automatically display when the user clicks the Orders tab to add an order. This is particularly helpful for users entering specific orders, regularly.
        * <strong>Performing Facility</strong> - Systems configured to capture Facility on order requests can specify a preferred default with this setting preference.

## Resources

### Help Documentation

* [Locations Manager Tab](../../general-functionality/system-configuration/locations-manager-tab.html)
* [Adding a Department](../../general-functionality/system-configuration/managing-departments.html)
* [Access Control - Adding/Deleting/Editing Users](../../general-functionality/system-administration/system-controls/access-control-adding-deleting-editing-users.html)
* [Access Control - Quick-Add Multiple Active Users](../../general-functionality/system-administration/system-controls/access-control-quick-add-multiple-active-users.html)
* [Reset Users Password](../../general-functionality/system-administration/system-controls/reset-user-passwords.html)
* [Chart Types Editor](../../general-functionality/system-configuration/chart-types-editor.html)
* [Chart Tab](../../general-functionality/system-configuration/chart-tabs.html)
* [Document Type Tab](../../general-functionality/system-configuration/document-type-tab.html)
* [Provider Organization Setup](../../general-functionality/system-administration/system-controls/provider-organization-setup.html)
* [Provider Organization - Adding Users to a PO](../../general-functionality/system-administration/system-controls/adding-users-to-a-provider-organization.html)
* [CPT Code Editor and Picklists](https://docs.google.com/document/d/17lF5jX7q3_oBclS7j9Y5bnpEScivaFnrSwrgQT-0yj8)
* [Fee Schedules](../../general-functionality/system-configuration/fee-schedules.html)
* [Insurance Summary - Demographics Tab](../../general-functionality/e-chart/insurance-summary-in-demographics-tab.html)
* [Insurance Eligibility Tab](../../general-functionality/e-chart/insurance-eligibility-tab.html)
* [My Settings](../../general-functionality/system-administration/security/my-settings.html)
* [Locations Management](../../general-functionality/system-configuration/locations-management.html)
* [System Files Management](../../general-functionality/system-configuration/system-files-management.html)



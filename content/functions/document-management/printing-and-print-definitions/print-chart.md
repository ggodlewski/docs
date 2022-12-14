---
title: "Print Chart"
date: "2020-03-09T17:46:39.608Z"
url: "functions/document-management/printing-and-print-definitions/print-chart.html"
version: 43
id: "10iTI1XYCr4psVflBlwJHnxnPKKcb3I64Yrq6LviXvD8"
source: "https://drive.google.com/open?id=10iTI1XYCr4psVflBlwJHnxnPKKcb3I64Yrq6LviXvD8"
menu:
    main:
        name: "Print Chart"
        identifier: "10iTI1XYCr4psVflBlwJHnxnPKKcb3I64Yrq6LviXvD8"
        parent: "1NHBPyY_YvI92JSil-rc3O0Kpu5qYLkdKWZTNjlzQpNY"
        weight: 770
---
Within every chart, there are several quick links available. One of these quick links is the **Print Chart** link, which allows users to fax or print pre-established or configured print definitions from the Scheduler, the Appointments chart tab, or from within the individual's E-Chart. In other words, using the Print Chart link provides users a way to print or fax predefined groupings of documents, forms, layouts, or the like, so that any specific packets of information, or stored documents, may easily be provided via fax, or else printed and provided to a performing facility or a patient, as needed. Print definitions can include individual documents or certain forms, multiple-page packets, or even chart information, such as a medication summary or a list of immunizations.



The print definitions used for the Print Chart functionality can be set up using the [Print Definition editor](https://system/?f=chart&s=printdefedit&tabmodule=admin&tabselect=Print+Definitions) of the **Control Panel**. Here, users with the appropriate security permissions may define the necessary print definitions and group the various types of documents, forms, and/or chart information needed for intake workflows, scheduled appointments, specific procedures, etc. These print definitions, can then be used to reduce costs and streamline workflows and communication, all by way of reducing unnecessary printing and simplifying the processes involved with potentially necessary printing.



For more information on how print definitions can be configured, see the [Print Definitions](print-definitions.html) help documentation.

## Print Chart from E-Chart 

After navigating to a specific chart from the [E-Chart module](https://system/?f=chart), users will find various places with the **Print Chart** link available. Clicking any of these Print Chart links will allow users to select and render a specific print definition, as needed.



![](print-chart.images/image7.png)



Once clicked, the Print Chart dialog window will open. There are three sections to consider, with various fields and options available in each. Review the information below, and use the Print Chart dialog window, accordingly.



![](print-chart.images/image9.png)



**Print Definition**: The Print Definition drop-down lists the print definitions programmed from the Print Definition editor of the Control Panel. Any print definitions restricted from the user will not be displayed in the drop-down selector. The appropriate print definition must be selected when printing or faxing.

**Definition Alert**: This field will appear when a selected print definition has been configured with an alert. Be sure to review any alerts that may appear when selecting a print definition.

**Comment**: The Comment field can be used to add a comment to a fax coversheet, or when printing, the comment will be stored with the history of the print job details. However, when using a Records Release print definition, the Comment field must be used to provide a reason for the Records Release.

**Range Start Date**: This is an optional field. Users may provide a start date/time range filter of the documents included in the selected print definitions.

**Range End Date**: This is an optional field. Users may provide an end date/time range filter of the documents included in the selected print definitions.



![](print-chart.images/image8.png)



**Print without headers**: This option is particularly useful when printing Word documents, forms, sketches, and the like, and it is only available to users with the Allow Printing Without Headers security permission set to Yes. When selected, no header information will be included on the printout, meaning the Doc ID, Author, Revised By, Document Type, DOS, Location, Revised Date, and Signed By information will not be displayed on the printed document. Users lacking the security permission will not see the *Print without headers*option, and all printed/faxed documents will include the patient summary header.



![](print-chart.images/image11.png)



{{% note %}}

When the **Print without headers** option is selected, another option will be made available–**Print Only Without Headers**. Selecting the Print Only Without Headers option will override the document type settings, removing *all* headers, when printing. This option is most useful for exporting PDFs for interface use.

{{% /note %}}


**Print one document per page**: This option allows users to print each document of the print definition on a separate page. This is particularly helpful when printing text entry notes, which tend to run together on a page.

**Print documents that have been Locked**: Some print definitions may have locked documents associated with them. When the user has the necessary security permission and this option is selected, the print definition will include the locked document(s) when printing/faxing.

**Print only documents that have NOT been printed**: Selecting this option will ensure only those documents not included previously will be rendered from the print definition when used again. This will reduce waste by printing only those things that have not been printed or rendered before.

**Use legacy print formatting**: By default, the Enterprise Health system prints documents using WebKit formatting, which is to say formatting designed with indentations, bulletting, and specific parsing for the document structure. Alternatively, legacy print formatting simply renders a generic html document (no indentations, bullets, etc.) for printing.



![](https://lh3.googleusercontent.com/SM960Ok3AoHeHjWMfiuPexJC_sBn2iuIXqoHUiMTyo_zkmtY5PCew_xRKnrjR1tEIHQ0xJc1n35RX4xGXdF2cLpEu1nB58kwWZpvL8tT1144wkRZe3Ml9IRKAjSgGRBPEeGaOaUjytbnVi1CTA)



Legacy printing is possible when the *Use legacy print formatting* option is available (i.e., the Use Webkit system setting is enabled) and selected.



![](print-chart.images/image2.png)



{{% tip %}}

When the Use WebKit system setting is enabled, printed html documents will have a cleaner, formatted appearance. If the *Use legacy print formatting* option is left unchecked, html documents will print using WebKit formatting, by default.

{{% /tip %}}


**Send To/Create New Batch**: The Send To section of the Print Chart dialog window allows users to choose how the selected print definition is to be handled. In other words, users may use the same dialog window to send the print definition to the printer, to the fax machine, through secure email, or if the documents being rendered are not being added to an existing batch, a new batch can be created. If an existing batch is being added to, simply select the **Add To** radio button and proceed. This will add the document(s) of the print definition into the pending batch selected. Otherwise, select the *Printer*, *Fax*, *Secure Email*, or *Create New Batch* radio button to proceed. If a new batch is needed for the print definition, for example, simply select the *Create New Batch* radio button and proceed by adding any necessary batch comment at the top of the dialog window and clicking the **Create Batch** button at the bottom. The print definition will then be housed in a batch until faxed/printed. When simply printing or faxing a print definition outside of a batch, users may skip this section and continue by clicking either the **Print** or **Fax** button, accordingly.

For more detailed information on general faxing and printing, see our [Printing Documents](printing-documents.html) or [Faxing Documents](../../fax-manager/faxing-documents.html) help documentation.

### Print Chart from Appointments Chart Tab 

As noted, the Print Chart functionality is available from various locations within the Enterprise Health system. In addition to the Summary chart tab quick links and the portlet sharing the same name, the Print Chart link can be found in the **Appointments** chart tab, found under the **Admin** parent chart tab, when in an individual's chart.



![](print-chart.images/image1.png)



Once in the Appointments chart tab, locate the appointment for which documents need printed, and click the **Print Chart** link found in the *Options* column.



![](print-chart.images/image4.png)



Once clicked, the Print Chart dialog window will open. Following the same instructions outlined in the  section of this document, users will notice only one difference when accessing the Print Chart functionality from the Appointments chart tab–the **Use Appointment Type Print Definition If Exists** option.



![](print-chart.images/image3.png)



**Use Appointment Type Print Definition If Exists**: This option, when selected, will render the print definition specific to the selected appointment type. In other words, print definitions associated in the configuration of a specific appointment type will be rendered when this option is selected. When an appointment type is configured with a print definition and this option is checked, any selection made in the Print Definition dropdown will be overridden. On the other hand, if the appointment type *does not* have an associated print definition, yet this option is selected, the print definition specified in the dropdown field will be respected and rendered.

{{% tip %}}

Appointment Type Print Definitions are configured in the [Appointment Types editor](https://system/?func=scheduler&s=apttypes) (i.e., Appt Types tab) of the **Scheduler** module. Here, users with the necessary permissions may configure appointment types with print definitions, as needed.

{{% /tip %}}


Print Chart from Scheduler

In addition to the various locations users can access the Print Chart functionality within the chart,  {{% system-name %}} includes this same functionality from the [Scheduler](https://system/?func=scheduler#Now) module. When viewing scheduled appointments from the Scheduler, simply click the **Print Chart** link *within* the specific scheduled appointment block, and any printing or faxing needing to be done according to the scheduled appointment can be addressed.



![](print-chart.images/image6.png)



Additionally, users have the ability to utilize the **Print Charts** link, found at the top of the Scheduler module. This allows users to print charts or any print definitions for all of the scheduled appointments, rather than each appointment, individually.



![](print-chart.images/image5.png)



Once either of these links are clicked, the Print Chart dialog window will open, allowing the user to print/fax, accordingly. The available options and workflow follow those explained in the preceding sections (i.e., Print Chart from E-Chart and Print Chart from Appointments Chart Tab).


---
title: "Adding OSHA Case"
date: "2020-03-13T13:18:41.709Z"
url: "functions/injury-care/case-management/adding-osha-case.html"
version: 58
id: "1Q2noX9h3XKnZQ1eSpVOXXyBkriiJ_PvpgI_F2D3bDhg"
source: "https://drive.google.com/open?id=1Q2noX9h3XKnZQ1eSpVOXXyBkriiJ_PvpgI_F2D3bDhg"
menu:
    main:
        name: "Adding OSHA Case"
        identifier: "1Q2noX9h3XKnZQ1eSpVOXXyBkriiJ_PvpgI_F2D3bDhg"
        parent: "16-7poNmo_A35wJg_Sxb-bc-fbNHrEfSfMrlJjzpvmq8"
        weight: 1650
---
A case is a full report of a workplace injury, or incident, for an employee (patient). The case is created in an initial visit (encounter), and is then linked to subsequent visits. A case links all follow up visits (encounters), restrictions, accommodations, conditions, and nature of injury information. All of the documents pertaining to the case are grouped together within the chart for reporting purposes. There are several case types, which designate different required fields as well as state specific incident questions and forms. The terms case and incident may be used interchangeably in a system.

## Create a New Injury OSHA Case

If you wish to document a new case, expand to open the Case section in the dynamic encounter.



![](adding-osha-case.images/image9.png)



Once the Case section is expanded, indicate which type of case to create on the chart by selecting the appropriate radio button. Depending on the type of case radio button selected will determine other fields or radio button data to complete. Once you open/create a case, any documentation, encounter visit documentations, etc can be linked to a specific case/incident the chart has had.



![](adding-osha-case.images/image8.png)



This help documentation will describe the steps for creating and documenting an Injury OSHA Standard case type.   Injury (OSHA Standard) case types would be your most common selected case type, even if the injury isn't OSHA reportable.  Injury Non-OSHA case types are typically used by clients who aren't in the US and need a way to document cases/incidents but aren't under US OSHA regulations.  

{{% note %}}

Your MIE Implementer can also turn on a feature that will automatically also generate a ‘Case Management' encounter when a case is created for a visit encounter.

{{% /note %}}


By default, the Case section in encounters will display the following case types: Injury (OSHA Standard), Injury (Non-OSHA Standard), Hospital, Absence Management, MSEA, and Medical Surveillance.



![](adding-osha-case.images/image10.png)



### Injury OSHA Standard Case Details

After selecting to create an Injury OSHA Standard case, a question will branch open to document if the injury/illness was result of a single event or developed over time.



![](adding-osha-case.images/image1.png)

#### Dates/Times of Injury or Illness

Upon documenting the radio button selection, the case section will branch open to document the details of the case.  The first section is to key in the date/time of onset, and other date/times to note for specific work information. Many of the fields and data pull onto report of injury forms and/or reports.  Several fields are required and noted with a red asterisk.



![](adding-osha-case.images/image14.png)



#### Return to Work (RTW)

The return to work (RTW) dates may be entered now or in later during the case management process if applicable.   



![](adding-osha-case.images/image12.png)



#### Work-Related

The work related section is to document details regarding if the incident is work related or not, and depending on what radio buttons are selected, other data fields may branch open to document.  Fields with a red asterisk are required to fill out before a case can be saved to the chart. The field Work Related will most commonly be the answer will always be Yes if you are a client who tracks and records cases/incidents on your employee's for injuries and illnesses.  The Workers' Comp Related field is separate data to note if the case/incident is Workers' Comp related and will be going to the third party insurance administrator for your company as a claim.  If you answer "yes" to Workers' Comp Related, other fields will expand to document more comprehensive data regarding the Worker's Comp claim.



![](adding-osha-case.images/image11.png)



The field Date Determined Recordable means it's an OSHA reportable injury or illness.  If a date is entered into this field, this case/incident details will populate on the OSHA log report.

### Location

The location section displays to document where the injury occurred specifically.  If selecting Onsite Location as to where the injury/illness occurred, you can then (optionally) fill out where specifically the injury/illness occurred onsite using an auto-complete of choices.  The choices displayed in the auto-complete are a sample default list and you would need to give a complete list of location areas to your MIE Implementer in an excel spreadsheet for an MIE developer to import.  It can be a general list or a very granular hierarchical location of choices. The auto-complete field is optional just to provide more granular reporting needs if client desires. Otherwise, one must just free-type in where the the event occured in the field noted by a red asterisk.



![](adding-osha-case.images/image13.png)



If selecting Offsite Location, then the fields that branch open are required free text fields to note the offsite location details.



![](adding-osha-case.images/image15.png)



### Incident Details

In the incident details section are some checkbox choices and also where you free-type answers to 3 required questions on how the injury occurred, what happened, and what harmed.



![](adding-osha-case.images/image18.png)



Event and Source drop-down fields are not displayed Injury-OSHA case type by default but can be configured into your system if needed.  Otherwise, these are only offered in the Non-OSHA case type. If you wish to have those input fields also, please contact your MIE Implementer to have that configured.    Drop-down choices for these can be customizable.



![](adding-osha-case.images/image7.png)



### Treatment

In the optional treatment section, you can indicate an answer if the patient received medical treatment prior for this case/incident and by whom.



![](adding-osha-case.images/image3.png)



Depending on various radio button answers selected, other fields may branch open to document in where some are required and others are optional.

The treatment provided by onsite health services radio button choice points to a location drop-down that shows choices of inside & outside locations set in your {{% system-name %}} system via the Locations Manager tab found in Control.



![](adding-osha-case.images/image17.png)



The treatment provided by hospital/er/urgent care facility radio button choice show free text fields available to key in information.  Again, information keyed in these sections usually overlay on specific forms that you generate from forms library.



![](adding-osha-case.images/image6.png)



The treatment provided by external provider or other radio button choices show free text fields available to key in information.



![](adding-osha-case.images/image2.png)



### Authorized Providers

This optional section is provided to be able to document what providers are working on the case/incident, especially if you maintain a directory of outside providers in {{% system-name %}} .  This auto-complete of choices in the authorized providers section points to the department "Physicians".  This will display active & login disabled users tied to that department. This is an optional section and doesn't need to be filled out unless you want to be granular in documenting this.



![](adding-osha-case.images/image5.png)



### Nature of Injury/Body Parts

Here you can document the nature of injury or illness using a drop-down selection list.  The fields  Nature of Injury and Body Part are drop-downs of choices.  Contact your MIE Implementer if need additional choices added to these drop-downs.



![](adding-osha-case.images/image4.png)



.. Note:: Selecting Contaminated Sharp as the nature of injury will expand 3 additional fields for you to document.  These additional fields of data pull on Sharps Log reports.



![](adding-osha-case.images/image19.png)



### Work Status (or Lost Time) Section

Lost time would be documented using the Restrictions and Accommodations section.  Refer to the [Restrictions and Accommodations](../adding-restrictions-and-accommodations.html) help documentation for more information.

### Restrictions and Accommodations

Refer to help documentation named [Restrictions and Accommodations](../adding-restrictions-and-accommodations.html).

## Linking Documents to Cases

Documents can be linked to cases.  This can be done when in Add Document mode, via the Edit Properties of an existing stored document.  Documents can also be linked to cases when indexing a document from WebScan. Scheduled appointments can also be linked to cases when in the Add Appointment wizard.

## Case/Incident Summary in Dynamic Encounters

Some dynamic encounters offer an Incident Summary section.  This is an expandable section to review or edit specific case data while a provider works their portion of the encounter.  Usually the nurse creates a case and documents the case details from the employee's/patient's statements, but while the provider is seeing the patient/employee, the provider may deem to change high priority fields/data of the case and this section offers that ability, instead of scrolling back up to the case section to expand and edit all the details.



![](adding-osha-case.images/image16.png)



{{% info %}}

Various forms, in forms library, can be programmed to pull in case data details that were documented.  Contact your MIE Implementer if have specific forms that need generated routinely that may need case (incident) data overlaid.

{{% /info %}}



---
title: "Injection Tab - Vials"
date: "2020-03-16T14:41:06.490Z"
url: "functions/injection-immunization-management/injection-tab-vials.html"
version: 49
id: "11_gJvEXt_A9TeALtLbhxsUzWimA0i3C3qi0TZ1w43dk"
source: "https://drive.google.com/open?id=11_gJvEXt_A9TeALtLbhxsUzWimA0i3C3qi0TZ1w43dk"
menu:
    main:
        name: "Injection Tab - Vials"
        identifier: "11_gJvEXt_A9TeALtLbhxsUzWimA0i3C3qi0TZ1w43dk"
        parent: "1bLRXxR-h5NWzJsXSk2cf_6ZjxljZuiBzTcQdmlvVrDA"
        weight: 2280
---
## Add Vials

There is a feature in the immunization/injections module to add Allergy Vials from the Add Vials link at the top right of the module.



![](injection-tab-vials.images/image9.png)



You will then see a screen where you can add multiple vials.

Enter the information in each field.  



![](injection-tab-vials.images/image14.png)



Click the ADD button when done entering the vial(s) you wish. After you enter vial(s), you will be taken back to the immunization/injection summary screen. You will see the summary list of immunizations, injections & vials. You can now add an injection(s) towards the vial(s) you entered.



![](injection-tab-vials.images/image15.png)



### Administering Injections from Vial(s)

To do this, you must first check-mark the vial(s) you wish to enter an injection for.  If you do not, you will get an error message saying you must first select a vial to add an injection to.  Note: There is a system setting named Vial Checkbox Checked by Default that can be enabled which will default to all vials having a checkmark on them.  Then one can simply "uncheckmark" which vial not dispensing from.

Then, click the ADD INJECTIONS FOR VIALS button under the vials summary listing.



![](injection-tab-vials.images/image6.png)



The correct # of injection screens will open according to how many vials you check-marked.

Fill out the injection fields with the information.  Fields will be auto-populated as it pulls from the vial someone previously entered.



![](injection-tab-vials.images/image12.png)



* Injection/Immunization:  This is a required field.  You must type the name of the injection/immunization into this field or you will get an alert when trying to save this without a name.  The system will attempt to auto-complete your typing & give you choices that match. You can highlight & select if you wish. Otherwise, you can continue to free-type in text.  
* Administering Location: If your practice only has 1 location it will automatically populate this field.  If your practice has several locations programmed into {{% system-name %}} , use the drop-down arrow to select the correct location of where the injection was administered.  If you have a location selected here, it considers this injection an in-house injection.  Meaning, the injection was administered at your location.  If a location is selected here, you will be required then to fill out the Manufacturer and Expiration Date fields.  These are required fields if a location is specified.
    * If the injection was given elsewhere and you are just documenting the injection for records, select No Location and it will not make those other fields required to fill out.
* Administration Date:  Automatically pops-up today's date and current time.  Change date or time to when the injection was given.
* Administrator: Select the name of the person that gave the injection.  There are 3 ways to select the administrator's name. You can start typing the last name in the first blank field and click SEARCH to pull up a list of users that match and select from there.  If you want to select a physician within your practice, use the drop-down arrow in the next field and select from there  (this is helpful to narrow down the search). If you are the injection administrator yourself (not recording this for anyone else) then choose ME box here.  The document will reflect your name as Injection Administrator. The name you choose/select, will then appear at the top of this field next to Injection Administrator.  Confirm and make a change if need to.
* Route:  Select the route of the injection, if you wish, from the drop-down of choices.
* Site:  Select the site the injection was given from the drop-down of choices. Your MIE Implementer can change a system setting to show all or a limited choice of sites to list for vial injections.
* Dose:  Enter the dose of the injection.
* Strength: Enter the strength of the injection.  You will also see the color code next to that strength chosen if your practice has vial colors system setting turned on.
* Comments / Reaction:  Free-text in this field any comments regarding the injection, etc.  If a patient later had a reaction to this injection, you would also type any comments regarding that here and submit an edit to the original record.  (See other instructions in Editing an Injection Record).

The following fields can be entered when editing an injection or now when you are entering the injection & know the reactions.  These are typically used for Allergy Injections, but can be used for any other injection.

* Peak Flow: Enter the peak flow in L/Min
* Next Due: You can enter a date the next inj/immunization is due if you wish (ex: if it's a series, etc).

{{% system-name %}} has the ability to have overdue injections pop up from One-Click Checkin when in the Scheduler.  

A system setting has to be manually created by MIE to enable this for a client.

Click ADD INJECTIONS button at the bottom to enter these injections from the vials into the patient's record. It will then place these injections into the Injection List of records for the patient.

### Documenting Injections from Vials within Encounters

When working in an encounter, your MIE Implementer can have the Vials section programmed to your encounter. This will allow you to dispense/document injections given from vials.  You can checkmark any vial(s) you are dispensing an injection from and the Add Injection from Vial screens will appear on your encounter screen.  You can then document the injection given from the vial(s) that were checkmarked to dispense from.



![](injection-tab-vials.images/image3.png)



## Vial Flowsheet

If you are a practice that uses the Vials for patients, you can have your MIE Implementer set up the Vial Flowsheet to be shown in the injections/immunizations summary screen.  The examples/screenshots below show this client using Vials for allergy injection patients. The vial flowsheet in the below example is named Allergy Injections but it can be custom labeled/titled to what you wish.  This shows a flowsheet of each injection given from each vial. This summary (vial flowsheet) shows at the top of the injections/immunization screen. Contact your MIE Implementer if you wish for this flow display of injections from your entered vials.



![](injection-tab-vials.images/image18.png)



To print a vial flow, contact your MIE Implementer to have a layout & tag programmed.  That layout would then be a section accessed to be able to print via a printdef.

## Edit a Vial

You can edit, copy or delete a vial from the Injections List summary screen.

To Edit a Vial, simply click the Edit link in the Options column next to the vial you wish to edit.



![](injection-tab-vials.images/image8.png)



Make the edits to the fields you wish.



![](injection-tab-vials.images/image10.png)



Click EDIT when done.

It will then take you back to the main injections summary screen, save & display the edits you made.

## Delete a Vial

You can edit, copy or delete a vial from the Injections List summary screen.

To Delete a Vial, simply click the Delete link in the Options column next to the vial you wish to delete.



![](injection-tab-vials.images/image5.png)



Click the DELETE button.  Once you click delete, it will delete the vial.  There is no confirmation screen or field to type in a reason for deletion.



![](injection-tab-vials.images/image13.png)



It will delete the vial & refresh you back to the main Injection summary screen.  The vial will no longer be displayed.

### Retrieve Deleted Vials

If you wish to view or retrieve a deleted vial, from the main Injections summary screen, click the link Show Deleted in the Vials summary category.



![](injection-tab-vials.images/image1.png)



The deleted vials will then show in that category summary for viewing.

If you wish to retrieve (undelete) a vial, simply click the link undelete from the options column.



![](injection-tab-vials.images/image11.png)



It then brings up the details of the vial.  Click UNDELETE button at the bottom to retrieve & undelete this vial.



![](injection-tab-vials.images/image19.png)



It will then refresh & bring you back to the main Injections summary screen.  You will see the vials listed that you undeleted.

## Copy a Vial

You can edit, copy or delete a vial from the Injections List summary screen.

To copy a Vial, simply click the Copy link in the Options column next to the vial you wish to copy.

Copy is a quick way to enter another vial using a previous/old vial information.



![](injection-tab-vials.images/image16.png)



The Copy Vial screen fields will appear.  It auto-populates the fields w/ the information from the vial you are copying.  You can make any changes to the fields you wish for this new copied vial & click the COPY button at the bottom.

This is just a quick way to enter another vial without having to re-enter field information that might be the same as other already entered vials for the patient.



![](injection-tab-vials.images/image2.png)



* Auto-Expire Previous:  This is check-marked by default.  When you copy a vial, most likely it is because you are tossing the old vial out.  So the original vial you copied gets expired as of the current date if this is check-marked to automatically-expire the previous (previous means original vial you are creating the copy from).  The original vial then won't show up on the current list because you automatically-expired it. It will then refresh & bring you back to the main Injections summary screen. You will see the new entered vial you created as a copy from a previous vial.

## Scan a Vial Sheet

Some practices want to scan in the allergy vial sheet that comes packaged with the vial (from the allergist).  This is the paper sheet that usually the nurse handwrites the date given, the sit, any reaction, etc. That sheet then goes back with the vial for additional documentation for the allergist.

Your system can be set up to have a Scan link in the options column for scanning in that vial sheet and store it as a document in the patient's chart.

Contact your MIE Implementer to set the doc.type to the system setting.  The doc.type has to be created, then the Implementer keys that doc.type into the system setting.  The Scan link will not show up as an option if the system setting isn't defined with a doc.type. In the screenshot below, this {{% system-name %}} system scans in vial sheets defined as doc.type PATVIAL.



![](injection-tab-vials.images/image7.png)



Using a flatbed scanner to scan a Vial sheet, simply click the Scan link in the Options column next to the vial you wish to edit.



![](injection-tab-vials.images/image17.png)



The document scan control will appear on the screen.  Proceed to scan in the vial sheet and upload.

(See other help instructions titled E-Chart Scan Documents for help with Document Scan Control and scanning).



![](injection-tab-vials.images/image4.png)




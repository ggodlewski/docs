---
title: "Inventory Mappings"
date: 2020-02-27T20:31:50.550Z
url: "general-functionality/system-administration/asset-management/inventory-mappings.html"
version: 30
id: 1nvcWeIakN3JOQyEK1j5fOJn6sXjalZuVXRKub1w4nos
source: https://drive.google.com/open?id=1nvcWeIakN3JOQyEK1j5fOJn6sXjalZuVXRKub1w4nos
menu:
    main:
        name: "Inventory Mappings"
        identifier: "1nvcWeIakN3JOQyEK1j5fOJn6sXjalZuVXRKub1w4nos"
        parent: "1aHv0u59NGVLFrvGN1I8FETs0j2WrIH_elfLoJjkL-ek"
        weight: 5700
---
## After you have added a new inventory item into your inventory in the Master Inventory List/Control tab, you then map it in the Mappings tab.

The Mappings tab is located in the sidemenu tab named *Inventory*. It will open to the default of showing you all of the current *Inventory Mappings*.

![](../../../external_files/3e4f85aa8dca1b1c34aeb1c8b62a48c0.png)

Mapping needs to be done because it is the process of matching the Master Inventory Item name to a recognized medication in the drug database, CDC immunization, or supply order within the database.

## Search for Current Inventory Mappings

First you will want to search for the inventory item to confirm if it's already mapped or not.

* <strong>Search</strong>: You can search for mappings using the search by fields. If you click the [ + ] sign in search by, you can open up another search to search a medication name and it's inventory name or 2 different searches, etc.

![](../../../external_files/47512138181497619ac72ffbbc773482.png)

* You can also render results to show by All Types, or get granular by selecting to see only current mappings that are Medication type, Injection Type, Order type or Barcode type.

![](../../../external_files/6e1fe5dc0b7378b94844056556c4ebc2.png)

### Columns in Results

Mapped ID column: shows you the Medication ID # it's mapped to from First DataBank (if it's a medication inventory item mapping), or it will be the CDC immunization code if it's an immunization/injection mapping, the {{% system-name %}} Order ID# if it's a supply order mapping or the barcode # if it's a Barcode mapping. For medications that are mapped to Medication ID's from First DataBank, you click that underlined id#, it will open up that drug guide for the medication.

![](../../../external_files/142b741b8491f0f25e424a834c3a3af4.png)

* <strong>Mapped Name</strong>: This is the recognized name of the medication from First DataBank, or the CDC recognized immunization or the recognized supply order. This is what the master inventory item is mapped to.
* <strong>Mapping Type</strong>: This is the type of mapping it is. If it's a medication inventory item mapping, an injection/immunization mapping, a supply order mapping or a barcode mapping for that specific inventory item.
* <strong>Inv ID</strong>: This is the {{% system-name %}} inventory ID number that is assigned to the master inventory item.
* <strong>Inventory Item</strong>: This is the name of the inventory item in the master inventory list.

## Add Mapping(s)

To add a mapping, first you must have the *Show Type:* selection specified.

The ‘Show Type' performs 2 functions:

* It limits the mapping types that are displayed in the Inventory Mappings search results list (see above pages).
* It changes the behaviors of the auto-complete in the ‘add a mapping' form from being medication autocomplete choices to an injection auto-complete.

{{% info %}}

It will not allow you to add a mapping if the Show Type: is set to All. You must select a Show Type first before you can add a mapping. If you want to add a mapping for a Medication, make sure the *Show Type:* is set to Medication. If you want to add a mapping for an Injection, make sure the *Show Type:* is set to Injection. If you want to add a mapping for a supply order, make sure the *Show Type:* is set to Order. If you want to add a mapping for a barcode hand-held scanner functionality, make sure the *Show Type:* is set to Barcode.

{{% /info %}}


![](../../../external_files/6e1fe5dc0b7378b94844056556c4ebc2.png)
### Add Medication Mapping(s)

The *Show Type:* needs to be selected to Medication.

Then click the Add a Mapping hyperlink at the top right of the Mappings tab (next to *Show Type* selection).

![](../../../external_files/a578f6cafcacaa39802cf575e28b42ea.png)

The Map Inventory fields will open at the top of the screen.

The two fields on the left are the auto-completes pointed to the medication name & form/strength from the First DataBank drug database. Begin typing and select from the auto-complete for the recognized drug database medication name and use the tab key to select the specific strength/form that First Databank states this drug is available in. This is what your Master Inventory Med item will be linked/mapped to in the recognized drug database {{% system-name %}} is linked to.

![](../../../external_files/859b9c863bff88bc97dbb98f6287f2ed.png)

Again, use the tab key to go over to the next field which is your Inventory Description field.

The Inventory Description field is to be the Master Inventory Item of that medication. You are linking the left side fields (recognized FDB medication & strength/form) to the ride sided field of your master inventory item name.

Begin typing in the name of the master inventoried medication in your system that you entered in the Control Inventory (Master Inventory List) tab. Select the master inventory item name. It will auto-complete for your selection.

## ![](../../../external_files/4718e1377e16f5a789e22a0a4ea89d5a.png)

Click SUBMIT button and it will say confirmation of *mapping inserted* at the top.

You will then see it listed in the Inventory Mappings Tab list of all current mappings for medications inventory items.

### Add Immunization Mapping(s)

The *Show Type:* needs to be selected to Injection.

Then click the Add a Mapping hyperlink at the top right of the Mappings tab (next to *Show Type* selection).

![](../../../external_files/8425c011547de339c8ff49cb991802ea.png)

The Map Inventory fields will open at the top of the screen.

The field on the left is the auto-complete pointed to the CDC immunizations listing. Begin typing and select from the auto-complete for the recognized CDC immunization. This is what your Master Inventory item will be linked/mapped to in the recognized immunization database {{% system-name %}} is linked to.

![](../../../external_files/02acad684e651826c3d6a8bbf9e3fcda.png)

Again, use the tab key to go over to the next field which is your Inventory Description field.

The Inventory Description field is to be the Master Inventory Item of that immunization. You are linking the left side fields (recognized CDC immunization) to the ride sided field of your master inventory item name.

Begin typing in the name of the master inventoried immunization in your system that you entered in the Control Inventory (Master Inventory List) tab. Select the master inventory item name. It will auto-complete for your selection.

![](../../../external_files/bf9f273177e8b534e6f419fab34660e5.png)

Click SUBMIT button and it will say confirmation of *mapping inserted* at the top.

You will then see it listed in the Inventory Mappings Tab list of all current mappings for injection immunizations inventory items.

### Add Order/Supply Mapping(s)

The *Show Type:* needs to be selected to Order.

Then click the Add a Mapping hyperlink at the top right of the Mappings tab (next to *Show Type* selection).

![](../../../external_files/989afafd16a0fb846acbfdf9faca6074.png)

The Map Inventory fields will open at the top of the screen.

The field on the left is the auto-complete pointed to the Supply Orders in {{% system-name %}} that were entered in the Order List Editor or Order Supply Editor tab. Begin typing and select from the auto-complete for the recognized order. This is what your Master Inventory item will be linked/mapped to in the recognized orders in {{% system-name %}} .

![](../../../external_files/f8fd49e30b43c64bc4f54a888ba124a6.png)

Again, use the tab key to go over to the next field which is your Inventory Description field.

The Inventory Description field is to be the Master Inventory Item of that supply order. You are linking the left side fields (recognized order) to the ride sided field of your master inventory item name.

Begin typing in the name of the master inventoried order in your system that you entered in the Control Inventory (Master Inventory List) tab. Select the master inventory item name. It will auto-complete for your selection.

![](../../../external_files/84a0b12b472db6b96fa67c81e8693cd9.png)

Click SUBMIT button and it will say confirmation of *mapping inserted* at the top.

You will then see it listed in the Inventory Mappings Tab list of all current mappings for supply order inventory items.

### Add Barcode Mapping(s)

The *Show Type:* needs to be selected to Barcode. MIE can interface with a barcode scanner device Motorola ES406080 hand-held scanner. This requires MIE Implementer and programmers set up. We have found with that specific type of scanner to not have the base plugged into the wall for it to work and that is manufacturer specs, not an MIE program issue.

Then click the Add a Mapping link at the top right of the Mappings tab (also next to *Show Type*).

![](../../../external_files/05c76a62865150ceb98b13db41db8fe4.png)

The Map Inventory screen fields will open at the top of the screen.

On the left side field, place your cursor in that field and then physically trigger the barcode scanner on the physical item's barcode on the packaging that you want it to read. The Barcode numbers/alpha should populate in that field.

![](../../../external_files/55ba5a99b74ad8c74811e44c7c79ac1b.png)

Again, use the tab key to go over to the next field which is your Inventory Description field.

The Inventory Description field is to be the Master Inventory Item of that inventory item. You are linking the left side fields (recognized barcode) to the ride sided field of your master inventory item name.

Begin typing in the name of the master inventoried order in your system that you entered in the Control Inventory (Master Inventory List) tab. Select the master inventory item name. It will auto-complete for your selection.

![](../../../external_files/e6a252f6ecaf3765c7215c5e1bc34bba.png)

Click SUBMIT button and it will say confirmation of *mapping inserted* at the top.

You will then see it listed in the Inventory Mappings Tab list of all current mappings for inventory items.

If you are using the Barcode scanner functionality, your inventory item in the master list should have 2 mappings tied it. One mapping should be to the inventory item "type" and the other mapping would be to its "barcode".

![](../../../external_files/508bf01a4a7a17750f02abd9a4ecdb5e.png)

## Edit/Delete Mapping(s)

If you need to edit a mapping, click the edit link in the options column of the Mappings Tab list for the specific mapping you need to edit.

![](../../../external_files/3635ed6081cb15a901e95997e3587f48.png)

The Edit Map Inventory screen will open. Edit what needs done to the inventory item mapping and use your tab key to go thru the fields.

![](../../../external_files/392a50403ca3c4a698d556c6ecf00a33.png)

If you selected a different medication name from the drug database, use your *tab* key on the keyboard to advance to the strength/form field. All choices for this drug from the database will show here for selection.

Click SUBMIT button and it will say the mapping was inserted, which means it was edited.

To delete a mapping, simply click the Delete option for the specific mapping item.

It will ask you to confirm the mapping deletion. Click DELETE button to perform the deletion or cancel to escape out.

![](../../../external_files/2867caadfba3bc7fdc40f6634d58d4f7.png)

## Merging Mappings

If you need to merge 2 different mappings that are the same (duplicates), check-mark which ones to merge in the MERGE column. Then click the MERGE SELECTED button at the bottom.

![](../../../external_files/451ddbf99ccc690c3c21ab1c7dbafccd.png)

The mappings & quantities would be merged into one mapping.

If you check-mark 2 inventory mappings that conflict with each other, you will get that warning message.

![](../../../external_files/c81ad91dad11e23391ebd0db1427cd6a.png)

You can check-mark them to merge again and click OVERRIDE button to override this warning or click Cancel to escape out.

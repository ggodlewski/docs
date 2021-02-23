---
title: "Make Order Feature - Encounter Plan Section"
date: 2020-03-26T17:32:33.043Z
url: "general-functionality/encounters/make-order-feature-encounter-plan-section.html"
author: Jeremia Ploor
version: 66
id: 1kEF-RWvZOJqe2pD7lr3XpwNbP73D0X8SXsRjGm4T-SA
source: https://drive.google.com/open?id=1kEF-RWvZOJqe2pD7lr3XpwNbP73D0X8SXsRjGm4T-SA
menu:
    main:
        name: "Make Order Feature - Encounter Plan Section"
        identifier: "1kEF-RWvZOJqe2pD7lr3XpwNbP73D0X8SXsRjGm4T-SA"
        parent: "199AEByNU97uYKqzI8RuvTDuojNy0KQvIe8uBmaL0-xo"
        weight: 1490
---
The ‘plan' area of an encounter allows the physician/user to create orders for the patient. The below explains how a physician/user enters items into the plan area by using Make Order link or Create Order link in the plan area and how it renders a complete order to print/fax right from the encounters view. This forces the physician/user to create the order right from the encounter and eliminates having to go to unordered orders or the patient's chart to render the order that the physician created in the encounter. You can ask MIE to remove the list option completely and only use the Make / Create Order feature or have both options. Only the make / create order feature will create the order right there in the encounter though. Using the Create xx Order link bypasses the unordered orders and inserts the order as a document directly into the patient's chart. If using the list link or auto-complete fields in the plan orders area, it creates an unordered order (see other help documentation titled *Encounters Plan Section-Unordered Orders.pdf*).

If the user/physician uses list (and not make / create order) or the auto-complete fields in the plan area, it creates an unordered order which the front/check out staff uses to create the orders before the patient leaves. See separate help documentation named *Encounters Plan Section-Unordered Orders.pdf* for this workflow option.

## Make Order Link/Create Order Link

Your plan section in encounters can be programmed to have a Make Order feature link or a Create Order link. This gives the physician/user the ability to make and create an order right from the plan and then it is ready to print/fax in the encounter view or print all. Using the make /create order link bypasses the unordered orders and inserts the order into the patient's chart. It is then available in the encounter PRINT ALL option to print these orders for the patient.

![](../../external_files/2c522d04a7f17d5eb5eb4e7ef19a7450.png) ![](../../external_files/ed48c8fec8f0f4fe48d9c34d5974df3c.png)

![](../../external_files/83b08a4efff8cc11a2a54c4baf4cf709.png)

To create an order in the plan section, the user must **first click Make / Create xxx Order** link from the specific category they want to make an order from. If you click list first and check-mark items—it will render it as an unordered order (see separate help documentation). You can have the ‘list' links removed to force creation of order from encounter.

To make an order right from the encounter, click Make / Create Order first in the specific section. When you click Make / Create xxx Order, it will open up the *Start Order Request* dialogue screen.

![](../../external_files/e6f1e09d1418a6fa3bf0e92486adc5fe.png)

In the *Start Order Request* screen, you must select and enter the fields:

* <strong>Location:</strong> Select the location that this order is to be completed at (optional field). The layout can be modified by MIE so that location of this <em>Make Order</em> feature shows all locations in your system, only outside locations or no outside locations. The setting is -1 for all, 1 for just outside, 0 for no outside. Please contact your MIE representative for this change. Your MIE Implementer can also change the system setting to make this a required field. This field also respects the orders location default you have set for yourself in MY SETTINGS.
* <strong>Facility:</strong> This is where the order will be sent if you have a lab or other interface set up where your e-orders get automatically sent to a facility via interface to the facility (ex: LabCorp, Quest etc). The <em>My Settings</em> preference "Preferred Facility" will default here, but can always select a specific performing facility in the drop-down. Otherwise, leave this blank and skip this field if you don't have any directional interface to lab/imaging facilities set up.
* <strong>Refer To:</strong> Ability to document whom you are referring this patient to via the order (mainly used when making Referral Orders). This <em>Refer To</em> field is a user autocomplete that only shows user choices whose <strong>user role</strong> is "referring physician" (not department but user role <em>aka</em> Def User Role in their username screen). Creating an order request in an encounter also supports using charts for referring physicians if the (System, External Provider, Use charts) setting is enabled.
* <strong>Ordering Physician:</strong> Select the Ordering Physician by using the drop-down arrow to select the physician that is ordering this. Your MIE Implementer can also change the system setting to make this a required field. This ordering physician field for the order via the encounter defaults to populate the same name as the performing provider on the encounter. If no performing provider has been set on the encounter, the ordering physician defaults to the user's MY SETTINGS preference of ‘Ordering Physician' if that has been set.
* <strong>Order Frequency:</strong> Type in how often to do the order, example: to do this standing order every 3 days or every 1 month, etc. If it isn't a standing order, leave as 0 (zero) days.
* <strong>Schedule Lab In:</strong> You can use the drop-down arrow to select an automated selection if the date for the order is not a specific date (more of a general time frame). You can also free-type in the free-text field next to it any other general date time frame, etc.
* <strong>Diagnosis:</strong> The 4 most recent conditions the patient has will appear here. There is a system setting you can ask your MIE Implementer to set to add more or less to this list.

![](../../external_files/e27c5da89101f113367f2f309a09a6da.png)

* By default it is set to 4. You can delete the diagnosis that appears by clicking on the grey minus button. You can also add another diagnosis in the field below that. When you start typing the name of the diagnosis, a series of auto-complete choices will appear and you can choose from there. You can also start typing the ICD-9 code and a series of auto-complete choices will appear and you can choose from there. To add multiple diagnoses to this order, simply search and select the diagnosis after you select from the auto-complete choices and it will automatically insert it in the field above it. To delete one, click the minus button next to the diagnosis. Any conditions/diagnosis that are entered on the order that the patient doesn't already have will be linked to the encounter as a part of the "Impression" and will not appear under the "Past Medical History". This respects the system setting "Save Diagnosis to Patient Conditions" that causes orders to save the conditions to the patient in the first place. When you are done, simply go to the next tab called Patient Instructions.
* <strong>Bill Type:</strong> Order requests can specify a bill type. If system setting <em>Require Bill Type</em> is enabled, this field will appear. There are four options: The default is None (unspecified), Self, Client, and Third Party. The system setting (Orders, Settings, Require Bill Type) will control whether this field is required or not on the order. If this setting is on (value set to 1), and ‘None' is chosen in the bill type dropdown, the user will be asked to choose a different option.

![](../../external_files/25617c3cc5436ca2c7b0d5bdb3daaff0.png)

* <strong>Patient Instructions:</strong> Free type any instructions for the patient regarding this order. These instructions may or may not print on the order sheet, depending on how your practice decided to layout the printable order sheet.
* <strong>Comments:</strong> Free type any comments regarding this order. It will print on the order sheet and will show up in the Comments category when looking at this patient's recent orders from the orders screen view.

Continue down this order screen and checkmark which order items you wish to order for the patient. The blank fields next to any order item are free-text boxes (like to document which side to do an xray or how many views or any additional comments regarding that order item).

![](../../external_files/4190cc8a601bf69e62fe846ba899bcd7.png)

Above or at the bottom there are function buttons. Click "REQUEST ORDERS" button to render the order. The "Hide Top Form" button simply hides the top portion of this orders screen and only shows the order items to checkmark.

![](../../external_files/bc0d2ce17a41a7c5839691741bee32f5.png)

You can toggle between order sets to checkmark orders from various order set's (ex: Lab, Imaging, etc) all at once and make it **one** order document instead of separate. There is the ability to switch picklists in the encounter order which is controlled by a dropdown containing all the order picklists in the system.

The last picklist visited before clicking the "Request Orders" button will be the name of the order document that it will store as, regardless of whether any orders were chosen on that last picklist or not. The user can choose which picklist is recorded by visiting that picklist (or returning to it) before clicking the "Request Orders" button. There is a help bubble explaining this next to the *set name* field also for additional help. Again, this gives ability to mark orders across various order sets but will store it as one order document – as the name of the last set name (picklist) you were in.

![](../../external_files/88f47b2b56b2645cc8642f767e46e7b2.png)

After clicking REQUEST ORDERS button, this will close that orders screen and then it will list your items you selected under the *Order Requests* category of the encounter.

![](../../external_files/b2117df5e6b37aaafb6b25d13a7e1fd6.png)

If your system is configured to require diagnosis for each order item, you will be prompted to confirm diagnosis for each order item you marked. If there are more than 3 order items on the order, you will have the ability to **apply diagnosis** to all order items quickly in mass instead of individually. If there are any order questions to answer on any order item, you will be prompted to answer those too. Click the FINISH button when done confirming diagnosis for each specific order item and any questions answered.

![](../../external_files/7dc38ebfb7852898d4882168054f1e7e.png) ![](../../external_files/f35fa0f4163aeb3b24efb26b796f0eab.png)

When click the FINISH button, it will prepare the order request for submission with the encounter but the order request will *not* be submitted until the encounter work is saved. You can edit the order request before you save your encounter work. You can click the *edit "xxx" order request* button. This will re-open the ‘Start Order Request' window and populate it as it was in its last state. Cancelling the order request from that window or the Finish Order Request window keeps the order intact. If any changes to the order are made, those changes will be reflected on the page.

![](../../external_files/461464f57542f2e3774d4a88f1961418.png)

If you click the SAVE button on the encounter to save your encounter work, you will see this section change to show the order requests and be able to *edit* them if need be. You can still edit the order at that point also.

![](../../external_files/538930f8fa0450649961d67aa6b9687d.png)

{{% info %}}

While working in the encounter and seeing the requested orders as the look above, the "look" can be configurable using tag attributes. Contact your MIE Implementer if you wish any of these additional tag attributes to show or hide additional information regarding order requests in encounters.

{{% /info %}}


![](../../external_files/50aa0ee16b35fdff79ff3de1b3d621eb.png)

* <strong>Comments</strong> can be shown. That would show the comments field from the order request (comments are hidden by default).
* <strong>Date of Service</strong> next to the ‘Edit Order Request' link on generated orders can be hidden. This is the date of the encounter, not the order date or order create date (currently date is default to be shown)
* <strong>Completion Date</strong> can be shown which shows the completion date of the order (completion date is hidden by default).
* <strong>Diagnosis code & description</strong> can be shown which shows the diagnosis and ICD code for that order item (diagnosis code/desc is hidden by default).

If you click the hyperlink edit order request (date) you will be taken to the order screen again to make any edits and click REQUEST ORDERS button at the bottom to render. See other help documentation on editing orders.

![](../../external_files/f5147cfb208ddb03d48756df8d3b258e.png)

When done with the encounter exam, the physician will submit the encounter.

If there were any orders made by the physician using this make/create order feature, those orders show on the encounter document "view". The orders show in the *plan* area of the encounter document along w/ any diagnosis required on the order item.

![](../../external_files/f9c448b606008e6fc93fc9b8724fe4eb.png)

The order itself (the document) would be pending to batch/print/fax in the encounters "view" to print and hand to the patient or fax out to a facility. There are several other places in {{% system-name %}} that you can print/fax/batch this order document. But from here, in the "view" of the encounter, look in the *Encounter Options* area at the very bottom of the screen.

![](../../external_files/4ca72bad9a7eb0d3ccddcde854c8717d.png)

You can batch and print all orders, prescriptions, drug guides, etc created from the encounter. You can also see the last time it was printed or faxed so you know if someone already rendered it.

You can also individually batch or individually print/fax by clicking the batch link next to each prescription, drug guide and/or e-order pending in the queue to print/fax. An order also shows the status of the e-order in a column. You can edit an e-order from this screen but it will only edit the order document, it will not edit/updated your encounter document. You can also simply open it up in ‘view' mode also to view. If you need to delete an order, click the Complete link, then set the order item(s) to *cancelled* in the screen it takes you to.

{{% tip %}}

If the user's preference for (‘Orders', ‘Encounter Orders', ‘Filter Pick List By Insurance') is set to ‘YES', the order pick list link in the plan section will first show the insurance choice window. The user will then be shown only picklists which have at least one order for the chosen insurance (or at least one order for the default insurance, if no insurance has been chosen). When no insurance is chosen for an order picklist in encounter orders (for instance, those chosen via the Labs or Imaging links in the Plan section) only those order items that do not have an insurance plan attached to them are displayed. This preference is mainly used by occupational health clients.

{{% /tip %}}


## Mark Order Complete

You can easily mark a pending order as "complete" even while working in the encounter or from the "view" of the encounter.

![](../../external_files/abd058eca736320243438eb74dc6e19e.png) ![](../../external_files/8855ded517900ce4834c3faf58ae2df2.png)

Clicking the hyperlink to Complete a pending order request will take you to the *Complete Order* screen to document the pending order as "complete". (See additional documentation regarding *Order Completion* screen.) You will see this hyperlink available for any type of order request done via the Make xxx Order functionality.

### Mark Lab Order Complete with Results

You can easily mark a pending lab order as "complete" and key in the lab results as discrete data to link to the originating lab order. You can do this even while working in the encounter o from the "view" of the encounter.

![](../../external_files/96f415e3cac3a760e11010defe02ac62.png) ![](../../external_files/1b872933e60f1f0f0daf4f1000e146f9.png)

Clicking the hyperlink to Complete with Results for a pending lab order request will take you to the *Complete Order with Results* screen to document the lab results of the order as discrete data and creates a Lab Results document in the patient's chart along with completing the order. (See additional help documentation regarding *Complete Order with Results* screen.) You will see this hyperlink available for any type of Lab order request done via the Make Lab Order functionality.

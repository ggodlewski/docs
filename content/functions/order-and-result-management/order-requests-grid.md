---
title: "Order Requests Grid"
date: "2020-03-13T19:30:15.508Z"
url: "functions/order-and-result-management/order-requests-grid.html"
version: 67
id: "199nDYD4Cbf7b43xTuYJNIEVtTkRYV9TVPWdD6JKZQnQ"
source: "https://drive.google.com/open?id=199nDYD4Cbf7b43xTuYJNIEVtTkRYV9TVPWdD6JKZQnQ"
menu:
    main:
        name: "Order Requests Grid"
        identifier: "199nDYD4Cbf7b43xTuYJNIEVtTkRYV9TVPWdD6JKZQnQ"
        parent: "103elDMKyCQlA8uZjycHzAZ90L6BR3FTzxRLYOKrgpo8"
        weight: 1910
---
## Order Requests

To view recent orders (existing orders) that the patient has had created/ordered for them, go to the *Order Requests* chart tab.

![](order-requests-grid.images/image3.png)

This will then show below any completed orders, standing orders, and pending orders for the patient in various buckets. There is also a search tool to search orders on this patient to render limited results.

From this summary screen (of completed, standing, pending orders), you can edit, print, or complete an existing order request.

The Pending Orders and Standing Orders lists are ordered by "Requested" beginning with the most recent. Additionally, all Orders lists now use the list view remember capability so that when a user makes a change to the order in that listview, that preferred order will be stored for that user and will be consulted next time that listview is rendered

To search for a specific existing order, you can use the search engine at the top. These fields help to narrow down your search. You don't have to select in each search field, unless you know the specific information/fields you are looking/narrowing to. Clicking CLEAR underneath the search fields will clear the search fields for you to start over.

Once you have found your order that you are either searching for, or see on the Pending , Standing, Pending or Completed Orders sections, you can Edit, Print an existing order, or you can Complete a pending order request.

## Edit Orders

You must have security permission to edit orders.

Click Edit next to an existing order request to edit it.

![](order-requests-grid.images/image5.png)

Change/edit what you need to. If you need to change/edit/delete an order item (test), it will show all ???current' tests ordered at the top, then you can click the [-] button to delete an order item, or check-mark an order item you need to add to this order, etc.

If you edit it, you would then need to click REQUEST ORDERS at the bottom of the screen after any changes, then if need to re-print it you can do so at that time. It will save the latest/edited version of this order.

![](order-requests-grid.images/image4.png)

## Print Orders

Click Print next to an existing order request to print it (or fax it via the print/fax module).

It will take you to the print module and then X out of the print view/screen when done.

![](order-requests-grid.images/image7.png)

There is a system setting that can be enabled (Orders/Settings/Print Order Requests Without Headers) that can be enabled which will automatically have the *print without headers* checkbox checked by default (a user can always override the checkmark) when printing order requests from this Recent Orders screen.

## View Orders

Click *View* next to an existing order request to view it on the screen.

![](order-requests-grid.images/image6.png)

It will take you to the document summary to view the stored order document on the screen. You can print/fax from here using the top right toolbar options. There are also hyperlinks to edit order or add result. Edit Order will allow you to edit an order directly from this document view. You will be taken to the edit order screen and can make edits and click ???request orders' to save. Add Result will allow you to result the order items within this order document. It will create and open a Results encounter where the order items will be applied as in progress. Expand the order item sections in the Results encounter to checkmark as ???completed' and document data/results to capture. Close & Archive the Results encounter when done. Note: The main order request would still need to be marked entirely as ???completed' via the Order Requests chart tab.

![](order-requests-grid.images/image9.png)

X out of the view screen when done to get back to {{% system-name %}} .

## View Results

If you see an option link named View Results it means a document has been linked to this order. So, there could be the lab report with the patient's lab results linked to this specific lab e-order. *See other help documentation named Link Document to E-Order.pdf* You can link documents to orders from the indexing module or while in this e-orders module marking an order complete. When any document is linked to a specific order item(s) you can view the result directly here or go to the document and see what orders it's linked to via its properties.

![](order-requests-grid.images/image8.png)

## Complete Orders

To complete an order individually, click Complete and it will show the items/order. The Complete Order screen will then appear.

![](order-requests-grid.images/image11.png)

You must type in the date the orders were done, or pending or cancelled, comments, etc. Checkmark or un-checkmark any additional order items. You can set the entire order STATUS to the appropriate status or you can set specific order items status individually. You can also link a document in the patient's chart to the specific order item by filling out the Doc Id field. When you link a document (doc.id) to an order here, that linked document will show in View Results on the order. Linking a result document to the order is a quick way to see results on an order instead of hunting through the chart. *See other help documentation named Link Document to E-Order.pdf for specifics on linking results to orders and marking them complete.*

![](order-requests-grid.images/image10.png)
Then click the COMPLETE button. It will then put this order in the completed section of the view.

Then in the view of the closed order, it would show the items/orders and next to it the dates and times they were completed at the very bottom of the order document screen.

![](order-requests-grid.images/image14.png)

If you mark to complete a *standing order*, it doesn't remove the standing order. ??It creates a completed version of that order.?? To remove the standing order, you have to edit it and take out the order frequency, and then complete it.

## Check Boxes in Options Column

The check-mark boxes next to any order in the Order Requests screen is a way to set the category of multiple orders at a time. Or you can use the ???check all' checkbox at the top of each grid section.

![](order-requests-grid.images/image12.png)

Simply check-mark the box of the order(s) that you want to select, and then at the bottom of the specific grid section you are in, then use the drop-down to select the ???category' you wish to (in mass) set these order requests as. Then click the button "*Change Order Category"* and it will render the selected order requests to be the category you selected it to be set as.

You can complete the entire order or mark certain order items as complete.

![](order-requests-grid.images/image13.png)

Selecting the *Completed* category does not complete the order. It just sets the order as the completed category, but keeps the order request in the ???pending order requests' grid section. You must still go through the complete link to set the order items within the request to completed.

You can view the category a specific order is set to by viewing the category column.

![](order-requests-grid.images/image15.png)

You can also complete all (multiple in mass) with a Results encounter using the button *Add Results*. See section *Add Results* in this help guide.

## Add Results

The system will display a hyperlink Add Results in the options column, if the encounter visit type "Results" is set as active in the {{% system-name %}} system. If the encounter visit type "Results" is inactive, the *Add Results* functionality is disabled and not visible. There is also an ability to complete & add results to order requests in mass by checkmarking the order request(s) then clicking button *Add Results* at the bottom of the grid.

![](order-requests-grid.images/image16.png)

This is ability to complete an order request and document the results within a Results encounter. It will also generate/create a new "Results" encounter in the chart if system setting *Reuse Encounter when Completing Order* is disabled (value 0) which is the default behavior. The "Results" encounter is a dynamic encounter that has the following sections:

* Encounter Info
* Case (so that the encounter can be linked to a specific case/incident)
* Results
    * one section for each pending order_item from the pending order request
    * Incomplete orders & completed orders sections

The contents of these sections are determined by the layout name field in each order item.

* If the name of the order is the same as the name of a flowsheet and the layout is?? "Obs Procedure", that flowsheet will be displayed
* if the name of the order does NOT match the name of a flowsheet, the order's layout will be displayed if the order has a layout, otherwise the "Generic Order" layout will be used
* The Generic Order layout is essentially a place to enter an observation.?? The observation will have the same name as the order it came from.

After clicking the "Add Results" link, you will be taken directly into the "Results" encounter (that created upon your click) with 5 sections, all of which begin collapsed.

![](order-requests-grid.images/image17.png)

Click on the title section of an order item you wish to result to expand the section for data entry. In this example I clicked on the ANA section to expand it and enter a result?? ??? this is an example of the Generic Order layout

![](order-requests-grid.images/image18.png)

First, make sure to checkmark the *completed* box if this order is complete (or any other specific checkbox). The *complete* status checkbox marks the order as complete in the system in various places. However, checking anything else or not checking any of the boxes at the top will leave the order "In progress".

Key in/enter a result for the order item, and click the *NEXT* button.

![](order-requests-grid.images/image19.png)

If you had more order item sections on the "results" encounter, the next order item section would expand open.

In this example, I have an order whose name is the same as a flow sheet, and the layout is Obs Procedure, so we display this flowsheet that is linked/named the same as the order item.

![](order-requests-grid.images/image20.png)

Enter results, and click the *NEXT* button, and this order item will be marked as completed (whether or not you check the completed box).

![](order-requests-grid.images/image21.png)

In this example, I have a PFT which is an order item tied to a specific layout, but that layout name is NOT Obs Procedure, nor does the name match any flowsheet in this system, so we display the specific layout in the system.

![](order-requests-grid.images/image22.png)

Deleting an encounter order section from a Results encounter marks the corresponding order item on the order request as "pending", unlinks the encounter order from it, and revisions the order_request.

Archive & close the encounter when done resulting. The Results encounter will then store a document as the doc.type "Results" in the chart. It also stores a separate document named "Lab Results" in the chart based on the order item results you keyed in. This is an example of the "view" of the encounter document:

![](order-requests-grid.images/image1.png)

At this point, if you go back to view recent in E-Orders chart tab, all the items on the order request that you marked as *completed* will show status of ???completed' and the order items within the order request itself also get marked "Completed".

Deleting an encounter order section from a Results encounter marks the corresponding order item on the order request as "pending", unlinks the encounter order from it, and revisions the order_request.

Clicking on the View Results hyperlink, in the options column of the completed order(s), you will open up to the Lab Results document this encounter created.

![](order-requests-grid.images/image2.png)

{{% note %}}

Completing order requests with the Results encounter will attach the order request(s) **can** be set to open the most recent encounter IF they are all linked to the same dynamic encounter (meaning the order was generated from a specific dynamic encounter), and that encounter is either not closed or the use has permission to reopen a closed encounter, instead of it generating/creating a new "Results" encounter in the chart. The system setting *Orders*, *Settings*, *Reuse Encounter When Completing Order* sets this behavior if system setting value is set to enabled (value 1).

{{% /note %}}



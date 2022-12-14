---
title: "Label Printing Feature"
date: "2020-03-24T15:23:57.818Z"
url: "functions/document-management/printing-and-print-definitions/label-printing-feature.html"
version: 60
id: "1GBdtPDh7IhPpfruWnKD_qi1WRONcy9p6XhabXBWXl10"
source: "https://drive.google.com/open?id=1GBdtPDh7IhPpfruWnKD_qi1WRONcy9p6XhabXBWXl10"
menu:
    main:
        name: "Label Printing Feature"
        identifier: "1GBdtPDh7IhPpfruWnKD_qi1WRONcy9p6XhabXBWXl10"
        parent: "1NHBPyY_YvI92JSil-rc3O0Kpu5qYLkdKWZTNjlzQpNY"
        weight: 780
---
{{% system-name %}} offers a label generating feature that generates labels with predefined chart information. The data and information printed on the labels is provided as part of the system standard; however, label layouts can be customized for clients, as needed.

{{% note %}}

Dymo Web Service is required for printing labels out of {{% system-name %}} .

{{% /note %}}


Dymo LabelWriter printers are recommended for printing labels from the {{% system-name %}} system. The Dymo LabelWriter models 300, 330, 400, and 450 Turbo have been tested with {{% system-name %}} and integrate with no problems. The Dymo LabelWriters are typically very easy to install at a workstation, consisting of simply plugging the USB port into the computer and installing the necessary drivers. Most Dymo printers will come with a starter roll of labels, and other sizes can be purchased for varying needs.

## Printing Labels

By default, labels print with the following demographic information included:

* Today's Date
* MR#
* Gender
* Chart Name
* Date of Birth

MIE can customize this layout, if necessary.

Printing labels can be done from various places throughout {{% system-name %}} . Depending on the workflow and user role, accessing labels for printing can be accomplished several different ways. Below, information is provided for accessing and printing labels from quick links, the chart header, the scheduler, as well as from an order request.

### From Chart Quick Links

Links for generating labels can be configured and made available on the **Quick Links** portlet of the **Summary** chart tab.

![](label-printing-feature.images/image1.png)

Whenever the **Dymo 450 1.25 x 2.25** link is clicked from the Quick Links portlet of the Summary chart tab, users will print a 1.25 x 2.25 sized label, with the standard demographic information, seen above.

Once the link has been clicked, a preview of the label data will show when the Print screen loads. Clicking the **Print** button will open the *Print Dialog* window, where the specific Dymo printer needs to be selected in order to print.

![](label-printing-feature.images/image3.png)

{{% tip %}}

Ensure the selected printer matches the Dymo installed for use. Also, to verify the label size being printed for the first time, click the **Preferences** button after selecting the appropriate Dymo LabelWriter printer. Then go into **Advanced**, and review the Paper/Dymo Label Size.

{{% /tip %}}


Another available link from the Quick Links portlet is the **Select Label** link. Clicking this will open a pop-up window, where the user can choose a different Dymo label size for printing. When an alternative size is selected, the label data preview will load, and clicking the **Print** button will open the Print Dialog box, as before.

![](label-printing-feature.images/image2.png)

### From Print Chart

Labels can also be generated using the Print Chart functionality, which allows for printing established Print Definitions. Printing labels using the **Print Chart** link is not configured in {{% system-name %}} by default.

![](label-printing-feature.images/image5.png)

In order to provide this functionality, MIE will need to create a custom layout, including all of the necessary data for the label. Then, the Print Definition can be established and programmed with a section mapped to the custom layout. Once the Print Definition is configured, users can print labels using the Print Chart link.

![](label-printing-feature.images/image4.png)

### From Scheduler View

A system setting ("Scheduler", "Settings", "Print Labels") is enabled, by default, so that users may generate and print labels for all scheduled appointments shown for the day in context. If the system setting is disabled, users will not see the **Print Labels** link in the upper-right corner of any of the Scheduler views.

![](label-printing-feature.images/image7.png)

Labels printed from the Scheduler contain the following demographic information, by default:

* Appointment Date
* Appointment Time
* MR#
* Gender
* Chart Name.

MIE can customize this layout, if necessary.

When the **Print Labels** link is clicked from a scheduler view, a preview of the data will load, with a Print button toward the top-middle of the page. Click the **Print** button to open the Print Dialog window and print one label for every scheduled patient appointment listed for the day. Otherwise, if the labels are no longer needed, instead of clicking the Print button, simply click the X in the upper-right corner to exit the screen.

![](label-printing-feature.images/image6.png)

### From Order Requests

Though not available in the standard product by default, a label can be custom programmed to print chart information onto a label that can then be used for the order being sent out. For instance, when sending a vial with an order, a label with the relevant data can be printed and affixed to the vial, prior to sending.

The *Order Label* layout must be established within {{% system-name %}} , with configuration done by MIE. Once the layout exists, the **Label** link will usually display in the Orders module. To view the Label link and print any custom configured labels, ensure the appropriate system setting ("Orders", "Defaults", "Auto Print on Summary") is enabled.

To print a label associated with an Order Request, click the **Label** link after successfully creating the Order Request.

![](label-printing-feature.images/image9.png)

Once the page loads, click the **Print** button. Verify the correct printer is selected, and click Print.

![](label-printing-feature.images/image8.png)

Labels for Order Requests can also be generated and printed from the **Order Requests** chart tab. This is where all Order Requests for the chart are listed according to category. In the *Options* column of the grid, a **Print Label** link is provided. Users may print labels for Order Requests, as needed.

![](label-printing-feature.images/image11.png)

#### From Encounter View

Orders are often created when working in an encounter. Because of this, {{% system-name %}} has made it so users may generate and print labels from the encounter view, whenever encounter-generated order requests are created.

At the end of the encounter view, a section is available for listing all encounter Order Requests: *This encounter has order requests*. There is a **Label** link in the *Options* column, which can be used for generating and printing a label for each Order Request.

![](label-printing-feature.images/image10.png)

For more information, please review the [Order Requests Chart Tab](../../order-and-result-management/e-orders-chart-tab.html) documentation.


---
title: "Quick View - Alerts Portlet"
date: "2020-03-09T21:13:03.975Z"
url: "functions/e-chart/quick-view-alerts-portlet.html"
version: 72
id: "186D5E2YzP5S2VzWpfh0w1LGZRRTIKXE32MdKPDITglY"
source: "https://drive.google.com/open?id=186D5E2YzP5S2VzWpfh0w1LGZRRTIKXE32MdKPDITglY"
menu:
    main:
        name: "Quick View - Alerts Portlet"
        identifier: "186D5E2YzP5S2VzWpfh0w1LGZRRTIKXE32MdKPDITglY"
        parent: "1DIVVSjNfv48-LekRsKDHFuHEm1gBYphsCC18iR2WikU"
        weight: 940
---
There is an interactive [Quick View](https://system/) available to end users. The Quick View offers various summary portlets that are used as quick references for viewing modules and data in {{% system-name %}} .  For example, your pending tasks, the appointment schedule, worklists, dashboards, and the like are types of portlets available for quick access and management. You can select which specific portlets to show on your view. One of the portlets is **Alerts**.

When logged into {{% system-name %}} , click on the [Quick View](https://system) sidemenu option.

![](quick-view-alerts-portlet.images/image14.png)

When in Quick View, default portlets will display, but there is an option to customize the Quick View for yourself if have the appropriate security permissions.

## Alerts Portlet

The **Alerts** portlet of the [Quick View](https://system/) shows a summary of each failed module name (what type of job failed), as well as a column of who the failed jobs are designated to. **Me** means the failed job was something the logged-in user had rendered to send. **Everyone** means the failed job was something another user in the system rendered to send.

![](quick-view-alerts-portlet.images/image7.png)

If you do not see the Alerts portlet in the Quick View tab, simply click the **Select Portlets** and select the **Alerts** portlet, then save. The selected portlets will display on the Quick View screen ,and you can move them around in the order you wish them to display.  Refer to other [Quick View Sidemenu](quick-view-sidemenu.html) help guide for more information regarding the {{% system-name %}} Quick View.

![](quick-view-alerts-portlet.images/image6.png)

## Alerts Notification Toolbar

An **Alerts** link and a counter are shown on the notification toolbar, so that the logged-in user can quickly see a count of the errors from the Print, Fax, Dicom and DataSend modules, generated for the logged-in user. If the logged-in user's **Show Alerts** [My Settings](https://system/) preference set to system, then the alert in the notification toolbar will also display a count including any errors system-wide, including the logged-in user's print or fax or dicom or failed jobs.

![](quick-view-alerts-portlet.images/image24.png)



## Alerts/Errors Dashboard

Clicking the [Manage Information](https://system/?f=layout&module=Warnings&name=AlertsPage&tabmodule=none) icon in the **Alerts** portlet of the Quick View, or clicking the **Alerts** link in the notification toolbar at the top, will take you to the Alerts/Errors dashboard to view and work any failed jobs.

![](quick-view-alerts-portlet.images/image19.png)

The Alerts/Errors dashboard is where you can view the specific failed job details and work any failed jobs, if needed.  

![](quick-view-alerts-portlet.images/image18.png)

Once you are in the Alerts/Errors screen, the alerts will display, based on the preference you have set.  If you are set to only show your own alerts/errors, then that is what will display.

### Select Portlets

The **Alerts** portlet is comprised of 4 individual portlets. The 4 individual portlets are **Print Alerts**, **Fax Alerts**, **AutoSend Item Alerts** and **DICOM Alerts**. Users may arrange the Alerts/Errors dashboard in any order they wish, or remove portlets no longer needed.  Simply click the **Select Portlets **link found in the top-right of the Alerts/Errors dashboard.

![](quick-view-alerts-portlet.images/image23.png)

{{% tip %}}

Even though you can change the dashboard to display in 2 or more columns, it is recommended you display the dashboard in a one-column format.  This allows users to see the entire sections, along with the options in order to work them from this dashboard.

![](quick-view-alerts-portlet.images/image8.png)

{{% /tip %}}


When done setting the portlets for the Alerts dashboard, click the **Save** button. When refreshed, users can then move the portlets around on the screen, as needed. You can still move the portlets in a different order, even in one column viewing.

### Preferences

To change the Alert/Errors preferences, click the **Preferences** link on the [Alert/Errors dashboard](https://system/?f=layout&module=Warnings&name=AlertsPage&tabmodule=none).

![](quick-view-alerts-portlet.images/image9.png)

From the Preferences pop-up screen, some {{% system-name %}} preference settings will display, so that you can change your selections as needed and click the** Save** button.  The two preferences that are tied to the Alerts/Errors dashboard and notifications are the **Show Alerts** and the **Show Alerts For** preferences.

![](quick-view-alerts-portlet.images/image2.png)

## Fax Alerts

The **Fax Alerts** portlet shows any failed faxes for the logged in user, or system-wide, based on the preference setting. Users can **Resend** the failed fax, **Acknowledge**, or **Stop** the fax from the portlet. Users can also click the **Manage Information** icon within the Fax Alerts portlet.

![](quick-view-alerts-portlet.images/image16.png)

Clicking the [Manage Information](https://system/?f=admin&t=faxman) icon will take you to the **Fax Manager** tab of the sidemenu. This is where usres can see the **Error Fax Spool**, with the specific details of the failed fax jobs and all the specific options available for working failed faxes.  For more information on this screen and how to work failed faxes, reference the [Fax Manager Tab](../fax-manager/fax-manager-tab-outbound-faxing.html) documentation.

![](quick-view-alerts-portlet.images/image22.png)

Another way to view details on a failed fax job, or get to the Fax Manager, is to click [Failed Fax Jobs](https://system/?f=admin&t=faxman) when looking at the Alerts portlet of Quick View. The portlet displays a quick summary of the failed jobs, but the failed items on the Alerts portlet provide hyperlinks to take users to the Fax Manager more easily, instead of from the Alerts/Errors main dashboard.

![](quick-view-alerts-portlet.images/image13.png)

## Print Alerts

The **Print Alerts** portlet shows failed print jobs for the logged-in user or system-wide, based on the preference setting. Users can view the failed print jobs from this screen and click the **Job ID** to see the details of the specific print job. And users can delete the print job from here, as well. You can also click the **Manage Information** icon within the Print Alerts portlet, as needed.

 ![](quick-view-alerts-portlet.images/image10.png)



Clicking the [Manage Information](https://system/?m=admin&t=printman&tabmodule=admin&tabselect=Print+Mgr) icon will take you to the **Print Manager** tab of the sidemenu. This is where users can see the **Error Print Spool**, with specific details of the failed print jobs, along with the option to delete the failed print jobs, as needed. When viewing a specific print job from the Job ID, users can reprint so that a view of what was to print will be generated. For more information on this screen and how to work failed print jobs, reference the [Print Manager](../system-administration/system-controls/print-manager.html) documentation.

![](quick-view-alerts-portlet.images/image20.png)

Another way to get to the Print Manager is to click [Failed Print Jobs](https://system/?m) when in the Alerts portlet of Quick View. The portlet displays a summary of failed jobs, but the failed items in the Alerts portlet provide hyperlinks to take users to the Print Manager quick and easily.

![](quick-view-alerts-portlet.images/image5.png)

## DICOM Alerts

The **DICOM Alerts** portlet shows failed DICOM jobs for the logged-in user or system-wide, based on the preference setting.  The {{% system-name %}} system must be setup for DICOM functionality for this portlet to be useful. You can view the specific failed DICOM jobs from this portlet.

![](quick-view-alerts-portlet.images/image11.png)

Clicking the [Manage Information](https://system/?func=dicom&dcfunc=queue) icon will take you to the **DICOM Setup** tab. This is where users can see the **Failed** category, with specific details of the failed DICOM jobs and their respective **Request ID**s. For more information on this screen and how to work failed DICOM jobs, reference the [Dicom Setup Tab](../document-management/imaging/dicom-setup-tab.html) documentation.

![](quick-view-alerts-portlet.images/image21.png)

Another way to get to the DICOM Setup tab is to click [Failed DICOM Jobs](https://system/?func=dicom&dcfunc=queue) when in the Alerts portlet of Quick View. The portlet displays a summary of failed jobs, but the failed items on the Alerts portlet provide hyperlinks to take users to the DICOM Setup tab quickly and easily.

![](quick-view-alerts-portlet.images/image4.png)

## Auto-Send Items Alerts

The **Auto-Send Item Alerts** portlet shows failed datasend jobs for the logged-in user or system-wide, based on the preference setting. The {{% system-name %}} system must be set up for auto-routes and auto-send functionality for this portlet to be useful. Options are also available to perform an **Acknowledge**ment, **Resend**, or **Deactivate** en masse, if necessary.

![](quick-view-alerts-portlet.images/image12.png)

* <strong>Acknowledge</strong>: Clicking this after an autoroute has failed indicates you acknowledge it errored out, removing it from the queue.  

{{% note %}} If information, or document or chart info, ever changes or gets updated, then the auto-send route will be resent. {{% /note %}}

* <strong>Resend</strong>: Clicking this will attempt to resend the failed route.
* <strong>Deactivate</strong>:  Clicking this means that you no longer want the errored route to be sent and wish it to never try sending again.

If you wish to work the data-send/auto-route failures en masse, select each failed route and use the drop-down **Select Error Routes** to select an option that will be applied to all that were checked.

![](quick-view-alerts-portlet.images/image25.png)

Clicking the [Manage Information](https://system/?func=dicom&dcfunc=queue) icon will take you to the **DataSend Queue** tab. This is where you can then see the **Error Routes** category, with specific details of the failed auto-send routes and the specific Route IDs.

![](quick-view-alerts-portlet.images/image3.png)

There is a **Break Sending Lock** security option for MIE Help Support. This option is for routes marked as **Sending** in the [DataSend Queue](https://system/?func=dicom&dcfunc=queue). This feature allows the unlocking of any routes which have been stuck for more than an hour. Users wishing to have this ability will need the **Unlock Sending Routes** security permission enabled. In the case of a coding error, routes can become stuck in the **In Progress** status. The Break Sending Lock option allows MIE Help Support, or others with the necessary permissions, to retry these stuck routes without reverting to a backend tool.

![](quick-view-alerts-portlet.images/image1.png)

Another way to get to the DataSend Queue tab is to click [Failed Auto-Send Items](https://system/?func=dicom&dcfunc=queue) when in the Alerts portlet of Quick View.  The portlet displays a summary of failed sends, but the failed items in the Alerts portlet provide hyperlinks to take users to the DataSend Queue tab quickly and easily.

![](quick-view-alerts-portlet.images/image17.png)

## No Pending Alerts

If there are no failed jobs for any of the 4 categories, then the portlet will display the message **No pending alerts**.

![](quick-view-alerts-portlet.images/image15.png)




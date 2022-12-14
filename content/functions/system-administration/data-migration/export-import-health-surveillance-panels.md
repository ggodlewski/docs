---
title: "Export/Import Health Surveillance Panels"
date: "2020-02-27T20:23:52.293Z"
url: "functions/system-administration/data-migration/export-import-health-surveillance-panels.html"
version: 28
id: "1j39ny5DDziJwxeD0un6Js_fsVo6zi4TPZO39svw95oU"
source: "https://drive.google.com/open?id=1j39ny5DDziJwxeD0un6Js_fsVo6zi4TPZO39svw95oU"
menu:
    main:
        name: "Export/Import Health Surveillance Panels"
        identifier: "1j39ny5DDziJwxeD0un6Js_fsVo6zi4TPZO39svw95oU"
        parent: "1uT8WLYj42KO6Q0YgNCoxLH8RikMH_C6IBQjUmhLSaWU"
        weight: 4800
---
Users must have security access to be in Health Surveillance Management control tab. On the sidemenu tab, click the CONTROL tab. Once in the Control tab, click the HEALTH SURVEILLANCE tab at the top menu of tabs.

![](export-import-health-surveillance-panels.images/image6.png)

The listing of current active Panels will display automatically on the screen under the Panel Search criteria fields. At the bottom of the listed active, current panels, you will see hyperlinks to Export Panels and/or Import Panels

![](export-import-health-surveillance-panels.images/image8.png)

Your MIE Implementer will most likely be utilizing this functionality the most, but if you have a Dev or QA system, you may be utilizing this functionality to export panels into your other dev or QA systems back and forth.

## Export Panels

First, you must go to the system you want to "export" panels from. This is essentially the same as a "copy/paste" type of functionality. You will go to the system you wish to export a panel(s) from. When you are in that system, and in the Health Surveillance Tab found in Control, click the Export Panels hyperlink. Checkmark the panel & details you wish to export into another system.

![](export-import-health-surveillance-panels.images/image7.png)

If you are in a system with a plethora of panels, you may want to utilize the "search" in the panel screen first, then click Export Panels because the export functionality will only pull panels to checkmark (to export) that are shown on the screen itself before clicking Export Panels. So in this example I only want to export a TB Surveillance panel from a system that has a ton of panels configured. So first 1) I used the panel search by typing in TB and clicked the "search" button to find the panel I wanted to export. Then 2) I clicked export panels, then 3) made sure only that panel named TB Surveillance was checkmarked. This weeds out all the other panels I don't want to copy in that the originating system may have. It saves me time from *un*checkmarking a lot of panels that I don't want to export.

![](export-import-health-surveillance-panels.images/image10.png)

Once you have your panel(s) checkmarked that you wish to **export**, click the SHOW DATA button. This places the HTML programming in the text box below it.

![](export-import-health-surveillance-panels.images/image9.png)

Click your mouse within the HTML programming text box, then on your keyboard, hit *Control* and the *A* key. This will highlight all the HTML programming in that text box. Right click (on your mouse) and select *Copy* (or Control and the C key). Then click the red X at the top right corner of the Export Panels pop-up window. You are now ready to import that panel programming into another system.

![](export-import-health-surveillance-panels.images/image2.png)

## Import Panels

To import a panel, you must have first copied an exported panel using the steps above. You must then go to the system you want to "import" the panel(s) into. This is essentially the same as a "copy/paste" type of functionality. You will go to the system you wish to import a panel(s) to. When you are in that system, and in the Health Surveillance Tab found in Control, click the Import Panels hyperlink. A blank text field will appear with the title *Import Panels*.

![](export-import-health-surveillance-panels.images/image1.png)

Within the blank text field you will click your mouse, then right click and select *"paste"* (or Control and the V key).

![](export-import-health-surveillance-panels.images/image4.png)

You will see the HTML panel data programming get pasted into the free text field of the Import Panels window. Click the IMPORT DATA to submit and import all the panel(s) previously selected to export and will thus import into this system.

![](export-import-health-surveillance-panels.images/image3.png)

Once you've clicked the IMPORT DATA button, a pop-up will show you statuses.

![](export-import-health-surveillance-panels.images/image5.png)

For auditing purposes, we recommend you going into the newly imported panel to make sure all action items/rules, order items, contraindications, appt types, visit types, events, etc are set and imported the way you wish. Of course, you can edit any panels once it's imported. This is a quick way to copy/paste panels from one system into another and then tweak/edit to what you need specific.


---
title: "Work Status"
date: "2020-03-13T12:22:51.837Z"
url: "functions/injury-care/work-status.html"
version: 65
id: "1EuB61nCaNeWo6leAxOJQb9kK8Vqqhba95SNwjTa-6_0"
source: "https://drive.google.com/open?id=1EuB61nCaNeWo6leAxOJQb9kK8Vqqhba95SNwjTa-6_0"
menu:
    main:
        name: "Work Status"
        identifier: "1EuB61nCaNeWo6leAxOJQb9kK8Vqqhba95SNwjTa-6_0"
        parent: "111B4lq1O-rlxqSGXZpADmFAnK_djV5fVFecDJ4R6mXY"
        weight: 1720
---
When written opinion data is keyed into the recommendation section of an encounter, it fills in the Work Status report. Work Status information/documents are found in an encounter additional view, the Work Status chart tab, patient portlet, portal employee page, and portal supervisor page. The Work Status is a summary of an employee's health surveillance status, and can be used by an employer to determine eligibility as to whether the employee is fit to perform his/her duties. It is designed to show current restrictions, off-work status, return to work date(s), and medical clearance determination in real-time.

The Work Status document is made up of several key parts: Demographics information, current restrictions/accommodations, health surveillance status, open claims, provider info, and whom to contact.

## Recommendations Section of Encounter

To work a health surveillance recommendation and generate a work status document, expand the Recommendations section of an encounter.

![](work-status.images/image1.png)

Under the grid showing any recommendations (medical opinions) that are on the patient's pending due list, there is a checkbox to *Generate Work Status Report*. When checkmarking this, it will create an additional view when the encounter is closed/archived and it will create a separate Work Status document. Note: A Work Status document can always be created via the Work Status Chart Tab instead, but this is ability to do it while working in an encounter and is optional here.

![](work-status.images/image3.png)

The free text box for *Work Status Introductions* is an optional are to free type an introduction if this work status document is going to go to someone specific (ie: shared to a supervisor) and you want to type in some free text for an introduction making it more personal or offering expanded content.

Then apply the specific recommendation to the encounter exam that an opinion will be generated on. See separate help documentation titled *Encounters-Recommendations Section.*

When done working in the Recommendations section of the encounter, when you go to the encounter ???view', the Recommendations section is shown along with any work status report generated introduction verbiage.

![](work-status.images/image2.png)

If the *generate a work status* checkbox was checkmarked in the Recommendations section of the encounter, upon close/archive of the encounter, it will produce a separate (additional view) document stored to the patients' chart named *Work Status Report* which you can see on the encounter ???view' of all documents archived from the encounter.

![](work-status.images/image5.png)

The additional view on the encounter if *generate work status report* was checkmarked:

![](work-status.images/image4.png)

Work Status reports are stored in the Work Status chart tab and document summary chart tab.

{{% note %}}

The Work Status Report and the recommendation (medical/written opinion) store as separate documents but collectively comprise information together.

{{% /note %}}


![](work-status.images/image7.png)
## Work Status Chart Tab

The Work Status chart tab in a patient/employee chart houses all Work Status information. The top portion of the screen displays the last most recent recommendations (health surveillance) status data. This information displayed here is the most recent, current, real-time status information done from encounters recommendations section.

![](work-status.images/image6.png)

At the bottom of the Work Status chart tab is a listview of previous stored Work Status report documents.

![](work-status.images/image10.png)

Not always does one *generate a work status report* when working in an encounter. Once can do it quickly for more up to date information here from the Work Status chart tab. Simply click the *Create Work Status Report* button found here in the tab under the current work status information displayed.

![](work-status.images/image8.png)

Once that button is clicked, the system will create a work status report document to store in the patient's chart of the information that was displayed within the Work Status tab that was displayed at the time of the button click. The stored document is accessible from the listview at the bottom of the tab. It can be shared via print, fax, batch, etc.

![](work-status.images/image15.png)

Work status stored documents are also accessible from within the patient's chart Summary chart tab within the portlet *Documents*.

![](work-status.images/image11.png)

And from the Document Summary chart tab within the patient's chart.

![](work-status.images/image13.png)

## Work Status Portlet

The Work Status portlet (in the Summary chart tab) of a patient/employee chart displays real-time Work Status information. This portlet is here for quick viewing. Any recommendation surveillance status that was marked as ???completed' will display surveillance status info in this portlet. The same information is visible in the Work Status chart tab. Previous stored/generated work status ???documents' are stored within the Document Summary tab or Work Status tab listview as described in pages above.

![](work-status.images/image16.png)

## Work Status Changes

Surveillance Changes section of displayed work status information (or in a generated work status report) will show data if the patient has previous status updates. If the patient had a previous health surveillance panel status and you had to re-enter recommendations on an existing current encounter, you will get the "Changes" section.

![](work-status.images/image17.png)

Whereas the "Status" section just lists all current surveillance panel statuses.

![](work-status.images/image18.png)

## Work Status Email

An email template named *Pat Work Status Report* can be utilized to email and share the same real-time work status information displayed in the Work Status chart tab and Work Status portlet from the Summary chart tab. This is available from within the patient's chart via the Email hyperlink.

![](work-status.images/image19.png)

![](work-status.images/image19.png) ![](work-status.images/image19.png)

## Portal

The Supervisor Portal can be setup with a Work Status menu.

![](work-status.images/image20.png)

From within the Work Status portal menu in the Supervisor Portal, if a supervisor user has employee charts linked to them, the supervisor can view shared Work Status documents if configured. The Work Status displayed here in the supervisor portal must be a stored document in the patient's chart. Therefore the ???generate work status report' steps must have been done to generate a stored document in the patient's chart. The last, most recent stored Work Status document is shown here in the Work Status menu of the Supervisor Portal.

![](work-status.images/image21.png)

## Optional System Settings

There are two system settings that can be enabled or disabled that affect the Work Status. If enabled or disabled by a superuser, it will enable or disable for the entire system. These are *Include Open Claims* and *Panel Membership Expiration Day Limit.*

![](work-status.images/image9.png)
* <strong>Panel Membership Expiration Day Limit:</strong> The default value is "0" indicating disabled.?? If enabled, key in a number (in the value field) which would then be interpreted as the number of days.?? The Work Status pages (portlet, chart tab, encounter views) will display any expired panel memberships based on the value of this system setting if enabled.?? Expired means it's past the ???next due date' on the panel status. This setting is used in the work status pages so that it displays expired panel memberships on a chart only pas a specific set (value) number of days.?? By default, the work status pages include any/all panels on a patient where the panel expire date is between this system setting value (0) days ago and today/now.?? If this system setting were to have a value of 5 and today's date were 9/14/2017, the work status will show/include all panel memberships for a chart between 9/9/17 and 9/14/17 whether active or expired.
* <strong>Include Open Claims:</strong> The default value is "1" indicating enabled. This displays any/all open cases (whether they be work comp or not) on the Work Status report tab, generated stored document, and elsewhere (ex: portal) where Work Status is viewed. If the system setting <em>Include Open Claims</em> is enabled (is enabled by default), the section <em>All Open Cases</em> will display any case the patient has in their chart on Work Status areas/documents regardless if the encounter (where the surveillance status was generated from) is tied to a specific case or not.

![](work-status.images/image12.png)

{{% note %}}

If the encounter the Surveillance Status was generated from is linked to a specific case, then the linked case information will display in the *Related Case* section anytime viewing a Work Status document or Work Status chart tab, etc. Meaning, *related case* section will always display on any work status area if the specific encounter (where surveillance status/recommendation was completed in) was linked to a case.
{{% /note %}}


![](work-status.images/image14.png)

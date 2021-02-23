---
title: "Routing Dictation"
date: 2020-02-27T19:51:41.120Z
url: "general-functionality/encounters/dictation-and-transcription/routing-dictation.html"
version: 18
id: 1G_lwgCWBmPq5y3sTMpOJwNK_nHZ-SLcW8C1kAxRMJc8
source: https://drive.google.com/open?id=1G_lwgCWBmPq5y3sTMpOJwNK_nHZ-SLcW8C1kAxRMJc8
menu:
    main:
        name: "Routing Dictation"
        identifier: "1G_lwgCWBmPq5y3sTMpOJwNK_nHZ-SLcW8C1kAxRMJc8"
        parent: "1jkkaykbJisElVA3anGLWgyfNIofH_SABJNTgiH2TMOY"
        weight: 1360
---
Dictation uploaded can be routed with special rules. Contact your MIE Implementer if you wish any dictation that uploads to be routed to a specific user (transcriptionist), for a specific job type, etc. Many different routes (rules) can be programmed to look at uploaded/incoming dictation. Please contact your MIE Implementer for help.

You must have security access to *Routing Tab Access* set to Yes. If you are set to no, you will not even see the Routing tab in the Dictation sidemenu tab. If you have security access to the Routing tab, you will see the Routing tab at the top of the Dictation sidemenu tab feature.

![](../../../external_files/3d9e1bd3cf6590e72a540514dbaed7e2.png)

The routing can be set up in {{% system-name %}} and to view any existing dictation routing rules can be viewed by clicking the sidemenu tab named DICTATION, then click the ROUTING tab at the top.

Your practice's existing active dictation routing rules will display. These rules can automatically route specific dictation job types and by specific dictators who created the dictation to a specific transcriptionist if you have routing rules set up.

![](../../../external_files/0ec24651d0d4ab24c4aca673b809e069.png)

Dictation can be routed regardless if it's uploaded via phone or from within {{% system-name %}} . Routing rules are processed in order of priority and searching for another rule stops when one rule matches the dictation.

## Add Dictation Route

You can add a dictation route if you are familiar with html where clauses. Otherwise, please contact your MIE Implementer and let them know what you want routed and they can set up for you.

To add a dictation route, simply click the Add Dictation Route link found in the Dictation Routing tab.

![](../../../external_files/0ec24651d0d4ab24c4aca673b809e069.png)

The Add Dictation Route fields will open on your screen.

![](../../../external_files/a590d35c99c1e51315a62163ecb68db7.png)

* <strong>Route ID:</strong> This is automatically set internally with programming within the software. {{% system-name %}} will give the new route a specific route ID that it tracks and works from.
* <strong>Priority:</strong> Set the priority of the rule. The higher the number, the higher the priority level the rule will search dictation for. This is not the priority of the dictation the dictation is set at; this is the priority of the dictation route that the system should search the dictation for and the higher the route priority is the route that will be searched for first. As soon as it finds a dictation that matches a route rule, it will stop and follow that dictation into that route rule.
* <strong>Comment:</strong> Must type out exactly what this route rule is searching for and who it's routed to and what the route rule is doing/searching for. This helps users see what the route is set for. This is a required field and you must type comments here.
* <strong>Where Clause:</strong> Enter in the html where clause of what the rule is to look for. Contact your MIE Implementer to set this up. If the html where clause is invalid, it will tell you that and not allow you to save the route.
* <strong>Set Clause:</strong> Enter in the html set clause of what the rule is to do once a dictation is found that matches this rule. Contact your MIE Implementer to set this up. If the html set clause is invalid, it will tell you that and not allow you to save the route.

Click the ADD ROUTE button once you have the route programmed. For help programming dictation routes and making sure correct priority of the rule is looked at, please contact your MIE Implementer.

You can also edit or delete routes that exist using those links in the options column.

![](../../../external_files/30079a768259bac8563cf1dc355bd569.png)

## Examples of Routes

This example shows a high priority rule set to look for any uploaded dictation set as priority 2 and priority 3 and will route those specific priority 2 & 3 dictations to user Judy Sample (user id#1122). The priority is set at 3 for the ‘route' because the higher the route priority, the higher the rule is placed to look for that dictation rule on dictations that are uploaded. The comment explains what this route rule is looking for and what it will do. The Where Clause is the html where clause that looks for the uploaded dictation priority that is set on the specific dictations. The Set Clause is the html set clause that assigns the uploaded dictation that it found (that matches this rule) and assigns it specifically to user #1122.

![](../../../external_files/348e7f4583e94ac08a347e5f5c8b5f32.png)

This dictation route example below shows an example of all dictation uploaded by Dr Sample (user ID #1110) will be assigned to transcriptionist user Margaret Beam (user id#2221). Their ID number is found in their username screen in control tab. All of Dr Sample's dictations will be routed and assigned to Margaret Beam to transcribe. These dictations will be placed/assigned then to her and placed in her pending queue to transcribe because of this route rule.

![](../../../external_files/832b47fcc9b9162ffe1bfc661b28ab8d.png)

This dictation route example below shows an example of all dictation uploaded as job type 6 (LETTER doc.type) is to be assigned to transcriptionist Penny Hall (user ID# 1010). All dictations uploaded as job type #6 will be assigned to Penny Hall to transcribe and assigned to her and only show in her pending queue to transcribe.

![](../../../external_files/dbdc2ac496f3ec54c0ebcbaa4f2900ac.png)

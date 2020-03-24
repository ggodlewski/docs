---
title: "Drug Guide Search"
date: 2020-02-27T20:04:35.130Z
url: "drug-guide-search.md"
id: 1yfB8xD-yey4VBd_Yzka0pkd_PGCMq8s9GmZHCCbZiLA
source: https://drive.google.com/open?id=1yfB8xD-yey4VBd_Yzka0pkd_PGCMq8s9GmZHCCbZiLA
menu:
    main:
        name: "Drug Guide Search"
        identifier: "1yfB8xD-yey4VBd_Yzka0pkd_PGCMq8s9GmZHCCbZiLA"
        parent: "1BT9iwpUSk65PGOkXhOqxTjwNvG-JzY6aKqNw1elTkKA"
        weight: 2130
---
{{% system-name %}} currently imports the First DataBank (FDB) update files on a weekly basis on Saturday mornings at 2 am. MIE then does a complete dump and reload of our databases based on these files. At the end of this process, we update a table in the database that keeps track of changes in the database. A nightly job on each of the client servers checks for updates in the database file, and updates the rxdb database on the server from our "home" version of the database if necessary.

We do not "message" after updates these updates. However, we do have a message on the Drug Guide that you can see what the version is. The Drug Guide Search feature is usually found in the sidemenu tab named References, however in your particular {{% system-name %}} system, it could be found in the Omniscope side tab or in the E-Chart tab. It is also found while prescribing in the e-meds module. Wherever your particular Drug Guide Search program is, when you get to that program you will see under the Drug Guide search field bar for example: **Drug database version: 2.400, last updated 2010-06-12 02:16:17**

This shows the last time we have updated the Drug database (not the rxdb as a whole, it looks specifically only for updates called ‘FDB Update') on the server box the system is looking at. This mainly gives MIE information to make sure the client is getting the updates we are putting out in our "home" base version. If there is a problem with the home base version for some reason (even if this is up to date), this will have an issue, but MIE would be alerted internally that there is an issue with the mainline not getting updated properly.

![](external_files/a6c94fdebda62bc8d59c4a431bbb84ee.png)

The Drug Guide program offers a search where you can look up a specific drug and see all the drug guide information for that drug. There are two ways to access the Drug Guide Search: (a) through the Drug Guide Search tab usually found in the References sidemenu tab or in the Omniscope sidemenu tab or in the E-Chart sidemenu tab (b) while prescribing in the e-meds module.

## Drug Guide Search Tab

This is where the Drug Guide Search program is found within the References sidemenu tab:

![](external_files/a6c94fdebda62bc8d59c4a431bbb84ee.png)

This is where the Drug Guide Search program is found within the E-Chart sidemenu tab:

![](external_files/922efbfe218ae640a6da0662d6cd1cd0.png)

Once you are in the Drug Guide Search program, there are search criteria fields you can set to find the drug you want to view guide information on.

* <strong>Search For:</strong> If you start typing the name of the drug (brand or generic) and it will auto-complete to match your typing and give you choices. The search criteria of ‘drug name' is automatically the default. You can change ‘how' you want to find the drug you need by changing the drop-down choice (see next page).

![](external_files/0ba3c2776b1a767d78a6449ba1ec576a.png)

* <strong>Additional Criteria Dropdown:</strong> You can change ‘how' you want to find the drug you need by changing the drop-down choice. It automatically defaults to search by ‘drug name' but you can select any other method of search you wish. Simply click your mouse on the drop-down and it will open other selections.
* <strong>Only Active Drugs:</strong> This is automatically check-marked unless you system setting has been changed. Having this checkmarked means you are narrowing down your drug search to only search and find active drugs, not drugs that have been marked inactive by First DataBank.

![](external_files/acbca28f5c9eda03da1490500d01c1fb.png)

Once you have your search criteria set in the above fields, click the SEARCH button. It will show any possible matches on your screen for you to select that match the search criteria you set. If you searched for something more specific and there was only one match, it will open your screen right to that drug and guide information.

The Drug Guide for the drug found is a lengthy document that shows various details of that drug when you scroll down the page.

![](external_files/f476e4cf68eae1ad685bc1eab9817ed9.png)

The drug guide also has a section for formulary. Currently {{% system-name %}} only displays Medicare Part D drug plans and formularies. You can select the patient's state/county and Medicare Part D drug plan and click the display button to show the applicable formulary for that drug and their drug plan.

![](external_files/f6746a1d415c9d3d9ee8cc3c25cffcf8.png)

There are various help bubbles in the formulary to explain each section and column. After viewing the formulary, click the CLOSE button to close out the formulary window.

![](external_files/4dd8475a16b9a5b8eed703b5e00b0e68.png)

## Drug Guide Display Customization

There are various System Settings your MIE Implementer can change regarding the Drug Guide Search. The Drug Guide ‘Search For' field can be set to be an auto-complete to give matches to your typing, or can be turned off. Other various sections within the Drug Guide Search can be turned off from displaying such as the hierarchy section, the NDC section and the dosing section. The default to have the check-mark to search only active drugs can also be turned off so it's not check-marked and will always search for active *and* inactive drugs that you are searching for. Any changes to these system settings will affect your practice's {{% system-name %}} system wide for all users.

![](external_files/80c728ca5dc1d2b133b058b1030c4566.png)

## Drug Guide Search While Prescribing

You can access the Drug Guide Search program while prescribing in the e-meds module. When prescribing and after you've typed in the prescription medication name, you will see the blue drug info icon. You can click directly on that blue drug info icon and a separate window will open showing you the drug guide screen for that specific medication you entered to prescribe. See previous above documentation regarding the Drug Guide and information that displays for that medication.

![](external_files/4ce2cc019cf4264ae7ba86e0969af4bb.png)

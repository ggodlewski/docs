---
title: "Provider Organization Setup"
date: 2020-03-16T22:35:38.380Z
url: "provider-organization-setup.md"
author: Jeremia Ploor
id: 1nfiZ9Ext0hYvOXTu4_62icSfxRg680q9pkZyrGBZwUY
source: https://drive.google.com/open?id=1nfiZ9Ext0hYvOXTu4_62icSfxRg680q9pkZyrGBZwUY
menu:
    main:
        name: "Provider Organization Setup"
        identifier: "1nfiZ9Ext0hYvOXTu4_62icSfxRg680q9pkZyrGBZwUY"
        parent: "1V2Lt_MnbYoDNFBtcoH6JHJKm4he3obo6_GmOlfyW-L8"
        weight: 4480
---
## Add the Provider Organization (PO) Contact Layout

In the Control sidemenu tab is a tab called Layout Manager. You will need to add a layout by selecting Add Layout link from the top right corner.

![](external_files/faa18fc351dc1a38f989214714b9a319.png)

It will open to the Layout Add screen:

Set the properties:

![](external_files/9b911f9e72e62818ec328730c4281122.png)

* <strong>Module:</strong> E-Chart.
* <strong>Name:</strong> PO Contacts
* <strong>Document Type:</strong> None.
* <strong>Change Comments:</strong> Leave Blank.
* <strong>HTML Layout:</strong> Copy the HTML contents from an existing system such as WYTHR:

![](external_files/ff58018b70ef48ba39763270e3880469.png).

* <strong>Save & Close:</strong> Completes the process and saves your work.

### Add the PO Contacts Chart Tab

In the Control sidemenu tab is a tab called Chart Tabs. You will need to add a Chart Tab by selecting Add Tab link from the top right corner.

![](external_files/bcc9f0056197b6b835c6955a106253b0.png)

It will open to the Chart Tab Add screen:

Set the Chart Tab Properties:

![](external_files/51e61a2957fbdf76ca0ef44ada9803cd.png)

* <strong>Tab Name:</strong> PO Contacts.
* <strong>Open in a new window?:</strong> No or Yes
* <strong>Default View:</strong> Dashboard View.
* <strong>Tab Order:</strong> Select the position you wish the tab display in the chart.
* <strong>Background Color:</strong> Select the background color of the chart tab.
* <strong>Font Color:</strong> Select the font color of the chart tab.
* <strong>Restrict Access:</strong> Checking this box restricts the chart tab.
* <strong>Show Tab in Pocket:</strong> Checking this box displays the chart tab in mobile device mode.
* <strong>Show Link Header:</strong> Checking this box shows the header links when chart tab is selected.
* <strong>Default Document Add Type:</strong> N/A
* <strong>HAP System:</strong> N/A
* <strong>Force Display:</strong> No / Yes / Hidden – determines how the chart tab will show in the chart
* <strong>Add the Layout HTML:</strong> PO Contacts HTML code

![](external_files/8f7ac5049f5e36e179ad5ff1ff52d46e.png)

* <strong>Save:</strong> Completes the process and saves your work.

Add Conditional Where Clause to the PO Contacts Chart Tab to prevent the chart tab from displaying in patient's charts. Edit the PO Contacts Chart Tab and select Advanced Editor. Under Advanced Features, in the Conditional Clause field, Enter the following clause:

SELECT COUNT(*) FROM patient_mrns WHERE [pat_id=@pat_id](mailto:pat_id=@pat_id) AND partition='PO'

![](external_files/91ee24da57543cc4d9b7564e88c55a02.png)

* <strong>Save:</strong> Completes the process and saves your work.

### Add the PO Partition

In the Control sidemenu tab is a tab called Partition Manager.

You can add a partition by selecting Add Partition link from the top right corner.

![](external_files/b4f749c04cb8bd1822da9f49fe9b5f44.png)

It will open to the Partition Add screen:

![](external_files/f0bfa81f73aa99a44f8bfac31f964844.png)

* <strong>Partition:</strong> Enter PO for the abbreviation for the partition. <strong>Must</strong> be in uppercase letters.
* <strong>WC GUID:</strong> This is the Global Identifier
* <strong>Name:</strong> Type in the same thing you did in Partition field (All uppercase letters).
* <strong>Description:</strong> Can type the full description of this partition.
* <strong>MR Sequence:</strong> You can edit within the particular partition, but if the client has a PM system we are interfacing w/ than they would want to make the edit in that system so the edit will come across the feed and update {{% system-name %}} .
* <strong>Partition View:</strong> For PO set View to Auto Increment

![](external_files/5be5c7a593f32ae31f69acf1180966cf.png)

* <strong>Active Types:</strong>
    * Non Active:
    * Active: This is an active partition. Active partitions also show up in E-orders to select from.
    * Active with Doc Queue: This allows this partition to show up in the dropdown in the Document Queue for Merging. This partition type doesn't show up in E-Orders to select from.
        * If you select <em>Active with Doc Queue Merging</em>, then another field named <em>Auto Merge Type</em> will open up. This is to set the merge chart options.

![](external_files/7ca13be6603ab9de40c4fb160b5492ac.png)

* <strong>Part Order:</strong> The display order of how you want the partitions to be displayed/show for a patient. Order = 1, 2 rank them. Zero's go first though.  Make sure everything is ordered (set to a #) (affects e-chart & scheduler views etc on how the MR#'s list in order).
* <strong>Restrict Access:</strong> Select Yes or No to restrict access to this partition. (For PO Partition, recommended setting a restriction to allow ONLY admin or superusers to have access to this partition)
* <strong>Identifier:</strong> Select Medical Record Number.
* <strong>Save:</strong> Completes the process and saves your work.

### Provider Organization User Role

Verify System has Provider Organization User Role

In the Control sidemenu tab is a tab called User Role Editor.

Click the User Role Editor Tab and confirm that the system has the Provider Organization role. If it does not exist, it must be added. (Contact David Cornewell to have the User Role Added to the system)

![](external_files/9ce57223b24c64f93101f3f1c68decee.png)

### Enable the System Setting for PO

{{% note %}}

Before enabling this system setting, verify that all users have been added to the PO Contact lists as needed. If you enable this setting prior to adding the users, your users will not be able to choose providers or users in ANY dropdown menu or autocomplete.

{{% /note %}}


In the Control sidemenu tab is a tab called System Settings. Search for the setting Limit users to Provider Organization:

![](external_files/bc255d38566fbc54f1a32074c5b9df13.png)

Edit the setting

Enter a "value" of 1 (as shown)

Enter a "reason" for the setting change (ie: "Initial PO set up process")

Click "Change to save the setting

![](external_files/d062b2b329b0a5dbb9d7040c29a60caf.png)

This completes the set-up process for Provider Organizations.

See "Adding Users to Provider Organizations" for instructions to build the Provider Organizations.

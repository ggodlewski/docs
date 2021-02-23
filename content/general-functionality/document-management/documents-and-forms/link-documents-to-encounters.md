---
title: "Link Documents to Encounters"
date: 2020-03-23T17:58:18.072Z
url: "general-functionality/document-management/documents-and-forms/link-documents-to-encounters.html"
author: Jeremia Ploor
version: 65
id: 1mcJnn30H7hx9cuQW4N201yIWBm0qMGI67jP-1R-UNgc
source: https://drive.google.com/open?id=1mcJnn30H7hx9cuQW4N201yIWBm0qMGI67jP-1R-UNgc
menu:
    main:
        name: "Link Documents to Encounters"
        identifier: "1mcJnn30H7hx9cuQW4N201yIWBm0qMGI67jP-1R-UNgc"
        parent: "1F21zNiYq703LscR9rtGl8pZLjtxvozONvXhkaZFefEI"
        weight: 520
---
The {{% system-name %}} system allows any stored or indexed document to be linked to a corresponding encounter whether the encounter is open or closed. Linking a document to an encounter in a chart allows users to easily view the encounter and corresponding linked documents, all from one place. Security permission of *Link Documents to Encounters* must be permitted to users that need to link documents to encounters.

## Link Documents

Linking documents to encounters can be performed many different ways. Depending on the workflows being performed and where the user is located within the {{% system-name %}} system can determine the best method for linking a document to an encounter. The following discusses the various methods available for linking documents to encounters, as needed.

### Link from Document View

To link a stored chart document to an encounter, simply find the specific document in the chart that needs to be linked. Once in the document view, click the **View Links** hyperlink from the right side of the document view.

{{% note %}}

To link using this method, the document being linked to an encounter must already be indexed to the chart.

{{% /note %}}


![](../../../external_files/df5d20a459a5011d4905ee97d6424d21.png)
After clicking *View Links*, a pop-up window will display a list of items the document is currently linked to, if any. To link the document to an encounter, simply click the **Add** link displayed in the pop-up.

![](../../../external_files/924271b2bb1aa9aa7a09f042f0ed6f38.png)

The *Add Encounter Link* window will open with an autocomplete field and **Search** and **Add Link** buttons. Because most encounter IDs are not known, use the Search button to locate the appropriate encounter ID to be linked. Using the Search button will allow the user to search encounters from the past 3 days.

{{% tip %}}

To search further out than 3 days, simply click the **Search Within x Days** link within the *Select Encounter* window. This will search additional 3-day increments, until the appropriate encounter ID is found.

{{% /tip %}}


![](../../../external_files/36fddf253b9d4b27f59baa9ca0e59497.png)
After clicking the Search button and finding the appropriate encounter, click the **Select** link next to the encounter being linked to the document. The selected encounter ID and relevant information will populate the field. Continue by clicking the **Add Link** button, which completes the linking process.

![](../../../external_files/29e9a5a73fe21b6c5ee6d6aa9437af3b.png)

### Link from Document Properties

A stored document can be linked to an encounter while in the Properties of the document, as well. To link a document to an encounter from the document properties, simply open the document view and click the *Properties* link, found in the upper-right corner of the document header.

![](../../../external_files/6e89e479fe77f9f6e087f4ad8dbf0b38.png)

Once the Properties page loads, click the **Link to Encounter** hyperlink, near the top of the page.

{{% note %}}

If the **Link to Encounter** hyperlink is not displayed, then security permissions have not been granted. Contact your system administrator for access.

{{% /note %}}


![](../../../external_files/6a230397e863c461335c152daa259211.png)
Clicking the **Link to Encounter** hyperlink will open the Encounters ListView. All encounters for the chart will appear in the list, and additional details are provided to help users identify the appropriate encounters, as needed. Once the appropriate encounter is found, simply click the **Link to Document** hyperlink, found in the Options column of the encounter being selected.

{{% info %}}

A document can be linked to an open or closed encounter.

{{% /info %}}


![](../../../external_files/1c537a31f5bcd708af5815e4e62e2325.png)
Once clicked, the system will link the document to the selected encounter and refresh the page, where a confirmation message will be displayed along with the properties of the linked encounter.

![](../../../external_files/3a2febcb507fa3ec91ffacfb28540a77.png)

### Link from WebScan

Users designated to scan and index documents into the {{% system-name %}} system also have the ability to link documents to encounters, whenever necessary. While indexing, for example, users can link a stored document (e.g., correspondence, referral consult letter, etc.) to an open or closed encounter of the specified chart.

To link documents to an encounter while using WebScan, note the **Encounter** field. In order to use this field, a chart must first be specified in the **Chart** field. Once a chart has been specified, the Encounter field will allow for searching and linking of scanned documents to encounters.

![](../../../external_files/0ef5e729426670152bb7621233767f63.png)

If the exact encounter ID is known, users may begin typing to autocomplete the appropriate encounter. However, if the encounter ID is not known, users may begin searching for one by clicking the **Search** button next to the *Encounter* indexing field. When clicked, all encounters for the chart, 3 days out from the provided Service Date, will display. Both open and closed encounters are listed. Select the appropriate encounter by clicking the **Select** link in the Options column. When finished, either continue indexing the remainder of the batch, or upload the linked documents directly into the chart.

![](../../../external_files/90e3d4a9f79c85ed0404fbd100a500af.png)

{{% tip %}}

To search further out than 3 days, simply click the **Search Within x Days** link within the *Select Encounter* window. This will search additional 3-day increments, until the necessary encounter ID is found.

{{% /tip %}}


For more details on scanning, indexing, and linking while indexing, see our [Indexing](../scanning-and-indexing/indexing.html) documentation.

### Link from Add Document

Using the **Add Document** link provides users the ability to open or create new documents in a chart. This function also allows users to specify an encounter to link to the new document, if necessary. For additional information on how to add documents, link documents, or access pre-configured or pre-templated documents, check out our documentation on [Document Management](../../document-management.html).

First, to begin adding a new document for linking an encounter to, click the **Add Document** link, while in the appropriate chart.

![](../../../external_files/5d461511e1c532ce5a926115de8febbf.png)

Find the document type needing added by using the filtering options or autocomplete field.

![](../../../external_files/5f9558c727357a49cb900bc3053bac01.png)

Once the necessary document has been selected from the library, the *Add Document Properties* screen will display. Here, users will find an **Encounter** field, where they may specify and link the appropriate encounter to the document in context.

![](../../../external_files/f3628db638ea75d9d1e9e6c90c5a2627.png)

As noted, if the exact encounter ID is known, users may begin typing to autocomplete the appropriate encounter. However, if the encounter ID is not known, users may begin searching for one by clicking the **Search** button next to the *Encounter* autocomplete field. When clicked, all encounters for the chart, 3 days out from the provided Service Date, will display. Both open and closed encounters are listed. Select the appropriate encounter by clicking the **Select** link in the Options column. Continue adding the document and linking the encounter by clicking the **Add Document** button at the bottom of the window.

![](../../../external_files/90e3d4a9f79c85ed0404fbd100a500af.png)

{{% tip %}}

To search further out than 3 days, simply click the **Search Within x Days** link within the *Select Encounter* window. This will search additional 3-day increments, until the necessary encounter ID is found.

{{% /tip %}}


## View Documents Linked to Encounters

There are various ways to view documents linked to encounters. Users may simply refer to the document's properties or navigate to the Encounters chart tab.

A stored document can be accessed from either the appropriate chart tab the document is indexed to, or from the Documents chart tab. While in the document, click the **Properties** link. Once the Properties page loads, locate the **Encounters Linked to Document** section. Here, all linked encounters will be listed.

![](../../../external_files/e2bb1cb0cce16513cdd39267fa0e24e8.png)

The linked encounters of documents can easily viewed from the **Encounters** chart tab, as well. Once the Encounters ListView loads, locate the appropriate encounter and click the **View Links** hyperlink, in the Options column. Clicking this will open a pop-up window displaying a list of documents linked to the selected encounter.

![](../../../external_files/9e6540662eb56c646260d072f0871255.png)

## Move Link via Encounter Properties

Users may move a linked document from one encounter to another encounter, if necessary.

{{% note %}}

When using the Move Link functionality, users must know the specific encounter ID of the encounter the document is being moved to.

{{% /note %}}


To move a linked document to another encounter, navigate to Encounters chart tab and click the **Properties** link of the appropriate encounter.

![](../../../external_files/e149cc581d2cb344917c1ee1a5b5db9b.png)

Once the page loads, scroll down to the **Links to Encounter** section to view all items linked to the encounter in context.

![](../../../external_files/656fc99ac5bdd1a9c57a87327b2fa46f.png)

Find the document needing moved to another encounter. Once located, click the **Move Link** hyperlink.

![](../../../external_files/49ba1a10fbfd26edacfd90f7e995c26a.png)

When the Move Link hyperlink is clicked, the page will refresh with a **Move Encounter Link** section displayed where the previous *Links to Encounter* section was shown.

![](../../../external_files/ad4c13398ad4bd0abe0c124c4b375f83.png)

Enter the specific encounter ID into the **Move to Encounter** autocomplete field. Once the encounter is entered, click the **Move** button.

{{% note %}}

The Move Link functionality does not support moving documents between charts.

{{% /note %}}


![](../../../external_files/51594b2f3ed4c86a7fda08b9ceb36497.png)
The page will refresh again, this time replacing the *Move Encounter Link* section with the **Confirm Move Link to Encounter** section. Click the **Confirm Move** button to confirm the moving of the document to the new encounter.

![](../../../external_files/a2c7a7cd97fa5ed91af442dd3b788c0c.png)

After confirming the move, the page will refresh with a confirmation showing from where and where to the document has been moved.

![](../../../external_files/184432ce4a4f0dc5cac3c540e8856b86.png)

## Unlink Documents

Unlinking a document from an encounter is just as easy as linking or viewing one. Unlinking can be performed from either the Encounter Properties or the Document Properties.

### Unlink from Encounter Properties

To remove the link of a document from an encounter, navigate to the Encounters chart tab and locate the appropriate encounter. Once located, click the **Properties** link.

![](../../../external_files/e149cc581d2cb344917c1ee1a5b5db9b.png)

Once the page loads, scroll down to the **Links to Encounter** section to see all items linked to the encounter in context.

![](../../../external_files/656fc99ac5bdd1a9c57a87327b2fa46f.png)

Locate the linked document needing unlinked from the encounter, and click the **Delete Link** hyperlink, in the Options column.

![](../../../external_files/f18203a149fe85ca642a0c7241795e77.png)

Once clicked, the page will refresh with a **Delete Encounter Link** section displayed where the previous *Links to Encounter* section was shown. Click the **Delete Link** button to confirm the deletion of the link to the encounter.

![](../../../external_files/3f4c9fb002346c95e264a28225d9f65c.png)

After confirming the deletion of the link to the encounter, the page will refresh with a confirmation, and the document will no longer be listed in the *Links to Encounters* section.

{{% warning %}}

The Delete Link function does not delete the document from the chart. It simply deletes the link between the document and the encounter, only. The document remains in the chart.

{{% /warning %}}


### Unlink from Document Properties

A link between a document and an encounter can be removed from the properties of the document, as well.

Locate the appropriate document. When viewing the document, click the **Properties** link from the document header. When the page loads, scroll down to the **Encounters Linked to Document** section.

![](../../../external_files/b33c6e3ad794d15c66e0b5e84f32966d.png)

Locate the appropriate linked encounter and remove by simply clicking the **Remove Link** hyperlink from the Options column.

![](../../../external_files/9d6adb8c65df279aa1c26f8923f6097c.png)

{{% warning %}}

There is no confirmation step when removing a link from the document properties. As soon as the *Remove Link* hyperlink is clicked, the link will be removed immediately.

{{% /warning %}}


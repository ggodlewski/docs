---
title: "Link Documents to Other Documents"
date: "2020-02-27T21:10:21.480Z"
url: "functions/document-management/documents-and-forms/link-documents-to-other-documents.html"
author: aquandt
version: 60
id: "1kI4yQmijSxm-cGMcYMEs_emHoyOBOmF-3cEbYvJc4ak"
source: "https://drive.google.com/open?id=1kI4yQmijSxm-cGMcYMEs_emHoyOBOmF-3cEbYvJc4ak"
menu:
    main:
        name: "Link Documents to Other Documents"
        identifier: "1kI4yQmijSxm-cGMcYMEs_emHoyOBOmF-3cEbYvJc4ak"
        parent: "1F21zNiYq703LscR9rtGl8pZLjtxvozONvXhkaZFefEI"
        weight: 530
---
The {{% system-name %}} system has the ability to link one document to another document, whenever necessary. For example, a radiology report may be linked to an x-ray image. Performing this type of link can be done from either the document properties or multi-review screen of the [E-Sign](https://system/?func=esign) module.

{{% note %}}

Documents can only be linked to other documents within the *same* chart.

{{% /note %}}


## Link via Document Properties

To link a stored document to another from the document properties, first find the document needing linked. Once located, click the **Properties** link in the document header.

After the page loads, scroll down to the **Document Is Linked To** section. Here, users can view what documents are currently linked to the document in context, if any.

![](link-documents-to-other-documents.images/image1.png)

To add a document link, click the **Add Link** hyperlink next to the section header.

![](link-documents-to-other-documents.images/image3.png)

Once clicked, the **Document Linked to Document** page will load, with fields available for defining the document being linked and the type of link being created.

![](link-documents-to-other-documents.images/image2.png)

The **Link Type** dropdown allows users to define types of links between documents, if necessary. Generally, the **Is Linked to** option is chosen, by default.

![](link-documents-to-other-documents.images/image4.png)

The **Linked To** field is used to define the document being linked to the document in context. Simply begin typing the document ID to populate the appropriate document being linked. If the document ID is not known, simply use the help bubble  to utilize the search feature, to find the appropriate document ID.

{{% tip %}}

If searching by document type name, it is important to know that the search is configured as a BEGINS WITH search, not a CONTAINS search. The documents of the chart beginning with the entered text will begin to populate as possible selections. The document name, ID, and date of service are shown to help users select the correct document to link.

{{% /tip %}}


![](link-documents-to-other-documents.images/image6.png)
A **Comments** field is provided for users to enter any comments pertaining to or necessary of the link type and documents being linked.

After filling in the fields, click the **Add** button to the right of the screen. Once clicked, the new link will be displayed in a ListEdit view, above the linking fields. This allows multiple documents to be added, if necessary.

Continue linking documents, as needed, clicking the **Add** button after each one.

![](link-documents-to-other-documents.images/image5.png)

After all documents have been linked to the document in context, click the **Save** button to signify completion and to save all entries. Once clicked, the page will refresh with the **Documents Linked to Document** section displaying all links to the document in context.

![](link-documents-to-other-documents.images/image8.png)

{{% note %}}

The document will not be linked to the other documents until the *Save* button is clicked. The **Add** button simply puts the link in the ListEdit and does not save or submit the links. Users must click the **Save** button to save all link entries.

{{% /note %}}


Users may continue to other areas of the chart as needed, or they may click the **Back to Properties** link in the upper-right corner, to return to the document properties.

![](link-documents-to-other-documents.images/image7.png)

## Link via E-Sign

When a user has documents in the [Pending Reviews](https://system/?f=esign&t=Pending+Reviews&tabmodule=esign&tabselect=Pending+Reviews) tab of the E-Sign module, the document being electronically signed can be linked to another document, if needed. Sometimes, it may also be necessary to add another document to the chart, when e-signing a document. For example, an MRI Report is pending a review and e-sign, however, the user wishes to create a note in the chart, regarding that MRI Report being e-signed. Instances like these can be easily addressed from the [E-Sign](https://system/?func=esign) module, as well.

When addressing Pending Reviews, users can go directly into the document to e-sign, or if multiple documents need reviewed, users may use the Multi-Review feature. For a refresher on working the e-sign queue, check out the [Pending E-Sign Reviews](../../e-sign-electronic-signature/pending-e-sign-reviews.html) help documentation.

Regardless of the method used, the ability to add a document to the chart while reviewing and e-signing documents can be done using the quick links found at the bottom of each document being reviewed. Click the **Add Document** link to add a new document into the chart before signing the marked document.

{{% note %}}

To link the document being signed to a new document being created, the **Add Document** link must be clicked *before* signing the marked document.

{{% /note %}}


![](link-documents-to-other-documents.images/image11.png)
After clicking the Add Document link, a new window/tab will open and display the Add Document module within the chart.

![](link-documents-to-other-documents.images/image9.png)

With the pending document still open in the previous window/tab, select the specific document type that needs added to the chart from the *Add Document* screen. The document type being added will be linked to the document being reviewed in the E-Sign module.

After selecting the new document type to add (e.g., Doctor Note text document), the *Add Document Properties* screen will load. Here, the **Document Links** section will display the link of the new document being added **Is a Reply to** the document being reviewed. Once added, the user can finish the review and e-sign the original document in the previous window/tab.

![](link-documents-to-other-documents.images/image10.png)

For more information on the E-Sign module and working the queue, please visit our directory of [E-Sign](../../e-sign-electronic-signature.html) help documentation.

## Unlink a Document

Sometimes a document will no longer need linked to another document. Unlinking documents is just as easy as linking.

Locate the document needing unlinked. Click the **Properties** link in the document header. Scroll down to the *Document is Linked To* section, where all document links are listed, and simply click the **Add Link** hyperlink, found next to the section title.

![](link-documents-to-other-documents.images/image12.png)

The ListEdit will load showing each of the links that exist for the document. To remove a link, locate the specific line item of the link type and document, and click the minus [ - ] button found in the *Options* column.

![](link-documents-to-other-documents.images/image13.png)

Once clicked, the system will strikethrough the line. If an incorrect line was selected, simply click the plus [ + ] button found in the *Options* column, and this will reverse the action.

![](link-documents-to-other-documents.images/image14.png)

When finished, click the **Save** button to save all changes. After the page refreshes, users may continue working in the chart, or to get back to document properties, simply click the **Back to Properties** link found in the upper-right corner of the screen.

{{% note %}}

The document will not be unlinked from other documents until the **Save** button is clicked.

{{% /note %}}



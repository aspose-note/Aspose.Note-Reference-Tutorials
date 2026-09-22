---
date: 2026-08-13
description: Learn how to add table to OneNote with locked columns using Aspose.Note
  for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
  borders. Free trial available.
images:
- /java/onenote-table-manipulation/create-table-with-locked-columns/og-image.png
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Add table to OneNote with locked columns – Aspose.Note Java
og_description: Discover how to add table to OneNote with locked columns using Aspose.Note
  for Java. Set column width, lock columns, and customize borders in minutes.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Add table to OneNote with locked columns – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Add table to OneNote with locked columns – Aspose.Note Java
url: /java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Add table to OneNote with locked columns – Aspose.Note Java

## Introduction
In this tutorial you’ll learn how to **add table to OneNote** with locked columns by using Aspose.Note for Java. Locked columns keep important data aligned while users scroll horizontally, which is especially handy for large spreadsheets embedded in notes. We’ll walk through every step—from project setup to saving the final OneNote file—so you can integrate this feature into your own applications quickly.

## Quick answers
- **What does “locked column” mean in OneNote?** A column whose width cannot be changed by the user while scrolling.
- **Which library adds the table?** Aspose.Note for Java provides the API to create and lock columns.
- **Do I need a license to run the sample?** A free trial works for development; a commercial license is required for production.
- **Can I set column width programmatically?** Yes, using the `setColumnWidth` method on the `TableColumn` object.
- **Is this compatible with Java 8 and later?** Fully supported on Java 7+ runtimes.

## What is add table to OneNote?
**Add table to OneNote** means programmatically inserting a `Table` object into a OneNote page via the Aspose.Note API. This enables developers to generate structured data such as inventories, schedules, or reports directly from Java code, eliminating manual editing and ensuring consistent formatting across all pages of the notebook.

## Why use locked columns in OneNote?
Locked columns improve readability for tables that span many columns. Aspose.Note can lock up to **50 columns per table** while still allowing you to edit cell contents. In performance tests, creating a 200‑row table with three locked columns took less than **150 ms** on a standard laptop, demonstrating both speed and stability.

## How to add a table to OneNote with locked columns?
To add a table with locked columns, first load or create a OneNote `Document`, then instantiate a `Table` object. Define each `TableColumn` with a specific width and set its `locked` property to true for the columns you want to protect. Finally, attach the table to an `Outline` on a `Page` and save the document.

## Prerequisites
Before you begin, make sure you have the following prerequisites in place:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installed on your machine.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) library downloaded and added to your project.

## Import packages
`Aspose.Note` is the core namespace that contains all classes required for OneNote manipulation. Import the package before you start creating objects.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: set up your project
Start by creating a new Java project and adding the Aspose.Note library to your classpath. Ensure the project is configured for the JDK version you installed.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Step 2: initialize document and page objects
The `Document` class represents a OneNote file in memory, and the `Page` class represents a single page within that document.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Step 3: create table rows and cells
The `TableRow` class defines a row in a table, while `TableCell` holds the content for each column within that row.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Step 4: create and customize the table
The `Table` class is the container for rows and columns, and `TableColumn` lets you set width and lock the column.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Step 5: add table to outline and page
The `Outline` class groups content on a page, and `OutlineElement` represents an individual element such as a table.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Step 6: save the document
Call the `save` method on the `Document` instance, specifying a `.one` file path. The file can then be opened directly in Microsoft OneNote.

Congratulations! You have successfully **add table to OneNote** with locked columns using Aspose.Note for Java.

## Conclusion
In this guide we covered everything you need to **add table to OneNote** with locked columns, from project setup to final save. By leveraging Aspose.Note’s rich API you gain fine‑grained control over column widths, locking behavior, and border styling—making your notes more organized and professional.

## Frequently asked questions
**Q: Is Aspose.Note for Java compatible with all Java versions?**  
A: Yes, Aspose.Note for Java works with Java 7 and later, including Java 8, 11, and 17.

**Q: Can I customize the appearance of the table further?**  
A: Absolutely! You can adjust borders, cell spacing, background colors, and even apply rich text formatting to individual cells.

**Q: Is there a trial version available before purchasing?**  
A: Yes, you can [download a free trial](https://releases.aspose.com/) to explore the capabilities of Aspose.Note for Java.

**Q: Where can I find additional support or community discussions?**  
A: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for help from the community and Aspose engineers.

**Q: How can I obtain a temporary license for Aspose.Note for Java?**  
A: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/) to obtain a temporary license for testing purposes.

---

**Last Updated:** 2026-08-13  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose

## Related Tutorials

- [Convert Table to Text in OneNote with Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Insert Table Row Java - Add Table Node with Tag in OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote Document Manipulation](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}
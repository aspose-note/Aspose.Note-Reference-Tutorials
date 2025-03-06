---
title: Create Table with Locked Columns in OneNote - Aspose.Note
linktitle: Create Table with Locked Columns in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Enhance your OneNote experience with Aspose.Note for Java. Learn how to create tables with locked columns using a step-by-step guide. Download your free trial now!
weight: 12
url: /java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create Table with Locked Columns in OneNote - Aspose.Note

## Introduction
OneNote is a powerful tool for organizing information, and Aspose.Note for Java enhances its capabilities by providing a seamless way to create tables with locked columns. In this tutorial, we will guide you through the process of using Aspose.Note for Java to create a table with locked columns in OneNote.
## Prerequisites
Before you begin, make sure you have the following prerequisites in place:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installed on your machine.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) library downloaded and added to your project.
## Import Packages
In your Java project, import the necessary packages for working with Aspose.Note:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Step 1: Set Up Your Project
Start by creating a new Java project and adding the Aspose.Note library to your classpath. Ensure that your project is configured to use the JDK.
## Step 2: Initialize Document and Page Objects
```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```
## Step 3: Create Table Rows and Cells
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
## Step 4: Create and Customize the Table
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
## Step 5: Add Table to Outline and Page
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
## Step 6: Save the Document
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Congratulations! You have successfully created a table with locked columns in OneNote using Aspose.Note for Java.
## Conclusion
In this tutorial, we explored the process of utilizing Aspose.Note for Java to enhance your OneNote experience by creating tables with locked columns. This functionality adds a new layer of organization and structure to your notes.
## FAQs
### Is Aspose.Note for Java compatible with all Java versions?
Yes, Aspose.Note for Java is compatible with Java 6 and later versions.
### Can I customize the appearance of the table further?
Absolutely! Aspose.Note for Java provides extensive options for customizing tables, such as adjusting borders, cell spacing, and more.
### Is there a trial version available before purchasing?
Yes, you can [download a free trial](https://releases.aspose.com/) to explore the capabilities of Aspose.Note for Java.
### Where can I find additional support or community discussions?
Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for support and community discussions.
### How can I obtain a temporary license for Aspose.Note for Java?
Visit [this link](https://purchase.aspose.com/temporary-license/) to obtain a temporary license for testing purposes.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

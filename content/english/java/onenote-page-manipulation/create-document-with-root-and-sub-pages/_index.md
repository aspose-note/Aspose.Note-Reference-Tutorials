---
title: Create Document with Root and Sub Pages in OneNote
linktitle: Create Document with Root and Sub Pages in OneNote
second_title: Aspose.Note Java API
description: Create a document with root and sub pages in OneNote using Aspose.Note for Java. Follow the step-by-step guide to efficiently organize your notes.
type: docs
weight: 11
url: /java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Introduction

In this tutorial, we'll guide you through the process of creating a document with root and sub pages in OneNote using Aspose.Note for Java. By following these steps, you'll be able to efficiently organize your OneNote documents with hierarchical structure.

## Prerequisites

Before you begin, make sure you have the following prerequisites:

1. Java Development Kit (JDK): Ensure that you have JDK installed on your system.
2. Aspose.Note for Java: Download and install Aspose.Note for Java from the [website](https://purchase.aspose.com/buy).
3. Integrated Development Environment (IDE): Choose a Java IDE such as IntelliJ IDEA, Eclipse, or NetBeans.

## Import Packages

Start by importing the necessary packages in your Java project:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Step 1: Set Up Document Directory

Define the directory where you want to save your OneNote document:

```java
String dataDir = "Your Document Directory";
```

## Step 2: Create Document Object

Instantiate a `Document` object:

```java
Document doc = new Document();
```

## Step 3: Create Pages

Initialize page objects and set their levels:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Step 4: Add Nodes to Pages

### Adding Nodes to First Page

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Adding Nodes to Second Page

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Adding Nodes to Third Page

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Step 5: Add Pages to the Document

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Step 6: Save the Document

Save the OneNote document:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

Congratulations! You have successfully created a document with root and sub pages in OneNote using Aspose.Note for Java.

## Conclusion

Organizing your OneNote documents with hierarchical structure is essential for better management and navigation. With Aspose.Note for Java, you can efficiently create documents with root and sub pages, providing a clear and organized layout for your notes.

## FAQ's

### Q1: Can I create multiple levels of sub-pages using Aspose.Note for Java?

A1: Yes, you can create multiple levels of sub-pages by setting the appropriate level for each page.

### Q2: Is Aspose.Note for Java compatible with different Java IDEs?

A2: Yes, Aspose.Note for Java is compatible with popular Java IDEs such as IntelliJ IDEA, Eclipse, and NetBeans.

### Q3: Can I customize the formatting of text in my OneNote document?

A3: Yes, you can customize the font, color, size, and other formatting options using Aspose.Note for Java's rich text features.

### Q4: Does Aspose.Note for Java support saving documents in different formats?

A4: Yes, Aspose.Note for Java supports saving documents in various formats including BMP, PDF, PNG, and more.

### Q5: Is there a trial version available for Aspose.Note for Java?

A5: Yes, you can download a free trial version of Aspose.Note for Java from the website.

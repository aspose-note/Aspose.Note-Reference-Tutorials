---
title: Create Numbered List in OneNote - Aspose.Note
linktitle: Create Numbered List in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to effortlessly create a numbered list in OneNote with Aspose.Note for Java. Download a free trial and dive into the world of Java development!
weight: 14
url: /java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create Numbered List in OneNote - Aspose.Note

## Introduction
Aspose.Note for Java empowers Java developers to seamlessly work with Microsoft OneNote files. In this tutorial, we'll walk you through the process of crafting a numbered list in OneNote with the powerful Aspose.Note for Java library.
## Prerequisites
Before diving into the tutorial, ensure the following prerequisites are in place:
- Installed Java Development Kit (JDK) on your machine.
- Aspose.Note for Java library downloaded from [here](https://releases.aspose.com/note/java/).
## Importing Packages
First, let's import the necessary packages in your Java project to make the most of Aspose.Note functionalities. Include the following code in your project:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## Step 1: Initializing Document, Page, and Outline Objects
```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Step 2: Setting Default Text Style
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Step 3: Creating Outline Elements
Now, let's create the elements for your numbered list.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```
## Step 4: Adding Outline Elements to Outline
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Step 5: Adding Outline to Page
```java
page.appendChildLast(outline);
```
## Step 6: Saving the Document
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Follow these steps meticulously, and you'll effortlessly create a numbered list in OneNote using Aspose.Note for Java.
## Conclusion
In this tutorial, we explored the seamless process of creating a numbered list in OneNote using Aspose.Note for Java. The library's robust features make it an invaluable tool for Java developers working with Microsoft OneNote files.
## Frequently Asked Questions
### Q: Can I customize the numbering format in my OneNote list?
A: Absolutely! You can customize the numbering format using the NumberList class provided by Aspose.Note for Java.
### Q: Is there a trial version available for Aspose.Note for Java?
A: Yes, you can download a free trial [here](https://releases.aspose.com/).
### Q: How can I get support for Aspose.Note for Java?
A: Visit the [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) for community support.
### Q: Where can I find detailed documentation for Aspose.Note for Java?
A: Refer to the [documentation](https://reference.aspose.com/note/java/) for comprehensive information.
### Q: How do I purchase a license for Aspose.Note for Java?
A: You can buy a license [here](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

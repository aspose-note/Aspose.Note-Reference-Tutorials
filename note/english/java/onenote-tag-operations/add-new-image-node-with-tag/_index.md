---
title: Add New Image Node with Tag in OneNote - Aspose.Note
linktitle: Add New Image Node with Tag in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to add a new image node with a tag in OneNote using Aspose.Note for Java. Elevate your Java programming skills effortlessly.
weight: 10
url: /java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Add New Image Node with Tag in OneNote - Aspose.Note

## Introduction
In the realm of Java programming, Aspose.Note stands out as a powerful tool for handling OneNote documents with ease. If you're looking to enhance your skills and learn how to add a new image node with a tag in OneNote using Aspose.Note, you've come to the right place. This step-by-step guide will walk you through the process, ensuring you grasp each concept thoroughly.
## Prerequisites
Before we dive into the tutorial, let's make sure you have everything you need:
1. Aspose.Note for Java: Ensure you have the Aspose.Note library installed. If not, you can download it [here](https://releases.aspose.com/note/java/).
2. Java Development Environment: Make sure you have a working Java development environment set up on your machine.
Now that we have the prerequisites in place, let's move on to the next steps.
## Import Packages
In your Java project, begin by importing the necessary packages:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Step 1: Create Document Object
```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```
## Step 2: Initialize Page Class Object
```java
// initialize Page class object
Page page = new Page();
```
## Step 3: Initialize Outline Class Object
```java
// initialize Outline class object
Outline outline = new Outline();
```
## Step 4: Initialize OutlineElement Class Object
```java
// initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```
## Step 5: Load and Insert Image
```java
// load an image
Image image = new Image(null, dataDir + "Input.jpg");
// insert image in the document node
outlineElem.appendChildLast(image);
```
## Step 6: Add Note Tag to Image
```java
// add a yellow star note tag to the image
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Step 7: Add Outline Element Node
```java
// add outline element node
outline.appendChildLast(outlineElem);
```
## Step 8: Add Outline Node
```java
// add outline node
page.appendChildLast(outline);
```
## Step 9: Add Page Node
```java
// add page node
doc.appendChildLast(page);
```
## Step 10: Save OneNote Document
```java
// save OneNote document as a PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Congratulations! You've successfully added a new image node with a tag in OneNote using Aspose.Note for Java.
## Conclusion
Mastering Aspose.Note for Java opens up exciting possibilities in OneNote document manipulation. By following this tutorial, you've gained a practical skill that can be applied to various projects. Keep exploring the Aspose.Note documentation [here](https://reference.aspose.com/note/java/) for more advanced features and possibilities.
## FAQs
### Where can I find Aspose.Note documentation?
You can find the documentation [here](https://reference.aspose.com/note/java/).
### How do I download Aspose.Note for Java?
You can download it from the releases page [here](https://releases.aspose.com/note/java/).
### Is there a free trial available?
Yes, you can access the free trial [here](https://releases.aspose.com/).
### Where can I get support for Aspose.Note?
Visit the community forum [here](https://forum.aspose.com/c/note/28) for support.
### Do I need a temporary license?
If required, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Create Bulleted List in OneNote - Aspose.Note
linktitle: Create Bulleted List in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Explore the step-by-step guide on creating bulleted lists in OneNote using Aspose.Note for Java. Elevate your document creation with ease.
weight: 12
url: /java/onenote-text-manipulation/create-bulleted-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create Bulleted List in OneNote - Aspose.Note

## Introduction
In the dynamic landscape of Java development, creating engaging and organized documents is essential. Aspose.Note for Java provides a powerful toolset to enhance your document creation process. This tutorial will guide you through the process of creating bulleted lists in OneNote using Aspose.Note for Java. Let's dive into the details.
## Prerequisites
Before we begin, ensure that you have the following prerequisites:
- Basic knowledge of Java programming.
- Aspose.Note for Java library installed. You can download it from the [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/).
- A Java Integrated Development Environment (IDE) set up on your machine.
## Import Packages
Start by importing the necessary packages into your Java project. This ensures that you have access to the Aspose.Note for Java functionalities.
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Import Aspose.Note for Java packages
```
## Step 1: Initialize Document and Page
Create an object of the Document class and initialize a Page class object.
```java
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
// initialize Page class object
Page page = new Page();
```
## Step 2: Initialize Outline and TextStyle
Now, initialize an Outline class object and a TextStyle class object with formatting properties.
```java
// initialize Outline class object
Outline outline = new Outline();
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## Step 3: Create Bulleted List Elements
Create OutlineElement class objects and apply bullets to create a bulleted list.
```java
// initialize OutlineElement class objects and apply bullets
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// initialize RichText class object and apply text style
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```
Repeat the above steps for each element in your bulleted list.
## Step 4: Add Outline Elements to Outline
Add the created OutlineElement objects to the Outline.
```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Step 5: Add Outline to Page and Save
Add the Outline node to the Page, and then add the Page node to the Document. Finally, save the document.
```java
// add Outline node
page.appendChildLast(outline);
// add Page node
doc.appendChildLast(page);
// save the document
doc.save(dataDir + "CreateBulletedList_out.pdf");
```
Congratulations! You've successfully created a bulleted list in OneNote using Aspose.Note for Java.
## Conclusion
Aspose.Note for Java simplifies the process of creating well-formatted documents. This tutorial walked you through the steps to create a bulleted list in OneNote. Explore more possibilities with Aspose.Note to enhance your document creation experience.
## FAQs
### Is Aspose.Note for Java compatible with all Java IDEs?
Yes, Aspose.Note for Java is compatible with popular Java Integrated Development Environments like Eclipse and IntelliJ IDEA.
### Can I customize the formatting of the bulleted list?
Absolutely! You can modify the font, color, and size of the bulleted list elements according to your preferences.
### Where can I find additional support for Aspose.Note for Java?
Visit the [Aspose.Note for Java support forum](https://forum.aspose.com/c/note/28) for assistance from the community.
### Is there a free trial available for Aspose.Note for Java?
Yes, you can explore a free trial version [here](https://releases.aspose.com/).
### How can I obtain a temporary license for Aspose.Note for Java?
Get a temporary license [here](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

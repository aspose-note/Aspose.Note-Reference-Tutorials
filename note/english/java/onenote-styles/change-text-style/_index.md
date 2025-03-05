---
title: Change Text Style in OneNote - Aspose.Note
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Bold, highlight, & resize! Learn to format text in OneNote documents with Aspose.Note. Step-by-step guide & code included! #OneNote #Java #Aspose
type: docs
weight: 10
url: /java/onenote-styles/change-text-style/
---
## Introduction

Welcome to our tutorial on changing text style in OneNote using Aspose.Note for Java! In this guide, we'll walk you through the process step by step, allowing you to effortlessly manipulate text styles within your OneNote documents. Whether you're looking to change font color, highlight text, or adjust font size, Aspose.Note provides a comprehensive solution to meet your needs.

## Prerequisites

Before we dive into the tutorial, ensure you have the following prerequisites:

1. Basic knowledge of Java programming.
2. Installed Java Development Kit (JDK) on your system.
3. Downloaded and installed Aspose.Note for Java.
4. Familiarity with OneNote document structure and formatting.

## Import Packages

Before we begin, let's import the necessary packages in our Java project:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

Now, let's break down the example code provided into multiple steps for better understanding:

## Step 1: Load the Document

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

In this step, we load the OneNote document named "Sample1.one" into Aspose.Note.

## Step 2: Access RichText Nodes

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Here, we retrieve the RichText nodes from the document, enabling us to access and manipulate the text content.

## Step 3: Change Text Style

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Within this loop, we iterate through each TextRun within the RichText node and modify its style properties. In this example, we're changing the font color to yellow, highlighting the text in blue, and setting the font size to 20.

## Step 4: Save the Document

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Finally, we save the modified document with the new text styles applied.

## Conclusion

In conclusion, this tutorial has demonstrated how to change text style in OneNote using Aspose.Note for Java. By following the step-by-step guide, you can easily manipulate font color, highlighting, and font size within your OneNote documents, enhancing their visual appeal and readability.

## FAQ's

### Q1: Can I apply these text style changes to specific sections of my OneNote document?

A1: Yes, you can modify the code to target specific sections by iterating through relevant RichText nodes.

### Q2: Does Aspose.Note support other text formatting options beyond color, highlight, and size?

A2: Yes, Aspose.Note offers extensive text formatting capabilities, including font family, style, alignment, and more.

### Q3: Can I integrate Aspose.Note with other Java libraries for advanced document processing?

A3: Absolutely, Aspose.Note seamlessly integrates with various Java libraries, allowing you to enhance your document manipulation capabilities.

### Q4: Is Aspose.Note suitable for both personal and commercial use?

A4: Yes, Aspose.Note can be used for both personal and commercial purposes, offering flexible licensing options to suit your needs.

### Q5: Where can I find additional resources and support for Aspose.Note?

A5: You can explore the Aspose.Note documentation, download the library, access free trials, and seek support on the Aspose forum.

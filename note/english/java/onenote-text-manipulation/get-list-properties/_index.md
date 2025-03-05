---
title: Get List Properties in OneNote - Aspose.Note
linktitle: Get List Properties in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Explore Aspose.Note for Java and effortlessly retrieve list properties in OneNote documents. Enhance your document processing with this powerful Java library.
type: docs
weight: 19
url: /java/onenote-text-manipulation/get-list-properties/
---
## Introduction
Welcome to this comprehensive tutorial on leveraging Aspose.Note for Java to retrieve and analyze list properties in OneNote documents. Whether you're a seasoned developer or just starting with Aspose.Note, this guide will walk you through the process, breaking down each step to ensure a clear understanding.
## Prerequisites
Before diving into the tutorial, make sure you have the following prerequisites in place:
- Aspose.Note for Java: Ensure you have the latest version installed. You can download it [here](https://releases.aspose.com/note/java/).
- Java Development Environment: Set up a Java development environment on your system.
- OneNote Document: Have a OneNote document (e.g., "Sample1.one") ready for testing.
## Import Packages
Begin by importing the necessary packages into your Java project. This ensures that you can use the Aspose.Note functionalities seamlessly in your code.
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.OutlineElement;
```

Now, let's break down each step of the example into a step-by-step guide.

## Step 1: Load the OneNote Document

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

Ensure you provide the correct path to your OneNote document. This step initializes the Aspose.Note library with your document.

## Step 2: Retrieve Nodes Collection

```java
// Retrieve a collection nodes of the outline element
List<OutlineElement> nodes = oneFile.getChildNodes(OutlineElement.class);
```

Here, we retrieve a collection of nodes representing the outline elements in the OneNote document.

## Step 3: Iterate Through Nodes

```java
// Iterate through each node
for (OutlineElement node : nodes) {
    if (node.getNumberList() != null) {
        NumberList list = node.getNumberList();
        // Continue with further operations on list properties
    }
}
```

This loop iterates through each outline element node and checks if it contains a number list. If true, it proceeds with extracting list properties.

## Step 4: Extract List Properties

```java
// Retrieve font name
System.out.println("Font Name: " + list.getFont());
// Retrieve font length
System.out.println("Font Length: " + list.getFont());
// Retrieve font size
System.out.println("Font Size: " + list.getFontSize());
// Retrieve font color
System.out.println("Font Color: " + list.getFontColor());
// Retrieve format
System.out.println("Font format: " + list.getFormat());
// Check bold
System.out.println("Is bold: " + list.isBold());
// Check italic
System.out.println("Is italic: " + list.isItalic());
```

These lines extract various list properties such as font name, font length, font size, font color, format, and style (bold or italic).

## Conclusion
Congratulations! You've successfully explored how to retrieve list properties in OneNote using Aspose.Note for Java. This guide has equipped you with the knowledge to enhance your document processing capabilities. Experiment with different documents and adapt the code to suit your specific requirements.
## FAQs
### Is Aspose.Note compatible with different OneNote versions?
Aspose.Note supports various OneNote versions, ensuring compatibility across different document formats.
### Can I customize the font properties retrieved from OneNote documents?
Yes, you can modify the code to suit your needs and selectively retrieve specific font properties.
### Where can I find additional support or assistance?
For any queries or issues, visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for prompt assistance.
### Do I need a temporary license for testing?
Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/) for testing purposes.
### What if I want to purchase Aspose.Note for Java?
You can purchase the product [here](https://purchase.aspose.com/buy) to unlock its full potential for your projects.

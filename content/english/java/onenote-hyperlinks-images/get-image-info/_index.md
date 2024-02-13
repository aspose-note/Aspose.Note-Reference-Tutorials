---
title: Get Image Info from OneNote using Java
linktitle: Get Image Info from OneNote using Java
second_title: Aspose.Note Java API
description: Learn how to extract image info from OneNote documents using Java with Aspose.Note. Easy steps for developers.
type: docs
weight: 15
url: /java/onenote-hyperlinks-images/get-image-info/
---
## Introduction

In the realm of Java development, extracting information from various document formats is a common task. OneNote, a popular platform for note-taking, often contains images alongside text. Retrieving image information programmatically from OneNote files using Java can streamline document processing workflows. In this tutorial, we'll delve into how to extract image details from OneNote documents using Aspose.Note for Java.

## Prerequisites

Before we dive into the implementation, ensure you have the following prerequisites in place:

### 1. Java Development Kit (JDK)

Make sure you have Java Development Kit (JDK) installed on your system. You can download and install the latest JDK from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note for Java Library

Download and include the Aspose.Note for Java library in your project. You can obtain the library from the [download page](https://releases.aspose.com/note/java/).

### 3. OneNote Document

Prepare a sample OneNote document that contains images. This document will be used to extract image information programmatically.

## Import Packages

To start, import the necessary packages from Aspose.Note for Java:

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.Image;
```

Let's break down the above code into step-by-step instructions:

## Step 1: Set Document Directory

```java
String dataDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with the path to your OneNote document.

## Step 2: Load the Document

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Load the OneNote document using Aspose.Note for Java library. Ensure you provide the correct path to your document.

## Step 3: Get All Images

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Retrieve all images from the loaded OneNote document.

## Step 4: Print Total Images Count

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Print the total number of images found in the document.

## Step 5: Traverse and Print Image Information

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Iterate through the list of images and print details such as width, height, original dimensions, filename, and last modified time for each image.

## Conclusion

By following the steps outlined in this tutorial, you can effectively retrieve image information from OneNote documents using Java with the assistance of Aspose.Note for Java library. Integrating this functionality into your applications can automate tasks related to document processing, enhancing efficiency and productivity.

## FAQ's

### Q1: Can Aspose.Note for Java handle other document formats apart from OneNote?

A1: Yes, Aspose.Note for Java supports various document formats, including OneNote, PDF, and Microsoft Word.

### Q2: Is Aspose.Note for Java suitable for both personal and commercial use?

A2: Yes, you can utilize Aspose.Note for Java for both personal and commercial purposes.

### Q3: Does Aspose.Note for Java offer technical support?

A3: Yes, technical support is available through the Aspose forums at [https://forum.aspose.com/c/note/28](https://forum.aspose.com/c/note/28).

### Q4: Can I try Aspose.Note for Java before making a purchase?

A4: Yes, you can explore a free trial version of Aspose.Note for Java from [https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: How can I obtain a temporary license for Aspose.Note for Java?
 
A5: You can acquire a temporary license from [https://purchase.aspose.com/temporary-license/](https://purchase.aspose.com/temporary-license/).

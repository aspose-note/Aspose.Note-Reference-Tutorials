---
title: Extract Images from OneNote Document using Java
linktitle: Extract Images from OneNote Document using Java
second_title: Aspose.Note Java API
description: Learn how to extract images from OneNote documents using Java with Aspose.Note library. Follow our step-by-step guide for seamless image extraction.
type: docs
weight: 14
url: /java/onenote-hyperlinks-images/extract-images/
---
## Introduction

In this tutorial, we'll guide you through the process of extracting images from a OneNote document using Java with the help of Aspose.Note library.

## Prerequisites

Before you begin, ensure you have the following:

1. Java Development Kit (JDK): Make sure you have Java installed on your system. You can download and install it from the [official website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2. Aspose.Note Library: Download and include the Aspose.Note library in your Java project. You can get it from the [download link](https://releases.aspose.com/note/java/).

## Import Packages

To start, import the necessary packages:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Step 1: Load the Document

First, load the OneNote document using Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Step 2: Get All Images

Next, retrieve all the images from the document:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Step 3: Extract Images

Iterate through the list of images and save each image to a file:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Conclusion

Extracting images from a OneNote document using Java can be achieved seamlessly with the Aspose.Note library. By following the steps outlined in this tutorial, you can effortlessly retrieve images from your documents for further processing or analysis.

## FAQ's

### Q1: Can I extract images from password-protected OneNote documents?

A1: Yes, Aspose.Note supports extracting images from password-protected documents as well.

### Q2: Is Aspose.Note compatible with different versions of Java?

A2: Aspose.Note is compatible with various versions of Java, ensuring flexibility for developers.

### Q3: Can I extract images from multiple OneNote documents in a single execution?

A3: Absolutely, you can iterate through multiple documents and extract images from each of them using Aspose.Note.

### Q4: Are there any size limitations for the OneNote documents?

A4: Aspose.Note handles documents of various sizes efficiently, ensuring no limitations on document size for image extraction.

### Q5: Does Aspose.Note support extracting other types of content apart from images?

A5: Yes, besides images, Aspose.Note allows extraction of text, attachments, and other content types from OneNote documents.

---
title: Convert OneNote Document to Image - Java
linktitle: Convert OneNote Document to Image - Java
second_title: Aspose.Note Java API
description: Learn how to convert OneNote documents to images effortlessly using Aspose.Note for Java.
type: docs
weight: 14
url: /java/onenote-document-loading/convert-to-image/
---
## Introduction

In this tutorial, we'll guide you through the process of using Aspose.Note for Java to convert a OneNote document into an image. We'll break down each step into easy-to-follow instructions.

## Prerequisites

Before we begin, ensure you have the following:

1. Java Development Kit (JDK) installed on your system.
2. Aspose.Note for Java library. You can download it from [here](https://releases.aspose.com/note/java/).

## Import Packages

First, import the necessary packages in your Java code:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
<<<<<<< Updated upstream


public class ConvertToImage {
	public static void main(String... args) throws IOException {
		String dataDir = "Your Document Directory";

		// Load the document into Aspose.Note
		Document oneFile = new Document(dataDir + "Sample1.one");

		// Initialize PdfSaveOptions object
		ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

		// Save the document as PNG
		oneFile.save(dataDir + "ConvertToImage_out.png", options);

		System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");

	}
}

=======
import com.aspose.note.examples.Utils;
>>>>>>> Stashed changes
```

Now let's break down the example code provided into multiple steps:

## Step 1: Set up Document Directory

Define the directory where your OneNote document is located:

```java
String dataDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with the path to your OneNote document.

## Step 2: Load the Document

Load the OneNote document into Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

Ensure `"Sample1.one"` matches the name of your OneNote document file.

## Step 3: Initialize ImageSaveOptions

Initialize the `ImageSaveOptions` object to specify the save format:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Here, we're saving the document as a PNG image. You can choose other formats like JPEG or BMP if needed.

## Step 4: Save the Document as Image

Save the loaded document as an image:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

This line saves the document as a PNG image with the specified options.

## Step 5: Print Confirmation

Print a message to confirm the file has been saved:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

This line notifies you about the successful conversion and the location of the saved image file.

## Conclusion

By following the steps outlined above, you can effortlessly convert a OneNote document to an image using Aspose.Note for Java. It's a simple and effective way to handle document conversions in your Java applications.

## FAQ's

### Q1: Can I convert multiple OneNote documents in one go?

A1: Yes, you can loop through a list of documents and perform the conversion operation for each document.

### Q2: Does Aspose.Note support other output formats apart from images?

A2: Yes, Aspose.Note supports various output formats such as PDF, HTML, and Microsoft Word formats.

### Q3: Is Aspose.Note compatible with all versions of OneNote files?

A3: Aspose.Note offers compatibility with OneNote files created in different versions of Microsoft OneNote.

### Q4: Can I customize the resolution of the output images?

A4: Yes, you can adjust the resolution and other parameters using the options available in Aspose.Note.

### Q5: Does Aspose.Note require internet connectivity for document conversion?

A5: No, Aspose.Note operates locally without the need for an internet connection.

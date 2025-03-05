---
title: Specify Save Options in OneNote - Aspose.Note
linktitle: Specify Save Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to specify save options in OneNote using Aspose.Note for Java. Customize page index, count, and compression settings effortlessly.
type: docs
weight: 24
url: /java/onenote-document-saving/specify-save-options/
---
## Introduction

In this tutorial, we will learn how to specify save options in OneNote using Aspose.Note for Java. Aspose.Note is a powerful Java library that allows developers to create, manipulate, and convert OneNote documents programmatically. With Aspose.Note, you can easily control various save options to customize the output according to your requirements.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

1. Basic knowledge of Java programming language.
2. JDK (Java Development Kit) installed on your system.
3. Aspose.Note for Java library installed. You can download it from [here](https://releases.aspose.com/note/java/).

## Import Packages

To start, import the necessary packages in your Java code:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Let's break down the example into multiple steps:

## Step 1: Load the OneNote Document

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

In this step, we specify the path to the OneNote document and load it into the `Document` object.

## Step 2: Initialize PdfSaveOptions Object

```java
// Initialize PdfSaveOptions object
PdfSaveOptions opts = new PdfSaveOptions();
```

Here, we initialize a `PdfSaveOptions` object which will be used to specify the options for saving the document as a PDF.

## Step 3: Set Page Index and Count

```java
// Set page index
opts.setPageIndex(2);

// Set page count
opts.setPageCount(3);
```

These lines set the index and count of the pages to be saved. In this example, we are saving pages starting from index 2 and a total of 3 pages.

## Step 4: Specify Compression Settings

```java
// Specify compression if required
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Here, we specify the image compression settings for the PDF. We set the compression to JPEG format and specify the JPEG quality as 90%.

## Step 5: Save the Document with Options

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Finally, we save the document with the specified options. The output PDF will be saved at the specified location with the given options.

## Conclusion

In this tutorial, we have learned how to specify save options in OneNote using Aspose.Note for Java. By customizing save options, you can control various aspects of the output document, such as page index, count, and compression settings.

## FAQ's

### Q1: Can Aspose.Note handle large OneNote documents?

A1: Yes, Aspose.Note is designed to handle large OneNote documents efficiently.

### Q2: Is Aspose.Note compatible with the latest Java versions?

A2: Yes, Aspose.Note is compatible with the latest Java versions.

### Q3: Can I convert OneNote documents to other formats using Aspose.Note?

A3: Yes, Aspose.Note supports conversion of OneNote documents to various formats such as PDF, DOCX, and HTML.

### Q4: Does Aspose.Note provide support for encryption and decryption of OneNote documents?

A4: Yes, Aspose.Note provides APIs for encryption and decryption of OneNote documents.

### Q5: Is Aspose.Note suitable for commercial use?

A5: Yes, Aspose.Note can be used for commercial purposes by purchasing a license.

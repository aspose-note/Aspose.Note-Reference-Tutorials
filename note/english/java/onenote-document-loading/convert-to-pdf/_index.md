---
title: Convert OneNote Document to PDF - Java
linktitle: Convert OneNote Document to PDF - Java
second_title: Aspose.Note Java API
description: Learn how to convert OneNote documents to PDF using Aspose.Note for Java. Enhance your document processing capabilities with this step-by-step guide.
type: docs
weight: 16
url: /java/onenote-document-loading/convert-to-pdf/
---
## Introduction

In this tutorial, we'll explore how to convert OneNote documents to PDF using Aspose.Note for Java. Aspose.Note is a powerful Java library that allows seamless manipulation of OneNote files, providing various functionalities to work with different elements within these documents. One common requirement is converting these files into PDF format, which can be easily achieved with Aspose.Note.

## Prerequisites

Before we begin, ensure you have the following prerequisites in place:

1. Java Development Kit (JDK): Make sure you have JDK installed on your system. You can download it from [here](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2. Aspose.Note for Java: You need to have Aspose.Note for Java library. If you haven't already, you can download it from [here](https://releases.aspose.com/note/java/).

## Import Packages

To get started, import the necessary packages into your Java project. You'll need the `com.aspose.note.Document` and `com.aspose.note.PdfSaveOptions` classes.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

Let's break down the process of converting a OneNote document to PDF into multiple steps:

## Step 1: Load the OneNote Document

First, load the OneNote document into Aspose.Note.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

Replace `"Your Document Directory"` with the path to your OneNote document.

## Step 2: Initialize PdfSaveOptions Object

Initialize a `PdfSaveOptions` object, which will specify the options for saving the document as PDF.

```java
PdfSaveOptions options = new PdfSaveOptions();
```

## Step 3: Set Page Index and Count (Optional)

You can optionally set the page index and count if you want to convert only specific pages of the OneNote document.

```java
// Set page index
// options.setPageIndex(2);

// Set page count
// options.setPageCount(3);
```

Uncomment and adjust these lines as needed.

## Step 4: Save the Document as PDF

Save the loaded OneNote document as a PDF file using the specified options.

```java
oneFile.save(dataDir + "ConvertToPdf_out.pdf", options);
```

## Step 5: Display Success Message

Finally, print a message indicating the successful conversion of the document to PDF.

```java
System.out.println("File saved: " + dataDir + "ConvertToPdf_out.pdf");
```

## Conclusion

In this tutorial, we've learned how to convert OneNote documents to PDF using Aspose.Note for Java. By following the step-by-step guide, you can easily integrate this functionality into your Java applications, enhancing your document processing capabilities.

## FAQ's

### Q1: Is Aspose.Note compatible with all versions of OneNote?

A1: Aspose.Note supports various versions of OneNote, ensuring compatibility with most OneNote documents.

### Q2: Can I customize the PDF conversion settings?

A2: Yes, you can customize the PDF conversion settings using the `PdfSaveOptions` class according to your requirements.

### Q3: Does Aspose.Note require a license for commercial use?

A3: Yes, Aspose.Note requires a license for commercial use. You can obtain a license from [here](https://purchase.aspose.com/buy).

### Q4: Is technical support available for Aspose.Note users?

A4: Yes, technical support is available for Aspose.Note users. You can access the support forum [here](https://forum.aspose.com/c/note/28).

### Q5: Can I try Aspose.Note before purchasing?

A5: Yes, you can request a free trial of Aspose.Note from [here](https://releases.aspose.com/).

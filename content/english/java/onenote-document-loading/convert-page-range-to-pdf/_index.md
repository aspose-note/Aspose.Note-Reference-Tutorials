---
title: Convert Specific Page Range to PDF in OneNote with Java
linktitle: Convert Specific Page Range to PDF in OneNote with Java
second_title: Aspose.Note Java API
description: Learn how to convert specific page ranges from OneNote to PDF seamlessly with Aspose.Note for Java. Preserve formatting and layout effortlessly.
type: docs
weight: 11
url: /java/onenote-document-loading/convert-page-range-to-pdf/
---
## Introduction

OneNote is a powerful tool for organizing notes, but sometimes you may need to export specific page ranges to PDF for sharing or archiving purposes. In this tutorial, we'll guide you through the process of converting a specific page range to PDF using Aspose.Note for Java.

## Prerequisites

Before we begin, make sure you have the following prerequisites:

1. Java Development Kit (JDK): Ensure that you have Java installed on your system.
2. Aspose.Note for Java: Download and install Aspose.Note for Java from [here](https://releases.aspose.com/note/java/).
3. Sample OneNote Document: Prepare a sample OneNote document from which you want to extract the specific page range.

## Import Packages

In your Java project, import the necessary packages for using Aspose.Note:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Load the OneNote Document

Load the OneNote document using Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

## Step 2: Initialize PDF Save Options

Initialize the PdfSaveOptions object and specify the page index and count:

```java
PdfSaveOptions opts = new PdfSaveOptions();
opts.setPageIndex(2);  // Starting page index
opts.setPageCount(3);  // Number of pages to include
```

## Step 3: Save as PDF

Save the specified page range as a PDF file:

```java
oneFile.save(dataDir + "ConvertSpecificPageRangeToPdf_out.pdf", opts);
System.out.println("File saved: " + dataDir + "ConvertSpecificPageRangeToPdf_out.pdf");
```

Congratulations! You have successfully converted a specific page range from a OneNote document to a PDF using Aspose.Note for Java.

## Conclusion

In this tutorial, we learned how to convert a specific page range from a OneNote document to PDF using Aspose.Note for Java. This functionality can be useful for various purposes such as sharing selective information or creating archival copies.

## FAQ's

### Q1: Can I specify multiple non-contiguous page ranges for conversion?

A1: Unfortunately, Aspose.Note for Java currently supports converting only contiguous page ranges to PDF.

### Q2: Does Aspose.Note for Java preserve the formatting of the original OneNote document?

A2: Yes, Aspose.Note ensures that the formatting and layout of the original OneNote document are preserved in the generated PDF.

### Q3: Is it possible to convert password-protected OneNote documents to PDF?

A3: Aspose.Note for Java does not support converting password-protected OneNote documents directly. You need to remove the password protection before conversion.

### Q4: Can I customize the appearance of the generated PDF file?

A4: Yes, you can customize various aspects such as page size, orientation, and header/footer settings using Aspose.Note's PDF Save Options.

### Q5: Does Aspose.Note for Java support batch conversion of multiple OneNote documents?

A5: Yes, you can batch convert multiple OneNote documents to PDF by looping through each document and applying the conversion process.

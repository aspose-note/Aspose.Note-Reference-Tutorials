---
title: Use Splitting Algorithm Method in OneNote - Aspose.Note
linktitle: Use Splitting Algorithm Method in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to split OneNote documents efficiently using Aspose.Note for Java.
type: docs
weight: 26
url: /java/onenote-document-saving/use-splitting-algorithm-method/
---
## Introduction

In this tutorial, we'll delve into using the Splitting Algorithm Method in Aspose.Note for Java. Aspose.Note is a powerful library that allows developers to work with Microsoft OneNote files programmatically. Utilizing the Splitting Algorithm can be particularly useful when you need to manipulate and export OneNote documents, especially when dealing with complex layouts or large files.

## Prerequisites

Before we begin, make sure you have the following prerequisites:

1. Java Development Kit (JDK): Ensure you have JDK installed on your system. You can download it from the [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
   
2. Aspose.Note for Java Library: Download and install the Aspose.Note for Java library from the [download link](https://releases.aspose.com/note/java/).

## Import Packages

In your Java project, import the necessary packages to utilize Aspose.Note functionalities.

```java
import java.io.IOException;

import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Define Document Directory

Set up the directory where your OneNote document is located.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the OneNote Document

Load the OneNote document using Aspose.Note's `Document` class.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Step 3: Set PDF Save Options

Create an instance of `PdfSaveOptions` to specify options for saving the document as PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Step 4: Set Page Splitting Algorithm

Choose the appropriate splitting algorithm according to your requirements. Here, we're using `KeepPartAndCloneSolidObjectToNextPageAlgorithm`.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Step 5: Save the Document

Save the document with the specified PDF save options.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Conclusion

In this tutorial, we explored how to utilize the Splitting Algorithm Method in Aspose.Note for Java to manipulate OneNote documents efficiently. By following the steps outlined above, you can seamlessly integrate this functionality into your Java applications, enhancing productivity and flexibility.

## FAQ's

### Q1: Can I use Aspose.Note for Java with other programming languages?

A1: Yes, Aspose.Note is available for multiple platforms and can be used with languages such as .NET, C++, and Python.

### Q2: Is Aspose.Note suitable for processing large OneNote files?

A2: Absolutely! Aspose.Note provides robust features for handling large files efficiently.

### Q3: Where can I find additional resources and support for Aspose.Note?

A3: You can refer to the [documentation](https://reference.aspose.com/note/java/) and [forum](https://forum.aspose.com/c/note/28) for support and guidance.

### Q4: Can I try Aspose.Note before purchasing?

A4: Yes, you can avail of a [free trial](https://releases.aspose.com/) to explore the features before making a purchase.

### Q5: How can I obtain a temporary license for Aspose.Note?

A5: You can request a [temporary license](https://purchase.aspose.com/temporary-license/) to evaluate the product under a trial period.

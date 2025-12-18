---
title: Convert OneNote to PDF with Keep Solid Objects Algorithm
linktitle: Convert OneNote to PDF with Keep Solid Objects Algorithm
second_title: Aspose.Note Java API
description: Learn how to convert OneNote to PDF and save document PDF Java using Aspose.Note's Keep Solid Objects Algorithm in Java.
weight: 25
url: /java/onenote-document-saving/use-keep-solid-objects-algorithm/
date: 2025-12-18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert OneNote to PDF with Keep Solid Objects Algorithm

## Introduction

In this tutorial we’ll walk you through how to **convert onenote to pdf** while preserving solid objects, using the Keep Solid Objects Algorithm provided by Aspose.Note for Java. Whether you’re generating reports, archiving notes, or building a document‑processing pipeline, keeping those solid objects intact is essential for document integrity. We'll also show you how to **save document pdf java** with the same settings.

## Quick Answers
- **What does the Keep Solid Objects Algorithm do?** It ensures that solid objects such as shapes and drawings stay together on a page when a OneNote file is split during PDF conversion.  
- **Do I need a license to try this?** Yes, a free trial license is available from Aspose.  
- **Which Java version is required?** Java 8 or higher is recommended.  
- **Can I adjust the height limit for cloned parts?** Absolutely – you can pass a custom height limit to the algorithm.  
- **Is this approach suitable for large OneNote files?** Yes, the algorithm works efficiently even with multi‑page notes.

## What is “convert onenote to pdf”?

Converting OneNote notebooks to PDF creates a portable, read‑only version of your notes that can be shared across platforms. The conversion process normally splits pages automatically, which can break complex drawings. The Keep Solid Objects Algorithm prevents that by keeping each solid object whole.

## Why use the Keep Solid Objects Algorithm?

- **Preserves visual fidelity** – shapes, charts, and drawings remain exactly as they appear in OneNote.  
- **Reduces manual post‑processing** – no need to re‑align objects after conversion.  
- **Improves PDF rendering** – maintains consistency across PDF viewers.  

## Prerequisites

Before we begin, make sure you have:

1. Java Development Kit (JDK) installed on your system.  
2. Aspose.Note for Java library. You can download it from [here](https://releases.aspose.com/note/java/).  

## Import Packages

First, import the necessary classes:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Load the Document

Load your OneNote file into an `Document` object:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Step 2: Configure PDF Save Options

Create a `PdfSaveOptions` instance and set the page‑splitting algorithm to `KeepSolidObjectsAlgorithm`:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Step 3: Adjust Height Limit (Optional)

If you need finer control over how cloned parts are handled, specify a height limit (in points). This is useful when dealing with very tall objects:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Step 4: Save the Document

Finally, save the OneNote document as a PDF using the configured options:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Common Issues and Solutions

- **Objects still split across pages** – Verify that you are using the latest version of Aspose.Note and that the height limit (if set) is large enough for your objects.  
- **Missing fonts or symbols** – Ensure the required fonts are installed on the machine where the conversion runs.  
- **Performance slowdown on huge notebooks** – Consider processing the notebook in smaller batches or increasing JVM heap size.

## FAQ's

### Q1: Can I adjust the height limit for cloned parts?

A1: Yes, you can adjust the height limit of cloned parts according to your requirements using the `heightLimitOfClonedPart` parameter.

### Q2: Where can I find more documentation?

A2: You can find detailed documentation on Aspose.Note for Java [here](https://reference.aspose.com/note/java/).

### Q3: Is there a free trial available?

A3: Yes, you can get a free trial of Aspose.Note for Java [here](https://releases.aspose.com/).

### Q4: How can I get support if I encounter any issues?

A4: You can get support from the Aspose community [here](https://forum.aspose.com/c/note/28).

### Q5: Where can I purchase a license?

A5: You can purchase a license for Aspose.Note for Java [here](https://purchase.aspose.com/buy).

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
title: Use Keep Solid Objects Algorithm in OneNote - Aspose.Note
linktitle: Use Keep Solid Objects Algorithm in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to preserve solid objects in your Aspose.Note documents when converting to PDF using the Keep Solid Objects Algorithm in Java.
weight: 25
url: /java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Use Keep Solid Objects Algorithm in OneNote - Aspose.Note

## Introduction

In this tutorial, we will explore how to utilize the Keep Solid Objects Algorithm in Aspose.Note for Java. This algorithm is invaluable for maintaining the integrity of solid objects within your documents when converting them to PDF format. We'll break down the process step by step, ensuring clarity and understanding at each stage.

## Prerequisites

Before we begin, ensure you have the following:

1. Java Development Kit (JDK) installed on your system.
2. Aspose.Note for Java library. You can download it from [here](https://releases.aspose.com/note/java/).

## Import Packages

First, let's import the necessary packages:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Load the Document

Load the document into Aspose.Note using the following code snippet:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Step 2: Configure PDF Save Options

Define PdfSaveOptions and set the PageSplittingAlgorithm to KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Step 3: Adjust Height Limit (Optional)

You can adjust the height limit of cloned parts if necessary:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Step 4: Save the Document

Finally, save the document with the specified PDF save options:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Conclusion

In this tutorial, we've learned how to utilize the Keep Solid Objects Algorithm in Aspose.Note for Java. This algorithm ensures that solid objects within your documents are preserved when converting them to PDF format, maintaining document integrity.

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


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

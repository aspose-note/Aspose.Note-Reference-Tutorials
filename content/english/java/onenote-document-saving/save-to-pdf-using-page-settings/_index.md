---
title: Save to PDF Using Page Settings in OneNote - Aspose.Note
linktitle: Save to PDF Using Page Settings in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to save OneNote documents to PDF in Java using Aspose.Note library. Step-by-step guide with code examples for different page settings.
type: docs
weight: 19
url: /java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## Introduction

In this tutorial, we will learn how to save OneNote documents to PDF format using different page settings with Aspose.Note for Java. We'll cover two methods: saving with Letter page settings and saving with A4 page settings without height limit.

## Prerequisites

Before we begin, make sure you have the following prerequisites in place:

1. Java Development Kit (JDK) installed on your system.
2. Aspose.Note for Java library downloaded and included in your Java project.
3. Basic understanding of Java programming language.

## Import Packages

Ensure that you have imported the necessary packages for using Aspose.Note for Java in your project. Here's the import statement:

```java
import com.aspose.note.*;

import java.io.IOException;
import java.nio.file.Paths;
```

## Save to PDF Using Letter Page Settings

### Step 1: Load the Document

Firstly, load the OneNote document into Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Step 2: Define Destination Path

Specify the destination path for the PDF file:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Step 3: Save the Document

Save the document with Letter page settings:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Save to PDF Using A4 Page Settings Without Height Limit

### Step 1: Load the Document

Similarly, load the OneNote document into Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Step 2: Define Destination Path

Specify the destination path for the PDF file:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Step 3: Save the Document

Save the document with A4 page settings without height limit:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

After following these steps, you'll have successfully saved your OneNote document to PDF using different page settings.

## Conclusion

In this tutorial, we have explored how to save OneNote documents to PDF format using Aspose.Note for Java library. By following the step-by-step guide, you can easily integrate this functionality into your Java applications.

## FAQ's

### Q1: Can I customize the page settings further?

A1: Yes, you can customize the page settings according to your requirements using Aspose.Note for Java.

### Q2: Does Aspose.Note support other output formats apart from PDF?

A2: Yes, Aspose.Note supports various output formats including images and HTML.

### Q3: Is Aspose.Note compatible with different versions of OneNote files?

A3: Yes, Aspose.Note supports OneNote files from different versions including .one and .onetoc2.

### Q4: Can I convert multiple OneNote files to PDF in a single run?

A4: Yes, you can batch process multiple OneNote files using Aspose.Note for Java.

### Q5: Is there any trial version available for testing purposes?

A5: Yes, you can get a free trial of Aspose.Note for Java from the website.

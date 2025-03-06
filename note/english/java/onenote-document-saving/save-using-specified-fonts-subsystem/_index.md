---
title: Save Using Specified Fonts Subsystem in OneNote
linktitle: Save Using Specified Fonts Subsystem in OneNote
second_title: Aspose.Note Java API
description: Learn how to save OneNote documents using specified fonts subsystem in Java with Aspose.Note. Ensure consistent font representation across platforms effortlessly.
weight: 22
url: /java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save Using Specified Fonts Subsystem in OneNote

## Introduction

Aspose.Note for Java provides robust capabilities for working with OneNote documents. One common requirement when working with such documents is ensuring that the fonts are maintained properly, especially if the document is to be exported or saved in different formats like PDF. This tutorial will guide you through the process of saving OneNote documents while specifying the fonts subsystem, ensuring consistent and accurate representation of text across various platforms.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites set up:

### 1. Java Development Kit (JDK)

Ensure you have Java Development Kit (JDK) installed on your system. You can download it from [here](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) if you haven't already.

### 2. Aspose.Note for Java Library

Download and set up the Aspose.Note for Java library. You can download it from the [website](https://releases.aspose.com/note/java/).

## Import Packages

Make sure to import the necessary packages in your Java project:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Now let's break down each example into multiple steps to understand the process better.

## Step 1: Save Using Document Fonts Subsystem with Default Font Name

This step demonstrates how to save a document in PDF format using a specified default font name.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

In this step:
- The OneNote document is loaded using Aspose.Note.
- The default font is specified as "Times New Roman".
- The document is saved in PDF format with the specified font.

## Step 2: Save Using Document Fonts Subsystem with Default Font from File

This step demonstrates how to save a document in PDF format using a default font loaded from a file.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

In this step:
- The font file "geo_1.ttf" is loaded.
- The default font is specified from the loaded font file.
- The document is saved in PDF format with the specified font.

## Step 3: Save Using Document Fonts Subsystem with Default Font from Stream

This step demonstrates how to save a document in PDF format using a default font loaded from a stream.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

In this step:
- The font file "geo_1.ttf" is loaded as a stream.
- The default font is specified from the loaded stream.
- The document is saved in PDF format with the specified font.

## Conclusion

In this tutorial, we learned how to save OneNote documents using specified fonts subsystem in Java using Aspose.Note. By following these steps, you can ensure consistent font representation across various platforms when exporting or saving your documents.

## FAQ's

### Q1: Can I specify different fonts for different parts of the document?

A1: Yes, you can specify different fonts for different parts of the document using Aspose.Note for Java.

### Q2: Is Aspose.Note compatible with all versions of OneNote?

A2: Aspose.Note supports various versions of OneNote, ensuring compatibility across different environments.

### Q3: How can I handle missing fonts when saving documents?

A3: Aspose.Note provides options to specify default fonts to handle missing fonts effectively during document saving.

### Q4: Can I customize the font properties such as size and style?

A4: Yes, you can customize font properties such as size, style, and color using Aspose.Note for Java.

### Q5: Is there a trial version available for Aspose.Note for Java?

A5: Yes, you can get a free trial of Aspose.Note for Java from the website.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Save Using Specified Fonts in Aspose.Note
linktitle: Save Using Specified Fonts in Aspose.Note
second_title: Aspose.Note .NET API
description: Learn how to save documents with specified fonts in Aspose.Note for .NET. Customize font settings easily for consistent document formatting.
type: docs
weight: 28
url: /net/loading-and-saving-operations/save-using-specified-fonts/
---
## Introduction

In this tutorial, we will learn how to save documents using specified fonts in Aspose.Note for .NET. We'll explore different methods to achieve this, step by step.

## Prerequisites

Before we begin, ensure you have the following:

1. Aspose.Note for .NET: Make sure you have installed Aspose.Note for .NET. You can download it from [here](https://releases.aspose.com/note/net/).

2. Development Environment: You need a development environment set up for .NET development.

## Import Namespaces

First, let's import the necessary namespaces:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Step 1: Saving with Default Font Name

In this step, we'll save a document using a specified default font name.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // The path to the documents directory.
    string dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Save the document as PDF with specified default font.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Step 2: Saving with Default Font from File

Next, let's save a document using a default font loaded from a file.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // The path to the documents directory.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Save the document as PDF with default font loaded from file.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Step 3: Saving with Default Font from Stream

Lastly, let's save a document using a default font loaded from a stream.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // The path to the documents directory.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Save the document as PDF with default font loaded from stream.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Conclusion

In this tutorial, we explored how to save documents using specified fonts in Aspose.Note for .NET. By following these steps, you can customize font settings according to your requirements, ensuring your documents are formatted as desired.

## FAQ's

### Q1: Can I use any font for saving documents in Aspose.Note?

A1: Yes, you can specify any font for saving documents. Just ensure the font file is accessible and loaded correctly.

### Q2: Is Aspose.Note compatible with different document formats?

A2: Aspose.Note primarily works with OneNote documents but provides options to save in various formats including PDF.

### Q3: How can I handle missing fonts when saving documents?

A3: Aspose.Note offers options to use default fonts in case the specified font is missing, ensuring consistent document formatting.

### Q4: Does Aspose.Note support font embedding in output documents?

A4: Yes, Aspose.Note allows embedding fonts to ensure document portability and consistent rendering across different platforms.

### Q5: Where can I get further assistance with Aspose.Note?

A5: For further assistance or technical support, you can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28).

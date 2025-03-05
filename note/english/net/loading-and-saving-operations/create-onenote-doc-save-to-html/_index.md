---
title: Create OneNote Document and Save to HTML in Aspose.Note
linktitle: Create OneNote Document and Save to HTML in Aspose.Note
second_title: Aspose.Note .NET API
description: Learn how to create and save Microsoft OneNote documents to HTML format in .NET applications using Aspose.Note API. Follow our comprehensive tutorial with step-by-step examples.
type: docs
weight: 14
url: /net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Introduction

Aspose.Note for .NET is a powerful API that allows developers to work with Microsoft OneNote documents programmatically in their .NET applications. With Aspose.Note, you can create, manipulate, and convert OneNote files effortlessly. In this tutorial, we will explore how to create a OneNote document and save it to HTML format using various options provided by the Aspose.Note for .NET API.

## Prerequisites

Before we begin, ensure you have the following prerequisites:

- Basic knowledge of C# programming language.
- Visual Studio installed on your system.
- Aspose.Note for .NET API installed in your project. You can download it from [here](https://releases.aspose.com/note/net/).
- Familiarity with the structure of Microsoft OneNote documents.

## Import Namespaces

Before we dive into the coding part, let's import the necessary namespaces:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Now, let's break down each example into multiple steps and see how to create a OneNote document and save it to HTML format using Aspose.Note for .NET.

## Step 1: Create a OneNote Document with Default Options

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Initialize OneNote document
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Default style for all text in the document.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Save into HTML format
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

In this step, we initialize a new OneNote document, add a page with a title, and save it to HTML format using default options.

## Step 2: Create and Save a Specific Page Range to HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Initialize OneNote document
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Default style for all text in the document.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Save into HTML format
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Here, we demonstrate how to create a document and save a specific page range to HTML format.

## Step 3: Save as HTML to Memory Stream with Embedded Resources

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Load the OneNote document
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Specify HTML saving options
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Save the document to a memory stream
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

This step illustrates how to save a OneNote document to HTML format with embedded resources (CSS, fonts, and images) into a memory stream.

## Step 4: Save as HTML to File with Resources in Separate Files

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Load the OneNote document
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Specify HTML saving options
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Save the document to HTML file with resources stored in separate files
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

In this step, we save a OneNote document to HTML format with all resources (CSS, fonts, and images) stored in separate files.

## Step 5: Save as HTML to Memory Stream with Callbacks to Save Resources

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Specify the saving callbacks configuration
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Specify HTML saving options
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Load the OneNote document
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Save the document to HTML format with resources managed by user-defined callbacks
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Manually append data to the CSS stream
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Here, we demonstrate how to save a OneNote document to HTML format with resources managed by user-defined callbacks.

## Conclusion

In this article, we've explored how to work with OneNote documents and save them to HTML format using Aspose.Note for .NET. By following the step-by-step guide, you can easily

 integrate this functionality into your .NET applications, allowing you to manipulate OneNote files efficiently.

## FAQ's

### Q1: Can I customize the appearance of the saved HTML file?

A1: Yes, you can customize the appearance by modifying the CSS stylesheets generated during the conversion process.

### Q2: Does Aspose.Note support conversion to other formats besides HTML?

A2: Yes, Aspose.Note supports conversion to various formats such as PDF, images, and Microsoft Word documents.

### Q3: Is Aspose.Note compatible with .NET Core applications?

A3: Yes, Aspose.Note is compatible with both .NET Framework and .NET Core applications.

### Q4: Can I extract text and images from OneNote documents using Aspose.Note?

A4: Yes, you can extract text and images as well as perform various other manipulations using Aspose.Note API.

### Q5: Is there a trial version available for testing Aspose.Note features?

A5: Yes, you can download a free trial version from [here](https://releases.aspose.com/).

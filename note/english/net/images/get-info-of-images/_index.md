---
title: How to extract image metadata from OneNote using Aspose.Note
linktitle: How to extract image metadata from OneNote using Aspose.Note
second_title: Aspose.Note .NET API
description: Learn how to extract image metadata and get image dimensions from OneNote files with Aspose.Note for .NET. Step‑by‑step guide for C# developers.
weight: 13
url: /net/images/get-info-of-images/
date: 2026-04-09
keywords:
  - extract image metadata
  - how to extract images
  - get image dimensions
  - load onenote document
  - c# get image properties
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extract Image Metadata with Aspose.Note for .NET

In this hands‑on tutorial you’ll learn **how to extract image metadata**—including width, height, original size, file name, and modification time—from Microsoft OneNote files using the Aspose.Note library for C#. Whether you need to display image thumbnails, validate image sizes, or build a catalog of embedded assets, extracting this information programmatically saves you countless manual steps.

## Quick Answers
- **What does “extract image metadata” mean?** Retrieving properties such as dimensions, file name, and timestamps from images stored inside a OneNote document.  
- **Which library handles this?** Aspose.Note for .NET.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Supported platforms?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Typical runtime?** Less than a second for a standard .one file.

## What is extract image metadata?
Extracting image metadata means programmatically reading the descriptive attributes (width, height, original dimensions, file name, last‑modified time, etc.) that accompany each image object inside a OneNote page. This data is useful for validation, reporting, or further image processing.

## Why extract image metadata from OneNote?
- **Automation** – Build tools that automatically generate image inventories.  
- **Validation** – Ensure images meet size requirements before publishing.  
- **Integration** – Combine OneNote content with other systems that need image details (CMS, DAM, etc.).  
- **Performance** – Avoid loading full image binaries when only dimensions are needed.

## Prerequisites
1. **C# fundamentals** – You should be comfortable writing basic C# code.  
2. **Aspose.Note for .NET** – Download and install the library from the official site [here](https://releases.aspose.com/note/net/).  
3. **A OneNote (.one) file** – Any existing OneNote document that contains images.

## Import Namespaces
Before we start, import the required namespaces:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Step 1: Load the OneNote document
First, load the target OneNote file into an `Aspose.Note.Document` object. This is the **load onenote document** step that prepares the API for further queries.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Replace `"Your Document Directory"` with the actual folder that holds your `.one` file.

## Step 2: Retrieve all image nodes
Now we’ll **how to extract images** by pulling every `Image` node from the document.

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

The `GetChildNodes<T>()` method scans the entire notebook hierarchy and returns a collection of image objects.

## Step 3: Iterate through each image and **c# get image properties**
We’ll loop through the collection and print out the metadata, including the **get image dimensions** and **extract original image size** values.

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

The output shows each image’s current width/height (as rendered in the page), the original dimensions stored in the file, the file name, and the timestamp of the last modification.

## Common Issues and Solutions
| Issue | Reason | Fix |
|-------|--------|-----|
| **NullReferenceException** when `images` is empty | Document contains no images | Verify the source `.one` file actually has embedded images. |
| **Incorrect dimensions** | Images are scaled in OneNote | Use `OriginalWidth`/`OriginalHeight` to obtain the true size. |
| **FileName is empty** | Image was pasted from clipboard | The API may not have a filename; handle `null` or empty strings in your code. |

## Frequently Asked Questions

**Q: Is Aspose.Note compatible with all versions of Microsoft OneNote?**  
A: Aspose.Note supports .one, .onepkg, and .onetoc2 formats, covering most OneNote versions from 2007 onward.

**Q: Can I modify the image properties after extraction?**  
A: Yes, you can change properties such as `Width`, `Height`, or `FileName` and then save the document.

**Q: Does Aspose.Note work with .NET Core?**  
A: Absolutely. The library is fully compatible with .NET Core, .NET 5, and .NET 6.

**Q: Is there a free trial available?**  
A: Yes, you can download a trial version from the Aspose website to explore all features.

**Q: Where can I get additional help or community support?**  
A: Visit the Aspose.Note forum [here](https://forum.aspose.com/c/note/28) for tips, sample code, and answers from the community.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.Note 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
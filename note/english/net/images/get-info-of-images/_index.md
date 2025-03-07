---
title: Get Information of Images in Aspose.Note
linktitle: Get Information of Images in Aspose.Note
second_title: Aspose.Note .NET API
description: Learn how to extract image information from Microsoft OneNote files using Aspose.Note for .NET. Follow our step-by-step guide for efficient development.
weight: 13
url: /net/images/get-info-of-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Get Information of Images in Aspose.Note

## Introduction

In the world of .NET development, Aspose.Note provides a powerful set of tools for working with Microsoft OneNote files. One common task developers often face is extracting information from images embedded within these notes. Whether it's obtaining dimensions, filenames, or modification times, Aspose.Note simplifies this process.

## Prerequisites

Before we dive into extracting image information with Aspose.Note, ensure you have the following:

1. Basic knowledge of C#: Familiarity with C# programming language is essential to understand the code examples.
2. Aspose.Note for .NET installed: Make sure you have the Aspose.Note library installed in your development environment. You can download it [here](https://releases.aspose.com/note/net/).

## Import Namespaces

Before we begin, let's import the necessary namespaces:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Step 1: Load the Document

First, load the target OneNote document into Aspose.Note:

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Replace `"Your Document Directory"` with the path to your OneNote file.

## Step 2: Retrieve Image Information

Next, retrieve all the image nodes from the document:

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

This code snippet fetches all the image nodes within the loaded OneNote document.

## Step 3: Iterate Through Images

Now, let's iterate through each image node to extract its metadata:

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

This loop prints out various attributes of each image, such as width, height, original dimensions, filename, and last modified time.

## Conclusion

With Aspose.Note for .NET, extracting image information from OneNote documents becomes a seamless process. By following the steps outlined in this tutorial, developers can efficiently retrieve metadata from embedded images, empowering them to build robust applications.

## FAQ's

### Q1: Is Aspose.Note compatible with all versions of Microsoft OneNote?

A1: Aspose.Note supports various formats of OneNote files, including .one, .onepkg, and .onetoc2, ensuring compatibility across different versions.

### Q2: Can I modify the image properties using Aspose.Note?

A2: Yes, Aspose.Note allows you to manipulate image properties such as dimensions, filenames, and modification times programmatically.

### Q3: Does Aspose.Note offer support for .NET Core?

A3: Yes, Aspose.Note provides support for .NET Core, enabling cross-platform development for your applications.

### Q4: Is there a free trial available for Aspose.Note?

A4: Yes, you can access a free trial of Aspose.Note to explore its features before making a purchase.

### Q5: Where can I find additional support or assistance with Aspose.Note?

A5: For any inquiries or assistance, you can visit the Aspose.Note forum [here](https://forum.aspose.com/c/note/28).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

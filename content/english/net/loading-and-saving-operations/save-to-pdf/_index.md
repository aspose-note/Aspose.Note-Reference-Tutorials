---
title: Save to PDF in Aspose.Note
linktitle: Save to PDF in Aspose.Note
second_title: Aspose.Note .NET API
description: Learn how to save Microsoft OneNote documents to PDF format using Aspose.Note for .NET. Step-by-step tutorial with code examples for Letter and A4 page layouts.
type: docs
weight: 26
url: /net/loading-and-saving-operations/save-to-pdf/
---
## Introduction

In this tutorial, we'll explore how to save documents to PDF format using Aspose.Note for .NET. Aspose.Note is a powerful library that enables developers to work with Microsoft OneNote files programmatically. We'll cover the prerequisites, import namespaces, and provide step-by-step guides for saving documents to PDF in various page layouts.

## Prerequisites

Before we begin, make sure you have the following:

- Visual Studio installed on your system.
- Aspose.Note for .NET library downloaded and installed. You can download it from [here](https://releases.aspose.com/note/net/).
- Basic knowledge of C# programming language.

## Import Namespaces

First, let's import the necessary namespaces to our C# code:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Now that we have the prerequisites covered and the namespaces imported, let's proceed with saving documents to PDF in different page layouts.

## Step 1: Save to PDF using Letter Page Settings


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // The path to the documents directory.
    string dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Save the document.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explanation:

- We load the OneNote document into Aspose.Note.
- Define the destination path for the saved PDF file.
- Save the document to PDF using `PdfSaveOptions` with `PageSettings` set to `Letter`.

## Step 2: Save to PDF using A4 Page Settings Without Height Limit

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // The path to the documents directory.
    string dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Save the document.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explanation:

- Similar to the previous step, we load the OneNote document into Aspose.Note.
- Define the destination path for the saved PDF file.
- Save the document to PDF using `PdfSaveOptions` with `PageSettings` set to `A4NoHeightLimit`.

## Conclusion

In this tutorial, we learned how to save documents to PDF format using Aspose.Note for .NET. We covered two different page layouts: Letter and A4 without height limit. With Aspose.Note, developers can easily manipulate OneNote files programmatically, providing flexibility and efficiency in document management tasks.

## FAQ's

### Q1: Can Aspose.Note handle complex OneNote files?

A1: Yes, Aspose.Note supports various features and functionalities to handle complex OneNote files effectively.

### Q2: Is Aspose.Note suitable for commercial projects?

A2: Absolutely, Aspose.Note can be used in commercial projects with ease. You can purchase a license [here](https://purchase.aspose.com/buy).

### Q3: Does Aspose.Note offer a free trial?

A3: Yes, you can explore Aspose.Note with a free trial available [here](https://releases.aspose.com/).

### Q4: Where can I find documentation for Aspose.Note?

A4: You can find detailed documentation [here](https://reference.aspose.com/note/net/).

### Q5: Need further assistance?

A5: Feel free to ask any questions or seek support on the Aspose.Note forum [here](https://forum.aspose.com/c/note/28).

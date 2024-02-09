---
title: Dark Theme Transformation with Aspose.Note for .NET
linktitle: Apply Dark Theme to Text in Aspose.Note
second_title: Aspose.Note .NET API
description: Transform your OneNote documents with Aspose.Note for .NET! Apply a sleek dark theme effortlessly. Download now and enhance your note-taking experience.
type: docs
weight: 11
url: /net/text-manipulation/apply-dark-theme-text/
---
## Introduction
Welcome to our step-by-step guide on applying a dark theme to text in Aspose.Note for .NET. Aspose.Note is a powerful .NET API that allows developers to work with Microsoft OneNote files programmatically. In this tutorial, we will explore how to give your OneNote documents a sleek and modern look by applying a dark theme to the text.
## Prerequisites
Before we dive into the tutorial, ensure you have the following prerequisites in place:
- Aspose.Note for .NET: Make sure you have Aspose.Note for .NET installed. If not, you can download it from the [Aspose.Note documentation](https://reference.aspose.com/note/net/).
- Development Environment: Set up your preferred .NET development environment, such as Visual Studio.
- Document Directory: Prepare the directory where your OneNote document is located.
## Import Namespaces
In your .NET project, import the necessary namespaces to work with Aspose.Note:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Step 1: Load the OneNote Document
Load your OneNote document into Aspose.Note using the following code:
```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
// Load the document into Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Step 2: Set Background Color
Set the background color of each page to black:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Step 3: Adjust Text Color
Adjust the font color of the text to white for better visibility:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Step 4: Save the Document
Save the modified OneNote document as a PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Conclusion
Congratulations! You have successfully applied a dark theme to text in your Aspose.Note document. This simple yet effective enhancement can give your OneNote files a more sophisticated appearance.
## Frequently Asked Questions
### Can I apply a dark theme to specific sections of my OneNote document?
Yes, you can customize the code to target specific pages or sections within your document.
### Does Aspose.Note support other export formats besides PDF?
Absolutely! Aspose.Note supports various export formats, including images and Microsoft Word.
### Is there a limit to the document size that Aspose.Note can handle?
Aspose.Note can handle documents of varying sizes, and its performance is optimized for efficiency.
### Can I revert to the original theme after applying the dark theme?
Yes, you can modify the code to switch between themes based on your preferences.
### Where can I get support for Aspose.Note-related queries?
For any assistance, visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) or explore the [documentation](https://reference.aspose.com/note/net/).

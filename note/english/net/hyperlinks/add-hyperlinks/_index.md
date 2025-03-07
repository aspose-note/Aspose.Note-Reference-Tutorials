---
title: Add Hyperlinks in Aspose.Note Documents
linktitle: Add Hyperlinks in Aspose.Note Documents
second_title: Aspose.Note .NET API
description: Learn how to add hyperlinks to Aspose.Note documents using Aspose.Note for .NET. Enhance document interactivity with this step-by-step tutorial.
weight: 10
url: /net/hyperlinks/add-hyperlinks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Add Hyperlinks in Aspose.Note Documents

## Introduction

In this tutorial, you will learn how to add hyperlinks to text within Aspose.Note documents using the .NET framework. Aspose.Note provides powerful features to manipulate OneNote documents programmatically. Adding hyperlinks can enhance the interactivity and usability of your documents, making them more engaging for users.

## Prerequisites:

Before you begin, make sure you have the following prerequisites:

1. Basic understanding of C# programming language.
2. Visual Studio installed on your system.
3. Aspose.Note for .NET library installed. You can download it from [here](https://releases.aspose.com/note/net/).
4. Familiarity with the structure and components of Aspose.Note documents.

## Import Namespaces:

First, you need to import the necessary namespaces into your C# project. These namespaces provide access to the classes and methods required for working with Aspose.Note documents.

```csharp
using System;
using System.Drawing;
```

## Step 1: Create a New Document Object:

Begin by creating a new instance of the Document class. This object will represent your Aspose.Note document, to which you will add the hyperlink.

```csharp
Document doc = new Document();
```

## Step 2: Define Text Styles:

Define the text styles for the regular text and the hyperlink text. You can customize various attributes such as font color, font name, and font size according to your preferences.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

## Step 3: Create RichText Objects:

Create RichText objects for the text segments you want to include in your document. Append the appropriate text and apply the desired text styles to each segment.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

## Step 4: Create Outline and Outline Element:

Create an Outline object and an OutlineElement object to structure your document content. Append the RichText object containing the hyperlink to the OutlineElement.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

## Step 5: Add Elements to Page:

Create a Title object and a Page object. Append the Outline object to the Page. Finally, append the Page to the Document.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Step 6: Save the Document:

Specify the file path where you want to save the Aspose.Note document and call the Save method to save it.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Conclusion:

In this tutorial, you've learned how to add hyperlinks to Aspose.Note documents using Aspose.Note for .NET. By following these steps, you can enhance the interactivity of your documents and provide users with a more dynamic experience.

## FAQ's

### Q1: Can I add multiple hyperlinks within the same document using Aspose.Note?

A1: Yes, you can add multiple hyperlinks to different text segments within a single Aspose.Note document.

### Q2: Can I customize the appearance of hyperlinks in Aspose.Note documents?

A2: Yes, you can customize various attributes such as font color, font size, and font style for hyperlinks in Aspose.Note documents.

### Q3: Does Aspose.Note support hyperlinks to external websites?

A3: Yes, Aspose.Note allows you to create hyperlinks that direct users to external websites or web pages.

### Q4: Is Aspose.Note compatible with all versions of Microsoft OneNote?

A4: Aspose.Note is designed to work with Microsoft OneNote 2010 and later versions.

### Q5: Can I add hyperlinks programmatically using Aspose.Note APIs?

A5: Yes, Aspose.Note provides APIs that allow you to add hyperlinks to text programmatically within your .NET applications.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

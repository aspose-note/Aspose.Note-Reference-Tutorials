---
title: Retrieve Bullet or Number List in Aspose.Note Text
linktitle: Retrieve Bullet or Number List in Aspose.Note Text
second_title: Aspose.Note .NET API
description: Unlock the potential of Aspose.Note for .NET with our step-by-step guide on retrieving bullet or number lists. Elevate your OneNote document manipulation skills!
type: docs
weight: 23
url: /net/text-manipulation/retrieve-bullet-number-list/
---
## Introduction
Welcome to the world of Aspose.Note for .NET, a robust and versatile library that empowers developers to handle OneNote document manipulation effortlessly. In this tutorial, we will delve into the process of retrieving bullet or number lists using Aspose.Note for .NET. Whether you're a seasoned developer or a coding enthusiast, this guide will equip you with the knowledge to navigate through the intricacies of working with lists in Aspose.Note.
## Prerequisites
Before we embark on this coding journey, make sure you have the following prerequisites in place:
- Aspose.Note for .NET: Ensure that you have the Aspose.Note library installed. If not, you can download it from the [official Aspose.Note for .NET documentation](https://reference.aspose.com/note/net/).
- Development Environment: Have a working development environment, preferably Microsoft Visual Studio, set up on your machine.
- Basic Knowledge of C#: Familiarize yourself with C# as this tutorial is written in this language.
## Import Namespaces
In order to interact with Aspose.Note for .NET, you need to import the necessary namespaces into your project. Include the following namespaces at the beginning of your code:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Now, let's break down the process of retrieving bullet or number lists step by step:
## Step 1: Set Your Document Directory
```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
```
Replace `"Your Document Directory"` with the actual path where your Aspose.Note document is located.
## Step 2: Load the Document
```csharp
// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
Ensure that you replace `"ApplyNumberingOnText.one"` with the name of your specific OneNote document.
## Step 3: Retrieve Collection of Nodes
```csharp
// Retrieve a collection of nodes of the outline element.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
This step retrieves a collection of outline nodes from the loaded document.
## Step 4: Iterate Through Each Node
```csharp
// Iterate through each node.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Continue to the next steps...
    }
}
```
This loop ensures that we are only dealing with nodes that contain a number list.
## Step 5: Retrieve Font Information
```csharp
// Retrieve font name
Console.WriteLine("Font Name: " + list.Font);
// Retrieve font length
Console.WriteLine("Font Length: " + list.Font.Length);
// Retrieve font size
Console.WriteLine("Font Size: " + list.FontSize);
// Retrieve font color
Console.WriteLine("Font Color: " + list.FontColor);
// Retrieve format
Console.WriteLine("Font format: " + list.Format);
// Check bold
Console.WriteLine("Is bold: " + list.IsBold);
// Check italic
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
These lines of code extract various font-related information from the number list.
## Conclusion
Congratulations! You've successfully learned how to retrieve bullet or number lists using Aspose.Note for .NET. As you continue your exploration, refer to the [official documentation](https://reference.aspose.com/note/net/) for more in-depth insights and functionalities.
## FAQs
### Can I use Aspose.Note for .NET with other programming languages?
Aspose.Note primarily supports .NET, but there are other versions of the library tailored for different platforms and languages.
### Is Aspose.Note compatible with the latest OneNote formats?
Yes, Aspose.Note supports a wide range of OneNote formats, ensuring compatibility with the latest versions.
### How can I obtain a temporary license for Aspose.Note?
Visit [this link](https://purchase.aspose.com/temporary-license/) to obtain a temporary license for evaluation purposes.
### What support options are available for Aspose.Note users?
You can explore and seek assistance in the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for any queries or issues you may encounter.
### Is there a free trial version of Aspose.Note for .NET?
Yes, you can access the free trial version of Aspose.Note for .NET [here](https://releases.aspose.com/).

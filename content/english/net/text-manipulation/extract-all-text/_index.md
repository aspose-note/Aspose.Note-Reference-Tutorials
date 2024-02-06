---
title: Extract All Text from Aspose.Note
linktitle: Extract All Text from Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 16
url: /net/text-manipulation/extract-all-text/
---

## Complete Source Code
```csharp

using System.IO;
using Aspose.Note;
using System;
using System.Linq;

namespace Aspose.Note.Examples.CSharp.Text
{
    public class ExtractingAllText
    {
        public static void Run()
        {
            // ExStart:ExtractingAllText
            // ExFor:Page.GetChildNodes
            // ExFor:RichText
            // ExFor:RichText.Text
            // ExSummary:Shows how to get all text from the document.

            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_Text();

            // Load the document into Aspose.Note.
            Document oneFile = new Document(dataDir + "Aspose.one");

            // Retrieve text
            string text = string.Join(Environment.NewLine, oneFile.GetChildNodes<RichText>().Select(e => e.Text)) + Environment.NewLine;

            // Print text on the output screen
            Console.WriteLine(text);

            // ExEnd:ExtractingAllText
        }
    }
}
```

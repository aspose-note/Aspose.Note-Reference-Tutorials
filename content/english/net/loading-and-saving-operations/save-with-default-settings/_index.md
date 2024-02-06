---
title: Save with Default Settings in Aspose.Note
linktitle: Save with Default Settings in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 29
url: /net/loading-and-saving-operations/save-with-default-settings/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Note;
using System;

namespace Aspose.Note.Examples.CSharp.Loading_Saving
{
    public class SaveWithDefaultSettings
    {
        public static void Run()
        {
            // ExStart:SaveWithDefaultSettings
            // ExFor:Document
            // ExFor:Document.Save(System.IO.Stream, Aspose.Note.SaveFormat)
            // ExFor:SaveFormat
            // ExSummary:Shows how to save a document in pdf format using default settings.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load the document into Aspose.Note.
            Document oneFile = new Document(dataDir + "Aspose.one");

            // Save the document as PDF
            dataDir = dataDir + "SaveWithDefaultSettings_out.pdf";
            oneFile.Save(dataDir, SaveFormat.Pdf);
            
            // ExEnd:SaveWithDefaultSettings
            
            Console.WriteLine("\nOneNote document saved successfully with default settings.\nFile saved at " + dataDir); 
        }
    }
}
```

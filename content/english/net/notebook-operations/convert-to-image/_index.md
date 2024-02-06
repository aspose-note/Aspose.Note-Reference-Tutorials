---
title: Convert Notebooks to Image in Aspose Note .NET
linktitle: Convert Notebooks to Image in Aspose Note .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 11
url: /net/notebook-operations/convert-to-image/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;

namespace Aspose.Note.Examples.CSharp.WorkingWithNoteBook
{
    public class ConvertToImage
    {
        public static void Run()
        {
            // ExStart:ConvertToImage
            // ExFor:Notebook
            // ExSummary:Shows how to save notebook as image.

            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_NoteBook();

            // Load a OneNote Notebook
            var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");

            dataDir = dataDir + "ConvertToImage_out.png";

            // Save the Notebook
            notebook.Save(dataDir);

            // ExEnd:ConvertToImage

            Console.WriteLine("\nNoteBook document converted to image successfully.\nFile saved at " + dataDir);
        }
    }
}
```

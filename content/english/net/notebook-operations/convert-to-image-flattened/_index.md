---
title: Convert Notebooks to Image (Flattened) in Aspose Note .NET
linktitle: Convert Notebooks to Image (Flattened) in Aspose Note .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 12
url: /net/notebook-operations/convert-to-image-flattened/
---

## Complete Source Code
```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.NoteBook
{
    class ConvertToImageAsFlattenedNotebook
    {
        public static void Run()
        {
            // ExStart:ConvertToImageAsFlattenedNotebook
            // ExFor:Notebook
            // ExFor:NotebookSaveOptions
            // ExFor:NotebookSaveOptions.Flatten
            // ExFor:NotebookImageSaveOptions
            // ExFor:ImageSaveOptions
            // ExFor:ImageSaveOptions.Resolution
            // ExSummary:Shows how to save flattened notebook as image.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load a OneNote Notebook
            var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");

            var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

            var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

            documentSaveOptions.Resolution = 400;
            notebookSaveOptions.Flatten = true;

            dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

            // Save the Notebook
            notebook.Save(dataDir, notebookSaveOptions);

            // ExEnd:ConvertToImageAsFlattenedNotebook
        }
    }
}

```

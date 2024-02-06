---
title: Load Notebooks Instantly in Aspose Note .NET
linktitle: Load Notebooks Instantly in Aspose Note .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 21
url: /net/notebook-operations/load-notebooks-instantly/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.NoteBook
{
    class LoadingNotebookInstantly
    {
        public static void Run()
        {
            // ExStart:LoadingNotebookInstantly
            // ExFor:Notebook
            // ExSummary:Shows how to iterate through preloaded documents of a notebook.

            // By default children loading is "lazy".
            // Therefore for instant loading has took place,
            // it is necessary to set the NotebookLoadOptions.InstantLoading flag.
            NotebookLoadOptions loadOptions = new NotebookLoadOptions { InstantLoading = true };

            String inputFile = "Notizbuch öffnen.onetoc2";
            String dataDir = "Your Document Directory";
            Notebook notebook = new Notebook(dataDir + inputFile, loadOptions);

            // All child documents are already loaded.
            foreach (INotebookChildNode notebookChildNode in notebook.OfType<Document>()) 
            {
               // Do something with child document
            }

            // ExEnd:LoadingNotebookInstantly
        }
    }
}

```

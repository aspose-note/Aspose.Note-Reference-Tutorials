---
title: Load Notebook Files with Load Options in Aspose Note .NET
linktitle: Load Notebook Files with Load Options in Aspose Note .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 20
url: /net/notebook-operations/load-notebook-files-with-load-options/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.NoteBook
{
    class LoadingNotebookFileWithLoadOptions
    {
        public static void Run()
        {
            // ExStart:LoadingNotebookFileWithLoadOptions
            // ExFor:Notebook
            // ExSummary:Shows how to iterate through documents of a notebook loading them lazily.

            string inputFile = "Notizbuch öffnen.onetoc2";
            string dataDir = RunExamples.GetDataDir_NoteBook();

            // By default children loading is "lazy".
            Notebook notebook = new Notebook(dataDir + inputFile);

            foreach (var notebookChildNode in notebook.OfType<Document>()) 
            {
	            // Actual loading of the child document happens only here.
	            // Do something with child document
            }

            // ExEnd:LoadingNotebookFileWithLoadOptions
        }
    }
}

```

---
title: Load Password-Protected Documents in Aspose Note .NET
linktitle: Load Password-Protected Documents in Aspose Note .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 22
url: /net/notebook-operations/load-password-protected-documents/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;

namespace Aspose.Note.Examples.CSharp.WorkingWithNoteBook
{
    public class LoadingPasswordProtectedDoc
    {
        public static void Run()
        {
            // ExStart:LoadingPasswordProtectedDoc
            // ExFor:Notebook
            // ExFor:NotebookLoadOptions
            // ExFor:NotebookLoadOptions.DeferredLoading
            // ExFor:LoadOptions
            // ExFor:LoadOptions.DocumentPassword
            // ExSummary:Shows how to an encrypted notebook.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            var notebook = new Notebook(dataDir + "test.onetoc2", new NotebookLoadOptions() { DeferredLoading = true });

            notebook.LoadChildDocument(dataDir + "Aspose.one");  
            notebook.LoadChildDocument(dataDir + "Locked Pass1.one", new LoadOptions() { DocumentPassword = "pass" });
            notebook.LoadChildDocument(dataDir + "Locked Pass2.one", new LoadOptions() { DocumentPassword = "pass2" });

            // ExEnd:LoadingPasswordProtectedDoc       
        }
    }
}

```

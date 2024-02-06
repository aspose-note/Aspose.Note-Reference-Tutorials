---
title: Create Password-Protected Documents in Aspose Note .NET
linktitle: Create Password-Protected Documents in Aspose Note .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 18
url: /net/notebook-operations/create-password-protected-documents/
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
    public class CreatingPasswordProtectedDoc
    {
        public static void Run()
        {
            // ExStart:CreatingPasswordProtectedDoc
            // ExFor:Document
            // ExFor:OneSaveOptions
            // ExFor:OneSaveOptions.DocumentPassword
            // ExSummary:Shows how to save document with encryption.

            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_NoteBook();

            Document document = new Document();
            document.Save(dataDir + "CreatingPasswordProtectedDoc_out.one", new OneSaveOptions() { DocumentPassword = "pass" });

            // ExEnd:CreatingPasswordProtectedDoc       
        }
    }
}

```

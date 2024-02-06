---
title: Save Document to OneNote Format in Aspose.Note
linktitle: Save Document to OneNote Format in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 20
url: /net/loading-and-saving-operations/save-doc-to-onenote-format/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.Loading_Saving
{
    class SaveDocToOneNoteFormat
    {
        public static void Run()
        {
            // ExStart:SaveDocToOneNoteFormat
            // ExFor:Document
            // ExFor:Document.Save(System.String)
            // ExSummary:Shows how to save a document.

            string inputFile = "Sample1.one";
            string dataDir = "Your Document Directory";
            string outputFile = "SaveDocToOneNoteFormat_out.one";
            
            Document doc = new Document(dataDir + inputFile);
            doc.Save(dataDir + outputFile);
            
            // ExEnd:SaveDocToOneNoteFormat
        }
    }
}

```

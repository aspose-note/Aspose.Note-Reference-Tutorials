---
title: Print Documents using Aspose.Note for .NET
linktitle: Print Documents using Aspose.Note for .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 10
url: /net/printing-document/print-documents/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.PrintingDocument
{
    class PrintDocument
    {
        public static void Run()
        {
            // ExStart:PrintDocument
            // ExFor:Document
            // ExFor:Document.Print
            // ExSummary:Shows how to sent document to a printer using standard Windows dialog with default options.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            var document = new Aspose.Note.Document(dataDir + "Aspose.one");

            document.Print();

            // ExEnd:PrintDocument
        }
    }
}

```

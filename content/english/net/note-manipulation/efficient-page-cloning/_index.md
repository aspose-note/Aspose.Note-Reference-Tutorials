---
title: Clone Pages Efficiently with Aspose.Note
linktitle: Clone Pages Efficiently with Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 16
url: /net/note-manipulation/efficient-page-cloning/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.Pages
{
    class PageClone
    {
        public static void Run()
        {
            // ExStart: PageClone
            // ExFor:Document
            // ExFor:Page.Clone
            // ExSummary:Shows how to clone a page.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load OneNote document
            Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });

            // Clone into new document without history
            var cloned = new Document();
            cloned.AppendChildLast(document.FirstChild.Clone());

            // Clone into new document with history
            cloned = new Document();
            cloned.AppendChildLast(document.FirstChild.Clone(true));

            // ExEnd: PageClone
        }
    }
}

```

---
title: Push and Manage Current Page Versions in Aspose.Note
linktitle: Push and Manage Current Page Versions in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 17
url: /net/note-manipulation/manage-current-page-versions/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;

namespace Aspose.Note.Examples.CSharp.Pages
{
    public class PushCurrentPageVersion
    {
        public static void Run()
        {
            // ExStart:PushCurrentPageVersion
            // ExFor:Page.Clone
            // ExSummary:Shows how to push current version of a page to history.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load OneNote document and get first child           
            Document document = new Document(dataDir + "Aspose.one");
            Page page = document.FirstChild;

            var pageHistory = document.GetPageHistory(page);

            pageHistory.Add(page.Clone());

            document.Save(dataDir + "PushCurrentPageVersion_out.one");

            // ExEnd:PushCurrentPageVersion
        }
    }
}
```

---
title: Modify Page History in Aspose.Note
linktitle: Modify Page History in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 15
url: /net/note-manipulation/modify-page-history/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;

namespace Aspose.Note.Examples.CSharp.Pages
{
    public class ModifyPageHistory
    {
        public static void Run()
        {
            // ExStart:ModifyPageHistory
            // ExFor:Document
            // ExFor:Document.GetPageHistory
            // ExFor:Page.Title
            // ExFor:Title
            // ExFor:Title.TitleText
            // ExSummary:Shows how to edit page's history.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load OneNote document and get first child           
            Document document = new Document(dataDir + "Aspose.one");
            Page page = document.FirstChild;

            var pageHistory = document.GetPageHistory(page);

            pageHistory.RemoveRange(0, 1);

            pageHistory[0] = new Page(document);
            if (pageHistory.Count > 1)
            {
                pageHistory[1].Title.TitleText.Text = "New Title";

                pageHistory.Add(new Page(document));

                pageHistory.Insert(1, new Page(document));

                document.Save(dataDir + "ModifyPageHistory_out.one");
            }

            // ExEnd:ModifyPageHistory
        }
    }
}
```

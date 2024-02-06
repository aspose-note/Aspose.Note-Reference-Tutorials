---
title: Set Background Color of Pages in Aspose.Note
linktitle: Set Background Color of Pages in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 19
url: /net/note-manipulation/set-page-background-color/
---

## Complete Source Code
```csharp
// -----------------------------------------------------------------------
//  <copyright file="SetPageBackgroundColor.cs" company="Aspose Pty Ltd">
//    Copyright (c) 2002-2022 Aspose Pty Ltd. All Rights Reserved.
//  </copyright>
// -----------------------------------------------------------------------

namespace Aspose.Note.Examples.CSharp.Pages
{
    using System.Drawing;
    using System.IO;

    public class SetPageBackgroundColor
    {
        public static void Run()
        {
            // ExStart:SetPageBackgroundColor
            // ExFor:Page
            // ExFor:Page.BackgroundColor
            // ExSummary:Shows how to set page's background color.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load OneNote document and get first child           
            Document document = new Document(Path.Combine(dataDir, "Aspose.one"));

            foreach (var page in document)
            {
                page.BackgroundColor = Color.BlueViolet;
            }

            document.Save(Path.Combine(dataDir, "SetPageBackgroundColor.one"));

            // ExEnd:SetPageBackgroundColor
        }
    }
}

```

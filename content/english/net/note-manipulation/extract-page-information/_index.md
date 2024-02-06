---
title: Extract Page Information with Aspose.Note for .NET
linktitle: Extract Page Information with Aspose.Note for .NET
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 13
url: /net/note-manipulation/extract-page-information/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;

namespace Aspose.Note.Examples.CSharp.Pages
{
    public class GetPageInformation
    {
        public static void Run()
        {
            // ExStart:GetPageInformation
            // ExFor:Document
            // ExFor:Page
            // ExFor:Page.LastModifiedTime
            // ExFor:Page.CreationTime
            // ExFor:Page.Title
            // ExFor:Page.Level
            // ExFor:Page.Author
            // ExSummary:Shows how to get meta information about a page.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load the document into Aspose.Note.
            Document oneFile = new Document(dataDir + "Aspose.one");

            foreach (Page page in oneFile)
            {
                Console.WriteLine("LastModifiedTime: {0}", page.LastModifiedTime);
                Console.WriteLine("CreationTime: {0}", page.CreationTime);
                Console.WriteLine("Title: {0}", page.Title);
                Console.WriteLine("Level: {0}", page.Level);
                Console.WriteLine("Author: {0}", page.Author);
                Console.WriteLine();
            }

            // ExEnd:GetPageInformation
        }
    }
}
```

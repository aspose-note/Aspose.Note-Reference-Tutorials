---
title: Insert Images with Hyperlinks in Aspose.Note
linktitle: Insert Images with Hyperlinks in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 15
url: /net/images/insert-image-hyperlink/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Note.Examples.CSharp.Images
{
    class ImageWithHyperlink
    {
        public static void Run()
        {
            // ExStart: ImageWithHyperlink
            // ExFor:Document
            // ExFor:Image
            // ExFor:Image.HyperlinkUrl
            // ExSummary:Shows how to bind a hyperlink to an image.

            // The path to the documents directory.
            string dataDir = "Your Document Directory"; 
            
            var document = new Document();

            var page = new Page(document);

            var image = new Image(document, dataDir + "image.jpg") { HyperlinkUrl = "http://image.com" };

            page.AppendChildLast(image);
            
            document.AppendChildLast(page);
            
            document.Save(dataDir + "Image with Hyperlink_out.one");
            
            // ExEnd: ImageWithHyperlink
        }
    }
}

```

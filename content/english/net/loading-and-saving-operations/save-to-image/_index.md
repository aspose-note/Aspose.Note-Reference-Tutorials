---
title: Save to Image in Aspose.Note
linktitle: Save to Image in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 23
url: /net/loading-and-saving-operations/save-to-image/
---

## Complete Source Code
```csharp
// -----------------------------------------------------------------------
//  <copyright file="SaveToBmpImageUsingImageSaveOptions.cs" company="Aspose Pty Ltd">
//    Copyright (c) 2002-2020 Aspose Pty Ltd. All Rights Reserved.
//  </copyright>
// -----------------------------------------------------------------------

namespace Aspose.Note.Examples.CSharp.Loading_and_Saving
{
    using System;

    using Aspose.Note.Saving;

    class SaveToBmpImageUsingImageSaveOptions
    {
        public static void Run()
        {
            // ExStart:SaveToBmpImageUsingImageSaveOptions
            // ExFor:Document.Save(System.String, Aspose.Note.Saving.SaveOptions)
            // ExFor:SaveFormat
            // ExFor:ImageSaveOptions
            // ExSummary:Shows how to save a document as image in Bmp format using ImageSaveOptions.

            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load the document into Aspose.Note.
            Document oneFile = new Document(dataDir + "Aspose.one");

            dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

            // Save the document.
            oneFile.Save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));

            // ExEnd:SaveToBmpImageUsingImageSaveOptions

            Console.WriteLine("\nOneNote document converted successfully to image in Bmp format.\nFile saved at " + dataDir);
        }
    }
}

```

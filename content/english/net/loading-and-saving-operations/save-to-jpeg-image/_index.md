---
title: Save to JPEG Image in Aspose.Note
linktitle: Save to JPEG Image in Aspose.Note
second_title: Aspose.Note .NET API
description: 
type: docs
weight: 25
url: /net/loading-and-saving-operations/save-to-jpeg-image/
---

## Complete Source Code
```csharp
// -----------------------------------------------------------------------
//  <copyright file="SaveToJpegImageUsingSaveFormat.cs" company="Aspose Pty Ltd">
//    Copyright (c) 2002-2020 Aspose Pty Ltd. All Rights Reserved.
//  </copyright>
// -----------------------------------------------------------------------

namespace Aspose.Note.Examples.CSharp.Loading_and_Saving
{
    using System;

    using Aspose.Note.Saving;

    class SaveToJpegImageUsingSaveFormat
    {
        public static void Run()
        {
            // ExStart:SaveToJpegImageUsingSaveFormat
            // ExFor:Document.Save(System.String, Aspose.Note.Saving.SaveOptions)
            // ExFor:SaveFormat
            // ExFor:ImageSaveOptions
            // ExSummary:Shows how to save a document as image in Jpeg format using SaveFormat.

            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_LoadingAndSaving();

            // Load the document into Aspose.Note.
            Document oneFile = new Document(dataDir + "Aspose.one");

            dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

            // Save the document.
            oneFile.Save(dataDir, SaveFormat.Jpeg);

            // ExEnd:SaveToJpegImageUsingSaveFormat

            Console.WriteLine("\nOneNote document converted successfully to image in Jpeg format.\nFile saved at " + dataDir);
        }
    }
}

```

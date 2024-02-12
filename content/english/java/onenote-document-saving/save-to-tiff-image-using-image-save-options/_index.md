---
title: Save to TIFF Image Using Image Save Options in OneNote
linktitle: Save to TIFF Image Using Image Save Options in OneNote
second_title: Aspose.Note Java API
description: 
type: docs
weight: 21
url: /java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

## Complete Source Code
```java


import com.aspose.note.*;
import com.aspose.note.examples.Utils;

import java.io.IOException;
import java.nio.file.Paths;

public class SaveToTiffImageUsingImageSaveOptions {
    public static void main(String... args) throws IOException {
        SaveToTiffUsingJpegCompression();
        SaveToTiffUsingPackBitsCompression();
        SaveToTiffUsingCcitt3Compression();

        System.out.println("\nDocument saved in TIFF format at " + Utils.getSharedDataDir(SaveOneNoteDocToStream.class) + "load");
    }

    public static void SaveToTiffUsingJpegCompression() throws IOException
    {
        // ExStart:SaveToTiffUsingJpegCompression
        // ExSummary:Shows how to save a document as image in Tiff format using Jpeg compression.

        // The path to the documents directory.
        String dataDir = Paths.get(Utils.getSharedDataDir(SaveOneNoteDocToStream.class), "load").toString();

        // Load the document into Aspose.Note.
        Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

        ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
        options.setTiffCompression(TiffCompression.Jpeg);
        options.setQuality(93);

        oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);

        // ExEnd:SaveToTiffUsingJpegCompression
    }

    public static void SaveToTiffUsingPackBitsCompression() throws IOException
    {
        // ExStart:SaveToTiffUsingPackBitsCompression
        // ExSummary:Shows how to save a document as image in Tiff format using PackBits compression.

        // The path to the documents directory.
        String dataDir = Paths.get(Utils.getSharedDataDir(SaveOneNoteDocToStream.class), "load").toString();

        // Load the document into Aspose.Note.
        Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

        ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
        options.setTiffCompression(TiffCompression.PackBits);

        oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);

        // ExEnd:SaveToTiffUsingPackBitsCompression
    }

    public static void SaveToTiffUsingCcitt3Compression() throws IOException
    {
        // ExStart:SaveToTiffUsingCcitt3Compression
        // ExSummary:Shows how to save a document as image in Tiff format using CCITT Group 3 fax compression.

        // The path to the documents directory.
        String dataDir = Paths.get(Utils.getSharedDataDir(SaveOneNoteDocToStream.class), "load").toString();

        // Load the document into Aspose.Note.
        Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

        ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
        options.setColorMode(ColorMode.BlackAndWhite);
        options.setTiffCompression(TiffCompression.Ccitt3);

        oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);

        // ExEnd:SaveToTiffUsingCcitt3Compression
    }
}

```

---
title: Save to BMP Image Using Image Save Options in OneNote
linktitle: Save to BMP Image Using Image Save Options in OneNote
second_title: Aspose.Note Java API
description: 
type: docs
weight: 16
url: /java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
---

## Complete Source Code
```java


import com.aspose.note.*;


import java.io.IOException;

public class SaveToBmpImageUsingImageSaveOptions {
    public static void main(String... args) throws IOException {
        // ExStart:SaveToBmpImageUsingImageSaveOptions
        // ExFor:Document.save(java.lang, com.aspose.note.SaveOptions)
        // ExFor:SaveFormat
        // ExFor:ImageSaveOptions
        // ExSummary:Shows how to save a document as image in Bmp format using ImageSaveOptions.

        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Load the document into Aspose.Note.
        Document oneFile = new Document(dataDir + "Aspose.one");

        dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

        // Save the document.
        oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));

        // ExEnd:SaveToBmpImageUsingImageSaveOptions
    }
}

```
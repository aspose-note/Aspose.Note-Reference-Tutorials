---
title: Save to Binary Image Using Fixed Threshold in OneNote
linktitle: Save to Binary Image Using Fixed Threshold in OneNote
second_title: Aspose.Note Java API
description: 
type: docs
weight: 14
url: /java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---

## Complete Source Code
```java


import com.aspose.note.*;


import java.io.IOException;

public class SaveToBinaryImageUsingFixedThreshold {
    public static void main(String... args) throws IOException {
        // ExStart:SaveToBinaryImageUsingFixedThreshold
        // ExFor:Document.save(java.lang, com.aspose.note.SaveOptions)
        // ExFor:SaveFormat
        // ExFor:ImageSaveOptions
        // ExFor:ImageSaveOptions.setColorMode(int)
        // ExFor:ImageSaveOptions.setBinarizationOptions(com.aspose.note.ImageBinarizationOptions)
        // ExFor:ColorMode
        // ExFor:ImageBinarizationOptions
        // ExFor:ImageBinarizationOptions.setBinarizationMethod(int)
        // ExFor:ImageBinarizationOptions.setBinarizationThreshold(int)
        // ExFor:BinarizationMethod
        // ExSummary:Shows how to save a document as binary image using fixed threshold.

        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Load the document into Aspose.Note.
        Document oneFile = new Document(dataDir + "Aspose.one");

        dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";

        ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
        binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
        binarizationOptions.setBinarizationThreshold(123);

        ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
        options.setColorMode(ColorMode.BlackAndWhite);
        options.setBinarizationOptions(binarizationOptions);

        // Save the document as gif.
        oneFile.save(dataDir, options);

        // ExEnd:SaveToBinaryImageUsingFixedThreshold
    }
}

```
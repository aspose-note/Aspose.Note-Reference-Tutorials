---
title: Specify Save Options in OneNote - Aspose.Note
linktitle: Specify Save Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 24
url: /java/onenote-document-saving/specify-save-options/
---

## Complete Source Code
```java


import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.examples.Utils;

import java.io.IOException;

public class SpecifySaveOptions {
    public static void main(String[] args) throws IOException {
        // ExStart:SpecifySaveOptions
        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Load the document into Aspose.Note.
        Document doc = new Document(dataDir + "Aspose.one");

        // Initialize PdfSaveOptions object
        PdfSaveOptions opts = new PdfSaveOptions();

        // Set page index
        opts.setPageIndex(2);

        // Set page count
        opts.setPageCount(3);

        //Specify compression if required
        opts.setImageCompression(PdfImageCompression.Jpeg);
        opts.setJpegQuality(90);
        
        dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
        doc.save(dataDir, opts);
        // ExEnd:SpecifySaveOptions
    }
}

```

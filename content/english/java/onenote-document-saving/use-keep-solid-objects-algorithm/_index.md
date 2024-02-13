---
title: Use Keep Solid Objects Algorithm in OneNote - Aspose.Note
linktitle: Use Keep Solid Objects Algorithm in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 25
url: /java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;


public class UsingKeepSolidObjectsAlgorithm {
	public static void main(String... args) throws IOException {
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory";

        // Load the document into Aspose.Note.
        Document doc = new Document(dataDir + "Aspose.one");
		// ExStart:KeepSOlidObjectsAlgoirthm-1
        PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
        pdfSaveOptions.setPageSplittingAlgorithm(new AlwaysSplitObjectsAlgorithm());
        // Or
        pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm());
        // Or
        pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
        // ExEnd:KeepSOlidObjectsAlgoirthm-1

        // ExStart:KeepSOlidObjectsAlgoirthm-2
        float heightLimitOfClonedPart = 500;
        pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(heightLimitOfClonedPart));
        // Or
        pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
        // ExEnd:KeepSOlidObjectsAlgoirthm-2

        // ExStart:KeepSOlidObjectsAlgoirthm-3
        pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(100));
        // ExEnd:KeepSOlidObjectsAlgoirthm-3
        // Or
        // ExStart:KeepSOlidObjectsAlgoirthm-4
        pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(400));
        // ExEnd:KeepSOlidObjectsAlgoirthm-4
        dataDir = dataDir + "UsingKeepSOlidObjectsAlgoirthm_out.pdf";
        doc.save(dataDir);
        }
}

```
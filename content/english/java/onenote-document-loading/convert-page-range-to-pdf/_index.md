---
title: Convert Specific Page Range to PDF in OneNote with Java
linktitle: Convert Specific Page Range to PDF in OneNote with Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 11
url: /java/onenote-document-loading/convert-page-range-to-pdf/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;


public class ConvertSpecificPageRangeToPdf {
	public static void main(String... args) throws IOException {
		// ExStart:SaveRangeOfPagesAsPDF
		// Load the document into Aspose.Note.
		String dataDir = "Your Document Directory";
		
		Document oneFile = new Document(dataDir + "Sample1.one");

		// Initialize PdfSaveOptions object
		PdfSaveOptions opts = new PdfSaveOptions();
		// Set page index
		opts.setPageIndex(2);
		// Set page count
		opts.setPageCount(3);

		// Save the document as PDF
		oneFile.save(dataDir +"ConvertSpecificPageRangeToPdf_out.pdf", opts);
		System.out.println("File saved: " + dataDir + "ConvertSpecificPageRangeToPdf_out.pdf");
		// ExEnd:SaveRangeOfPagesAsPDF
	}
}

```

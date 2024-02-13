---
title: Convert Notebook to PDF in OneNote - Aspose.Note
linktitle: Convert Notebook to PDF in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 15
url: /java/onenote-notebook-operations/convert-notebook-to-pdf/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;


public class ConvertToPdf {
	public static void main(String... args) throws IOException {

		String dataDir = "Your Document Directory";
		
		// Load the document into Aspose.Note
		Document oneFile = new Document(dataDir+"Sample1.one");

		// Initialize PdfSaveOptions object
		PdfSaveOptions options = new PdfSaveOptions();

		// Set page index. Uncomment to skip first two pages
		// options.setPageIndex(2);

		// Set page count. Uncomment to convert only 3 pages, starting from
		// options.getPageIndex().
		// options.setPageCount(3);

		// Save the document as PDF
		oneFile.save(dataDir + "ConvertToPdf_out.pdf", options);

		System.out.println("File saved: " + dataDir + "ConvertToPdf_out.pdf");

	}
}

```
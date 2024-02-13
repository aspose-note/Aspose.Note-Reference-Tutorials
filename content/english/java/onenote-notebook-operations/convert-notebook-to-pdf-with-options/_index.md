---
title: Convert Notebook to PDF with Options in OneNote - Aspose.Note
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 17
url: /java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;


public class ConvertToPDFWithOptions {
	public static void main(String... args) throws IOException {
		// ExStart:ConvertToPDFWithOptions
		String dataDir = "Your Document Directory";
		
		// Load a OneNote Notebook
		Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");

		NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();

		PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

		documentSaveOptions.setPageSplittingAlgorithm (new KeepSolidObjectsAlgorithm());

		dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";

		// Save the Notebook
		notebook.save(dataDir, notebookSaveOptions);
		// ExEnd:ConvertToPDFWithOptions
	}

}

```

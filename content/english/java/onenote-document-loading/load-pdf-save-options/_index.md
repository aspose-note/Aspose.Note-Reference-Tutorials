---
title: Load OneNote Document into Aspose.Note using PdfSaveOptions
linktitle: Load OneNote Document into Aspose.Note using PdfSaveOptions
second_title: Aspose.Note Java API
description: 
type: docs
weight: 23
url: /java/onenote-document-loading/load-pdf-save-options/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;


public class LoadDocIntoAsposeNoteUsingPdfsaveoptions {
	public static void main(String... args) throws IOException {
		// Load the document into Aspose.Note.
		String dataDir = "Your Document Directory";
		Document oneFile = new Document(dataDir + "Sample1.one");
		// Save the document as PDF
		oneFile.save(dataDir + "LoadDocIntoAsposeNoteUsingPdfsaveoptions_out.pdf", new PdfSaveOptions());
	}
}

```

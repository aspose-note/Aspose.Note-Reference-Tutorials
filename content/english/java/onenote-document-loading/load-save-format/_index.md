---
title: Load OneNote Document into Aspose.Note using SaveFormat - Java
linktitle: Load OneNote Document into Aspose.Note using SaveFormat - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 24
url: /java/onenote-document-loading/load-save-format/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.SaveFormat;


public class LoadDocIntoAsposeNoteUsingSaveformat {
	public static void main(String... args) throws IOException {
		// ExStart:SaveDocToOneNoteFormatUsingSaveFormat
		// Load the document into Aspose.Note.
		String dataDir = "Your Document Directory";
		Document oneFile = new Document(dataDir + "Sample1.one");

		// Save the document as PDF
		oneFile.save(dataDir + "LoadDocIntoAsposeNoteUsingSaveformat_out.pdf", SaveFormat.Pdf);
		// ExEnd:SaveDocToOneNoteFormatUsingSaveFormat
	}
}

```

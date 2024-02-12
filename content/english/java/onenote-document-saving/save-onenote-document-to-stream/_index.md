---
title: Save OneNote Document to Stream - Aspose.Note
linktitle: Save OneNote Document to Stream - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 13
url: /java/onenote-document-saving/save-onenote-document-to-stream/
---

## Complete Source Code
```java


import java.io.ByteArrayOutputStream;
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
import com.aspose.note.examples.Utils;

public class SaveOneNoteDocToStream {
	public static void main(String... args) throws IOException {
		// ExStart:SaveOneNoteDocToStream
		// Load the document into Aspose.Note.
		String dataDir = Utils.getSharedDataDir(SaveOneNoteDocToStream.class) + "load/";

		Document doc = new Document(dataDir + "Sample1.one");

		ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

		doc.save(dstStream, SaveFormat.Pdf);
		// ExEnd:SaveOneNoteDocToStream
	}
}

```

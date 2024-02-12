---
title: Save Document to OneNote Format - Aspose.Note
linktitle: Save Document to OneNote Format - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 10
url: /java/onenote-document-saving/save-document-to-onenote-format/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.examples.Utils;

public class SaveDocToOneNoteFormat {

	public static void main(String... args) throws IOException {
		// ExStart:SaveDocToOneNoteFormat
		String dataDir = "Your Document Directory";
		
		Document doc = new Document(dataDir + "Sample1.one");
		doc.save(dataDir + "SaveDocToOneNoteFormat_out.one");
		// ExEnd:SaveDocToOneNoteFormat
	}
}

```

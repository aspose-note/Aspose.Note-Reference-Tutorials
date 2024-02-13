---
title: Save Document to OneNote Using SaveFormat - Aspose.Note
linktitle: Save Document to OneNote Using SaveFormat - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 12
url: /java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.SaveFormat;


public class SaveDocToOneNoteFormatUsingSaveformat {

	public static void main(String... args) throws IOException {
		// ExStart:SaveDocToOneNoteFormatUsingSaveFormat
		String dataDir = "Your Document Directory";
		
		Document document = new Document(dataDir + "Sample1.one");

		document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
		// ExEnd:SaveDocToOneNoteFormatUsingSaveFormat
	}
}

```

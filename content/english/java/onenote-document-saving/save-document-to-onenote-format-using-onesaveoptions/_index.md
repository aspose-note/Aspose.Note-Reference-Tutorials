---
title: Save Document to OneNote Using OneSaveOptions - Aspose.Note
linktitle: Save Document to OneNote Using OneSaveOptions - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 11
url: /java/onenote-document-saving/save-document-to-onenote-format-using-onesaveoptions/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.OneSaveOptions;
import com.aspose.note.examples.Utils;

public class SaveDocToOneNoteFormatUsingOnesaveoptions {

	public static void main(String... args) throws IOException {
		// ExStart:SaveDocToOneNoteFormatUsingOnesaveoptions
		String dataDir = "Your Document Directory";

		Document document = new Document(dataDir + "Sample1.one");

		document.save(dataDir + "SaveDocToOneNoteFormatUsingOnesaveoptions_out.one", new OneSaveOptions());
		// ExEnd:SaveDocToOneNoteFormatUsingOnesaveoptions
	}
}

```

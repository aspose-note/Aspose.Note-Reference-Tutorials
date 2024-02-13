---
title: Load Password-Protected OneNote Document - Java
linktitle: Load Password-Protected OneNote Document - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 27
url: /java/onenote-document-loading/load-password-protected-onenote/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;


public class LoadPasswordProtectedOneNoteDoc {
	public static void main(String... args) throws IOException {
		// ExStart:PasswordProtectedDoc
		String dataDir = "Your Document Directory";

		LoadOptions loadOptions = new LoadOptions();

		loadOptions.setDocumentPassword("password");

		Document doc = new Document(dataDir + "Sample1.one", loadOptions);
		
		System.out.println(doc.getFileFormat());
		// ExEnd:PasswordProtectedDoc
	}
}

```

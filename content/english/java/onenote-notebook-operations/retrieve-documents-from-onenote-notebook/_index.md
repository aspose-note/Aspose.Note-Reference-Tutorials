---
title: Retrieve Documents from OneNote Notebook - Aspose.Note
linktitle: Retrieve Documents from OneNote Notebook - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 25
url: /java/onenote-notebook-operations/retrieve-documents-from-onenote-notebook/
---

## Complete Source Code
```java


import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.Notebook;
import com.aspose.note.examples.Utils;

public class RetrieveDocumentsfromOneNoteNotebook {
	public static void main(String... args) throws IOException {
		// ExStart:RetrieveDocumentsfromOneNoteNotebook
		String dataDir = "Your Document Directory";
		Notebook rootNotebook = new Notebook(dataDir + "test.onetoc2");

		List<Document> allDocuments = rootNotebook.getChildNodes(Document.class);
		for (Document document : allDocuments) {
			System.out.println(document.getDisplayName());
		}
		// ExEnd:RetrieveDocumentsfromOneNoteNotebook
	}

}

```

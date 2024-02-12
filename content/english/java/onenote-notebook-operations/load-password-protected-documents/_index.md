---
title: Load Password-Protected Documents in OneNote - Aspose.Note
linktitle: Load Password-Protected Documents in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 22
url: /java/onenote-notebook-operations/load-password-protected-documents/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.LoadOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookLoadOptions;
import com.aspose.note.examples.Utils;

public class LoadPasswordProtectedDocuments {
	public static void main(String... args) throws IOException {
		// ExStart:LoadingPasswordProtectedDoc
		// Load the document into Aspose.Note.
		String dataDir = "Your Document Directory";
		
		NotebookLoadOptions loadOptions = new NotebookLoadOptions();
		loadOptions.setDeferredLoading(true);
		Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2", loadOptions);

		notebook.loadChildDocument(dataDir + "Neuer Abschnitt 1.one");

		LoadOptions documentLoadOptions1 = new LoadOptions();
		documentLoadOptions1.setDocumentPassword("pass");
		notebook.loadChildDocument(dataDir + "Locked Pass1.one", documentLoadOptions1);

		LoadOptions documentLoadOptions2 = new LoadOptions();
		documentLoadOptions2.setDocumentPassword("pass");
		notebook.loadChildDocument(dataDir + "Locked Pass2.one", documentLoadOptions2);
		// ExEnd:LoadingPasswordProtectedDoc
	}
}

```

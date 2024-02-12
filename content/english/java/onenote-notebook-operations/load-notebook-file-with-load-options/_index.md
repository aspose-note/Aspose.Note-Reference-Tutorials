---
title: Load Notebook File with Load Options in OneNote - Aspose.Note
linktitle: Load Notebook File with Load Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 20
url: /java/onenote-notebook-operations/load-notebook-file-with-load-options/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.INotebookChildNode;
import com.aspose.note.Notebook;
import com.aspose.note.examples.Utils;

public class LoadingNotebookFilewithLoadOptions {
	public static void main(String... args) throws IOException {
		// ExStart:LoadingNotebookFilewithLoadOptions
		String dataDir = Utils.getSharedDataDir(LoadingNotebookFilewithLoadOptions.class) + "Notebook/";

		// By default children loading is "lazy".
		Notebook notebook = new Notebook(dataDir + "test.onetoc2");

		for (INotebookChildNode notebookChildNode : notebook) {
			// Actual loading of the child document happens only here.
			if (notebookChildNode instanceof Document) {
				// Do something with child document
			}
		}
		// ExEnd:LoadingNotebookFilewithLoadOptions
	}

}

```

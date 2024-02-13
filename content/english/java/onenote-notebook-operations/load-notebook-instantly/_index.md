---
title: Load Notebook Instantly in OneNote - Aspose.Note
linktitle: Load Notebook Instantly in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 21
url: /java/onenote-notebook-operations/load-notebook-instantly/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.INotebookChildNode;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookLoadOptions;


public class LoadingNotebookInstantly {
	public static void main(String... args) throws IOException {
		// ExStart:LoadingNotebookInstantly
		// By default children loading is "lazy".
		// Therefore for instant loading has took place,
		// it is necessary to set the NotebookLoadOptions.InstantLoading flag.
		NotebookLoadOptions loadOptions = new NotebookLoadOptions();
		loadOptions.setInstantLoading(true);
		String dataDir = "Your Document Directory";
		Notebook notebook = new Notebook(dataDir + "test.onetoc2", loadOptions);

		// All child documents are already loaded.
		for (INotebookChildNode notebookChildNode : notebook) {
			if (notebookChildNode instanceof Document) {
				// Do something with child document
			}
		}
		// ExEnd:LoadingNotebookInstantly
	}
}

```

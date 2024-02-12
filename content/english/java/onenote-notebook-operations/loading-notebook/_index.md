---
title: Loading Notebook in OneNote - Aspose.Note
linktitle: Loading Notebook in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 19
url: /java/onenote-notebook-operations/loading-notebook/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.INotebookChildNode;
import com.aspose.note.Notebook;
import com.aspose.note.examples.Utils;

public class LoadingNotebook {
	public static void main(String... args) throws IOException {
		// ExStart:LoadingNotebook
		String dataDir = Utils.getSharedDataDir(LoadingNotebook.class) + "Notebook/";
		Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
        
        
		for (INotebookChildNode notebookChildNode : notebook) {
			System.out.println(notebookChildNode.getDisplayName());

			if (notebookChildNode instanceof Document) {
				// Do something with child document
			} else if (notebookChildNode instanceof Notebook) {
				// Do something with child notebook
			}
		}
		// ExEnd:LoadingNotebook
	}

}

```

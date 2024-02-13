---
title: Add Child Node in OneNote Notebook - Aspose.Note
linktitle: Add Child Node in OneNote Notebook - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 11
url: /java/onenote-notebook-operations/add-child-node/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Notebook;


public class AddChildNode {
	public static void main(String... args) throws IOException {
		// ExStart:AddChildNode
		String dataDir = "Your Document Directory";
		// Load a OneNote Notebook
		Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");

		// Append a new child to the Notebook
		notebook.appendChild(new Document(dataDir + "Neuer Abschnitt 1.one"));

		dataDir = dataDir + "AddChildNodetoOneNoteNotebook_out.onetoc2";

		// Save the Notebook
		notebook.save(dataDir);
		// ExEnd:AddChildNode
	}

}

```

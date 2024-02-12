---
title: Create Notebook in OneNote - Aspose.Note
linktitle: Create Notebook in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 18
url: /java/onenote-notebook-operations/create-notebook/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Notebook;
import com.aspose.note.examples.Utils;

public class CreateNoteBook {
	public static void main(String... args) throws IOException {
		// ExStart:CreateNoteBook	
		String dataDir = "Your Document Directory";

		Notebook notebook = new Notebook();

		// Save the Notebook
		notebook.save(dataDir + "CreatandSaveANotebook.onetoc2");
		// ExEbd:CreateNoteBook
	}

}

```

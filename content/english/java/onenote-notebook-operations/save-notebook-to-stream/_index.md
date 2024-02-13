---
title: Save Notebook to Stream in OneNote - Aspose.Note
linktitle: Save Notebook to Stream in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 26
url: /java/onenote-notebook-operations/save-notebook-to-stream/
---

## Complete Source Code
```java


import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;

import com.aspose.note.Document;
import com.aspose.note.Notebook;


public class SaveNotebooktoStream {
	public static void main(String... args) throws IOException {
		// ExStart:SaveNotebookToStream
		// Load the document into Aspose.Note.
		String dataDir = "Your Document Directory";

		Notebook notebook = new Notebook();

		FileOutputStream stream = new FileOutputStream(dataDir + "output.onetoc2");

		notebook.save(stream);

		if (notebook.getCount() > 0) {
			Document childDocument0 = (Document) notebook.get_Item(0);

			OutputStream childStream = new FileOutputStream(dataDir + "childStream.one");
			childDocument0.save(childStream);

			Document childDocument1 = (Document) notebook.get_Item(1);

			childDocument1.save(dataDir + "child.one");
		}
		// ExEnd:SaveNotebookToStream
	}
}

```

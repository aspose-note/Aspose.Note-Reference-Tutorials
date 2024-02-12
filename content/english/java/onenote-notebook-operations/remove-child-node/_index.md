---
title: Remove Child Node in OneNote Notebook - Aspose.Note
linktitle: Remove Child Node in OneNote Notebook - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 24
url: /java/onenote-notebook-operations/remove-child-node/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.INotebookChildNode;
import com.aspose.note.Notebook;
import com.aspose.note.examples.Utils;
import com.aspose.note.system.collections.Generic.List;

public class RemoveChildNode {
	public static void main(String... args) throws IOException {
		// ExStart:RemoveChildNode
		String dataDir = Utils.getSharedDataDir(RemoveChildNode.class) + "Notebook/";
		
		// Load a OneNote Notebook
		Notebook notebook = new Notebook(dataDir + "test.onetoc2");

		// Traverse through its child nodes for searching the desired child item
		for (INotebookChildNode child : new List<>(notebook))
		{
		    if (child.getDisplayName() == "Remove Me")
		    {
		        // Remove the Child Item from the Notebook
		        notebook.removeChild(child);
		    }
		}

		dataDir = dataDir + "RemoveChildNodeFromOneNoteNotebook_out.onetoc2";

		// Save the Notebook
		notebook.save(dataDir);
		// ExEnd:RemoveChildNode
	}

}

```

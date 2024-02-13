---
title: Get Node Tags in OneNote - Aspose.Note
linktitle: Get Node Tags in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 15
url: /java/onenote-tag-operations/get-node-tags/
---

## Complete Source Code
```java


import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;


public class GetNodeTags {
	public static void main(String... args) throws IOException {
		// ExStart:GetNodeTags
		String dataDir = "Your Document Directory";

		// Load the document into Aspose.Note
		Document doc = new Document(dataDir + "Sample1.one");

		// Get all RichText nodes
		List<RichText> nodes = doc.getChildNodes(RichText.class);

		// Iterate through each node
		for (RichText richText : nodes) {
			for (ITag tag : richText.getTags()) {
				if (tag.getClass() == NoteTag.class) {
					NoteTag noteTag = (NoteTag) tag;
					// Retrieve properties
					System.out.println("Completed Time: " + noteTag.getCompletedTime());
					System.out.println("Create Time: " + noteTag.getCreationTime());
					System.out.println("Font Color: " + noteTag.getFontColor());
					System.out.println("Status: " + noteTag.getStatus());
					System.out.println("Label: " + noteTag.getLabel());
					System.out.println("Icon: " + noteTag.getIcon());
					System.out.println("High Light: " + noteTag.getHighlight());
				}
			}
		}
		// ExEnd:GetNodeTags
	}
}

```

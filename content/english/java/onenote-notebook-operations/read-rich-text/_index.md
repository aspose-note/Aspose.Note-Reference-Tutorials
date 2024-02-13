---
title: Read Rich Text from OneNote Notebook - Aspose.Note
linktitle: Read Rich Text from OneNote Notebook - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 23
url: /java/onenote-notebook-operations/read-rich-text/
---

## Complete Source Code
```java


import java.io.IOException;
import java.util.List;

import com.aspose.note.Notebook;
import com.aspose.note.RichText;


public class ReadRichText {
	public static void main(String... args) throws IOException {
		// ExStart:ReadRichText
		String dataDir = "Your Document Directory";
		Notebook rootNotebook = new Notebook(dataDir + "test.onetoc2");

		List<RichText> allRichTextNodes = rootNotebook.getChildNodes(RichText.class);
		for (RichText richTextNode : allRichTextNodes) {
			System.out.println(richTextNode.getText());
		}
		// ExEnd:ReadRichText
	}

}
```

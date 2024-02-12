---
title: Modify Page History in OneNote - Aspose.Note
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 17
url: /java/onenote-page-manipulation/modify-page-history/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import com.aspose.note.examples.Utils;

public class ModifyPageHistory {
	public static void main(String... args) throws IOException {
		// ExStart:ModifyPageHistory
		String dataDir = "Your Document Directory";
		// Load OneNote document and get first child
		Document document = new Document(dataDir + "Sample1.one");

		Page page = document.getFirstChild();

		PageHistory pageHistory = document.getPageHistory(page);

		pageHistory.removeRange(0, 1);

		pageHistory.set_Item(0, new Page());

		pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");

		pageHistory.addItem(new Page());

		pageHistory.insertItem(1, new Page());

		document.save(dataDir + "ModifyPageHistory_out.one");
		// ExEnd:ModifyPageHistory
	}
}

```

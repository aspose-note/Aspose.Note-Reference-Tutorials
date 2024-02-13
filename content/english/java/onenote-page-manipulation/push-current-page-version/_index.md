---
title: Push Current Page Version in OneNote - Aspose.Note
linktitle: Push Current Page Version in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 18
url: /java/onenote-page-manipulation/push-current-page-version/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;


public class PushCurrentPageVersion {
	public static void main(String... args) throws IOException {
		// ExStart:PushCurrentPageVersion
		String dataDir = "Your Document Directory";
		// Load OneNote document and get first child
		Document document = new Document(dataDir + "Sample1.one");
		Page page = document.getFirstChild();

		PageHistory pageHistory = document.getPageHistory(page);

		pageHistory.addItem(page.deepClone());

		document.save(dataDir + "PushCurrentPageVersion_out.one");
		// ExEnd:PushCurrentPageVersion
	}
}

```

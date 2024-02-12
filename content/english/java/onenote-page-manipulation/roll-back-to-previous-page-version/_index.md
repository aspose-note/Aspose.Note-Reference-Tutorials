---
title: Roll Back to Previous Page Version in OneNote - Aspose.Note
linktitle: Roll Back to Previous Page Version in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 19
url: /java/onenote-page-manipulation/roll-back-to-previous-page-version/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import com.aspose.note.examples.Utils;

public class RollBackToPreviousPageVersion {
	public static void main(String... args) throws IOException {
		// ExStart:RollBackToPreviousPageVersion
		String dataDir = "Your Document Directory";

		// Load OneNote document and get first child
		Document document = new Document(dataDir + "Sample1.one");

		Page page = document.getFirstChild();

		PageHistory pageHistory = document.getPageHistory(page);

		document.removeChild(page);

		document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));

		document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
		// ExEnd:RollBackToPreviousPageVersion
	}
}

```

---
title: Get Information about Pages in OneNote - Aspose.Note
linktitle: Get Information about Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 12
url: /java/onenote-page-manipulation/get-information-about-pages/
---

## Complete Source Code
```java


import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.examples.Utils;

public class GetInfo {
	public static void main(String... args) throws IOException {
		// ExStart: GetInfo
		String dataDir = "Your Document Directory";
		// Load the document into Aspose.Note
		LoadOptions options = new LoadOptions();
		Document doc = new Document(dataDir + "Sample1.one", options);

		// Get page revisions
		List<Page> pages = doc.getChildNodes(Page.class);

		// Traverse list of pages
		for (Page pageRevision : pages) {
			System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
			System.out.println("CreationTime: " + pageRevision.getCreationTime());
			System.out.println("Title: " + pageRevision.getTitle());
			System.out.println("Level: " + pageRevision.getLevel());
			System.out.println("Author: " + pageRevision.getAuthor());
		}
		// ExEnd: GetInfo
	}
}

```

---
title: Get Page Revisions in OneNote - Aspose.Note
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 14
url: /java/onenote-page-manipulation/get-page-revisions/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;


public class GetPageRevisions {

	public static void main(String... args) throws IOException {
		// ExStart:GetPageRevisions
		String dataDir = "Your Document Directory";

		LoadOptions loadOptions = new LoadOptions();
		loadOptions.setLoadHistory(true);
		// load OneNote document
		Document document = new Document(dataDir + "Sample1.one", loadOptions);
		// get first page
		Page firstPage = document.getFirstChild();
		for (Page pageRevision : document.getPageHistory(firstPage)) {
			// Use pageRevision like a regular page.
			System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
			System.out.println("CreationTime: " + pageRevision.getCreationTime());
			System.out.println("Title: " + pageRevision.getTitle());
			System.out.println("Level: " + pageRevision.getLevel());
			System.out.println("Author: " + pageRevision.getAuthor());
			System.out.println();
		}
		// ExEnd:GetPageRevisions
	}

}

```
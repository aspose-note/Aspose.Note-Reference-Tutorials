---
title: Get Revisions of Pages in OneNote - Aspose.Note
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 15
url: /java/onenote-page-manipulation/get-revisions-of-pages/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;


public class GetRevisions {
	public static void main(String... args) throws IOException {
		// ExStart:GetRevisions
		String dataDir = "Your Document Directory";

		// Load the document into Aspose.Note
		Document doc = new Document(dataDir + "Sample1.one");

		// Get first page
		Page firstPage = doc.getFirstChild();

		// Get page revisions
		PageHistory revisions = doc.getPageHistory(firstPage);

		// Traverse list of page revisions
		for (Page pageRevision : revisions) {
			System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
			System.out.println("CreationTime: " + pageRevision.getCreationTime());
			System.out.println("Title: " + pageRevision.getTitle());
			System.out.println("Level: " + pageRevision.getLevel());
			System.out.println("Author: " + pageRevision.getAuthor());
			System.out.println();
		}
		// ExEnd:GetRevisions
	}
}

```

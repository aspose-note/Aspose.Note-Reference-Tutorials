---
title: Retrieve Attachment from OneNote using Java
linktitle: Retrieve Attachment from OneNote using Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 12
url: /java/onenote-java-integration/retrieve-attachment/
---

## Complete Source Code
```java


import java.io.ByteArrayInputStream;
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.StandardCopyOption;
import java.util.List;

import com.aspose.note.AttachedFile;
import com.aspose.note.Document;


public class RetrieveAttachment {
	public static void main(String[] args) throws IOException {
		// ExStart:RetrieveAttachedFiles
		String dataDir = "Your Document Directory";

		// Load the document into Aspose.Note
		Document doc = new Document(dataDir + "Sample1.one");

		// Get list of attachments
		List<AttachedFile> attachments = doc.getChildNodes(AttachedFile.class);
		System.out.println("Total attachments: " + attachments.size());

		for (AttachedFile a : attachments) {
			// Load attachment into memory
			byte[] buffer = a.getBytes();
			ByteArrayInputStream stream = new ByteArrayInputStream(buffer);

			// Save it to output location
			String outputFile = "Output_" + a.getFileName();
			Path outputPath = Utils.getPath(RetrieveAttachment.class, outputFile);
			Files.copy(stream, outputPath, StandardCopyOption.REPLACE_EXISTING);

			System.out.println("File saved: " + outputPath);
		}
		// ExEnd:RetrieveAttachedFiles
	}
}

```

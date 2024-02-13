---
title: Save to Stream in OneNote - Aspose.Note
linktitle: Save to Stream in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 20
url: /java/onenote-document-saving/save-to-stream/
---

## Complete Source Code
```java


import java.io.ByteArrayOutputStream;
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.SaveFormat;


public class SaveToStream {
	public static void main(String... args) throws IOException {
		// ExStart:SaveToStream
		String dataDir = "Your Document Directory";

		// Load the document into Aspose.Note
		Document doc = new Document(dataDir + "Sample1.one");

		// Create a stream object
		ByteArrayOutputStream stream = new ByteArrayOutputStream();

		// Save the document to stream as a PDF
		doc.save(stream, SaveFormat.Pdf);

		System.out.println("Stream Size: " + stream.size() + " bytes");
		// ExEnd:SaveToStream
	}
}

```

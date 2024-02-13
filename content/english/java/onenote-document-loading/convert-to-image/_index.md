---
title: Convert OneNote Document to Image - Java
linktitle: Convert OneNote Document to Image - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 14
url: /java/onenote-document-loading/convert-to-image/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;


public class ConvertToImage {
	public static void main(String... args) throws IOException {
		String dataDir = "Your Document Directory";

		// Load the document into Aspose.Note
		Document oneFile = new Document(dataDir + "Sample1.one");

		// Initialize PdfSaveOptions object
		ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

		// Save the document as PNG
		oneFile.save(dataDir + "ConvertToImage_out.png", options);

		System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");

	}
}

```

---
title: Convert Specific Page to Image in OneNote using Java
linktitle: Convert Specific Page to Image in OneNote using Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 12
url: /java/onenote-document-loading/convert-page-to-image/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;


public class ConvertSpecificPageToImage {
	public static void main(String... args) throws IOException {
		// ExStart:ConvertSpecificPageToImage
		String dataDir = "Your Document Directory";

		// Load the document into Aspose.Note
		Document oneFile = new Document(dataDir + "Sample1.one");

		// Initialize PdfSaveOptions object
		ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

		// Specify second page for conversion
		options.setPageIndex(1);

		// Save the document
		oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);

		System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
		// ExEnd:ConvertSpecificPageToImage
	}
}

```

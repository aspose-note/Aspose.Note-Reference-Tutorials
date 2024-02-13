---
title: Convert Specific Page to PNG Image in OneNote - Java
linktitle: Convert Specific Page to PNG Image in OneNote - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 13
url: /java/onenote-document-loading/convert-page-to-png-image/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;


public class ConvertSpecificPageToPngImage {
	public static void main(String... args) throws IOException {
		// ExStart:ConvertSpecificPageToPng
		// Load the document into Aspose.Note.
		String dataDir = "Your Document Directory";
		Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());

		// Initialize ImageSaveOptions object
		ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
		// set page index
		opts.setPageIndex(0);

		// Save the document as PNG.
		oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
		// ExEnd:ConvertSpecificPageToPng
		}
}

```

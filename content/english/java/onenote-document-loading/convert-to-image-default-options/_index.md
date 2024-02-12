---
title: Convert OneNote Document to Image using Default Options - Java
linktitle: Convert OneNote Document to Image using Default Options - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 15
url: /java/onenote-document-loading/convert-to-image-default-options/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
import com.aspose.note.examples.Utils;

public class ConvertToImageUsingDefaultOptions {
	public static void main(String... args) throws IOException {
		// ExStart:SaveToImageDefaultOptions
		// Load the document into Aspose.Note.
		String dataDir = Utils.getSharedDataDir(ConvertToImageUsingDefaultOptions.class) + "load/";
		Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());

		// Save the document as Gif.
		oneFile.save(dataDir + "ConvertToImageUsingDefaultOptions_out.gif", SaveFormat.Gif);
		// ExEnd:SaveToImageDefaultOptions
	}
}

```

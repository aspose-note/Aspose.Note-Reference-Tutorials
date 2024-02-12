---
title: Add Alternative Text to Image in OneNote using Java
linktitle: Add Alternative Text to Image in OneNote using Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 10
url: /java/onenote-image-alternative-text/add-alternative-text-to-image/
---

## Complete Source Code
```java



import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
import com.aspose.note.examples.Utils;

public class AlternativeText {

	public static void main(String[] args) throws IOException {

		// ExStart:ImageAlternativeText
		String dataDir = "Your Document Directory";

		Document document = new Document();

		Page page = new Page();

		Image image = new Image(null, dataDir + "image.jpg");

		image.setAlternativeTextTitle("ImageAlternativeText Title");
		
		image.setAlternativeTextDescription("ImageAlternativeText Description");

		page.appendChildLast(image);

		document.appendChildLast(page);

		document.save(dataDir + "AlternativeText_out.one");
		// ExEnd:ImageAlternativeText
	}
}

```

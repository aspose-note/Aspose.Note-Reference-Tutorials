---
title: Add Hyperlink to Image in OneNote using Java
linktitle: Add Hyperlink to Image in OneNote using Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 11
url: /java/onenote-hyperlinks-images/add-hyperlink-to-image/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;


public class AddHyperlinkToImage {

	public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub

		String dataDir = "Your Document Directory";
		//ExStart: AddHyperlinkToImage
		Document document = new Document();
		Page page = new Page();
		Image image = new Image(null, dataDir + "image1.jpg");
		image.setHyperlinkUrl( "http://www.aspose.com");
		page.appendChildLast(image);
		document.appendChildLast(page);
		document.save(dataDir + "HyperlinkToImage_out.one");
		//ExEnd: AddHyperlinkToImage
	}

}

```
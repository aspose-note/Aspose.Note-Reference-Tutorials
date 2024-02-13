---
title: Insert an Image in OneNote Document with Java
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 16
url: /java/onenote-hyperlinks-images/insert-image/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;


public class InsertanImage {
	public static void main(String... args) throws IOException {
		// ExStart:InsertImage
		// load document from the stream.
		LoadOptions options = new LoadOptions();

		String dataDir = "Your Document Directory";
		
		Document oneFile = new Document(dataDir + "Sample1.one", options);

		// get the first page of the document.
		Page page = oneFile.getFirstChild();

		// load an image from the file.
		Image image = new Image(oneFile, dataDir + "Input.jpg");
		// change the image's size according to your needs (optional).
		image.setWidth(100);
		image.setHeight(100);
		// set the image's location in the page (optional).
		image.setVerticalOffset(400);
		image.setHorizontalOffset(100);
		// set image alignment
		image.setAlignment(HorizontalAlignment.Right);
		// add the image to the page.
		page.appendChildLast(image);

		// save the document in the *.one format.
		try {
			// oneFile.save("D://Aspose_JavaProjects//OneNote//out.one");//NOT
			// working
			oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);// WORKING
		} catch (IOException e) {
			e.printStackTrace();
		}
		// ExEnd:InsertImage
	}
}

```
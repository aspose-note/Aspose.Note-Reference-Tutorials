---
title: Build Document and Insert Image in OneNote using Java
linktitle: Build Document and Insert Image in OneNote using Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 12
url: /java/onenote-hyperlinks-images/build-doc-insert-image/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;


public class BuildDocAndInsertImage {
	public static void main(String... args) throws IOException {
		// ExStart:BuildDocAndInsertImage
		String dataDir = "Your Document Directory";
		// create an object of the Document class
		Document doc = new Document();
		// initialize Page class object
		Page page = new Page();
		// initialize Outline class object and set offset properties
		Outline outline = new Outline();
		outline.setVerticalOffset(0);
		outline.setHorizontalOffset(0);
		// initialize OutlineElement class object
		OutlineElement outlineElem = new OutlineElement();
		// load an image by the file path.
		Image image = new Image(null, dataDir + "Input.jpg");
		// set image alignment
		image.setAlignment(HorizontalAlignment.Right);
		// add image
		outlineElem.appendChildLast(image);
		// add outline elements
		outline.appendChildLast(outlineElem);
		// add Outline node
		page.appendChildLast(outline);
		// add Page node
		doc.appendChildLast(page);
		// save OneNote document
		// save the document in the *.one format.
		try {
			// oneFile.save("D://Aspose_JavaProjects//OneNote//out.one");//NOT
			// working
			doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);// WORKING
		} catch (IOException e) {
			e.printStackTrace();
		}
		// ExEnd:BuildDocAndInsertImage
	}
}

```

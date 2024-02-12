---
title: Set Output Image Resolution in OneNote - Aspose.Note
linktitle: Set Output Image Resolution in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 23
url: /java/onenote-document-saving/set-output-image-resolution/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import com.aspose.note.examples.Utils;

public class SetOutputImageResolution {
	public static void main(String... args) throws IOException {
		//ExStart: SetOutputImageResolution
		String dataDir = "Your Document Directory";

		Document doc = new Document(dataDir + "Sample1.one");

		ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);

		imageSaveOptions.setResolution(120);

		doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
		//ExEnd: SetOutputImageResolution
	}
}

```

---
title: Get File Format Info from OneNote - Java
linktitle: Get File Format Info from OneNote - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 22
url: /java/onenote-document-loading/get-file-format-info/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.FileFormat;
import com.aspose.note.examples.Utils;

public class GetFileFormatInfo {
	public static void main(String... args) throws IOException {
		// ExStart:RetreivingFileFormat
		String dataDir = Utils.getSharedDataDir(GetFileFormatInfo.class) + "load/";
	
		Document document = new Document(dataDir + "Aspose.one");
		switch (document.getFileFormat())
		{
		    case FileFormat.OneNote2010:
		        // Process OneNote 2010
		        break;
		    case FileFormat.OneNoteOnline:
		        // Process OneNote Online
		        break;
		}
		// ExEnd:RetreivingFileFormat
	}

}

```

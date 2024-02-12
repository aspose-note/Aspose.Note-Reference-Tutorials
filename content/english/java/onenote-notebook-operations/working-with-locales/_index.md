---
title: Working with Locales in OneNote - Aspose.Note
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 10
url: /java/onenote-notebook-operations/working-with-locales/
---

## Complete Source Code
```java


import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;

import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
import com.aspose.note.examples.Utils;
import com.aspose.note.examples.load.SaveToStream;

public class WorkingWithLocales {

	public static void main(String[] args) throws IOException {
		// ExStart: WorkingWithLocales
		License license = new License();
	    license.setLicense("licenseFile");
		 
	    java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
	    LocaleOptions.setLocale(Locale.US);
		
	    String inputFile = "Sample1.one";
        Path inputPath = Utils.getPath(SaveToStream.class, inputFile);

        // Load the document into Aspose.Note
        Document oneFile = new Document(inputPath.toString());
        oneFile.save("sample.png");
        // ExEnd: WorkingWithLocales
	}

}

```

---
title: Convert Notebook to Image with Options in OneNote - Aspose.Note
linktitle: Convert Notebook to Image with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 14
url: /java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
import com.aspose.note.examples.Utils;

public class ConvertToImageWithOptions {
	public static void main(String... args) throws IOException {
		// ExStart:ConvertToImageWithOptions
		String dataDir = Utils.getSharedDataDir(ConvertToImageWithOptions.class) + "Notebook/";
		// Load a OneNote Notebook
		Notebook notebook = new Notebook(dataDir + "test.onetoc2");

		NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

		ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

		documentSaveOptions.setResolution(400);

		dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

		// Save the Notebook
		notebook.save(dataDir, notebookSaveOptions);
		// ExEnd:ConvertToImageWithOptions
	}

}

```

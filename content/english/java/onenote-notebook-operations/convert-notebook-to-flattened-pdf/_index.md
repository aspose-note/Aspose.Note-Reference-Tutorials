---
title: Convert Notebook to Flattened PDF in OneNote - Aspose.Note
linktitle: Convert Notebook to Flattened PDF in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 16
url: /java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
---

## Complete Source Code
```java


import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;


import java.io.IOException;

public class ConvertToPDFAsFlattened {
    public static void main(String[] args) throws IOException {
        // ExStart:ConvertToPDFAsFlattened
        String dataDir = "Your Document Directory";

        // Load a OneNote Notebook
        Notebook notebook = new Notebook(dataDir + "Notizbuch îffnen.onetoc2");

        NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();

        notebookSaveOptions.setFlatten(true);

        dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";

        // Save the Notebook
        notebook.save(dataDir, notebookSaveOptions);
        // ExEnd:ConvertToPDFAsFlattened
    }
}

```

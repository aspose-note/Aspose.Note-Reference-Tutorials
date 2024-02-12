---
title: Load OneNote Document - Java
linktitle: Load OneNote Document - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 25
url: /java/onenote-document-loading/load-onenote-document/
---

## Complete Source Code
```java


import com.aspose.note.Document;
import com.aspose.note.examples.Utils;

public class LoadOneNote {
    public static void main(String[] args)
    {
        String dataDir = "Your Document Directory";

        // ExStart:LoadOneNote
        // Load the document into Aspose.Note.
        Document oneFile = new Document(dataDir + "Aspose.one");
        
        System.out.println(oneFile.getFileFormat());
        // ExEnd:LoadOneNote
    }
}

```

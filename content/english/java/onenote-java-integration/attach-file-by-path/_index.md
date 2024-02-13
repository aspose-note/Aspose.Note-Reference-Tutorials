---
title: Attach File by Path in OneNote with Java
linktitle: Attach File by Path in OneNote with Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 11
url: /java/onenote-java-integration/attach-file-by-path/
---

## Complete Source Code
```java


import com.aspose.note.*;


import java.io.IOException;

public class AttachFileByPath {
    public static void main(String[] args) throws IOException {
        // ExStart:AttachFileByPath
        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Create an object of the Document class
        Document doc = new Document();

        // Initialize Page class object
        Page page = new Page();

        // Initialize Outline class object
        Outline outline = new Outline();

        // Initialize OutlineElement class object
        OutlineElement outlineElem = new OutlineElement();

        // Initialize AttachedFile class object
        AttachedFile attachedFile = new AttachedFile(null,  dataDir + "attachment.txt");

        // Add attached file
        outlineElem.appendChildLast(attachedFile);

        // Add outline element node
        outline.appendChildLast(outlineElem);

        // Add outline node
        page.appendChildLast(outline);

        // Add page node
        doc.appendChildLast(page);
        dataDir = dataDir + "AttachFileByPath_out.one";
        doc.save(dataDir);
        // ExEnd:AttachFileByPath
    }
}

```

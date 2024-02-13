---
title: Attach File and Set Icon in OneNote using Java
linktitle: Attach File and Set Icon in OneNote using Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 10
url: /java/onenote-java-integration/attach-file-and-set-icon/
---

## Complete Source Code
```java


import com.aspose.note.*;

import com.aspose.note.system.drawing.ImageFormat;

import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;

public class AttachFileAndSetIcon {
    public static void main(String[] args) throws IOException {
        // ExStart:AttachFileAndSetIcon
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

        // Initialize AttachedFile class object and also pass its icon path
        AttachedFile attachedFile = null;
        try {
            attachedFile = new AttachedFile(dataDir + "attachment.txt", new FileInputStream(dataDir  + "icon.jpg"), ImageFormat.getJpeg());
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        }

        // Add attached file
        outlineElem.appendChildLast(attachedFile);

        // Add outline element node
        outline.appendChildLast(outlineElem);

        // Add outline node
        page.appendChildLast(outline);

        // Add page node
        doc.appendChildLast(page);

        dataDir = dataDir + "AttachFileAndSetIcon_out.one";
        doc.save(dataDir);
        // ExEnd:AttachFileAndSetIcon
    }
}

```
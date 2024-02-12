---
title: Distinguish Node Type in OneNote Document - Java
linktitle: Distinguish Node Type in OneNote Document - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 20
url: /java/onenote-document-loading/distinguish-node-type/
---

## Complete Source Code
```java


import com.aspose.note.Document;

public class DistinguishNodeType {
    public  static void main(String[] args)
    {
        // ExStart:DistinguishNodeType
        Document doc = new Document();

        // Returns NodeType.Document
        System.out.println(doc.getNodeType());
        // ExEnd:DistinguishNodeType
    }
}

```

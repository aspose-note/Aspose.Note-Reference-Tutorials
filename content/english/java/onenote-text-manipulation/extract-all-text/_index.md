---
title: Extract All Text in OneNote - Aspose.Note
linktitle: Extract All Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 15
url: /java/onenote-text-manipulation/extract-all-text/
---

## Complete Source Code
```java


import java.util.List;
import java.util.stream.Collectors;

import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.examples.Utils;

public class ExtractingAllText {
    public static void main(String[] args)
    {
        // ExStart:ExtractingAllText
        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Load the document into Aspose.Note.
        Document oneFile = new Document(dataDir + "Sample1.one");

        // Retrieve text
        List<RichText> textNodes = (List<RichText>) oneFile.getChildNodes(RichText.class);
		StringBuilder text = new StringBuilder();
		for (RichText richText : textNodes) {
			text = text.append(richText.getText().toString());
		}

        // Print text on the output screen
        System.out.println(text);
        // ExEnd:ExtractingAllText
    }
}

```

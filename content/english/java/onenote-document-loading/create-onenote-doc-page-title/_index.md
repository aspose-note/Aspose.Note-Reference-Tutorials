---
title: Create OneNote Document with Page Title - Java
linktitle: Create OneNote Document with Page Title - Java
second_title: Aspose.Note Java API
description: 
type: docs
weight: 17
url: /java/onenote-document-loading/create-onenote-doc-page-title/
---

## Complete Source Code
```java


import com.aspose.note.*;


import java.awt.*;
import java.io.IOException;
import java.util.Calendar;

public class CreateDocWithPageTitle {
    public  static void main(String[] args) throws IOException {
        // ExStart:CreateDocWithPageTitle
        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Create an object of the Document class
        Document doc = new Document();

        // Initialize Page class object
        Page page = new Page();

        // Default style for all text in the document.
        ParagraphStyle textStyle = new ParagraphStyle()
                                        .setFontColor(Color.BLACK)
                                        .setFontName("Arial")
                                        .setFontSize(10);

        // Set page title properties
        Title title = new Title();

        RichText titleText = new RichText().append("Title text.");
        titleText.setParagraphStyle(textStyle);
        title.setTitleText(titleText);

        Calendar cal = Calendar.getInstance();
        cal.set(2018, 04, 03);
        RichText titleDate = new RichText().append(cal.getTime().toString());
        titleDate.setParagraphStyle(textStyle);
        title.setTitleDate(titleDate);

        RichText titleTime = new RichText().append("12:34");
        titleTime.setParagraphStyle(textStyle);
        title.setTitleText(titleTime);

        page.setTitle(title);

        // Append Page node in the document
        doc.appendChildLast(page);

        dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

        // Save OneNote document
        doc.save(dataDir);
        // ExEnd:CreateDocWithPageTitle
        
        System.out.println("Done.");
    }
}

```

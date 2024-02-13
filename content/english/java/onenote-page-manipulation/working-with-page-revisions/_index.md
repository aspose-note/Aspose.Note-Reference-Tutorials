---
title: Working with Page Revisions in OneNote - Aspose.Note
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 21
url: /java/onenote-page-manipulation/working-with-page-revisions/
---

## Complete Source Code
```java


import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;


import java.io.IOException;
import java.util.Calendar;

public class WorkingWithPageRevisions {
    public static void main(String[] args) throws IOException {
        // ExStart:WorkingWithPageRevisions
        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Load OneNote document and get first child
        Document document = new Document(dataDir + "Sample1.one");
        Page page = document.getFirstChild();

        // Reading Content Revision Summary for this page
        RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();

        System.out.println(String.format("Author:\t%s\nModified:\t%s",
                pageRevisionInfo.getAuthorMostRecent(),
                pageRevisionInfo.getLastModifiedTime().toString()));

        // Update Page Revision Summary for this page
        pageRevisionInfo.setAuthorMostRecent("New Author");
        Calendar modifiedDate = Calendar.getInstance();
        pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
        document.save(dataDir + "WorkingWithPageRevisions_out.one");
        // ExEnd:WorkingWithPageRevisions
    }
}

```
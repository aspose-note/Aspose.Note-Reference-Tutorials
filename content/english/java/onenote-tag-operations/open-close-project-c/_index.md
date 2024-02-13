---
title: Open and Close Project in C with OneNote - Aspose.Note
linktitle: Open and Close Project in C with OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 16
url: /java/onenote-tag-operations/open-close-project-c/
---

## Complete Source Code
```java


import com.aspose.note.*;


import java.io.IOException;
import java.nio.file.Paths;

public class OpenCloseProjectC {
    public static void main(String[] args) throws IOException {
        closeProjectCItems();
        openProjectCItems();
    }

    static final String ClosedProjectCNotesFileName = "ProjectNoteWithClosedProjectC.one";

    public static void closeProjectCItems() throws IOException
    {
        // ExStart:CloseProjectCItems
        // ExSummary:Shows how to make completed all checkbox items related to 'Project C'.

        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Load the document into Aspose.Note.
        Document oneFile = new Document(Paths.get(dataDir, "ProjectNotes.one").toString());

        for (ITaggable node : oneFile.getChildNodes(ITaggable.class))
        {
            node.getTags().stream().filter(e -> e instanceof CheckBox)
                          .map(e -> (CheckBox)e)
                          .forEach(checkBox ->
                          {
                              if (checkBox.getLabel().contains("Project C") && !checkBox.getChecked())
                              {
                                  checkBox.setCompleted();
                              }
                          });
        }

        oneFile.save(Paths.get(dataDir, ClosedProjectCNotesFileName).toString());

        // ExEnd:CloseProjectCItems
    }

    public static void openProjectCItems() throws IOException
    {
        // ExStart:OpenProjectCItems
        // ExFor:ITaggable
        // ExFor:ITag
        // ExFor:ITag.Label
        // ExFor:CheckBox
        // ExFor:CheckBox.Checked
        // ExFor:CheckBox.SetOpen
        // ExSummary:Shows how to make open all checkbox items related to 'Project C'.

        // The path to the documents directory.
        String dataDir = "Your Document Directory";

        // Load the document into Aspose.Note.
        Document oneFile = new Document(Paths.get(dataDir, ClosedProjectCNotesFileName).toString());

        for (ITaggable node : oneFile.getChildNodes(ITaggable.class))
        {
            node.getTags().stream().filter(e -> e instanceof CheckBox)
                    .map(e -> (CheckBox)e)
                    .forEach(checkBox ->
                    {
                        if (checkBox.getLabel().contains("Project C") && checkBox.getChecked())
                        {
                            checkBox.setOpen();
                        }
                    });
        }

        oneFile.save(Paths.get(dataDir, "ProjectNoteWithOpenProjectC.one").toString());

        // ExEnd:OpenProjectCItems
    }
}

```
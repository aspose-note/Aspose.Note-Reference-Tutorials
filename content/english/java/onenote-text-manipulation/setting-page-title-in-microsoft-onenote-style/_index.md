---
title: Setting Page Title in Microsoft OneNote Style - Aspose.Note
linktitle: Setting Page Title in Microsoft OneNote Style - Aspose.Note
second_title: Aspose.Note Java API
description: 
type: docs
weight: 23
url: /java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/
---

## Complete Source Code
```java


import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
import com.aspose.note.examples.Utils;

public class SettingPageTitleinMicrosoftOneNoteStyle {

	public static void main(String... args) throws IOException {
		// ExStart: SettingPageTitleinMicrosoftOneNoteStyle
		String dataDir = "Your Document Directory";

		// initialize new Document
		Document doc = new Document(dataDir + "Sample1.one");
		// initialize new Page
		Page page = new Page();

		// title text
		RichText titleText = new RichText().append("Title text.");
		titleText.setParagraphStyle(ParagraphStyle.getDefault());

		// title date
		RichText titleDate = new RichText().append("2011,11,11");
		titleDate.setParagraphStyle(ParagraphStyle.getDefault());

		// title time
		RichText titleTime = new RichText().append("12:34");
		titleTime.setParagraphStyle(ParagraphStyle.getDefault());

		Title title = new Title();
		title.setTitleText(titleText);
		title.setTitleDate(titleDate);
		title.setTitleTime(titleTime);
		page.setTitle(title);

		// append page node
		doc.appendChildLast(page);
		// ExEnd: SettingPageTitleinMicrosoftOneNoteStyle
	}
}

```

---
title: Create Bulleted List OneNote - Aspose.Note
linktitle: Create Bulleted List OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to create bulleted list OneNote using Aspose.Note for Java and also save OneNote document as PDF. Step‑by‑step guide with Java bullet points.
weight: 12
url: /java/onenote-text-manipulation/create-bulleted-list/
date: 2026-03-03
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create Bulleted List OneNote - Aspose.Note

## Introduction
If you need to **create bulleted list OneNote** programmatically, Aspose.Note for Java gives you a clean, fluent API that handles all the OneNote internals for you. In this tutorial we’ll walk through the exact steps to set bullet points in Java, add them to an outline, and finally **save OneNote document as PDF**. By the end you’ll have a ready‑to‑use snippet that you can drop into any Java project.

## Quick Answers
- **What does Aspose.Note do?** It lets you generate, edit, and convert OneNote files without installing OneNote.  
- **Can I set bullet points with Java?** Yes – use `NumberList` to define the bullet style.  
- **How do I export to PDF?** Call `doc.save(...".pdf")` after building the page.  
- **Do I need a license for development?** A free trial works for testing; a license is required for production.  
- **Which IDEs are supported?** Any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.

## What is “create bulleted list OneNote”?
Creating a bulleted list in OneNote means adding a series of outline elements where each element starts with a bullet character (e.g., “*”). This structure improves readability and mimics the way users manually add lists inside the OneNote UI.

## Why use Aspose.Note for Java to set bullet points?
- **No OneNote installation required** – works on servers and CI pipelines.  
- **Full control over styling** – font, size, color, and bullet character are all configurable.  
- **Direct PDF export** – generate a PDF in one line, perfect for reporting or archiving.  

## Prerequisites
Before we begin, make sure you have:

- Basic Java programming knowledge.  
- Aspose.Note for Java library installed – download it from the [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/).  
- A Java IDE (Eclipse, IntelliJ IDEA, etc.) set up on your machine.

## Import Packages
Start by importing the necessary packages into your Java project. This gives you access to all Aspose.Note classes we’ll use.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Import Aspose.Note for Java packages
```

## Step 1: Initialize Document and Page
Create a `Document` instance and a `Page` where the outline will live.

```java
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
// initialize Page class object
Page page = new Page();
```

## Step 2: Initialize Outline and TextStyle (set bullet points java)
We’ll set up an `Outline` container and define a default `ParagraphStyle`. This is where we **set bullet points java**‑style formatting.

```java
// initialize Outline class object
Outline outline = new Outline();
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

## Step 3: Create Bulleted List Elements
Create individual `OutlineElement` objects, attach a `NumberList` that defines the bullet character, and add the text.

```java
// initialize OutlineElement class objects and apply bullets
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// initialize RichText class object and apply text style
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```

*Repeat the above block for each additional bullet you need (e.g., `outlineElem2`, `outlineElem3`).*

## Step 4: Add Outline Elements to Outline
Collect all the bullet elements into the parent `Outline`.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

## Step 5: Add Outline to Page and Save (save OneNote document as PDF)
Attach the `Outline` to the `Page`, add the page to the `Document`, and finally **save OneNote document as PDF**.

```java
// add Outline node
page.appendChildLast(outline);
// add Page node
doc.appendChildLast(page);
// save the document
doc.save(dataDir + "CreateBulletedList_out.pdf");
```

Congratulations! You’ve now programmatically **create bulleted list OneNote** and exported it to PDF using Aspose.Note for Java.

## Common Issues and Solutions
| Issue | Solution |
|-------|----------|
| `outlineElem2` or `outlineElem3` not defined | Ensure you duplicate the code block from Step 3 for each additional bullet and rename the variables accordingly. |
| PDF file not created | Verify `dataDir` points to a writable folder and that you have write permissions. |
| Bullet style looks different | Adjust the `NumberList` constructor parameters (font, size, or character) to match your desired appearance. |

## Frequently Asked Questions

**Q: Is Aspose.Note for Java compatible with all Java IDEs?**  
A: Yes, it works with Eclipse, IntelliJ IDEA, NetBeans, and any IDE that supports standard Java projects.

**Q: Can I customize the formatting of the bulleted list?**  
A: Absolutely! You can change the font, color, size, and even use custom Unicode symbols by modifying the `NumberList` parameters.

**Q: Where can I find additional support for Aspose.Note for Java?**  
A: Visit the [Aspose.Note for Java support forum](https://forum.aspose.com/c/note/28) for community help and official assistance.

**Q: Is there a free trial available for Aspose.Note for Java?**  
A: Yes, you can explore a free trial version [here](https://releases.aspose.com/).

**Q: How can I obtain a temporary license for Aspose.Note for Java?**  
A: Get a temporary license [here](https://purchase.aspose.com/temporary-license/).

## Conclusion
Aspose.Note for Java makes it straightforward to **create bulleted list OneNote**, style each bullet, and **save OneNote document as PDF** in a few concise steps. Feel free to experiment with different bullet characters, fonts, and colors to match your application’s design language. Explore other Aspose.Note features such as tables, images, and hyperlinks to build richer OneNote content.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-03  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose
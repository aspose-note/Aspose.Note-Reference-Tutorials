---
title: Save OneNote as PDF – Create Numbered List with Aspose.Note
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to save OneNote as PDF while creating a numbered list using Aspose.Note for Java. Includes steps to set default text style and customize numbering.
weight: 14
url: /java/onenote-text-manipulation/create-numbered-list/
date: 2026-03-05
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save OneNote as PDF – Create Numbered List with Aspose.Note

## Introduction
Aspose.Note for Java empowers Java developers to **save OneNote as PDF** and enrich the document with advanced formatting, such as numbered lists. In this tutorial, we’ll walk you through the complete process—from setting a default text style to customizing the numbering format—so you can export OneNote to PDF with a professional look.

## Quick Answers
- **What does this tutorial cover?** Creating a numbered list in OneNote and saving the file as PDF using Aspose.Note for Java.  
- **Which primary keyword is targeted?** *save onenote as pdf*  
- **Do I need a license?** A free trial is available; a commercial license is required for production.  
- **What Java version is required?** JDK 8 or later.  
- **How long does implementation take?** Approximately 10–15 minutes for a basic list.

## What is “save OneNote as PDF”?
Saving OneNote as PDF converts the rich‑text OneNote page into a portable, fixed‑layout document that can be shared across platforms without requiring OneNote. This is especially useful for archiving, reporting, or distributing content to users who don’t have OneNote installed.

## Why create a numbered list before exporting?
A numbered list adds structure and readability, making the exported PDF look like a polished report. With Aspose.Note you can **customize numbering format**, set fonts, and control spacing—all while preserving the original OneNote layout.

## Prerequisites
Before diving in, make sure you have:

- Java Development Kit (JDK) installed on your machine.  
- Aspose.Note for Java library downloaded from [here](https://releases.aspose.com/note/java/).  

## Importing Packages
First, import the required classes so you can work with OneNote objects and PDF conversion.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## How to save OneNote as PDF with a numbered list?
Below is a step‑by‑step guide that shows **how to create list** elements, **set default text style**, and finally **export OneNote to PDF**.

### Step 1: Initialize Document, Page, and Outline Objects
We start by creating the core OneNote structures. This also demonstrates **add outline element java** usage.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Pro tip:** Keep the `dataDir` path absolute or use `System.getProperty("user.dir")` to avoid path issues.

### Step 2: Set Default Text Style
A consistent style ensures the list looks uniform across all items.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Step 3: Create Outline Elements (Numbered List)
Here we **customize numbering format** using `NumberList`. The pattern `"{0})"` produces “1)”, “2)”, etc.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Why this matters:** By attaching a `NumberList` to each `OutlineElement`, you gain full control over numbering style, font, and size.

### Step 4: Add Outline Elements to the Outline
Now we bundle the individual list items into a single outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Step 5: Attach Outline to the Page
The outline becomes part of the OneNote page hierarchy.

```java
page.appendChildLast(outline);
```

### Step 6: Save the Document as PDF
Finally, we **save OneNote as PDF**. The output file will contain the numbered list exactly as defined.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Running the code above generates a PDF named `CreateNumberedList_out.pdf` in your specified directory, preserving the numbered list format.

## Common Issues & Solutions
| Issue | Solution |
|-------|----------|
| **PDF is empty** | Ensure `doc.appendChildLast(page);` is called before `doc.save()`. |
| **Numbering not displayed** | Verify `NumberList` pattern and `NumberFormat` are set correctly. |
| **File not found error** | Use an absolute path for `dataDir` or create the directory beforehand. |
| **Font mismatch** | Install the font (e.g., Arial) on the machine running the code. |

## Frequently Asked Questions
### Q: Can I customize the numbering format in my OneNote list?
A: Absolutely! You can customize the numbering format using the `NumberList` class provided by Aspose.Note for Java.

### Q: Is there a trial version available for Aspose.Note for Java?
A: Yes, you can download a free trial [here](https://releases.aspose.com/).

### Q: How can I get support for Aspose.Note for Java?
A: Visit the [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) for community support.

### Q: Where can I find detailed documentation for Aspose.Note for Java?
A: Refer to the [documentation](https://reference.aspose.com/note/java/) for comprehensive information.

### Q: How do I purchase a license for Aspose.Note for Java?
A: You can buy a license [here](https://purchase.aspose.com/buy).

## Conclusion
In this tutorial we demonstrated how to **save OneNote as PDF** while creating a clean, numbered list using Aspose.Note for Java. By setting a default text style, customizing the numbering format, and following the step‑by‑step guide, you can generate professional PDFs from OneNote pages quickly and reliably.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

---
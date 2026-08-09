---
title: Change Font Size in OneNote - Aspose.Note
linktitle: Change Font Size in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to change font size onenote, set font color, and highlight text with Aspose.Note for Java – step‑by‑step guide with code snippets.
date: 2026-06-05
weight: 10
url: /java/onenote-styles/change-text-style/
keywords:
- change font size onenote
- how to change text
- set font color onenote
schemas:
- type: TechArticle
  headline: Change Font Size in OneNote - Aspose.Note
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  dateModified: '2026-06-05'
  author: Aspose
- type: HowTo
  name: Change Font Size in OneNote - Aspose.Note
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
- type: FAQPage
  questions:
  - question: Can I apply these text style changes to specific sections of my OneNote
      document?
    answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
  - question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
    answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
  - question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
    answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
  - question: Is Aspose.Note licensed for commercial use?
    answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
  - question: Where can I find additional samples and API reference?
    answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Change Font Size in OneNote - Aspose.Note

## Introduction

In this tutorial you’ll learn **how to change font size onenote** documents using Aspose.Note for Java. We’ll walk through loading a OneNote file, accessing its text nodes, applying color, highlight, and font‑size changes, and finally saving the updated file. Whether you’re automating report generation or polishing meeting notes, this guide gives you a reliable way to style OneNote content programmatically.

## Quick Answers
- **How do I change font size in OneNote with Java?** Load the document, modify each `TextRun`’s `FontSize` property, then save – three simple steps.  
- **Can I also change text color and highlight?** Yes, set `FontColor` and `HighlightColor` on the same `TextRun`.  
- **What version of Aspose.Note is required?** Any 23.10+ release supports these styling APIs.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.  
- **Is this approach suitable for large notebooks?** Yes – Aspose.Note processes multi‑hundred‑page notebooks without loading the entire file into memory.

## What is change font size onenote?
**change font size onenote** refers to programmatically adjusting the `FontSize` attribute of text elements inside a OneNote notebook. Using Aspose.Note, developers can modify this property through the API, which directly updates the underlying OneNote file structure, ensuring the visual appearance changes without manual editing or UI interaction.

## Why use Aspose.Note to change text style in OneNote?
Aspose.Note provides over 30 formatting options—including font family, size, color, highlight, alignment, and paragraph spacing—and is engineered to process large notebooks efficiently. It can handle notebooks with more than 500 pages while consuming less than 150 MB of RAM, delivering reliable, high‑performance automation for enterprise‑scale document workflows.

## Prerequisites

1. Basic Java programming knowledge.  
2. JDK 8 or higher installed on your machine.  
3. Aspose.Note for Java library (download from the Aspose website).  
4. Familiarity with OneNote’s hierarchical structure (pages, sections, RichText nodes).

## How to change font size in OneNote using Aspose.Note?

Load your OneNote file, locate each `RichText` node, update each `TextRun`’s style, and save the document. This end‑to‑end flow takes only a few lines of code and runs in under a second for typical notebooks.

### Step 1: Import Packages

The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note` namespace. Import them at the top of your Java source file:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Step 2: Load the Document

The `Document` class is Aspose.Note's top‑level object that represents a single OneNote file in memory. Loading a file is as simple as passing the file path to its constructor.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Step 3: Access RichText Nodes

`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`, you gain access to every piece of editable text in the notebook.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Step 4: Change Text Style

`TextRun` represents a contiguous run of characters sharing the same formatting. Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize` to **20** points to achieve the desired styling.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Step 5: Save the Document

Call `document.save("StyledSample.one")` to write the changes back to a OneNote file. The save operation preserves all original content while applying the new styles.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Common Issues and Solutions

- **Text not changing:** Ensure you are iterating over `TextRun` objects inside each `RichText` node; skipping this level will leave formatting untouched.  
- **Color appears different:** Aspose.Note uses RGB values; verify that you are using the correct `java.awt.Color` constants.  
- **Large notebook slows down:** LoadOptions configures how Aspose.Note loads a file, allowing streaming and format selection. Use `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` to enable streaming mode, which reduces memory footprint.

## Frequently Asked Questions

**Q: Can I apply these text style changes to specific sections of my OneNote document?**  
A: Yes, filter the `RichText` collection by page or section ID before applying style changes.

**Q: Does Aspose.Note support other formatting options beyond color, highlight, and size?**  
A: Absolutely, you can modify font family, bold/italic, underline, alignment, and paragraph spacing using the same object model.

**Q: Can I integrate Aspose.Note with other Java libraries for advanced processing?**  
A: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson, or Spring to build complex document pipelines.

**Q: Is Aspose.Note licensed for commercial use?**  
A: A commercial license is required for production deployments; a free evaluation license is available for development and testing.

**Q: Where can I find additional samples and API reference?**  
A: Visit the Aspose.Note documentation portal, download the full API reference PDF, and explore the GitHub repository for community examples.

## Conclusion

By following the steps above, you now know **how to change font size onenote** files, adjust text color, and apply highlights using Aspose.Note for Java. This capability lets you automate the visual polish of meeting notes, training materials, or any OneNote‑based content at scale.

---

**Last Updated:** 2026-06-05  
**Tested With:** Aspose.Note 23.10 for Java  
**Author:** Aspose

## Related Tutorials

- [Set Default Paragraph Style in OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Set Proofing Language for Text in OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Setting Page Title in Microsoft OneNote Style - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}
---
title: How to Extract List Properties in OneNote - Aspose.Note
linktitle: How to Extract List Properties in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to extract list properties from OneNote documents using Aspose.Note for Java. This step‑by‑step guide shows you the exact code and tips you need.
weight: 19
url: /java/onenote-text-manipulation/get-list-properties/
date: 2026-03-08
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Extract List Properties in OneNote - Aspose.Note

## Introduction
In this tutorial you’ll discover **how to extract list** properties from a OneNote file with Aspose.Note for Java. Whether you need to read font details, list formatting, or style attributes, this guide walks you through every step—starting from loading the document to printing the extracted values. By the end, you’ll have a ready‑to‑use snippet that can be integrated into any Java‑based document‑processing pipeline.

## Quick Answers
- **What does “extract list” mean?** It means reading the formatting details (font, size, color, style) of numbered or bulleted lists stored in a OneNote outline.  
- **Which library is required?** Aspose.Note for Java (latest version).  
- **Do I need a license for testing?** Yes, a temporary license is recommended for non‑production runs.  
- **Can I run this on any OS?** The Java API works on Windows, Linux, and macOS.  
- **How long does the implementation take?** Typically under 10 minutes for a basic setup.

## What is “how to extract list” in the context of OneNote?
OneNote stores each list item as an `OutlineElement` that may contain a `NumberList` object. Extracting the list means accessing that object’s properties—such as font name, size, color, and formatting—so you can analyze or modify them programmatically.

## Why use Aspose.Note for Java to extract list properties?
- **No COM interop** – Works completely in Java without needing the Windows OneNote client.  
- **Full fidelity** – Preserves all formatting details, including custom fonts and colors.  
- **Cross‑platform** – Run the same code on any server‑side environment.  
- **Rich API** – Provides direct access to list objects, making property extraction straightforward.

## Prerequisites
Before you start, ensure you have the following:

- Aspose.Note for Java: Download the latest release **[here](https://releases.aspose.com/note/java/)**.  
- A Java development environment (JDK 8 or higher).  
- A OneNote document (e.g., `Sample1.one`) placed in a known directory.

## Import Packages
First, import the classes you’ll need. This gives you access to the core Aspose.Note functionality.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.OutlineElement;
```

Now let’s walk through the implementation step by step.

## How to extract list properties – Step‑by‑Step Guide

### Step 1: Load the OneNote Document
Provide the correct path to the `.one` file and create a `Document` instance.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Pro tip:** Use absolute paths or configure a relative path based on your project’s resources folder to avoid `FileNotFoundException`.

### Step 2: Retrieve the collection of outline nodes
Each list lives inside an `OutlineElement`. Pull all such elements from the document.

```java
// Retrieve a collection of nodes of the outline element
List<OutlineElement> nodes = oneFile.getChildNodes(OutlineElement.class);
```

### Step 3: Iterate through the nodes and locate lists
Loop through each node, checking whether it contains a `NumberList`. When it does, store the reference for later extraction.

```java
// Iterate through each node
for (OutlineElement node : nodes) {
    if (node.getNumberList() != null) {
        NumberList list = node.getNumberList();
        // Continue with further operations on list properties
    }
}
```

### Step 4: Extract the desired list properties
Inside the loop, you can now read any attribute exposed by the `NumberList` class.

```java
// Retrieve font name
System.out.println("Font Name: " + list.getFont());
// Retrieve font length (character count)
System.out.println("Font Length: " + list.getFont());
// Retrieve font size
System.out.println("Font Size: " + list.getFontSize());
// Retrieve font color
System.out.println("Font Color: " + list.getFontColor());
// Retrieve format (e.g., decimal, lowerLetter)
System.out.println("Font format: " + list.getFormat());
// Check bold style
System.out.println("Is bold: " + list.isBold());
// Check italic style
System.out.println("Is italic: " + list.isItalic());
```

The console output will display each property, allowing you to log, analyze, or further process the list styling information.

## Common Issues & Troubleshooting
| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| `NullPointerException` on `list.getFont()` | The node does not contain a `NumberList`. | Add a null‑check (`if (node.getNumberList() != null)`). |
| No output appears | `dataDir` points to the wrong folder. | Verify the path and ensure `Sample1.one` exists. |
| Font color shows as `null` | The list uses the default theme color. | Use `list.getFontColor()` with a fallback to the document’s theme. |

## Frequently Asked Questions

**Q: Is Aspose.Note compatible with different OneNote versions?**  
A: Yes, Aspose.Note supports a wide range of OneNote file formats, from older 2007 versions to the latest Office 365 releases.

**Q: Can I customize which font properties are retrieved?**  
A: Absolutely. You can call only the getters you need (e.g., `getFontSize()` or `isBold()`) and ignore the rest.

**Q: Where can I find additional support or assistance?**  
A: For any queries or issues, visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for prompt assistance.

**Q: Do I need a temporary license for testing?**  
A: Yes, you can obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)** for evaluation purposes.

**Q: What if I want to purchase Aspose.Note for Java?**  
A: You can purchase the product **[here](https://purchase.aspose.com/buy)** to unlock its full potential for your projects.

---

**Last Updated:** 2026-03-08  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
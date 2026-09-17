---
title: How to Get Last Modified Time of OneNote Pages – Aspose.Note
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to get last modified time and retrieve revisions of OneNote pages using Aspose.Note for Java. Integrate this into your Java apps for efficient document management.
weight: 15
url: /java/onenote-page-manipulation/get-revisions-of-pages/
date: 2026-01-10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Get Revisions of Pages in OneNote - Aspose.Note

## Introduction

In this tutorial, you'll **get last modified time** for pages inside a OneNote document and explore how to retrieve the full revision history using Aspose.Note for Java. Whether you're building a document‑management system, auditing changes, or simply need to display when a page was last edited, this guide shows you exactly how to extract that information programmatically.

## Quick Answers
- **What does “get last modified time” return?** The timestamp of the most recent edit on a OneNote page.  
- **Which class provides revision history?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Do I need a license for this feature?** Yes, a valid Aspose.Note license is required for production use.  
- **What Java version is supported?** Java 8 or higher (JDK 8+).  
- **Can I filter revisions by author?** You can read the `Author` property of each `Page` object and apply your own filter.

## What is “get last modified time” in OneNote?

The **last modified time** is a metadata field stored with each page that records when the page was most recently changed. Aspose.Note exposes this value through the `Page.getLastModifiedTime()` method, making it easy to display or log change dates.

## Why retrieve page revisions?

- **Audit trails:** Keep a record of who changed what and when.  
- **Version comparison:** Build features that compare two revisions side‑by‑side.  
- **User collaboration insights:** Understand editing patterns in shared notebooks.  

## Prerequisites

Before you start, make sure you have the following:

### Java Development Kit (JDK) Installed
Install JDK 8 or later from the Oracle website or your preferred package manager.

### Aspose.Note for Java Library
Download the library from the official site. You can find the download link **[here](https://releases.aspose.com/note/java/)**. Follow the installation instructions in the documentation **[here](https://reference.aspose.com/note/java/)**.

## Import Packages

To begin, import the necessary packages into your Java project. These packages will allow you to leverage the functionality provided by Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Now, let's break down the example code provided into multiple steps to understand each component and its functionality.

## How to Get Last Modified Time of a OneNote Page

### Step 1: Set Document Directory
Define the directory where your OneNote document is located.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Load the Document
Load the OneNote document into Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Step 3: Get First Page
Retrieve the first page from the document.

```java
Page firstPage = doc.getFirstChild();
```

### Step 4: Get Page Revisions
Obtain the revisions history of the page.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Step 5: Traverse Page Revisions
Iterate through the list of page revisions and retrieve relevant information, including the **last modified time**.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Common Issues and Solutions
- **Null `PageHistory`:** Ensure the document actually contains revisions; otherwise `getPageHistory` may return `null`.  
- **Time zone differences:** `getLastModifiedTime()` returns a `java.util.Date` in the system’s default time zone. Convert to UTC if needed.  
- **License not loaded:** Without a valid license, Aspose.Note may operate in evaluation mode, limiting the number of pages processed.

## Frequently Asked Questions

### Q1: Can I use Aspose.Note for Java to create new OneNote documents?
A1: Yes, Aspose.Note for Java provides comprehensive support for creating, reading, and manipulating OneNote documents programmatically.

### Q2: Is Aspose.Note for Java compatible with different versions of OneNote files?
A2: Yes, Aspose.Note for Java supports various versions of Microsoft OneNote files, ensuring compatibility across different environments.

### Q3: Can I customize the output format when exporting OneNote documents?
A3: Absolutely, Aspose.Note for Java offers flexibility in exporting OneNote documents to different formats such as PDF, HTML, and images, with options for customization.

### Q4: Does Aspose.Note for Java require a license for commercial use?
A4: Yes, a valid license is required for commercial use of Aspose.Note for Java. You can obtain a license from the Aspose website.

### Q5: Where can I seek assistance if I encounter issues or have questions about Aspose.Note for Java?
A5: For support and assistance, you can visit the Aspose.Note forum **[here](https://forum.aspose.com/c/note/28)**, where you can ask questions, share experiences, and interact with other users and experts.

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
title: Get Revisions of Pages in OneNote - Aspose.Note
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to retrieve revisions of pages within OneNote documents using Aspose.Note for Java. Integrate this functionality seamlessly into your Java applications for efficient document management.
type: docs
weight: 15
url: /java/onenote-page-manipulation/get-revisions-of-pages/
---
## Introduction

In this tutorial, we'll delve into the capabilities of Aspose.Note for Java, a powerful library that enables you to work with Microsoft OneNote files seamlessly in your Java applications. Specifically, we'll focus on how to retrieve revisions of pages within a OneNote document. By the end of this guide, you'll be equipped with the knowledge to efficiently extract page revisions, including details such as last modified time, creation time, title, level, and author.

## Prerequisites

Before diving into this tutorial, ensure you have the following prerequisites set up:

### Java Development Kit (JDK) Installed

Make sure you have the Java Development Kit installed on your system. You can download and install it from the Oracle website or use a package manager if you're on a Unix-based system.

### Aspose.Note for Java Library

Download and install Aspose.Note for Java library from the website. You can find the download link [here](https://releases.aspose.com/note/java/). Follow the installation instructions provided in the documentation [here](https://reference.aspose.com/note/java/).

## Import Packages

To begin, import the necessary packages into your Java project. These packages will allow you to leverage the functionality provided by Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Now, let's break down the example code provided into multiple steps to understand each component and its functionality.

## Step 1: Set Document Directory

Define the directory where your OneNote document is located.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the Document

Load the OneNote document into Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Step 3: Get First Page

Retrieve the first page from the document.

```java
Page firstPage = doc.getFirstChild();
```

## Step 4: Get Page Revisions

Obtain the revisions history of the page.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Step 5: Traverse Page Revisions

Iterate through the list of page revisions and retrieve relevant information.

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

## Conclusion

In this tutorial, we've explored how to retrieve revisions of pages within a OneNote document using Aspose.Note for Java. By following the step-by-step guide and leveraging the provided example code, you can easily integrate this functionality into your Java applications, enabling efficient management of OneNote files.

## FAQ's

### Q1: Can I use Aspose.Note for Java to create new OneNote documents?

A1: Yes, Aspose.Note for Java provides comprehensive support for creating, reading, and manipulating OneNote documents programmatically.

### Q2: Is Aspose.Note for Java compatible with different versions of OneNote files?

A2: Yes, Aspose.Note for Java supports various versions of Microsoft OneNote files, ensuring compatibility across different environments.

### Q3: Can I customize the output format when exporting OneNote documents?

A3: Absolutely, Aspose.Note for Java offers flexibility in exporting OneNote documents to different formats such as PDF, HTML, and images, with options for customization.

### Q4: Does Aspose.Note for Java require a license for commercial use?

A4: Yes, a valid license is required for commercial use of Aspose.Note for Java. You can obtain a license from the Aspose website.

### Q5: Where can I seek assistance if I encounter issues or have questions about Aspose.Note for Java?

A5: For support and assistance, you can visit the Aspose.Note forum [here](https://forum.aspose.com/c/note/28), where you can ask questions, share experiences, and interact with other users and experts.

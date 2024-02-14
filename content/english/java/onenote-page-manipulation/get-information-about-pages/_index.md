---
title: Get Information about Pages in OneNote - Aspose.Note
linktitle: Get Information about Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to extract page information from OneNote documents using Aspose.Note for Java. Easy-to-follow tutorial for developers.
type: docs
weight: 12
url: /java/onenote-page-manipulation/get-information-about-pages/
---
## Introduction

In this tutorial, we will guide you through the process of extracting information about pages in OneNote using Aspose.Note for Java. Aspose.Note is a powerful API that allows you to work with Microsoft OneNote documents programmatically. Whether you need to access page revisions, creation times, titles, or authors, Aspose.Note simplifies the task with its intuitive interface.

## Prerequisites

Before we begin, ensure you have the following:

1. Java Development Kit (JDK): Make sure you have JDK installed on your system.
2. Aspose.Note for Java: Download and install the Aspose.Note for Java library. You can get it from the [website](https://purchase.aspose.com/buy).
3. Sample OneNote Document: Prepare a sample OneNote document that you will use to retrieve information from.

## Import Packages

First, you need to import the necessary packages to work with Aspose.Note in your Java project.

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Step 1: Load the OneNote Document

Begin by loading the OneNote document using Aspose.Note.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

Replace `"Your Document Directory"` with the path to your OneNote document.

## Step 2: Retrieve Page Information

Next, retrieve information about the pages in the OneNote document.

```java
// Get page revisions
List<Page> pages = doc.getChildNodes(Page.class);

// Traverse list of pages
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

This code snippet iterates through each page in the document and prints out information such as the last modified time, creation time, title, level, and author of each page.

## Conclusion

In this tutorial, you learned how to retrieve information about pages in OneNote using Aspose.Note for Java. By following the steps outlined above, you can seamlessly integrate Aspose.Note into your Java applications to extract valuable data from OneNote documents.

## FAQ's

### Q1: Can I use Aspose.Note for Java to edit OneNote documents?

A1: Yes, Aspose.Note provides a comprehensive set of features for editing and manipulating OneNote documents programmatically.

### Q2: Is Aspose.Note compatible with all versions of OneNote?

A2: Aspose.Note supports various versions of OneNote, ensuring compatibility across different environments.

### Q3: Can I convert OneNote documents to other formats using Aspose.Note?

A3: Absolutely, Aspose.Note allows you to convert OneNote documents to formats such as PDF, HTML, and images effortlessly.

### Q4: Does Aspose.Note offer technical support to developers?

A4: Yes, Aspose provides dedicated technical support to assist developers with any issues they encounter while using Aspose.Note.

### Q5: Is there a trial version available for Aspose.Note for Java?

A5: Yes, you can download a free trial version of Aspose.Note for Java from [here](https://releases.aspose.com/).

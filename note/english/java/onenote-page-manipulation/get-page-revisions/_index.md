---
title: Get Page Revisions in OneNote - Aspose.Note
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to retrieve page revisions in OneNote using Aspose.Note for Java. Follow our step-by-step guide for efficient tracking of changes.
weight: 14
url: /java/onenote-page-manipulation/get-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Get Page Revisions in OneNote - Aspose.Note

## Introduction

OneNote is a powerful tool for organizing and managing your notes, but sometimes you need to track changes and revisions made to your pages. With Aspose.Note for Java, you can easily retrieve page revisions programmatically. In this tutorial, we'll guide you through the process of getting page revisions in OneNote using Aspose.Note for Java.

## Prerequisites

Before we get started, make sure you have the following prerequisites in place:

### 1. Java Development Kit (JDK)

Ensure you have Java Development Kit (JDK) installed on your system. You can download and install JDK from the Oracle website.

### 2. Aspose.Note for Java

Download and install Aspose.Note for Java from the[download link](https://releases.aspose.com/note/java/).

### 3. Sample OneNote Document

Prepare a sample OneNote document (`Sample1.one`) that contains the pages you want to retrieve revisions from.

## Import Packages

First, you need to import the necessary packages from Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Now, let's break down the provided example into multiple steps:

## Step 1: Set Up Document Directory

Define the directory path where your OneNote document is located.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load OneNote Document

Load the OneNote document using `LoadOptions` to enable loading history.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Step 3: Get First Page

Retrieve the first page from the loaded document.

```java
Page firstPage = document.getFirstChild();
```

## Step 4: Iterate Through Page Revisions

Iterate through each page revision and retrieve relevant information such as last modified time, creation time, title, level, and author.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Conclusion

In this tutorial, we've learned how to retrieve page revisions in OneNote using Aspose.Note for Java. By following these steps, you can efficiently track changes made to your OneNote pages programmatically.

## FAQ's

### Q1: Can I use Aspose.Note for Java to modify page revisions?

A1: No, Aspose.Note for Java currently supports retrieving page revisions but not modifying them.

### Q2: Is Aspose.Note for Java compatible with different versions of OneNote documents?

A2: Yes, Aspose.Note for Java supports various versions of OneNote documents, allowing you to work with different file formats seamlessly.

### Q3: Does Aspose.Note for Java require a license to use?

A3: Yes, you need to purchase a license to use Aspose.Note for Java in commercial projects. However, you can also obtain a temporary license for evaluation purposes.

### Q4: Can I seek support if I encounter any issues while using Aspose.Note for Java?

A4: Yes, you can seek support from the Aspose.Note forum [here](https://forum.aspose.com/c/note/28).

### Q5: Is there a free trial available for Aspose.Note for Java?

A5: Yes, you can access a free trial of Aspose.Note for Java from the [website](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

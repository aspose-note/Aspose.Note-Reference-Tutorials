---
title: Get File Format Info from OneNote - Java
linktitle: Get File Format Info from OneNote - Java
second_title: Aspose.Note Java API
description: Learn to extract file format details from OneNote files in Java with Aspose.Note. Enhance your Java applications by following this comprehensive tutorial.
weight: 22
url: /java/onenote-document-loading/get-file-format-info/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Get File Format Info from OneNote - Java

## Introduction

In this tutorial, we will explore how to retrieve file format information from a OneNote file using Java with the help of Aspose.Note. Aspose.Note for Java is a powerful API that allows developers to work with Microsoft OneNote files programmatically, enabling tasks such as reading, writing, and manipulating OneNote documents seamlessly.

## Prerequisites

Before we begin, ensure that you have the following prerequisites set up:

1. Java Development Kit (JDK): Make sure you have JDK installed on your system. You can download and install JDK from [here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2. Aspose.Note for Java Library: Download and include the Aspose.Note for Java library in your project. You can find the download link [here](https://releases.aspose.com/note/java/).

## Import Packages

First, import the necessary packages to your Java project to begin working with Aspose.Note. Here's how you can do it:

## Step 1: Import Aspose.Note Package

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.FileFormat;
```

Now, let's proceed with retrieving file format information from a OneNote file.

## Step 1: Initialize Document Object

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```

## Step 2: Switch Statement for File Format

Use a switch statement to determine the file format of the OneNote document.

```java
switch (document.getFileFormat()) {
    case FileFormat.OneNote2010:
        // Process OneNote 2010
        break;
    case FileFormat.OneNoteOnline:
        // Process OneNote Online
        break;
}
```

## Conclusion

In this tutorial, we learned how to retrieve file format information from a OneNote file using Java with Aspose.Note. By following the steps outlined above, you can seamlessly integrate this functionality into your Java applications, enabling efficient manipulation of OneNote documents programmatically.

## FAQs

### Q1: Can I use Aspose.Note for Java to edit OneNote files?

A1: Yes, Aspose.Note for Java provides comprehensive features to edit, create, and manipulate OneNote files programmatically.

### Q2: Is Aspose.Note for Java compatible with all versions of OneNote files?

A2: Aspose.Note for Java supports various versions of OneNote files, including OneNote 2010 and OneNote Online.

### Q3: Where can I find support for Aspose.Note for Java?

A3: You can find support and assistance for Aspose.Note for Java on the [Aspose.Note forum](https://forum.aspose.com/c/note/28).

### Q4: Is there a free trial available for Aspose.Note for Java?

A4: Yes, you can access a free trial of Aspose.Note for Java from [here](https://releases.aspose.com/).

### Q5: How can I purchase a license for Aspose.Note for Java?

A5: You can purchase a license for Aspose.Note for Java from the [purchase page](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Save OneNote Document to Stream - Aspose.Note
linktitle: Save OneNote Document to Stream - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to save OneNote documents to a stream using Aspose.Note for Java. Follow our step-by-step tutorial for efficient integration into your Java applications.
type: docs
weight: 13
url: /java/onenote-document-saving/save-onenote-document-to-stream/
---
## Introduction

Welcome to our tutorial on using Aspose.Note for Java to save OneNote documents to a stream. Aspose.Note is a powerful Java library that enables developers to work with Microsoft OneNote files programmatically. In this tutorial, we'll guide you through the process of saving a OneNote document to a stream using Aspose.Note.

## Prerequisites

Before we begin, ensure you have the following prerequisites:

- Basic understanding of Java programming.
- JDK installed on your system.
- Aspose.Note for Java library downloaded and added to your project. You can download it from [here](https://releases.aspose.com/note/java/).

## Import Packages

First, let's import the necessary packages:

```java
import java.io.ByteArrayOutputStream;
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Step 1: Load the OneNote Document

The first step is to load the OneNote document into Aspose.Note.

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Step 2: Save Document to Stream

Next, we'll save the loaded document to a stream, in this case, to a ByteArrayOutputStream.

```java
ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
doc.save(dstStream, SaveFormat.Pdf);
```

## Conclusion

In this tutorial, we've learned how to use Aspose.Note for Java to save a OneNote document to a stream. By following these steps, you can efficiently integrate OneNote document processing into your Java applications.

## FAQ's

### Q1: Can I save the OneNote document in formats other than PDF?

A1: Yes, Aspose.Note supports saving documents in various formats like DOCX, HTML, JPEG, PNG, etc. 

### Q2: Is there a free trial available for Aspose.Note for Java?

A2: Yes, you can download a free trial from [here](https://releases.aspose.com/).

### Q3: Where can I find more support or ask questions related to Aspose.Note?

A3: You can visit the Aspose.Note forum [here](https://forum.aspose.com/c/note/28).

### Q4: How can I purchase a license for Aspose.Note for Java?

A4: You can buy a license from [here](https://purchase.aspose.com/buy).

### Q5: Do I need a temporary license for evaluation purposes?

A5: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/).

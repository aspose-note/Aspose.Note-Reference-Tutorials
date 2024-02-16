---
title: Set Output Image Resolution in OneNote - Aspose.Note
linktitle: Set Output Image Resolution in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to adjust image resolution in OneNote documents using Aspose.Note for Java. Follow our step-by-step guide for easy implementation
type: docs
weight: 23
url: /java/onenote-document-saving/set-output-image-resolution/
---
## Introduction

Are you looking to manipulate the resolution of images within your OneNote documents using Java? Aspose.Note for Java offers a robust solution for such tasks. In this tutorial, we'll walk through the steps to set the output image resolution using Aspose.Note.

## Prerequisites

Before we begin, ensure you have the following prerequisites:

1. Java Development Kit (JDK): Install JDK on your system.
2. Aspose.Note for Java: Download and install Aspose.Note for Java from the [website](https://releases.aspose.com/note/java/).
3. Integrated Development Environment (IDE): Choose your preferred IDE like Eclipse or IntelliJ IDEA.

## Import Packages

In your Java project, import the necessary Aspose.Note packages:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step 1: Load the OneNote Document

Start by loading the OneNote document into your Java application:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

Replace `"Your Document Directory"` with the actual directory where your OneNote document resides.

## Step 2: Set Image Save Options

Define the image save options and specify the desired resolution:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

Here, we're setting the resolution to `120 dpi`. You can adjust this value according to your requirements.

## Step 3: Save the Document with Modified Resolution

Save the document with the updated image resolution:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

This will save the modified document with the specified resolution.

## Conclusion

In this tutorial, we've explored how to set the output image resolution in OneNote documents using Aspose.Note for Java. By following these simple steps, you can efficiently manipulate the resolution of images to meet your application's requirements.


## FAQ's

### Q1: Can I adjust the image resolution to a value higher than 120 dpi?

A1: Yes, you can set the resolution to any desired value according to your needs.

### Q2: Does Aspose.Note support other image formats besides JPEG?

A2: Yes, Aspose.Note supports various image formats such as PNG, BMP, GIF, etc.

### Q3: Is Aspose.Note compatible with all versions of Java?

A3: Aspose.Note is compatible with Java 1.6 or later versions.

### Q4: Can I manipulate other aspects of images in OneNote documents using Aspose.Note?

A4: Yes, Aspose.Note provides comprehensive features for image manipulation, including resizing, cropping, and rotation.

### Q5: Where can I get support for Aspose.Note-related queries?

A5: You can seek assistance from the Aspose.Note community forum [here](https://forum.aspose.com/c/note/28).

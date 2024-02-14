---
title: Convert Notebook to Flattened Image in OneNote - Aspose.Note
linktitle: Convert Notebook to Flattened Image in OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Learn how to convert a notebook to a flattened image in OneNote using Aspose.Note for Java. Preserve all elements in a single image file effortlessly.
type: docs
weight: 13
url: /java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## Introduction

In this tutorial, we will guide you through the process of converting a notebook to a flattened image in OneNote using Aspose.Note for Java. This allows you to save your notebook as an image file, ensuring that all elements are preserved in a single image format.

## Prerequisites

Before we begin, ensure you have the following:

1. Java Development Kit (JDK) installed on your system.
2. Aspose.Note for Java library downloaded and set up in your Java project. You can download the library from [here](https://releases.aspose.com/note/java/).
3. Basic knowledge of Java programming.

## Import Packages

To start, you need to import the necessary packages from Aspose.Note for Java:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step 1: Set Up Document Directory

Firstly, define the directory where your notebook file is located:

```java
String dataDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with the path to your notebook file.

## Step 2: Load Notebook

Next, load the notebook file using the `Notebook` class:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Ensure to replace `"test.onetoc2"` with the name of your notebook file.

## Step 3: Set Image Save Options

Now, set up the options for saving the notebook as an image. We will specify the save format as PNG and set the resolution to 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

You can adjust the resolution as per your requirements.

## Step 4: Flatten Notebook

To ensure that all elements are flattened into a single image, set the `flatten` option to `true`:

```java
saveOptions.setFlatten(true);
```

This ensures that the resulting image maintains the layout of your notebook.

## Step 5: Save Image

Finally, save the notebook as a flattened image:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Replace `"ExportImageasFlattenedNotebook_out.png"` with your desired output file name.

## Conclusion

In conclusion, using Aspose.Note for Java, you can easily convert your notebook to a flattened image in OneNote. This process ensures that all elements are preserved in a single image format, facilitating easy sharing and viewing.

## FAQ's

### Q1: Can I adjust the resolution of the output image?

A1: Yes, you can adjust the resolution according to your requirements by modifying the `setResolution` method parameter.

### Q2: Does Aspose.Note support other image formats for export?

A2: Yes, Aspose.Note supports various image formats such as PNG, JPEG, BMP, etc., for exporting notebooks.

### Q3: Can I customize the output image further?

A3: Yes, Aspose.Note provides extensive options for customizing the output image, including page size, orientation, and quality settings.

### Q4: Is there a trial version available for Aspose.Note for Java?

A4: Yes, you can obtain a free trial version from [here](https://releases.aspose.com/).

### Q5: Where can I find support for Aspose.Note for Java?

A5: You can find support and resources on the Aspose.Note forum [here](https://forum.aspose.com/c/note/28).

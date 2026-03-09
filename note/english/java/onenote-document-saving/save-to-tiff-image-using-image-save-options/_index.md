---
title: Save to TIFF Image Using TIFF JPEG Compression in OneNote
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
description: Learn how to save OneNote documents as TIFF files using TIFF JPEG compression, PackBits, or CCITT Group 3 Fax in Java. Control image quality, file size, and color mode with Aspose.Note. #OneNote #Java #Aspose
weight: 21
url: /java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
date: 2025-12-17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save to TIFF Image Using TIFF JPEG Compression in OneNote

## Introduction

In this tutorial you’ll discover **how to save a OneNote document to a TIFF file using TIFF JPEG compression** and two other popular compression methods. We'll walk through the required setup, import the necessary Java packages, and provide clear step‑by‑step code for each compression option. By the end you’ll be able to control **TIFF image quality**, reduce file size, and even produce black‑and‑white TIFFs for fax‑style output.

## Quick Answers
- **What is TIFF JPEG compression?** A loss‑y compression method that reduces TIFF file size while preserving visual quality.  
- **Which library handles the conversion?** Aspose.Note for Java.  
- **Do I need a license?** A free trial works for testing; a license is required for production.  
- **Can I change the image quality?** Yes, set the `quality` property on `ImageSaveOptions`.  
- **Is batch conversion possible?** Absolutely – loop through documents and apply the same options.

## What is TIFF JPEG Compression?
TIFF JPEG compression stores image data in the TIFF container but applies JPEG’s lossy algorithm to shrink the file. It’s ideal when you need a balance between **tiff image quality** and smaller file size, especially for web or archival scenarios.

## Why Use Different TIFF Compression Types?
- **JPEG** – Good for photographs; offers adjustable quality.  
- **PackBits** – Simple, loss‑less run‑length encoding; useful for graphics with large uniform areas.  
- **CCITT Group 3 Fax** – Black‑and‑white only; perfect for scanned documents and fax transmission.  

Choosing the right compression lets you meet storage constraints without sacrificing the visual fidelity required for your application.

## Prerequisites

- Java Development Kit (JDK) installed.  
- Aspose.Note for Java library added to your project (Maven/Gradle or manual JAR).  
- Basic familiarity with Java syntax.

## Import Packages

First, bring the necessary Aspose.Note classes into your Java file:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Step 1: Save to TIFF Using TIFF JPEG Compression

Below is the complete method that loads a OneNote file and saves it as a TIFF with JPEG compression. Adjust the `quality` value (0‑100) to control **tiff image quality**.

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Explanation**

- `ImageSaveOptions` tells Aspose.Note to output a TIFF file.  
- `setTiffCompression(TiffCompression.Jpeg)` selects JPEG compression.  
- `setQuality(93)` (optional) fine‑tunes the image quality; lower values produce smaller files.

### How to Save TIFF with JPEG Compression in Java
1. Point `dataDir` to the folder containing your `.one` file.  
2. Call `SaveToTiffUsingJpegCompression()` from your main method or service.  
3. The resulting `.tiff` file will appear in the same directory.

## Step 2: Save to TIFF Using PackBits Compression

If you need a loss‑less option, PackBits is a simple run‑length algorithm that works well for graphics with solid colors.

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Explanation**

- `setTiffCompression(TiffCompression.PackBits)` switches the compression method.  
- No quality setting is needed because PackBits is loss‑less.

## Step 3: Save to TIFF Using CCITT Group 3 Fax Compression (Black‑and‑White TIFF)

For fax‑style documents you often want a **black and white TIFF**. CCITT Group 3 provides high compression for monochrome images.

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Explanation**

- `setColorMode(ColorMode.BlackAndWhite)` forces a monochrome output.  
- `setTiffCompression(TiffCompression.Ccitt3)` applies the fax‑oriented compression.

## Common Issues & Tips

| Issue | Solution |
|-------|----------|
| **Output file is larger than expected** | Try reducing the JPEG `quality` value or switch to PackBits if lossless is acceptable. |
| **Colors appear washed out** | Ensure you’re not unintentionally setting `ColorMode.BlackAndWhite` when you need full color. |
| **Unsupported image format error** | Verify you’re using a recent version of Aspose.Note; older builds may lack certain compression enums. |
| **LicenseException at runtime** | Install a valid Aspose.Note license (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Frequently Asked Questions

**Q: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these options?**  
A: Yes. Aspose.Note focuses on OneNote files, but Aspose’s other libraries (PDF, Words) provide similar `ImageSaveOptions` for their respective formats.

**Q: How does TIFF JPEG compression differ from standard JPEG files?**  
A: The image data is stored inside a TIFF container, preserving metadata and allowing multiple pages, while the compression algorithm remains JPEG.

**Q: Is it possible to batch‑process many `.one` files?**  
A: Absolutely. Loop through a folder, call any of the three methods per file, and collect the resulting TIFFs.

**Q: Can I control the DPI/resolution of the output TIFF?**  
A: Yes. Use `options.setResolution(int dpi)` before saving.

**Q: Does Aspose.Note support asynchronous processing?**  
A: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture` or thread pools for parallel execution.

## Conclusion

You now have a complete, **java tiff conversion** toolkit that lets you save OneNote documents as TIFF files using JPEG, PackBits, or CCITT Group 3 Fax compression. Adjust the quality, color mode, and resolution to meet your specific **tiff image quality** requirements, and integrate these methods into batch workflows for maximum productivity.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
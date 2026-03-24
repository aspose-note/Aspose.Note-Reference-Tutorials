---
date: 2026-03-24
description: Aspose.Note for Java kullanarak OneNote'u görüntü olarak kaydetmeyi ve
  OneNote'u görüntüye dönüştürmeyi öğrenin. Java geliştiricileri için adım adım rehber.
linktitle: Save OneNote as Image – Convert Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u Görüntü Olarak Kaydet – Defteri Aspose.Note ile Görüntüye Dönüştür
url: /tr/java/onenote-notebook-operations/convert-notebook-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u Görüntü Olarak Kaydet – Defteri Görüntüye Dönüştürün Aspise.Note ile

## Introduction

Bu öğreticide **OneNote'u görüntü olarak nasıl kaydedeceğinizi** öğreneceksiniz; bir OneNote defterini PNG (veya başka bir görüntü formatı) olarak Aspose.Note for Java kütüphanesini kullanarak dönüştürerek. Defter sayfalarını görüntülere dönüştürmek, OneNote dosyalarını desteklemeyen platformlarda notları paylaşmanız, PDF'lere gömmeniz veya slayt sunumlarına eklemeniz gerektiğinde kullanışlıdır.

## Quick Answers
- **What library is needed?** Aspose.Note for Java.  
- **Which image formats are supported?** PNG, JPEG, BMP, GIF, TIFF, etc.  
- **Do I need a license?** A free trial works for testing; a commercial license is required for production.  
- **How long does the conversion take?** Typically a few seconds per notebook, depending on size.  
- **Can I batch‑process notebooks?** Yes – just loop through the files and reuse the same code.

## What is **save OneNote as image**?

OneNote'u görüntü olarak kaydetmek, bir `.one` defterinin her sayfasını bir raster görüntü dosyasına (ör. PNG) render etmek anlamına gelir. Bu, OneNote gerektirmeden her yerde görüntülenebilen taşınabilir, sadece‑okunur bir temsil oluşturur.

## Why convert OneNote to image?

- **Cross‑platform sharing** – Alıcılar içeriği herhangi bir cihazda görüntüleyebilir.  
- **Embedding in documents** – Görüntüyü Word, PowerPoint veya PDF'lere ekleyin.  
- **Archiving** – Orijinal defter düzenlense bile değişmeyecek görsel bir anlık görüntü saklayın.  
- **Presentation‑ready** – Yüksek çözünürlüklü PNG'leri doğrudan slaytlara yerleştirin.

## Prerequisites

Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Java Development Kit (JDK)** – En son JDK'yı [website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) adresinden indirin.  
2. **Aspose.Note for Java library** – JAR dosyasını [Aspose website](https://releases.aspose.com/note/java/) üzerinden alın ve projenizin classpath'ine ekleyin.

## Import Packages

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Şimdi dönüşüm sürecini adım adım inceleyelim.

## Step 1: Load the Notebook Document

```java
// Specify the directory where your notebook file is located
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

API'yi `Sample1.one` dosyasını içeren klasöre yönlendiriyor ve dosyayı bir `Document` nesnesine yüklüyoruz. Buradan sayfalara, bölümlere ve diğer defter öğelerine erişebilirsiniz.

## Step 2: Initialize ImageSaveOptions

```java
// Initialize PdfSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions`, Aspose.Note'un çıktıyı nasıl render edeceğini belirler. Bu örnekte PNG seçiyoruz, ancak `SaveFormat.Png` yerine `SaveFormat.Jpeg`, `SaveFormat.Bmp` vb. kullanarak **OneNote'u görüntüye dönüştürmek** için farklı bir format seçebilirsiniz.

## Step 3: Save the Document as Image

```java
// Save the document as PNG
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

`save()` çağrısı render edilen defter sayfalarını `ConvertToImage_out.png` dosyasına yazar. Defter birden fazla sayfa içeriyorsa, Aspose.Note otomatik olarak ayrı görüntü dosyaları oluşturur (ör. `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`).

## Step 4: Print Confirmation

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Basit bir konsol mesajı, **save OneNote as image** işleminin başarılı olduğunu ve çıktı dosyasının nerede bulunduğunu bildirir.

## Common Issues & Tips

- **Large notebooks** – `OutOfMemoryError` alırsanız JVM heap'ini (`-Xmx`) artırın.  
- **Resolution control** – Baskı kalitesinde görüntüler için DPI'yi artırmak amacıyla `options.setResolution(300);` kullanın.  
- **Batch conversion** – Yukarıdaki adımları bir `for` döngüsü içinde `.one` dosyalarının listesi üzerinde çalıştırarak toplu dönüşüm yapın.  

## FAQ's

### Q1: Can I convert notebooks to other image formats besides PNG?

A1: Yes, you can. The Aspose.Note library supports various image formats such as JPEG, BMP, GIF, TIFF, etc. You can specify the desired format in the `ImageSaveOptions` object accordingly.

### Q2: Is Aspose.Note compatible with all versions of OneNote?

A2: Aspose.Note provides comprehensive support for various versions of OneNote, ensuring compatibility across different environments and file formats.

### Q3: Can I customize the image output settings during conversion?

A3: Absolutely. Aspose.Note offers extensive options for customizing the output image, including resolution, quality, color depth, and more. You can tailor these settings according to your requirements.

### Q4: Does Aspose.Note support batch conversion of multiple notebooks?

A4: Yes, you can batch convert multiple notebooks to images efficiently using Aspose.Note. Simply iterate through your list of notebook files and apply the conversion process outlined in this tutorial.

### Q5: Where can I find additional resources and support for Aspose.Note?

A5: For further documentation, examples, and community support, visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) and explore the [documentation](https://reference.aspose.com/note/java/).

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.Note for Java 24.8  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
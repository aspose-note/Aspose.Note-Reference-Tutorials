---
date: 2025-11-29
description: Aspose.Note for Java kullanarak OneNote sayfasını PNG olarak dışa aktarmayı
  öğrenin. Sayfa indeksini ayarlama, sayfayı dönüştürme ve görüntüyü kaydetme adımlarını
  adım adım izleyin.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Aspose.Note kullanarak Java’da OneNote Sayfasını PNG Görüntüsü Olarak Dışa
  Aktarın
url: /tr/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java’da Aspose.Note Kullanarak OneNote Sayfasını PNG Görüntüsü Olarak Dışa Aktarma

## Introduction

Bu öğreticide **OneNote sayfasını** Aspose.Note for Java kütüphanesini kullanarak bir PNG görüntüsüne nasıl dışa aktaracağınızı keşfedeceksiniz. Ortamınızı hazırlamaktan sayfa indeksini ayarlamaya ve sonunda sayfayı yüksek kaliteli bir PNG dosyası olarak kaydetmeye kadar ihtiyacınız olan her şeyi adım adım göstereceğiz. Sonunda, OneNote belgeleriyle çalışan herhangi bir Java uygulamasına bu yeteneği ekleyebileceksiniz.

## Quick Answers
- **What library is needed?** Aspose.Note for Java.  
- **Can I export a single page?** Yes—use `setPageIndex` to target the exact page.  
- **Supported image formats?** PNG, JPEG, GIF, BMP, TIFF (PNG shown here).  
- **Do I need a license?** A free trial is available; a license is required for production.  
- **How long does implementation take?** Typically under 10 minutes for a basic conversion.

## What is “export OneNote page”?

OneNote sayfasını dışa aktarmak, bir `.one` belgesi içindeki belirli bir sayfayı bağımsız bir görüntü dosyasına (bu örnekte PNG) dönüştürmek anlamına gelir. Bu, OneNote ortamı dışındaki yerlerde OneNote içeriğini paylaşmanız, gömmeniz veya işlemeniz gerektiğinde faydalıdır.

## Why use Aspose.Note for Java to convert OneNote to PNG?
- **No Microsoft Office dependency** – works on any platform that runs Java.  
- **Fine‑grained control** – you can pick any page via `setPageIndex`.  
- **High‑quality output** – PNG retains vector graphics and text clarity.  
- **Batch‑ready** – easy to loop through pages for bulk conversion.

## Prerequisites

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **Aspose.Note for Java** – en son JAR dosyasını [Aspose web sitesinden](https://releases.aspose.com/note/java/) indirin.  
3. **Bir OneNote belgesi** (`.one`) – dışa aktarmak istediğiniz sayfayı içeren dosya.

## Import Packages

İlk olarak, gerekli Java sınıflarını içe aktarın:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Load the OneNote Document

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

`Document` sınıfını kullanarak OneNote dosyasını diskteki konumundan okuruz. `LoadOptions` nesnesi, gerekirse yükleme davranışını özelleştirmenizi sağlar.

### Step 2: Initialize ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions`, Aspose.Note’a çıktının **PNG** formatında olmasını istediğimizi bildirir. `SaveFormat` değerini değiştirerek JPEG, BMP vb. formatlara geçiş yapabilirsiniz.

### Step 3: Set the Page Index (How to convert OneNote page)

```java
// set page index
opts.setPageIndex(0);
```

`setPageIndex` yöntemi, dışa aktarılacak sayfayı seçer. Sayfa numaralandırması **0**’dan başlar, bu yüzden `0` ilk sayfayı ifade eder. Farklı bir sayfayı dışa aktarmak için bu değeri ayarlayın.

### Step 4: Save the Document as PNG (Save OneNote as PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

`save` çağrısı, seçilen sayfayı diskte bir PNG dosyasına yazar. `ConvertSpecificPageToPngImage_out.png` dosya adı sadece bir örnektir—istediğiniz adı verebilirsiniz.

## Common Issues & Tips

- **Incorrect page index** – Indexleme 0’dan başlar. Boş bir görüntü alıyorsanız indeks değerini kontrol edin.  
- **Missing Aspose.Note JAR** – JAR dosyasının sınıf yolunuzda (classpath) olduğundan emin olun; aksi takdirde `ClassNotFoundException` alırsınız.  
- **Large pages** – Çok büyük sayfalar için JVM yığın boyutunu (`-Xmx`) artırarak `OutOfMemoryError` hatasından kaçının.

## Frequently Asked Questions

### Q1: Can I convert multiple pages to PNG images in one go using Aspose.Note for Java?
A1: Yes, you can loop through the document’s pages, update `opts.setPageIndex(i)`, and call `save` for each iteration.

### Q2: Does Aspose.Note for Java support other image formats besides PNG?
A2: Absolutely. You can set `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, or `SaveFormat.Tiff` in `ImageSaveOptions`.

### Q3: Is there a free trial available for Aspose.Note for Java?
A3: Yes, you can download a free trial from the [website](https://releases.aspose.com/).

### Q4: Can I get technical assistance if I encounter any issues with Aspose.Note for Java?
A4: Absolutely, you can seek support from the Aspose community forum [here](https://forum.aspose.com/c/note/28).

### Q5: Where can I purchase a license for Aspose.Note for Java?
A5: You can buy a license from the [purchase page](https://purchase.aspose.com/buy).

### Q6: How do I export a page that contains embedded images?
A6: Embedded images are rendered automatically in the PNG output; no extra code is required.

### Q7: Can I set the DPI or image resolution?
A7: Yes, use `opts.setResolution(int dpi)` before calling `save` to control output quality.

---

**Last Updated:** 2025-11-29  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
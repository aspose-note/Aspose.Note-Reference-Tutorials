---
date: 2025-12-04
description: OneNote'u PNG görüntüsü olarak kaydetmeyi Aspose.Note for Java ile öğrenin.
  Bu kılavuz ayrıca OneNote'u görüntü ve PDF'ye dönüştürmeyi gösterir.
linktitle: How to Save OneNote as PNG Image with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Aspose.Note for Java ile OneNote'u PNG Görüntüsü Olarak Kaydetme
url: /tr/java/onenote-document-loading/convert-to-image/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note for Java ile OneNote'u PNG Görüntüsü Olarak Kaydetme

## Introduction

Bu öğreticide **OneNote** belgelerini yüksek kaliteli PNG görüntüleri olarak nasıl kaydedeceğinizi **Aspose.Note for Java** kütüphanesini kullanarak öğreneceksiniz. OneNote'u görüntü formatlarına (PNG gibi) dönüştürmek, notları web sayfalarına yerleştirmeniz, küçük resimler oluşturmanız veya yazdırılabilir varlıklar üretmeniz gerektiğinde yaygın bir gereksinimdir. Ortamınızı kurmaktan dosyayı dışa aktarmaya kadar her adımı göstereceğiz; böylece bu yeteneği Java uygulamalarınıza hızlıca entegre edebilirsiniz.

## Quick Answers
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java.  
- **Başka formatlara dönüştürebilir miyim?** Evet – OneNote'u PDF, JPEG, BMP vb. formatlara da dönüştürebilirsiniz.  
- **İnternet bağlantısına ihtiyacım var mı?** Hayır, dönüşüm yerel olarak gerçekleşir.  
- **Bu kılavuzda hangi görüntü formatı kullanılıyor?** PNG (`SaveFormat`'ı değiştirerek JPEG veya BMP'ye geçebilirsiniz).  
- **Dönüşüm ne kadar sürer?** Standart bir OneNote dosyası için genellikle bir saniyenin altında.

## What is “how to save OneNote” in practice?

OneNote'u bir görüntü olarak kaydetmek, bir `.one` dosyasının her sayfasını raster bir formata (PNG, JPEG, …) render etmek anlamına gelir. Bu, OneNote yüklü olmayan kullanıcılarla notları paylaşmak veya statik görsel varlıklar oluşturmak için faydalıdır.

## Why use Aspose.Note for Java to convert OneNote to PNG?

- **Harici bağımlılık yok** – tamamen Java içinde çalışır.  
- **Tam doğruluk** – renkleri, yazı tiplerini ve düzeni korur.  
- **Esnek çıktı** – PNG, JPEG, BMP, PDF, HTML ve daha fazlasını destekler.  
- **Kurumsal hazır** – Java 8+ destekleyen herhangi bir platformda çalışır.

## Prerequisites

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **Aspose.Note for Java** kütüphanesi – resmi siteden en son JAR'ı indirin: [Aspose.Note for Java indirme](https://releases.aspose.com/note/java/).  
3. Dönüştürmek istediğiniz mevcut bir **OneNote (.one)** dosyası (ör. `Sample1.one`).

## Import Packages

First, import the classes we’ll need. This code block remains unchanged:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Set up Document Directory  
Define the folder that contains your OneNote file. Replace the placeholder with the actual path on your machine.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Load the OneNote Document  
Create a `Document` object by loading the `.one` file.

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Pro tip:** Daha sonra **OneNote'u PDF'e dönüştürmeniz** gerekirse, aynı `Document` örneğini farklı bir `SaveOptions` ile yeniden kullanabilirsiniz.

### Step 3: Initialize ImageSaveOptions  
Tell Aspose.Note which image format you want. Here we choose PNG, but you could also use `SaveFormat.Jpeg` or `SaveFormat.Bmp`.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

> This line also satisfies the secondary keyword **convert onenote to png** and **save onenote as png**.  
> Bu satır aynı zamanda **convert onenote to png** ve **save onenote as png** anahtar kelimelerini de karşılar.

### Step 4: Save the Document as an Image  
Export the OneNote page(s) to a PNG file.

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

> The method `save` automatically handles multi‑page documents by creating separate image files for each page.  
> `save` yöntemi, çok sayfalı belgeleri otomatik olarak her sayfa için ayrı görüntü dosyaları oluşturarak işler.

### Step 5: Print Confirmation  
Let the user know where the output was written.

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **FileNotFoundException** | Yanlış `dataDir` yolu | Klasör yolunun `/` veya `\\` ile bittiğini ve dosya adının doğru olduğunu doğrulayın. |
| **Unsupported format** | Kütüphane sürümü tarafından desteklenmeyen eski bir görüntü formatına kaydetmeye çalışmak | Aspose.Note'u en son sürüme güncelleyin veya desteklenen bir `SaveFormat` seçin. |
| **Large OneNote files cause OutOfMemoryError** | Yetersiz yığın (heap) alanı | JVM yığınını artırın (`-Xmx2g`) veya `Document.getPages()` döngüsüyle sayfaları tek tek işleyin. |

## Frequently Asked Questions

**S: Bir seferde birden fazla OneNote dosyasını dönüştürebilir miyim?**  
C: Evet. Dosya adları koleksiyonunda döngü oluşturup, her birini `new Document(...)` ile yükleyin ve kaydetme adımlarını tekrarlayın.

**S: Aspose.Note OneNote'u PDF'e dönüştürmeyi destekliyor mu?**  
C: Kesinlikle. **convert onenote to pdf** yapmak için `ImageSaveOptions` yerine `PdfSaveOptions` kullanın.

**S: PNG çıktısının çözünürlüğünü nasıl değiştirebilirim?**  
C: `save` çağırmadan önce `options.setResolutionX(int)` ve `options.setResolutionY(int)` değerlerini ayarlayın.

**S: OneNote'u JPEG gibi başka görüntü formatlarına dönüştürmenin bir yolu var mı?**  
C: Evet, `ImageSaveOptions` yapıcısında `SaveFormat.Png` yerine `SaveFormat.Jpeg` veya `SaveFormat.Bmp` kullanın.

**S: Dönüşüm için internet bağlantısına ihtiyacım var mı?**  
C: Hayır. Aspose.Note tüm işlemleri yerel olarak yapar; dış hizmetler çağrılmaz.

## Conclusion

Bu basit adımları izleyerek artık **OneNote** dosyalarını **Aspose.Note for Java** kullanarak PNG görüntüleri olarak nasıl kaydedeceğinizi biliyorsunuz. Bu yetenek, notları web sitelerine gömmek, yazdırılabilir varlıklar üretmek veya defterlerinizi statik görüntüler olarak arşivlemek gibi birçok senaryoya kapı açar. Diğer çıktı formatlarıyla (PDF veya JPEG gibi) da deney yapmaktan çekinmeyin ve kodu daha büyük otomasyon boru hatlarına entegre edin.

---

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
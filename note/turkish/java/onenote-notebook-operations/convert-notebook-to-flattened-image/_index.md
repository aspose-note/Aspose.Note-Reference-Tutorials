---
date: 2026-03-21
description: Aspose.Note for Java ile OneNote'u PNG'ye dönüştürerek defteri düzleştirmeyi
  öğrenin. Bu kılavuz, görüntü çözünürlüğünü ayarlamayı, OneNote'u resim olarak kaydetmeyi
  ve defterleri verimli bir şekilde düzleştirmeyi kapsar.
linktitle: How to Flatten Notebook – Convert OneNote to PNG
second_title: Aspose.Note Java API
title: Defteri Düzleştirme – OneNote'u PNG'ye Dönüştürme
url: /tr/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Flatten Notebook – Convert OneNote to PNG

## Introduction

Bu öğreticide **not defterini düzleştirme** (flatten notebook) içeriğini, Aspose.Note for Java kullanarak bir OneNote not defterini yüksek kaliteli PNG görüntüsüne dönüştürerek nasıl yapacağınızı keşfedeceksiniz. Bir rapora not defteri anlık görüntüsü eklemeniz, meslektaşlarınızla yalnızca okunabilir bir görünüm paylaşmanız veya uyumlu bir görüntüyü arşivlemeniz gerektiğinde, bu adım‑adım kılavuz, çözünürlüğü kontrol ederken OneNote’u görüntü olarak nasıl kaydedeceğinizi tam olarak gösterir.

## Quick Answers
- **“Flatten notebook” ne demektir?** Tüm sayfa öğelerini tek bir raster görüntüye birleştirir.  
- **Hangi format kullanılır?** PNG varsayılan olup kayıpsız kalite sağlar.  
- **DPI’yı değiştirebilir miyim?** Evet, `ImageSaveOptions` üzerindeki `setResolution` metodunu kullanın.  
- **Lisans gerekir mi?** Değerlendirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Tüm işletim sistemlerinde destekleniyor mu?** Java API’si, Java’nın çalıştığı her yerde çalışır.

## What is converting OneNote to PNG?

OneNote’u PNG’ye dönüştürmek, not defterindeki her sayfanın bitmap temsili oluşturur ve metin, çizimler ve gömülü nesneleri tek bir görüntü dosyasında korur. Bu, dokümantasyon, sunumlar veya uyum arşivleri için özellikle faydalıdır.

## Why convert OneNote to PNG with Aspose.Note?

- **Full fidelity** – Tüm görsel öğeler korunur.  
- **Single‑file output** – Birden fazla sayfa dosyası yönetmeye gerek kalmaz.  
- **Customizable resolution** – Kalite gereksinimlerinize göre DPI’yı ayarlayabilirsiniz.  
- **No Office installation** – Microsoft OneNote’a tamamen bağımsız çalışır.

## Prerequisites

Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

1. Sisteminizde Java Development Kit (JDK) yüklü.  
2. Aspose.Note for Java kütüphanesini indirdiniz ve Java projenize eklediniz. Kütüphaneyi [buradan](https://releases.aspose.com/note/java/) indirebilirsiniz.  
3. Java programlamaya temel düzeyde hakimiyet.

## Import Packages

Başlamak için Aspose.Note for Java’dan gerekli paketleri içe aktarın:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Set Up Document Directory

İlk olarak, not defteri dosyanızın bulunduğu dizini tanımlayın:

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini not defteri dosyanızın yolu ile değiştirin.

### Step 2: Load Notebook

Sonra, `Notebook` sınıfını kullanarak not defteri dosyasını yükleyin:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

`"test.onetoc2"` ifadesini not defteri dosyanızın adıyla değiştirin.

### Step 3: Set Image Save Options (set image resolution java)

Şimdi, not defterini görüntü olarak kaydetmek için seçenekleri ayarlayın. Kaydetme formatını PNG olarak belirleyecek ve çözünürlüğü 400 DPI olarak ayarlayacağız:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Gereksinimlerinize göre çözünürlüğü ayarlayabilirsiniz. Burada **görüntü çözünürlüğünü** (image resolution) ayarlayarak çıktı kalitesini kontrol edersiniz.

### Step 4: Flatten Notebook (how to flatten notebook)

Tüm öğelerin tek bir görüntüye düzleştirildiğinden emin olmak için `flatten` seçeneğini `true` olarak ayarlayın:

```java
saveOptions.setFlatten(true);
```

`flatten` değerini `true` yapmak, oluşturulan PNG’nin not defterinizin tam düzenini korumasını sağlar.

### Step 5: Save Image (save onenote as image)

Son olarak, not defterini düzleştirilmiş bir görüntü olarak kaydedin:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

`"ExportImageasFlattenedNotebook_out.png"` ifadesini istediğiniz çıktı dosya adıyla değiştirin. Bu adım **OneNote’u bir görüntü olarak kaydeder**, böylece istediğiniz yerde paylaşabilir veya yerleştirebilirsiniz.

## Common Use Cases

- **Documentation:** Not defteri görüntüsünü teknik kılavuzlar veya kullanıcı rehberlerine ekleyin.  
- **Presentations:** PowerPoint’te yüksek çözünürlüklü PNG slaytını kullanın; font veya nesne uyumluluğu sorunları yaşamazsınız.  
- **Archiving:** Uyumluluk denetimleri için not defterinin yalnızca okunabilir bir anlık görüntüsünü saklayın.

## Troubleshooting Tips

- **File not found:** `dataDir` yolunu iki kez kontrol edin ve `.onetoc2` dosyasının mevcut olduğundan emin olun.  
- **Low quality image:** DPI’yı artırmak için `documentSaveOptions.setResolution(600);` satırını değiştirin.  
- **Missing elements:** `saveOptions.setFlatten(true);` etkin olduğundan emin olun; aksi takdirde bazı katmanlar ayrı kalabilir.

## Frequently Asked Questions

**Q1: Çıktı görüntüsünün çözünürlüğünü ayarlayabilir miyim?**  
A1: Evet, `setResolution` metodunun parametresini değiştirerek gereksinimlerinize uygun çözünürlüğü ayarlayabilirsiniz.

**Q2: Aspose.Note dışa aktarma için başka görüntü formatlarını destekliyor mu?**  
A2: Evet, Aspose.Note PNG, JPEG, BMP gibi çeşitli görüntü formatlarını destekler.

**Q3: Çıktı görüntüsünü daha da özelleştirebilir miyim?**  
A3: Evet, Aspose.Note sayfa boyutu, yönlendirme ve kalite ayarları gibi geniş özelleştirme seçenekleri sunar.

**Q4: Aspose.Note for Java için bir deneme sürümü mevcut mu?**  
A4: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

**Q5: Aspose.Note for Java için destek nereden alınabilir?**  
A5: Aspose.Note forumunda destek ve kaynakları [buradan](https://forum.aspose.com/c/note/28) bulabilirsiniz.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
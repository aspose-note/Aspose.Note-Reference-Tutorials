---
date: 2026-02-05
description: Aspose.Note for Java kullanarak **OneNote'u PNG olarak kaydetmeyi** öğrenin
  ve birkaç satır kodla OneNote'u PNG, JPEG, BMP veya PDF'ye nasıl dönüştüreceğinizi
  keşfedin.
linktitle: How to save onenote as png with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Aspose.Note for Java ile OneNote'u PNG olarak nasıl kaydederiz
url: /tr/java/onenote-document-loading/convert-to-image/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note for Java ile onenote'u png olarak kaydetme

## Introduction

Bu öğreticide **Aspose.Note for Java** kütüphanesini kullanarak **onenote'u png olarak kaydetmeyi** keşfedeceksiniz. OneNote'u bir görüntü formatına (örneğin PNG) dönüştürmek, notları web sayfalarına gömmek, küçük resimler oluşturmak veya son kullanıcıların OneNote yüklü olmasını gerektirmeden yazdırılabilir varlıklar üretmek istediğinizde sıkça ihtiyaç duyulan bir gereksinimdir. Geliştirme ortamınızı kurmaktan dosyayı dışa aktarmaya kadar her adımı adım adım göstereceğiz; böylece bu yeteneği Java uygulamalarınıza hızlıca entegre edebilirsiniz.

## Quick Answers
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java.  
- **onenote'u diğer formatlara dönüştürebilir miyim?** Evet – onenote'u PDF, JPEG, BMP vb. formatlara da dönüştürebilirsiniz.  
- **İnternet bağlantısına ihtiyacım var mı?** Hayır, dönüşüm makinenizde yerel olarak çalışır.  
- **Bu rehberde hangi görüntü formatı kullanılıyor?** PNG (`SaveFormat`'ı değiştirerek JPEG veya BMP'ye geçebilirsiniz).  
- **Dönüşüm ne kadar sürer?** Standart bir OneNote dosyası için genellikle bir saniyenin altında.  
- **API Java 8+ ile uyumlu mu?** Kesinlikle, Java 8 veya daha üstünü destekleyen herhangi bir platformda çalışır.

## What is “save onenote as png” in practice?

OneNote'u PNG görüntüsü olarak kaydetmek, bir `.one` defterinin her sayfasını raster bir formata dönüştürmek anlamına gelir. Bu **onenote görüntü dönüşümü**, OneNote'u olmayan kullanıcılarla notları paylaşmak, statik görsel varlıklar oluşturmak veya defterleri evrensel olarak görüntülenebilir bir formatta arşivlemek için faydalıdır.

## Why use Aspose.Note for Java to convert onenote to png?

- **Harici bağımlılık yok** – saf Java, yerel bileşen yok.  
- **Tam doğruluk** – renkler, yazı tipleri ve düzen tam olarak korunur.  
- **Esnek çıktı** – PNG, JPEG, BMP, PDF, HTML ve daha fazlasını destekler.  
- **Kurumsal kullanım için hazır** – Java 8+ destekleyen herhangi bir platformda çalışır ve üretim kullanımı için lisanslanabilir.  

## Prerequisites

Başlamadan önce şunların olduğundan emin olun:

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **Aspose.Note for Java** kütüphanesi – resmi siteden en son JAR'ı indirin: [Aspose.Note for Java download](https://releases.aspose.com/note/java/).  
3. Dönüştürmek istediğiniz mevcut bir **OneNote (.one)** dosyası (ör. `Sample1.one`).  

## Import Packages

İhtiyacımız olan sınıfları içe aktarın. Bu kod bloğu değişmeden kalır:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Set up Document Directory  
OneNote dosyanızın bulunduğu klasörü tanımlayın. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Load the OneNote Document  
`.one` dosyasını yükleyerek bir `Document` nesnesi oluşturun.

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **İpucu:** Daha sonra **onenote'u PDF'ye dönüştürmek** isterseniz, aynı `Document` örneğini farklı bir `SaveOptions` ile yeniden kullanabilirsiniz.

### Step 3: Initialize ImageSaveOptions  
Aspose.Note'a istediğiniz görüntü formatını söyleyin. Burada PNG seçiyoruz, ancak `SaveFormat.Jpeg` veya `SaveFormat.Bmp` de kullanılabilir.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

> Bu satır aynı zamanda ikincil anahtar kelime **convert onenote to png** ve **save onenote as png**'i de karşılar.

### Step 4: Save the Document as an Image  
OneNote sayfalarını PNG dosyası olarak dışa aktarın.

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

> `save` yöntemi, çok sayfalı belgeleri otomatik olarak her sayfa için ayrı görüntü dosyaları oluşturarak (ör. `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`, …) yönetir.

### Step 5: Print Confirmation  
Kullanıcıya çıktının nereye yazıldığını bildirin.

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

## Common Use Cases for save onenote as png

| Senaryo | Neden PNG? | Tipik İş Akışı |
|----------|------------|----------------|
| **Web makalesine not ekleme** | PNG, kayıpsız kalite ve geniş tarayıcı desteği sağlar. | Dönüştürün, ardından PNG'yi bir `<img>` etiketiyle ekleyin. |
| **Belge yönetim sistemi için küçük resim oluşturma** | Küçük dosya boyutu ve net metin render'ı. | Dönüştürün, ardından herhangi bir görüntü işleme kütüphanesiyle yeniden boyutlandırın. |
| **Uyumluluk için defterleri arşivleme** | PNG, statik ve düzenlenemez bir formattır. | Tüm `.one` dosyalarını toplu işleyin ve PNG'leri güvenli bir depoda saklayın. |

## Common Issues and Solutions

| Sorun | Sebep | Çözüm |
|-------|-------|------|
| **FileNotFoundException** | `dataDir` yolunun yanlış olması | Klasör yolunun bir eğik çizgi (`/` veya `\\`) ile bittiğini ve dosya adının doğru olduğunu doğrulayın. |
| **Unsupported format** | Kütüphane sürümü tarafından desteklenmeyen eski bir görüntü formatına kaydetmeye çalışmak | Aspose.Note'u en son sürüme güncelleyin veya desteklenen bir `SaveFormat` seçin. |
| **Large OneNote files cause OutOfMemoryError** | Yetersiz yığın alanı | JVM yığınını (`-Xmx2g`) artırın veya `Document.getPages()` döngüsüyle sayfaları tek tek işleyin. |

## Frequently Asked Questions

**S: Birden fazla OneNote dosyasını tek bir toplu işlemde dönüştürebilir miyim?**  
C: Evet. Dosya adları koleksiyonunda döngü oluşturup, her birini `new Document(...)` ile yükleyin ve kaydetme adımlarını tekrarlayın.

**S: Aspose.Note onenote'u PDF'ye dönüştürmeyi destekliyor mu?**  
C: Kesinlikle. `ImageSaveOptions` yerine `PdfSaveOptions` kullanarak **onenote'u pdf'ye dönüştürün**.

**S: PNG çıktısının çözünürlüğünü nasıl değiştirebilirim?**  
C: `save` çağırmadan önce `options.setResolutionX(int)` ve `options.setResolutionY(int)` değerlerini ayarlayın.

**S: OneNote'u JPEG gibi diğer görüntü formatlarına dönüştürmenin bir yolu var mı?**  
C: Evet, `ImageSaveOptions` yapıcısında `SaveFormat.Png` yerine `SaveFormat.Jpeg` veya `SaveFormat.Bmp` kullanın.

**S: Dönüşüm için internet bağlantısına ihtiyacım var mı?**  
C: Hayır. Aspose.Note tüm işlemleri yerel olarak gerçekleştirir; dış hizmetler çağrılmaz.

**S: Şifre korumalı OneNote dosyalarını nasıl ele alırım?**  
C: Şifreyi `Document` yapıcısına gönderin: `new Document(path, password)`.

## Conclusion

Bu basit adımları izleyerek, artık **Aspose.Note for Java** kullanarak **onenote'u png olarak kaydetmeyi** biliyorsunuz. Bu yetenek, web sitelerine not ekleme, yazdırılabilir varlıklar oluşturma veya defterlerinizi statik görüntüler olarak arşivleme gibi birçok senaryonun kapısını açar. PDF veya JPEG gibi diğer çıktı formatlarıyla denemeler yapmaktan çekinmeyin ve kodu daha büyük otomasyon hatlarına entegre edin.

---

**Son Güncelleme:** 2026-02-05  
**Test Edilen Sürüm:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
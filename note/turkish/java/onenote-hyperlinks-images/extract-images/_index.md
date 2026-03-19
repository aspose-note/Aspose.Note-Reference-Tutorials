---
date: 2026-03-19
description: Aspose.Note kütüphanesini kullanarak Java ile OneNote görüntülerini nasıl
  çıkaracağınızı öğrenin. Bu adım adım kılavuz, .one dosyalarından görüntüleri hızlı
  ve güvenilir bir şekilde nasıl çıkaracağınızı gösterir.
linktitle: extract onenote images java – Extract Images from OneNote
second_title: Aspose.Note Java API
title: OneNote Görsellerini Java ile Çıkarma – OneNote'tan Görselleri Çıkar
url: /tr/java/onenote-hyperlinks-images/extract-images/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# extract onenote images java – Java kullanarak OneNote Belgesinden Görselleri Nasıl Çıkarılır

## Giriş

Bu öğreticide **how to extract onenote images java** konusunu Aspose.Note for Java kütüphanesi ile keşfedeceksiniz. Görselleri raporlama, arşivleme ya da bir OCR hattına besleme ihtiyacınız olsun, size tüm iş akışını adım adım göstereceğiz — bir `.one` defteri yüklemekten her resmi diske ayrı bir dosya olarak kaydetmeye kadar.

## Hızlı Yanıtlar
- **Önerilen kütüphane nedir?** Aspose.Note for Java  
- **Şifre korumalı bir defterden görselleri çıkarabilir miyim?** Evet, Aspose.Note bunu destekler.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim için lisans gereklidir.  
- **Hangi Java sürümleri destekleniyor?** Java 8 ve üzeri (Java 15 dahil).  
- **Çıkarma işlemi ne kadar sürer?** Standart bir defter için genellikle birkaç saniye.  

## **extract images from .one** nedir?

OneNote dosyasından görselleri çıkarmak, bir `.one` defterine gömülü tüm resimleri programlı olarak bulmak ve her birini ayrı bir görüntü dosyası (PNG, JPEG, GIF vb.) olarak yazmak anlamına gelir. Bu, grafiklerinizi OneNote ortamı dışına yeniden kullanmak istediğinizde kullanışlıdır.

## Java kullanarak OneNote görsellerini neden çıkarmalısınız?

- **Otomasyon:** Elle tıklamaya gerek kalmadan onlarca ya da yüzlerce defteri işleyin.  
- **Tutarlılık:** Tüm dosyalarda aynı çıkarma mantığını garanti eder.  
- **Entegrasyon:** Çıktıyı OCR, görüntü analizi veya içerik yönetim sistemleri gibi diğer Java tabanlı iş akışlarına kolayca bağlayabilirsiniz.  

## Önkoşullar

Başlamadan önce aşağıdaki öğelerin hazır olduğundan emin olun:

1. **Java Development Kit (JDK)** – Java 8 veya daha yenisini kurun. [website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) adresinden indirebilirsiniz.  
2. **Aspose.Note Library** – En son Aspose.Note for Java paketini indirin ve projenizin sınıf yoluna ekleyin. [download link](https://releases.aspose.com/note/java/) adresinden temin edebilirsiniz.  

## Paketleri İçe Aktarma

Başlamak için gerekli Java sınıflarını içe aktarın:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Adım 1: OneNote Belgesini Yükleyin

İlk olarak, API'yi `.one` dosyanızı içeren klasöre yönlendirin ve defteri yükleyin:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Adım 2: Tüm Görselleri Alın

Aspose.Note'tan belgede bulunan her `Image` düğümünü isteyin. Bu, **extract onenote images java** sürecinin çekirdeğidir:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Adım 3: Her Görseli Diske Kaydedin

Koleksiyonu döngüyle gezerek ham baytları alın ve her resmi benzersiz bir isimle dosyaya yazın:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

### Arka Planda Ne Oluyor?

- `image.getBytes()` orijinal görüntü verisini (PNG, JPEG, GIF vb.) döndürür.  
- `image.getFileName()` orijinal ismi korur, kaynağı izlemeyi kolaylaştırır.  

## Yaygın Sorunlar ve Çözümler
- **Görsel bulunamadı:** Kaynak `.one` dosyasının gömülü resimler içerdiğini doğrulayın.  
- **Dosya izin hataları:** `dataDir` klasörünün Java süreci tarafından yazılabilir olduğundan emin olun.  
- **Desteklenmeyen görüntü formatları:** Aspose.Note PNG, JPEG, GIF, BMP ve TIFF'i işler. Daha egzotik formatlar için önce OneNote'ta defteri dönüştürmeyi düşünün.  

## Sıkça Sorulan Sorular

**S: Şifre korumalı OneNote belgelerinden görselleri çıkarabilir miyim?**  
C: Evet, Aspose.Note şifreli defterleri açmayı ve görsellerini çıkarmayı destekler.

**S: Aspose.Note farklı Java sürümleriyle uyumlu mu?**  
C: Kütüphane Java 8 ve üzeriyle çalışır, bu yüzden Java 11, Java 15 veya daha yeni sürümlerde çalıştırabilirsiniz.

**S: Tek bir çalıştırmada birden fazla OneNote dosyasından görselleri çıkarabilir miyim?**  
C: Kesinlikle. Çıkarma mantığını `.one` dosya yollarının listesi üzerinde dönen bir döngüye yerleştirmeniz yeterlidir.

**S: İşleyebileceğim defterlerin boyutunda bir sınırlama var mı?**  
C: Aspose.Note büyük defterleri verimli bir şekilde işler; görüntü çıkarma için sabit bir boyut sınırı yoktur.

**S: Aspose.Note başka içerik türlerini de çıkarmaya izin veriyor mu?**  
C: Evet, benzer API'ler kullanarak metin, tablolar, gömülü dosyalar ve diğer nesneleri de çıkarabilirsiniz.

---

**Son Güncelleme:** 2026-03-19  
**Test Edilen:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
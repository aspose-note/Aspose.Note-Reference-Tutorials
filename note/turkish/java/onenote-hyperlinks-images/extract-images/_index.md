---
date: 2025-12-21
description: Java ve Aspose.Note kullanarak OneNote belgelerinden resimleri nasıl
  çıkaracağınızı öğrenin. Bu adım adım kılavuz, resimleri hızlı ve güvenilir bir şekilde
  nasıl çıkaracağınızı gösterir.
linktitle: How to Extract Images from OneNote Document using Java
second_title: Aspose.Note Java API
title: Java Kullanarak OneNote Belgesinden Görselleri Nasıl Çıkarabilirsiniz
url: /tr/java/onenote-hyperlinks-images/extract-images/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Belgesinden Görüntüleri Java ile Nasıl Çıkarılır

## Giriş

Bu öğreticide, Aspose.Note kütüphanesinin yardımıyla Java kullanarak bir OneNote belgesinden **görüntüleri nasıl çıkaracağınızı** adım adım göstereceğiz. Görselleri raporlama, arşivleme veya daha ileri işlemeler için ihtiyacınız olsun, bu rehber tüm süreci size anlatacaktır.

## Hızlı Yanıtlar
- **Önerilen kütüphane nedir?** Aspose.Note for Java  
- **Şifre korumalı bir defterden görüntü çıkarabilir miyim?** Evet, Aspose.Note bunu destekler.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü çalışır; üretim için lisans gereklidir.  
- **Hangi Java sürümleri destekleniyor?** Java 8 ve üzeri (Java 15 dahil).  
- **Çıkarma işlemi ne kadar sürer?** Standart bir defter için genellikle birkaç saniye.

## OneNote'tan görüntü çıkarma nedir?
Görüntü çıkarmak, bir OneNote (.one) dosyasına gömülmüş tüm resimleri programlı olarak bulmak ve her birini diskte ayrı bir görüntü dosyası olarak kaydetmek anlamına gelir. Bu, grafiklerinizi defter ortamının dışına yeniden kullanmak istediğinizde faydalıdır.

## Neden OneNote'tan Java ile görüntü çıkarılmalı?
- **Otomasyon:** Birçok defteri manuel çaba harcamadan toplu işleyin.  
- **Tutarlılık:** Tüm dosyalarda aynı çıkarma mantığını garanti eder.  
- **Entegrasyon:** Diğer Java tabanlı iş akışlarıyla (ör. OCR, görüntü analizi) kolayca birleştirilebilir.  

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – Sisteminizde Java yüklü olduğundan emin olun. [website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) adresinden indirebilirsiniz.

2. **Aspose.Note Library** – Aspose.Note kütüphanesini indirin ve Java projenize ekleyin. [download link](https://releases.aspose.com/note/java/) adresinden temin edebilirsiniz.

## Paketleri İçe Aktarma

Başlamak için gerekli paketleri içe aktarın:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Adım 1: Belgeyi Yükleme

İlk olarak, Aspose.Note kullanarak OneNote belgesini yükleyin:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Adım 2: Tüm Görüntüleri Al

Sonra, belgedeki tüm görüntüleri alın:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Adım 3: Görüntüleri Çıkarma

Görüntü listesini döngüyle gezerek her birini dosyaya kaydedin:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Yaygın Sorunlar ve Çözümler
- **Görüntü bulunamadı:** Kaynak `.one` dosyasının gömülü resimler içerdiğinden emin olun.  
- **Dosya izin hataları:** `dataDir` yolunun yazılabilir olduğunu doğrulayın.  
- **Desteklenmeyen görüntü formatları:** Aspose.Note çoğu yaygın formatı (PNG, JPEG, GIF) işler. Bir format desteklenmiyorsa, önce OneNote'ta defteri dönüştürmeyi düşünün.

## Sonuç

Yukarıdaki adımları izleyerek, artık Java ve Aspose.Note kütüphanesini kullanarak bir OneNote belgesinden **görüntüleri nasıl çıkaracağınızı** biliyorsunuz. Bu mantığı daha büyük uygulamalara entegre edebilir, toplu işleme otomasyonu sağlayabilir veya sadece grafikleri yeniden kullanım için alabilirsiniz.

## Sıkça Sorulan Sorular

**Q: Şifre korumalı OneNote belgelerinden görüntü çıkarabilir miyim?**  
A: Evet, Aspose.Note şifre korumalı defterlerden görüntü çıkarmayı destekler.

**Q: Aspose.Note farklı Java sürümleriyle uyumlu mu?**  
A: Aspose.Note Java 8 ve üzeri sürümlerle çalışır, böylece ortamlar arasında esneklik sağlar.

**Q: Tek bir çalıştırmada birden fazla OneNote belgesinden görüntü çıkarabilir miyim?**  
A: Kesinlikle. Dosya yolu listesini döngüyle işleyerek aynı çıkarma mantığını her belgeye uygulayabilirsiniz.

**Q: OneNote belgeleri için boyut sınırlamaları var mı?**  
A: Aspose.Note büyük defterleri verimli bir şekilde işler; görüntü çıkarma için katı bir boyut sınırı yoktur.

**Q: Aspose.Note yalnızca görüntüler dışında başka içerik türlerini çıkarmayı destekliyor mu?**  
A: Evet, aynı zamanda metin, ekler ve diğer gömülü nesneleri de çıkarabilirsiniz.

---

**Son Güncelleme:** 2025-12-21  
**Test Edilen Sürüm:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
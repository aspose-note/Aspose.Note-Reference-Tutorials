---
date: 2025-12-05
description: Aspose.Note for Java kullanarak OneNote'u PDF'ye nasıl dönüştüreceğinizi
  ve OneNote'u PDF olarak nasıl kaydedeceğinizi öğrenin. PdfSaveOptions ile belge
  dönüştürme görevlerinizi basitleştirin.
linktitle: Load OneNote Document into Aspose.Note using PdfSaveOptions
second_title: Aspose.Note Java API
title: Aspose.Note ve PdfSaveOptions Kullanarak OneNote'u PDF'ye Dönüştür
url: /tr/java/onenote-document-loading/load-pdf-save-options/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note ve PdfSaveOptions ile OneNote'u PDF'ye Dönüştürme

## Giriş

Bu kapsamlı rehberde, Aspose.Note for Java kullanarak **OneNote'u PDF'ye nasıl dönüştüreceğinizi** öğreneceksiniz. OneNote dosyasını yükleme, dönüşümü yapılandırma ve son olarak sonucu PDF olarak kaydetme adımlarını birlikte inceleyeceğiz. Eğitim sonunda, bu iş akışını kendi Java uygulamalarınıza entegre etmekte rahat olacaksınız.

## Hızlı Yanıtlar
- **Dönüşümü hangi kütüphane yönetir?** Aspose.Note for Java with `PdfSaveOptions`.
- **Temel uygulama ne kadar sürer?** Çalışan bir prototip için yaklaşık 5‑10 dakika.
- **Üretim için lisansa ihtiyacım var mı?** Evet, ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.
- **PDF çıktısını özelleştirebilir miyim?** Kesinlikle – `PdfSaveOptions` sayfa boyutu, kenar boşlukları ve daha fazlasını ayarlamanıza izin verir.
- **Desteklenen OneNote formatları?** Hem `.one` hem de `.onepkg` dosyaları desteklenir.

## OneNote'u PDF'ye Dönüştürme – Giriş

Aspose.Note, Java'da Microsoft OneNote dosyalarıyla çalışmayı basitleştirir. Rapor oluşturmak, notları arşivlemek veya OneNote içeriğini daha büyük bir iş akışına entegre etmek isterken, bu dosyaları PDF'ye dönüştürmek genellikle ilk adımdır.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

### 1. Java Geliştirme Ortamı
Önerilen en yeni JDK (Java 17 veya üzeri). Oracle web sitesinden indirin veya OpenJDK kullanın.

### 2. Aspose.Note for Java Kütüphanesi
En son Aspose.Note for Java paketini [resmi indirme sayfasından](https://releases.aspose.com/note/java/) alın ve JAR'ı projenizin sınıf yoluna ekleyin.

### 3. Örnek OneNote Belgesi
Dönüştürmek istediğiniz bir `.one` veya `.onepkg` dosyası. Test için, öğreticide `Sample1.one` kullanılıyor.

## Paketleri İçe Aktarma

İhtiyacınız olan sınıfları ilk olarak içe aktarın. Bu içe aktarmalar, temel belge modeline ve PDF dönüşüm seçeneklerine erişim sağlar.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## OneNote'u PdfSaveOptions ile PDF Olarak Kaydet

Aşağıda süreci iki net adıma ayırıyoruz: kaynak dosyayı yüklemek ve PDF olarak kaydetmek. Her adım, **neden** yaptığımızı anlamanız için kısa bir açıklama içerir.

### Adım 1: OneNote Belgesini Yükle

`Document` örneğini, diskteki OneNote dosyasına işaret ederek oluşturuyoruz.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

*Why this matters:* Loading the file into a `Document` object gives you full programmatic control over its contents, allowing further manipulation before conversion if needed.

### Adım 2: Belgeyi PDF Olarak Kaydet

Şimdi `save` metodunu çağırıyoruz ve yeni bir `PdfSaveOptions` örneği gönderiyoruz. Bu, Aspose.Note'a OneNote sayfalarını PDF sayfaları olarak işleme talimatı verir.

```java
// Save the document as PDF
oneFile.save(dataDir + "LoadDocIntoAsposeNoteUsingPdfsaveoptions_out.pdf", new PdfSaveOptions());
```

*Tip:* **OneNote'u PDF olarak kaydetmek** istediğinizde özel ayarlar (ör. belirli sayfa boyutu veya görüntü sıkıştırması) kullanmak istiyorsanız, `save()`'a göndermeden önce `PdfSaveOptions` nesnesini yapılandırın.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Dosya bulunamadı** | Yanlış `dataDir` yolu | Dizin yolunu doğrulayın ve dosya adının tam olarak eşleştiğinden emin olun. |
| **Desteklenmeyen OneNote sürümü** | Çok eski bir `.one` dosyası kullanmak | Önce OneNote'ta dosyayı güncelleyin veya daha geniş uyumluluk sağlayan Aspose.Note'un en son sürümünü kullanın. |
| **PDF çıktısı boş görünüyor** | Sunucuda eksik yazı tipleri | Gerekli yazı tiplerini yükleyin veya `PdfSaveOptions.setEmbedStandardFonts(true)` ile gömün. |

## Sıkça Sorulan Sorular

**S: Aspose.Note tüm OneNote sürümleriyle uyumlu mu?**  
E: Evet, Aspose.Note son OneNote formatlarını destekler, `.one` ve `.onepkg` dahil. Daha eski dosyalar önce OneNote'ta açılıp yeniden kaydedilmesi gerekebilir.

**S: PDF çıktısını (sayfa boyutu, kenar boşlukları vb.) özelleştirebilir miyim?**  
E: Kesinlikle. `PdfSaveOptions`, sonucu ince ayar yapmak için `setPageSize()`, `setMarginTop()` ve `setImageCompression()` gibi özellikler sunar.

**S: Aspose.Note PDF dışındaki formatlara dönüşümü destekliyor mu?**  
E: Evet, ilgili kaydetme seçeneklerini kullanarak OneNote dosyalarını DOCX, HTML, JPEG, PNG ve daha fazlasına dönüştürebilirsiniz.

**S: Ücretsiz deneme sürümü mevcut mu?**  
E: Evet, tam işlevsel bir deneme sürümünü [Aspose.Note indirme sayfasından](https://releases.aspose.com/) indirebilirsiniz.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
E: Aspose topluluk forumu sorularınızı sormak için harika bir yerdir: [destek forumu](https://forum.aspose.com/c/note/28).

---

**Son Güncelleme:** 2025-12-05  
**Test Edilen Versiyon:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
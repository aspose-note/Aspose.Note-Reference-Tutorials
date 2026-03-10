---
date: 2025-12-18
description: Java'da Aspose.Note ile belirtilen yazı tipleri alt sistemini kullanarak
  **OneNote'u PDF olarak kaydetmeyi** öğrenin. Bu kılavuz ayrıca OneNote'u PDF'ye
  dönüştürmeyi, özel yazı tipi dosyalarını yüklemeyi ve varsayılan yazı tiplerini
  belirtmeyi gösterir.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Belirtilen Yazı Tipleri Alt Sistemiyle OneNote'u PDF Olarak Kaydet
url: /tr/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Belirtilen Yazı Tipi Alt Sistemini Kullanarak OneNote'u PDF Olarak Kaydet

## Giriş

## Hızlı Yanıtlar
- **“OneNote'u PDF olarak kaydetmek” ne anlama geliyor?** Bir .one dosyasını, düzeni ve stilini koruyarak PDF'ye dönüştürür.  
- **Hangi API yazı tiplerini yönetir?** `DocumentFontsSubsystem` size varsayılan bir yazı tipi tanımlama veya özel bir yazı tipi dosyası/akışı yükleme imkanı verir.  
- **Üretim için lisansa ihtiyacım var mı?** Evet, deneme dışı kullanım için ticari bir Aspose.Note lisansı gereklidir.  
- **Bir kerede birden fazla dosyayı dönüştürebilir miyim?** Kesinlikle – `Document` yükleme ve kaydetme mantığını döngü içinde çalıştırmanız yeterli.  
- **Hangi Java sürümü gerekiyor?** Java 15 veya üzeri (örnek JDK 15 kullanıyor).

## “Yazı Tipi Alt Sistemiyle OneNote'u PDF Olarak Kaydetmek” nedir?

Yazı tipi alt sistemiyle OneNote'u PDF olarak kaydetmek, dönüşüm sürecinde Aspose.Note'un eksik glifleri sağladığınız yazı tipiyle değiştirmesi anlamına gelir. Bu, orijinal yazı tipi yüklü olmasa bile PDF'nin her cihazda aynı görünmesini garanti eder.

## OneNote'u PDF'e dönüştürürken yazı tipi alt sistemini neden kontrol etmelisiniz?

- **Tutarlı marka kimliği** – kurumsal belgeler tam olarak aynı yazı tipini korur.  
- **Çapraz platform güvenilirliği** – PDF'ler Windows, macOS, Linux ve mobil cihazlarda aynı şekilde görüntülenir.  
- **Azaltılmış hatalar** – eksik yazı tipi uyarıları ortadan kalkar, temiz çıktı üretir.

## Ön Koşullar

### 1. Java Development Kit (JDK)

Sisteminizde Java Development Kit (JDK) yüklü olduğundan emin olun. Henüz yüklemediyseniz, [buradan](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) indirebilirsiniz.

### 2. Aspose.Note for Java Library

Aspose.Note for Java kütüphanesini indirin ve kurun. [web sitesinden](https://releases.aspose.com/note/java/) indirebilirsiniz.

## Paketleri İçe Aktarma

Make sure to import the necessary packages in your Java project:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Şimdi süreci daha iyi anlamak için her örneği birden fazla adıma ayıralım.

## Document Fonts Subsystem'i varsayılan bir yazı tipiyle kullanarak **OneNote'u PDF Olarak Kaydetme**

### Adım 1: Document Fonts Subsystem'i Varsayılan Yazı Tipi Adı ile Kaydetme

Bu adım, varsayılan bir yazı tipi adı belirterek **OneNote'u PDF olarak kaydetmenin** basit bir yolunu gösterir.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Bu adımda:
- OneNote belgesi Aspose.Note kullanılarak yüklenir.
- **Varsayılan yazı tipi**, **"Times New Roman"** olarak belirtilir.
- Belge, seçilen yazı tipiyle PDF formatında kaydedilir.

### Adım 2: Document Fonts Subsystem'i Dosyadan Varsayılan Yazı Tipi ile Kaydetme

Burada **özel bir yazı tipi dosyası** yüklenir ve PDF'ye dönüştürürken yedek olarak kullanılır.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Ana noktalar:
- **Özel yazı tipi dosyası** `geo_1.ttf` **diskten yüklenir**.
- `usingDefaultFontFromFile` **dosyadan varsayılan yazı tipini belirler**, orijinal yazı tipi eksik olduğunda PDF'nin bu yazı tipini kullanmasını sağlar.
- Ortaya çıkan PDF, istenen görünümü korur.

### Adım 3: Document Fonts Subsystem'i Akıştan Varsayılan Yazı Tipi ile Kaydetme

Bazen yazı tipi bir veritabanında saklanabilir veya ağ üzerinden alınabilir. Bu örnek, **yazı tipi akışı kullanmayı** gösterir.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Burada şu gerçekleşir:
- Yazı tipi dosyası bir **InputStream** olarak açılır; bu, yazı tipinin dosya dışı bir kaynağa ait olduğu durumlarda faydalıdır.
- `usingDefaultFontFromStream` **yazı tipi akışı** kullanarak yedek yazı tipini tanımlar.
- OneNote dosyası, akış tabanlı yazı tipiyle PDF olarak kaydedilir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Nasıl Çözülür |
|-------|--------------|---------------|
| **Eksik yazı tipi uyarıları** | Kaynak .one dosyası, makinede bulunmayan bir yazı tipine başvurur. | `usingDefaultFont`, `usingDefaultFontFromFile` veya `usingDefaultFontFromStream` aracılığıyla varsayılan bir yazı tipi sağlayın. |
| **Özel yazı tipi dosyası bulunamadı** | `.ttf` dosyasının yolu yanlış. | Mutlak yollar kullanın veya çalışma dizininden göreceli yolu doğrulayın. |
| **Akış kapatılmadı** | `close()` çağrılmadan önce bir istisna oluşur. | Otomatik kapatma için try‑with‑resources kullanın (`try (InputStream stream = ...) { ... }`). |

## Sıkça Sorulan Sorular

**S: Belgenin farklı bölümleri için farklı yazı tipleri belirleyebilir miyim?**  
C: Evet, Aspose.Note'taki `Font` sınıfını kullanarak bireysel zengin metin öğelerine özel yazı tipi ayarları uygulayabilirsiniz.

**S: Aspose.Note tüm OneNote sürümleriyle uyumlu mu?**  
C: Aspose.Note, son masaüstü ve mobil sürümlerinden OneNote dosyalarını destekler, geniş bir uyumluluk sağlar.

**S: Belgeleri kaydederken eksik yazı tiplerini nasıl ele alabilirim?**  
C: Yukarıda gösterilen yazı tipi alt sistemi yöntemlerini (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) kullanarak bir yedek sağlayabilirsiniz.

**S: Yazı tipi özelliklerini, örneğin boyut ve stil gibi, özelleştirebilir miyim?**  
C: Kesinlikle – API, bir koşul (run) bazında boyut, stil, renk ve diğer nitelikleri ayarlamanıza izin verir.

**S: Aspose.Note for Java için bir deneme sürümü mevcut mu?**  
C: Evet, Aspose web sitesinden ücretsiz bir deneme sürümü indirilebilir.

## Sonuç

Bu öğreticide, Aspose.Note ile Java'da yazı tipi alt sistemini kontrol ederken **OneNote'u PDF olarak kaydetmeyi** öğrendik. Varsayılan bir yazı tipi adı belirleme, özel bir yazı tipi dosyası yükleme veya bir yazı tipi akışı kullanma gibi üç yaklaşımı izleyerek OneNote belgelerinizi dışa aktarırken veya kaydederken platformlar arasında tutarlı bir yazı tipi temsili garanti edebilirsiniz.

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
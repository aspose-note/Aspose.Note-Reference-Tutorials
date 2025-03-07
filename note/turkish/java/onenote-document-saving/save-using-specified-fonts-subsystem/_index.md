---
title: OneNote'ta Belirtilen Yazı Tipleri Alt Sistemini Kullanarak Kaydetme
linktitle: OneNote'ta Belirtilen Yazı Tipleri Alt Sistemini Kullanarak Kaydetme
second_title: Aspose.Note Java API'si
description: Aspose.Note ile Java'da belirtilen yazı tipi alt sistemini kullanarak OneNote belgelerini nasıl kaydedeceğinizi öğrenin. Platformlar arasında tutarlı yazı tipi gösterimini zahmetsizce sağlayın.
weight: 22
url: /tr/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Belirtilen Yazı Tipleri Alt Sistemini Kullanarak Kaydetme

## giriiş

Aspose.Note for Java, OneNote belgeleriyle çalışmak için güçlü yetenekler sağlar. Bu tür belgelerle çalışırken ortak gereksinimlerden biri, özellikle belge PDF gibi farklı formatlarda dışa aktarılacak veya kaydedilecekse, yazı tiplerinin düzgün şekilde korunmasını sağlamaktır. Bu eğitim, yazı tipi alt sistemini belirlerken OneNote belgelerini kaydetme sürecinde size rehberlik edecek ve metnin çeşitli platformlarda tutarlı ve doğru şekilde temsil edilmesini sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulları oluşturduğunuzdan emin olun:

### 1. Java Geliştirme Kiti (JDK)

 Sisteminizde Java Development Kit'in (JDK) kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Burada](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) eğer henüz yapmadıysanız.

### 2. Java Kütüphanesi için Aspose.Note

 Aspose.Note for Java kütüphanesini indirin ve kurun. adresinden indirebilirsiniz.[İnternet sitesi](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Gerekli paketleri Java projenize aktardığınızdan emin olun:

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

## 1. Adım: Varsayılan Yazı Tipi Adıyla Belge Yazı Tipleri Alt Sistemini Kullanarak Kaydetme

Bu adım, belirli bir varsayılan yazı tipi adını kullanarak bir belgenin PDF formatında nasıl kaydedileceğini gösterir.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document("missing-font.one");

    // Varsayılan yazı tipini belirtin.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Belgeyi PDF olarak kaydedin.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Bu adımda:
- OneNote belgesi Aspose.Note kullanılarak yüklenir.
- Varsayılan yazı tipi "Times New Roman" olarak belirtilmiştir.
- Belge, belirtilen yazı tipiyle PDF formatında kaydedilir.

## Adım 2: Dosyadan Varsayılan Yazı Tipiyle Belge Yazı Tipleri Alt Sistemini Kullanarak Kaydetme

Bu adım, bir dosyadan yüklenen varsayılan yazı tipini kullanarak bir belgenin PDF formatında nasıl kaydedileceğini gösterir.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document("missing-font.one");

    // Yazı tipi dosyasının yolunu belirtin.
    String fontFile = "geo_1.ttf";

    // Dosyadan varsayılan yazı tipini belirtin.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Belgeyi PDF olarak kaydedin.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Bu adımda:
- "geo_1.ttf" yazı tipi dosyası yüklendi.
- Varsayılan yazı tipi, yüklenen yazı tipi dosyasından belirtilir.
- Belge, belirtilen yazı tipiyle PDF formatında kaydedilir.

## 3. Adım: Akıştan Varsayılan Yazı Tipiyle Belge Yazı Tipleri Alt Sistemini Kullanarak Kaydetme

Bu adım, bir akıştan yüklenen varsayılan yazı tipini kullanarak bir belgenin PDF formatında nasıl kaydedileceğini gösterir.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document("missing-font.one");

    // Yazı tipi dosyasının yolunu belirtin.
    String fontFile = "geo_1.ttf";

    // Yazı tipi dosyasını akış olarak yükleyin.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Akıştan varsayılan yazı tipini belirtin.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Belgeyi PDF olarak kaydedin.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Bu adımda:
- "geo_1.ttf" yazı tipi dosyası akış olarak yüklenir.
- Varsayılan yazı tipi, yüklenen akıştan belirtilir.
- Belge, belirtilen yazı tipiyle PDF formatında kaydedilir.

## Çözüm

Bu eğitimde, Aspose.Note'u kullanarak Java'da belirtilen yazı tipi alt sistemini kullanarak OneNote belgelerinin nasıl kaydedileceğini öğrendik. Bu adımları izleyerek belgelerinizi dışa aktarırken veya kaydederken çeşitli platformlarda tutarlı yazı tipi gösterimi sağlayabilirsiniz.

## SSS'ler

### S1: Belgenin farklı bölümleri için farklı yazı tipleri belirtebilir miyim?

Cevap1: Evet, Aspose.Note for Java'yı kullanarak belgenin farklı bölümleri için farklı yazı tipleri belirleyebilirsiniz.

### S2: Aspose.Note, OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note, OneNote'un çeşitli sürümlerini destekleyerek farklı ortamlar arasında uyumluluk sağlar.

### S3: Belgeleri kaydederken eksik yazı tiplerini nasıl halledebilirim?

Cevap3: Aspose.Note, belge kaydetme sırasında eksik yazı tiplerini etkili bir şekilde ele almak için varsayılan yazı tiplerini belirleme seçenekleri sunar.

### S4: Boyut ve stil gibi yazı tipi özelliklerini özelleştirebilir miyim?

Cevap4: Evet, Aspose.Note for Java'yı kullanarak boyut, stil ve renk gibi yazı tipi özelliklerini özelleştirebilirsiniz.

### S5: Aspose.Note for Java'nın deneme sürümü mevcut mu?

Cevap5: Evet, web sitesinden Aspose.Note for Java'nın ücretsiz deneme sürümünü edinebilirsiniz.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

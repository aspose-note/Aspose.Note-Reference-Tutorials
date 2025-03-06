---
title: OneNote'ta Görüntü Kaydetme Seçeneklerini Kullanarak TIFF Görüntüsüne Kaydetme
linktitle: OneNote'ta Görüntü Kaydetme Seçeneklerini Kullanarak TIFF Görüntüsüne Kaydetme
second_title: Aspose.Note Java API'si
description: OneNote belgelerini TIFF'e dönüştürün ve dosya boyutunu ve kalitesini kontrol edin! Java'da Jpeg, PackBits veya Faks sıkıştırmasını seçin. Kod örneklerini alın ve nasıl yapılacağını öğrenin! #OneNote #Java #Aspose
weight: 21
url: /tr/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Görüntü Kaydetme Seçeneklerini Kullanarak TIFF Görüntüsüne Kaydetme

## giriiş

Bu eğitimde, Aspose.Note for Java'da farklı sıkıştırma yöntemleri kullanarak bir belgeyi TIFF görüntü formatında nasıl kaydedeceğinizi öğreneceksiniz. Önkoşulları, içe aktarma paketlerini ele alacağız ve her sıkıştırma yöntemi için adım adım kılavuz sunacağız.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
- Aspose.Note for Java kütüphanesi indirildi ve yapılandırıldı.
- Java programlama dilinin temel anlayışı.

## Paketleri İçe Aktar

Öncelikle gerekli paketleri Java dosyanıza aktarmanız gerekir:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 1. Adım: JPEG Sıkıştırmasını Kullanarak TIFF'e Kaydetme

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Belgeler dizininin yolu.
    String dataDir = "Your Document Directory";

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Belgeyi kullanarak yükleyin`Document` sınıf.
-  Bir örneğini oluşturun`ImageSaveOptions` ve TIFF sıkıştırma türünü JPEG olarak belirtin.
- İstediğiniz kaliteyi ayarlayın (isteğe bağlı).
- Belirtilen seçenekleri kullanarak belgeyi TIFF formatında kaydedin.

## Adım 2: PackBits Sıkıştırmasını Kullanarak TIFF'e Kaydetme

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Belgeler dizininin yolu.
    String dataDir = "Your Document Directory";

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Belgeyi kullanarak yükleyin`Document` sınıf.
-  Bir örneğini oluşturun`ImageSaveOptions` ve TIFF sıkıştırma türünü PackBits olarak belirtin.
- Belirtilen seçenekleri kullanarak belgeyi TIFF formatında kaydedin.

## 3. Adım: CCITT Grup 3 Faks Sıkıştırmasını Kullanarak TIFF'e Kaydetme

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Belgeler dizininin yolu.
    String dataDir = "Your Document Directory";

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Belgeyi kullanarak yükleyin`Document` sınıf.
-  Bir örneğini oluşturun`ImageSaveOptions` ve TIFF sıkıştırma türünü CCITT Grup 3 Faks olarak belirtin.
- Renk modunu siyah beyaz olarak ayarlayın.
- Belirtilen seçenekleri kullanarak belgeyi TIFF formatında kaydedin.

## Çözüm

Bu eğitimde Aspose.Note for Java'da farklı sıkıştırma yöntemleri kullanarak bir belgeyi TIFF görüntü formatında nasıl kaydedeceğinizi öğrendiniz. Adım adım kılavuzu takip ederek gereksinimlerinizi karşılamak için Aspose.Note'un özelliklerinden verimli bir şekilde yararlanabilirsiniz.

## SSS'ler

### S1: Aspose.Note for Java'yı diğer belge formatlarını TIFF'e dönüştürmek için kullanabilir miyim?

Cevap1: Evet, Aspose.Note for Java, OneNote belgeleri de dahil olmak üzere çeşitli belge formatlarından TIFF'e dönüştürmeyi destekler.

### S2: TIFF'e kaydederken sıkıştırma türünü belirtmenin önemi nedir?

Cevap2: Sıkıştırma türünü belirlemek, görüntü kalitesini ve dosya boyutunu kontrol etmenize olanak tanır. Farklı sıkıştırma yöntemleri, kalite ve sıkıştırma oranı arasında dengeler sunar.

### S3: Aspose.Note for Java, belgelerin toplu işlenmesine uygun mudur?

C3: Evet, Aspose.Note for Java, toplu işleme için API'ler sağlayarak belge dönüştürme görevlerini verimli bir şekilde otomatikleştirmenize olanak tanır.

### S4: Sıkıştırma ayarlarını daha da özelleştirebilir miyim?

Cevap4: Evet, çıktıyı ihtiyaçlarınıza göre uyarlamak için kalite, çözünürlük ve sıkıştırma yöntemi gibi parametreleri ayarlayabilirsiniz.

### S5: Aspose.Note for Java teknik destek sunuyor mu?

C5: Evet, Aspose forumlar ve destek talebine dayalı sistemler aracılığıyla kapsamlı teknik destek sağlıyor.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

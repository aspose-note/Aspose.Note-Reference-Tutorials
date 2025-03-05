---
title: OneNote'ta Sayfa Ayarlarını Kullanarak PDF'ye Kaydetme - Aspose.Note
linktitle: OneNote'ta Sayfa Ayarlarını Kullanarak PDF'ye Kaydetme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note kitaplığını kullanarak OneNote belgelerini Java'da PDF'ye nasıl kaydedeceğinizi öğrenin. Farklı sayfa ayarlarına yönelik kod örnekleri içeren adım adım kılavuz.
type: docs
weight: 19
url: /tr/java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## giriiş

Bu eğitimde, Aspose.Note for Java ile farklı sayfa ayarlarını kullanarak OneNote belgelerini PDF formatında nasıl kaydedeceğimizi öğreneceğiz. İki yöntemi ele alacağız: Letter sayfa ayarlarıyla kaydetme ve yükseklik sınırı olmadan A4 sayfa ayarlarıyla kaydetme.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2. Aspose.Note for Java kütüphanesi indirildi ve Java projenize dahil edildi.
3. Java programlama dilinin temel anlayışı.

## Paketleri İçe Aktar

Aspose.Note for Java'yı projenizde kullanmak için gerekli paketleri içe aktardığınızdan emin olun. İşte ithalat beyanı:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Mektup Sayfası Ayarlarını Kullanarak PDF'ye Kaydetme

### 1. Adım: Belgeyi Yükleyin

Öncelikle OneNote belgesini Aspose.Note'a yükleyin:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Adım 2: Hedef Yolunu Tanımlayın

PDF dosyasının hedef yolunu belirtin:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### 3. Adım: Belgeyi Kaydedin

Belgeyi Letter sayfa ayarlarıyla kaydedin:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Yükseklik Sınırı Olmadan A4 Sayfa Ayarlarını Kullanarak PDF'ye Kaydetme

### 1. Adım: Belgeyi Yükleyin

Benzer şekilde OneNote belgesini Aspose.Note'a yükleyin:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Adım 2: Hedef Yolunu Tanımlayın

PDF dosyasının hedef yolunu belirtin:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### 3. Adım: Belgeyi Kaydedin

Belgeyi yükseklik sınırı olmadan A4 sayfa ayarlarıyla kaydedin:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Bu adımları izledikten sonra OneNote belgenizi farklı sayfa ayarlarını kullanarak başarıyla PDF'ye kaydetmiş olacaksınız.

## Çözüm

Bu eğitimde, Aspose.Note for Java kütüphanesini kullanarak OneNote belgelerinin PDF formatında nasıl kaydedileceğini araştırdık. Adım adım kılavuzu takip ederek bu işlevselliği Java uygulamalarınıza kolayca entegre edebilirsiniz.

## SSS'ler

### S1: Sayfa ayarlarını daha da özelleştirebilir miyim?

Cevap1: Evet, Aspose.Note for Java'yı kullanarak sayfa ayarlarını gereksinimlerinize göre özelleştirebilirsiniz.

### S2: Aspose.Note, PDF dışında diğer çıktı formatlarını da destekliyor mu?

Cevap2: Evet, Aspose.Note resimler ve HTML de dahil olmak üzere çeşitli çıktı formatlarını destekler.

### S3: Aspose.Note, OneNote dosyalarının farklı sürümleriyle uyumlu mudur?

Cevap3: Evet, Aspose.Note, .one ve .onetoc2 dahil olmak üzere farklı sürümlerdeki OneNote dosyalarını destekler.

### S4: Tek seferde birden fazla OneNote dosyasını PDF'ye dönüştürebilir miyim?

Cevap4: Evet, Aspose.Note for Java'yı kullanarak birden fazla OneNote dosyasını toplu olarak işleyebilirsiniz.

### S5: Test amaçlı herhangi bir deneme sürümü mevcut mu?

Cevap5: Evet, web sitesinden Aspose.Note for Java'nın ücretsiz deneme sürümünü edinebilirsiniz.
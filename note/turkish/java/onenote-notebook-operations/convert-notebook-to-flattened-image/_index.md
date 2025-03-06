---
title: OneNote'ta Not Defterini Düzleştirilmiş Görüntüye Dönüştürme - Aspose.Note
linktitle: OneNote'ta Not Defterini Düzleştirilmiş Görüntüye Dönüştürme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak bir not defterini OneNote'ta düzleştirilmiş bir görüntüye nasıl dönüştüreceğinizi öğrenin. Tüm öğeleri tek bir görüntü dosyasında zahmetsizce koruyun.
weight: 13
url: /tr/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Not Defterini Düzleştirilmiş Görüntüye Dönüştürme - Aspose.Note

## giriiş

Bu eğitimde, Aspose.Note for Java'yı kullanarak bir not defterini OneNote'ta düzleştirilmiş bir görüntüye dönüştürme sürecinde size rehberlik edeceğiz. Bu, not defterinizi bir görüntü dosyası olarak kaydetmenize olanak tanır ve tüm öğelerin tek bir görüntü formatında korunmasını sağlar.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2.  Aspose.Note for Java kütüphanesi indirildi ve Java projenize kuruldu. Kütüphaneyi adresinden indirebilirsiniz.[Burada](https://releases.aspose.com/note/java/).
3. Java programlamanın temel bilgisi.

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Aspose.Note for Java'dan içe aktarmanız gerekir:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 1. Adım: Belge Dizinini Ayarlayın

Öncelikle not defteri dosyanızın bulunduğu dizini tanımlayın:

```java
String dataDir = "Your Document Directory";
```

 Yer değiştirmek`"Your Document Directory"` not defteri dosyanızın yolu ile birlikte.

## 2. Adım: Not Defterini Yükleyin

 Daha sonra not defteri dosyasını kullanarak yükleyin.`Notebook` sınıf:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Değiştirildiğinden emin olun`"test.onetoc2"` not defteri dosyanızın adıyla.

## 3. Adım: Görüntü Kaydetme Seçeneklerini Ayarlayın

Şimdi not defterini resim olarak kaydetme seçeneklerini ayarlayın. Kayıt formatını PNG olarak belirleyip çözünürlüğü 400 DPI olarak ayarlayacağız:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Çözünürlüğü ihtiyaçlarınıza göre ayarlayabilirsiniz.

## Adım 4: Not Defterini Düzleştirin

Tüm öğelerin tek bir görüntüde düzleştirildiğinden emin olmak için`flatten` seçeneği`true`:

```java
saveOptions.setFlatten(true);
```

Bu, ortaya çıkan görüntünün dizüstü bilgisayarınızın düzenini korumasını sağlar.

## Adım 5: Resmi Kaydet

Son olarak not defterini düzleştirilmiş bir görüntü olarak kaydedin:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Yer değiştirmek`"ExportImageasFlattenedNotebook_out.png"` İstediğiniz çıktı dosyası adı ile.

## Çözüm

Sonuç olarak, Aspose.Note for Java'yı kullanarak not defterinizi OneNote'ta kolayca düzleştirilmiş bir görüntüye dönüştürebilirsiniz. Bu süreç, tüm öğelerin tek bir görüntü formatında korunmasını sağlayarak paylaşımı ve görüntülemeyi kolaylaştırır.

## SSS'ler

### S1: Çıktı görüntüsünün çözünürlüğünü ayarlayabilir miyim?

 A1: Evet, çözünürlüğü gereksinimlerinize göre değiştirerek ayarlayabilirsiniz.`setResolution` yöntem parametresi.

### S2: Aspose.Note dışa aktarma için diğer görüntü formatlarını destekliyor mu?

Cevap2: Evet, Aspose.Note not defterlerini dışa aktarmak için PNG, JPEG, BMP vb. gibi çeşitli görüntü formatlarını destekler.

### S3: Çıktı görüntüsünü daha da özelleştirebilir miyim?

Cevap3: Evet, Aspose.Note, sayfa boyutu, yönlendirme ve kalite ayarları da dahil olmak üzere çıktı görüntüsünü özelleştirmek için kapsamlı seçenekler sunar.

### S4: Aspose.Note for Java'nın deneme sürümü mevcut mu?

 Cevap4: Evet, adresinden ücretsiz deneme sürümünü edinebilirsiniz.[Burada](https://releases.aspose.com/).

### S5: Aspose.Note for Java desteğini nerede bulabilirim?

 Cevap5: Aspose.Note forumunda destek ve kaynak bulabilirsiniz[Burada](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

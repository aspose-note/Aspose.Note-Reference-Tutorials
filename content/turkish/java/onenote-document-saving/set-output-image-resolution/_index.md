---
title: OneNote'ta Çıktı Görüntüsü Çözünürlüğünü Ayarlama - Aspose.Note
linktitle: OneNote'ta Çıktı Görüntüsü Çözünürlüğünü Ayarlama - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote belgelerinde görüntü çözünürlüğünü nasıl ayarlayacağınızı öğrenin. Kolay uygulama için adım adım kılavuzumuzu izleyin
type: docs
weight: 23
url: /tr/java/onenote-document-saving/set-output-image-resolution/
---
## giriiş

OneNote belgelerinizdeki görsellerin çözünürlüğünü Java kullanarak değiştirmek mi istiyorsunuz? Aspose.Note for Java bu tür görevler için güçlü bir çözüm sunar. Bu eğitimde Aspose.Note'u kullanarak çıktı görüntü çözünürlüğünü ayarlama adımlarını inceleyeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Java Geliştirme Kiti (JDK): Sisteminize JDK'yı yükleyin.
2. Aspose.Note for Java: Aspose.Note for Java'yı şu adresten indirip yükleyin:[İnternet sitesi](https://releases.aspose.com/note/java/).
3. Entegre Geliştirme Ortamı (IDE): Eclipse veya IntelliJ IDEA gibi tercih ettiğiniz IDE'yi seçin.

## Paketleri İçe Aktar

Java projenizde gerekli Aspose.Note paketlerini içe aktarın:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 1. Adım: OneNote Belgesini Yükleyin

OneNote belgesini Java uygulamanıza yükleyerek başlayın:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Yer değiştirmek`"Your Document Directory"` OneNote belgenizin bulunduğu gerçek dizinle.

## 2. Adım: Görüntü Kaydetme Seçeneklerini Ayarlayın

Görüntü kaydetme seçeneklerini tanımlayın ve istediğiniz çözünürlüğü belirtin:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Burada çözünürlüğü şu şekilde ayarlıyoruz:`120 dpi`. Bu değeri ihtiyaçlarınıza göre ayarlayabilirsiniz.

## 3. Adım: Belgeyi Değiştirilmiş Çözünürlükle Kaydetme

Belgeyi güncellenmiş görüntü çözünürlüğüyle kaydedin:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Bu, değiştirilen belgeyi belirtilen çözünürlükte kaydedecektir.

## Çözüm

Bu eğitimde, Aspose.Note for Java kullanarak OneNote belgelerinde çıktı görüntü çözünürlüğünün nasıl ayarlanacağını araştırdık. Bu basit adımları izleyerek, uygulamanızın gereksinimlerini karşılamak için görüntülerin çözünürlüğünü etkili bir şekilde değiştirebilirsiniz.


## SSS'ler

### S1: Görüntü çözünürlüğünü 120 dpi'den daha yüksek bir değere ayarlayabilir miyim?

Cevap1: Evet, çözünürlüğü ihtiyaçlarınıza göre istediğiniz herhangi bir değere ayarlayabilirsiniz.

### S2: Aspose.Note, JPEG'in yanı sıra diğer görüntü formatlarını da destekliyor mu?

Cevap2: Evet, Aspose.Note PNG, BMP, GIF vb. gibi çeşitli görüntü formatlarını destekler.

### S3: Aspose.Note Java'nın tüm sürümleriyle uyumlu mu?

Cevap3: Aspose.Note, Java 1.6 veya sonraki sürümlerle uyumludur.

### S4: Aspose.Note'u kullanarak OneNote belgelerindeki görsellerin diğer yönlerini değiştirebilir miyim?

Cevap4: Evet, Aspose.Note yeniden boyutlandırma, kırpma ve döndürme dahil olmak üzere görüntü işleme için kapsamlı özellikler sağlar.

### S5: Aspose.Note ile ilgili sorgular için nereden destek alabilirim?

 Cevap5: Aspose.Note topluluk forumundan yardım isteyebilirsiniz[Burada](https://forum.aspose.com/c/note/28).
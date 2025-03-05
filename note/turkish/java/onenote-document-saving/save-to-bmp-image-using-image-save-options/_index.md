---
title: OneNote'ta Görüntü Kaydetme Seçeneklerini Kullanarak BMP Görüntüsüne Kaydetme
linktitle: OneNote'ta Görüntü Kaydetme Seçeneklerini Kullanarak BMP Görüntüsüne Kaydetme
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote belgelerini programlı olarak BMP görüntülerine nasıl kaydedeceğinizi öğrenin. Kod örnekleri içeren adım adım kılavuz.
type: docs
weight: 16
url: /tr/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
---
## giriiş

Aspose.Note for Java, Java geliştiricilerinin Microsoft OneNote dosyalarıyla programlı olarak çalışmasını sağlayan güçlü bir kütüphanedir. Aspose.Note for Java ile OneNote belgelerini sorunsuz bir şekilde oluşturabilir, işleyebilir ve dönüştürebilirsiniz. Bu eğitimde, Aspose.Note for Java tarafından sağlanan Görüntü Kaydetme Seçeneklerini kullanarak bir OneNote belgesinin bir BMP görüntüsüne nasıl kaydedileceğini inceleyeceğiz.

## Önkoşullar

Bu eğitime devam etmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Java programlama dili hakkında temel bilgiler.
2. Sisteminize JDK (Java Development Kit) kuruldu.
3. Eclipse veya IntelliJ IDEA gibi Entegre Geliştirme Ortamı (IDE).
4.  Aspose.Note for Java kütüphanesi. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Öncelikle Aspose.Note for Java'nın işlevselliklerini kullanabilmek için gerekli paketleri içe aktarmanız gerekiyor. Aşağıdaki import ifadesini Java dosyanıza ekleyin:

```java
import com.aspose.note.*;
import java.io.IOException;
```

Şimdi verilen örneği birden çok adıma ayıralım:

## 1. Adım: Belgeyi Yükleyin

```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";

// Belgeyi Aspose.Note'a yükleyin.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Bu adımda OneNote belgemizin bulunduğu dizinin yolunu belirtiyoruz. Daha sonra belgeyi kullanarak yüklüyoruz.`Document` Java için Aspose.Note tarafından sağlanan sınıf.

## Adım 2: BMP Görüntüsüne Kaydetme

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Belgeyi kaydedin.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

 Bu adımda OneNote belgesinden oluşturulacak BMP imajının çıktı yolunu belirtiyoruz. biz kullanıyoruz`save` yöntemi`Document` belgeyi bir BMP görüntüsü olarak kaydetmek için sınıf, çıktı yolunu ve bir örneğini sağlayarak`ImageSaveOptions` istenilen ile`SaveFormat` (bu durumda,`SaveFormat.Bmp`).

## Çözüm

Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote belgesini BMP görüntüsüne nasıl kaydedeceğimizi öğrendik. Adım adım kılavuzu izleyerek, bu işlevselliği Java uygulamalarınıza sorunsuz bir şekilde entegre edebilir ve OneNote belgelerini kolaylıkla yönetebilmenizi sağlayabilirsiniz.

## SSS'ler

### S1: OneNote belgelerini BMP'nin yanı sıra diğer görüntü formatlarına da kaydedebilir miyim?

Cevap1: Evet, Aspose.Note for Java'yı kullanarak OneNote belgelerini JPEG, PNG, GIF ve TIFF gibi çeşitli görüntü formatlarında kaydedebilirsiniz.

### S2: Aspose.Note for Java, farklı belge formatları arasında dönüştürmeyi destekliyor mu?

C2: Evet, Aspose.Note for Java, OneNote belgeleri ile PDF, DOCX, HTML ve daha fazlası gibi diğer formatlar arasında dönüştürmeyi destekler.

### S3: Aspose.Note for Java, OneNote'un en son sürümleriyle uyumlu mu?

C3: Evet, Aspose.Note for Java, OneNote'un en son sürümleriyle uyumluluğun sağlanması amacıyla düzenli olarak güncellenmektedir.

### S4: Aspose.Note for Java'yı kullanarak OneNote belgelerinin içeriğini programlı olarak değiştirebilir miyim?

Cevap4: Evet, Aspose.Note for Java'yı kullanarak OneNote belgelerinin içeriğini, yapısını ve formatını programlı olarak değiştirebilirsiniz.

### S5: Aspose.Note for Java teknik destek sağlıyor mu?

 C5: Evet, Aspose ürünleri için teknik destek sağlıyor. Ziyaret edebilirsiniz[Aspose.Note forumu](https://forum.aspose.com/c/note/28) yardım için.
---
title: OneNote'ta Kaydetme Formatını Kullanarak JPEG Görüntüsüne Kaydetme
linktitle: OneNote'ta Kaydetme Formatını Kullanarak JPEG Görüntüsüne Kaydetme
second_title: Aspose.Note Java API'si
description: OneNote belgesini kolayca JPEG görüntüsüne dönüştürün! Bu Java eğitimi Aspose.Note'un nasıl kullanıldığını gösterir. Kod örnekleriyle dönüştürün ve otomatikleştirin! #OneNote #Java #Aspose
weight: 18
url: /tr/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Kaydetme Formatını Kullanarak JPEG Görüntüsüne Kaydetme

## giriiş

Bu eğitimde, Aspose.Note for Java'yı kullanarak bir belgeyi JPEG görüntü formatında kaydetme sürecini ayrıntılı olarak ele alacağız. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan, dönüştürme, düzenleme ve içerik çıkarma gibi çeşitli işlemleri mümkün kılan güçlü bir Java API'sidir.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Java Geliştirme Ortamı: Sisteminizde Java Geliştirme Kitinin (JDK) kurulu olduğundan emin olun.
2.  Aspose.Note for Java Kütüphanesi: Aspose.Note for Java kütüphanesini indirin ve yükleyin. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Öncelikle Java kodumuz için gerekli olan paketleri import edelim:

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 1. Adım: Belgeyi Yükleyin

 İlk adım belgeyi Aspose.Note'a yüklemektir. Bu, aşağıdakiler kullanılarak gerçekleştirilebilir:`Document` Aspose.Note tarafından sağlanan sınıf.

```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";

// Belgeyi Aspose.Note'a yükleyin.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2. Adım: JPEG Görüntüsü olarak kaydedin

 Daha sonra çıktı dosyası yolunu belirleyeceğiz ve belgeyi JPEG resim formatında kaydedeceğiz.`save()` yöntemiyle birlikte`SaveFormat.Jpeg` parametre.

```java
// Çıkış dosyası yolunu belirtin.
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// Belgeyi kaydedin.
oneFile.save(dataDir, SaveFormat.Jpeg);
```

## Çözüm

Bu eğitimde Aspose.Note for Java kullanarak bir belgeyi JPEG görüntüsü olarak nasıl kaydedeceğimizi öğrendik. Verilen adımları izleyerek OneNote dosyalarınızı programlı olarak sorunsuz bir şekilde JPEG formatına dönüştürebilir, Java uygulamalarınızda çeşitli entegrasyon ve otomasyon olanaklarını etkinleştirebilirsiniz.

## SSS'ler

### S1: Aspose.Note karmaşık OneNote dosyalarını işleyebilir mi?

Cevap1: Evet, Aspose.Note, karmaşık OneNote dosyalarını verimli bir şekilde işleyecek ve doğru dönüştürme ve manipülasyon sağlayacak şekilde tasarlanmıştır.

### S2: Aspose.Note for Java'nın deneme sürümü mevcut mu?

 Cevap2: Evet, Aspose.Note for Java'nın ücretsiz deneme sürümünü şu adresten edinebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.Note for Java desteğini nasıl alabilirim?

 Cevap3: Aspose.Note for Java için destek almak için şu adresi ziyaret edebilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28).

### S4: Aspose.Note for Java için geçici bir lisans satın alabilir miyim?

 Cevap4: Evet, adresinden geçici bir lisans satın alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.Note for Java'nın ayrıntılı belgelerini nerede bulabilirim?

Cevap5: Aspose.Note for Java'nın ayrıntılı belgelerini burada bulabilirsiniz[Burada](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

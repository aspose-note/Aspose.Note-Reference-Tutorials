---
title: OneNote Belgesini Yayına Kaydet - Aspose.Note
linktitle: OneNote Belgesini Yayına Kaydet - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote belgelerini bir akışa nasıl kaydedeceğinizi öğrenin. Java uygulamalarınızla verimli entegrasyon için adım adım eğitimimizi izleyin.
weight: 13
url: /tr/java/onenote-document-saving/save-onenote-document-to-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Belgesini Yayına Kaydet - Aspose.Note

## giriiş

OneNote belgelerini bir akışa kaydetmek için Aspose.Note for Java'yı kullanma eğitimimize hoş geldiniz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasını sağlayan güçlü bir Java kitaplığıdır. Bu eğitimde, Aspose.Note'u kullanarak bir OneNote belgesini bir akışa kaydetme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- Java programlamanın temel anlayışı.
- Sisteminizde JDK yüklü.
-  Aspose.Note for Java kütüphanesi indirildi ve projenize eklendi. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Öncelikle gerekli paketleri içe aktaralım:

```java
import java.io.ByteArrayOutputStream;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## 1. Adım: OneNote Belgesini Yükleyin

İlk adım OneNote belgesini Aspose.Note'a yüklemektir.

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## 2. Adım: Belgeyi Akışa Kaydetme

Daha sonra, yüklenen belgeyi bir akışa, bu durumda bir ByteArrayOutputStream'e kaydedeceğiz.

```java
ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
doc.save(dstStream, SaveFormat.Pdf);
```

## Çözüm

Bu eğitimde, OneNote belgesini bir akışa kaydetmek için Aspose.Note for Java'nın nasıl kullanılacağını öğrendik. Bu adımları izleyerek OneNote belge işlemeyi Java uygulamalarınıza verimli bir şekilde entegre edebilirsiniz.

## SSS'ler

### S1: OneNote belgesini PDF dışındaki formatlarda kaydedebilir miyim?

Cevap1: Evet, Aspose.Note, belgelerin DOCX, HTML, JPEG, PNG vb. gibi çeşitli formatlarda kaydedilmesini destekler. 

### S2: Aspose.Note for Java'nın ücretsiz deneme sürümü mevcut mu?

 C2: Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.Note ile ilgili daha fazla desteği nerede bulabilirim veya soru sorabilirim?

 Cevap3: Aspose.Note forumunu ziyaret edebilirsiniz[Burada](https://forum.aspose.com/c/note/28).

### S4: Aspose.Note for Java lisansını nasıl satın alabilirim?

 Cevap4: Şu adresten lisans satın alabilirsiniz:[Burada](https://purchase.aspose.com/buy).

### S5: Değerlendirme amacıyla geçici bir lisansa ihtiyacım var mı?

 Cevap5: Evet, adresinden geçici lisans alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

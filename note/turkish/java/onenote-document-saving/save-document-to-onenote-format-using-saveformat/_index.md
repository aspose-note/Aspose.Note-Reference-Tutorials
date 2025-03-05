---
title: SaveFormat'ı Kullanarak Belgeyi OneNote'a Kaydetme - Aspose.Note
linktitle: SaveFormat'ı Kullanarak Belgeyi OneNote'a Kaydetme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak belgeleri OneNote formatında nasıl kaydedeceğinizi öğrenin. Java uygulamalarınızla sorunsuz entegrasyon için bu adım adım öğreticiyi izleyin.
type: docs
weight: 12
url: /tr/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---
## giriiş

Aspose.Note for Java, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasını sağlayan güçlü bir kitaplıktır. SaveFormat'ı kullanarak bir belgeyi OneNote biçimine kaydetmek basit bir işlemdir. Bu eğitimde, bu görevi gerçekleştirmek için gereken adımları inceleyeceğiz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2.  Aspose.Note for Java kütüphanesi indirildi. Şu adresten alabilirsiniz:[Burada](https://releases.aspose.com/note/java/).
3. Java programlama dilinin temel anlayışı.

## Paketleri İçe Aktar

 Öncelikle gerekli paketleri Java projenize aktarmanız gerekir. Bu,`com.aspose.note` Aspose.Note işlevleriyle çalışmak için paket.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## 1. Adım: Belge Dizinini Ayarlayın

Belgenizin bulunduğu dizini ve çıktı dosyasını nereye kaydetmek istediğinizi tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Belgeyi Yükleyin

 Belgeyi kullanarak Java uygulamanıza yükleyin.`Document` Aspose.Note tarafından sağlanan sınıf.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## 3. Adım: Belgeyi OneNote Formatına Kaydetme

Yüklenen belgeyi kullanarak OneNote biçimine kaydedin.`save` yöntemi ve istenen çıktı dosyası formatının şu şekilde belirtilmesi:`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## Çözüm

Bu eğitimde Aspose.Note for Java'da SaveFormat'ı kullanarak bir belgeyi OneNote formatında nasıl kaydedeceğimizi öğrendik. Bu basit adımları izleyerek bu işlevselliği Java uygulamalarınıza sorunsuz bir şekilde entegre edebilirsiniz.

## SSS'ler

### S1: Aspose.Note for Java, Microsoft OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap1: Aspose.Note for Java, Microsoft OneNote'un çeşitli sürümlerini destekleyerek farklı ortamlar arasında uyumluluk sağlar.

### S2: Aspose.Note for Java'yı satın almadan önce deneyebilir miyim?

 Cevap2: Evet, Aspose.Note for Java'nın ücretsiz deneme sürümünü şu adresten indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.Note for Java belgelerini nerede bulabilirim?

 Cevap3: Aspose.Note for Java'nın ayrıntılı belgelerini burada bulabilirsiniz[Burada](https://reference.aspose.com/note/java/).

### S4: Aspose.Note for Java için nasıl teknik destek alabilirim?

 Cevap4: Teknik yardım ve destek için Aspose.Note forumunu ziyaret edebilirsiniz.[Burada](https://forum.aspose.com/c/note/28).

### S5: Aspose.Note for Java için geçici bir lisans seçeneği mevcut mu?

 Cevap5: Evet, Aspose.Note for Java için geçici bir lisansı şu adresten edinebilirsiniz:[Burada](https://purchase.aspose.com/temporary-license/).
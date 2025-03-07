---
title: Java kullanarak OneNote Belgesinden Görüntüleri Çıkarma
linktitle: Java kullanarak OneNote Belgesinden Görüntüleri Çıkarma
second_title: Aspose.Note Java API'si
description: Aspose.Note kitaplığıyla Java kullanarak OneNote belgelerinden görüntüleri nasıl çıkaracağınızı öğrenin. Sorunsuz görüntü ayıklama için adım adım kılavuzumuzu izleyin.
weight: 14
url: /tr/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java kullanarak OneNote Belgesinden Görüntüleri Çıkarma

## giriiş

Bu eğitimde, Aspose.Note kütüphanesinin yardımıyla Java kullanarak bir OneNote belgesinden resim çıkarma sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1.  Java Geliştirme Kiti (JDK): Sisteminizde Java'nın kurulu olduğundan emin olun. adresinden indirip kurabilirsiniz.[İnternet sitesi](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note Kütüphanesi: Aspose.Note kütüphanesini indirin ve Java projenize ekleyin. Şu adresten alabilirsiniz:[İndirme: {link](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri içe aktarın:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## 1. Adım: Belgeyi Yükleyin

Öncelikle Aspose.Note'u kullanarak OneNote belgesini yükleyin:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Adım 2: Tüm Görselleri Alın

Ardından belgedeki tüm görüntüleri alın:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## 3. Adım: Görüntüleri Çıkarın

Görüntü listesini yineleyin ve her görüntüyü bir dosyaya kaydedin:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Çözüm

Aspose.Note kütüphanesi ile Java kullanarak OneNote belgesinden görsellerin çıkarılması sorunsuz bir şekilde gerçekleştirilebilir. Bu eğitimde özetlenen adımları izleyerek, daha fazla işlem veya analiz için belgelerinizden görüntüleri zahmetsizce alabilirsiniz.

## SSS'ler

### S1: Parola korumalı OneNote belgelerinden resim çıkarabilir miyim?

Cevap1: Evet, Aspose.Note şifre korumalı belgelerden görsellerin çıkarılmasını da destekler.

### S2: Aspose.Note Java'nın farklı sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note, Java'nın çeşitli sürümleriyle uyumludur ve geliştiricilere esneklik sağlar.

### S3: Tek bir yürütmede birden çok OneNote belgesindeki görüntüleri çıkarabilir miyim?

Cevap3: Kesinlikle, Aspose.Note'u kullanarak birden fazla belgeyi yineleyebilir ve her birinden görüntü çıkarabilirsiniz.

### S4: OneNote belgeleri için herhangi bir boyut sınırlaması var mı?

Cevap4: Aspose.Note, çeşitli boyutlardaki belgeleri verimli bir şekilde işler ve görüntü çıkarma için belge boyutunda sınırlama olmamasını sağlar.

### S5: Aspose.Note görsellerin dışında diğer içerik türlerinin çıkarılmasını destekliyor mu?

Cevap5: Evet, Aspose.Note, resimlerin yanı sıra metin, ek ve diğer içerik türlerinin OneNote belgelerinden çıkarılmasına da olanak tanır.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

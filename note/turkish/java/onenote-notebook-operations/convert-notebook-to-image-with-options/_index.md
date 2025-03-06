---
title: OneNote'taki Seçeneklerle Not Defterini Görüntüye Dönüştürme - Aspose.Note
linktitle: OneNote'taki Seçeneklerle Not Defterini Görüntüye Dönüştürme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak bir Not Defterini seçeneklerle bir görüntüye nasıl dönüştüreceğinizi öğrenin. Java uygulamalarınızla sorunsuz entegrasyon için adım adım eğitimimizi izleyin.
weight: 14
url: /tr/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'taki Seçeneklerle Not Defterini Görüntüye Dönüştürme - Aspose.Note

## giriiş

Bu derste, Aspose.Note for Java'yı kullanarak bir Notebook'u çeşitli seçeneklerle bir görüntüye dönüştürme sürecini derinlemesine inceleyeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan ve Java uygulamalarına sorunsuz entegrasyon sağlayan güçlü bir Java API'sidir.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun.
2. Aspose.Note for Java JAR dosyaları: Aspose.Note for Java kütüphanesini şu adresten indirin:[Burada](https://releases.aspose.com/note/java/) ve bunu projenizin sınıf yoluna ekleyin.

## Paketleri İçe Aktar

Öncelikle Java uygulamamız için gerekli paketleri import edelim:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 1. Adım: Dizüstü Bilgisayarı Yükleyin

Başlamak için görüntüye dönüştürmek istediğimiz OneNote not defterini yüklememiz gerekiyor.

```java
String dataDir = "Your Document Directory";
// OneNote Not Defteri Yükleme
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## 2. Adım: Kaydetme Seçeneklerini Ayarlayın

Daha sonra, istenen format (PNG, JPEG vb.) ve çözünürlük de dahil olmak üzere görsel kaydetme seçeneklerini tanımlayacağız.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

## 3. Adım: Not Defterini Görüntü Olarak Kaydetme

Şimdi not defterini belirtilen seçeneklerle resim olarak kaydedeceğiz.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Not Defterini Kaydet
notebook.save(dataDir, notebookSaveOptions);
```

## Çözüm

Bu eğitimde Aspose.Note for Java'yı kullanarak bir Notebook'u çeşitli seçeneklerle bir görüntüye nasıl dönüştüreceğimizi öğrendik. Bu adımları izleyerek, bu işlevselliği Java uygulamalarınıza sorunsuz bir şekilde entegre edebilir, OneNote dosyalarını programlı olarak değiştirme olanaklarını açabilirsiniz.

## SSS'ler

### S1: Aspose.Note karmaşık OneNote dosyalarını işleyebilir mi?

Cevap1: Evet, Aspose.Note karmaşık OneNote dosyalarını verimli bir şekilde işleyebilir ve bunlar üzerinde programlı olarak çeşitli işlemler gerçekleştirmenize olanak tanır.

### S2: Aspose.Note for Java'nın mevcut projelere entegrasyonu kolay mı?

A2: Kesinlikle! Aspose.Note for Java, Java projelerinize entegre edilmesi kolay basit bir API sunarak zamandan ve emekten tasarruf etmenizi sağlar.

### S3: Dizüstü bilgisayarı dönüştürürken görüntü çıktısını özelleştirebilir miyim?

Cevap3: Evet, Aspose.Note çözünürlük, format ve daha fazlası gibi seçenekleri belirleyerek görüntü çıktısını özelleştirmenize olanak tanır.

### S4: Aspose.Note geliştiricilere destek sunuyor mu?

C4: Evet, Aspose, forumları ve belgeleri aracılığıyla geliştiricilere mükemmel destek sağlayarak sorunsuz entegrasyon ve sorun giderme sağlar.

### S5: Aspose.Note for Java'nın ücretsiz deneme sürümü mevcut mu?

 Cevap5: Evet, Aspose.Note for Java'nın ücretsiz deneme sürümünden şu adresten yararlanabilirsiniz:[Burada](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

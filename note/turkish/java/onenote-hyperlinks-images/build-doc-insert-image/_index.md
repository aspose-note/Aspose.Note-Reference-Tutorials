---
title: Java kullanarak OneNote'ta Belge Oluşturun ve Görüntü Ekleyin
linktitle: Java kullanarak OneNote'ta Belge Oluşturun ve Görüntü Ekleyin
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote belgeleri oluşturmayı ve resim eklemeyi öğrenin. Kusursuz entegrasyon için adım adım eğitim.
weight: 12
url: /tr/java/onenote-hyperlinks-images/build-doc-insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java kullanarak OneNote'ta Belge Oluşturun ve Görüntü Ekleyin

## giriiş

Bu eğitimde, OneNote belgeleri oluşturmak ve bunlara resim eklemek için Aspose.Note for Java'yı nasıl kullanacağımızı keşfedeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasını sağlayan güçlü bir Java API'sidir. Süreç boyunca size rehberlik etmek için her adımı ayrıntılı olarak ele alacağız.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun.
2.  Aspose.Note for Java kütüphanesi: Aspose.Note for Java kütüphanesini şuradan indirip yükleyin:[İnternet sitesi](https://releases.aspose.com/note/java/).
3. IDE (Entegre Geliştirme Ortamı): Kodlama için IntelliJ IDEA veya Eclipse gibi Java destekli herhangi bir IDE kullanın.

## Paketleri İçe Aktar

Gerekli paketleri Java kodunuza aktararak başlayın:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## 1. Adım: Belgeyi Ayarlayın

Öncelikle yeni bir OneNote belgesi oluşturun ve gerekli nesneleri başlatın:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 2. Adım: Anahattı Başlat

Belgenin taslağını ayarlayın ve öteleme özelliklerini belirtin:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## 3. Adım: Resim Ekle

Bir görsel yükleyin ve hizalamasını belirtin:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## 4. Adım: Anahat Öğesine Görüntü Ekleme

Resmi bir anahat öğesine ekleyin:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Adım 5: Anahat ve Sayfa Düğümleri Ekleme

Taslağı ve sayfa düğümlerini belgeye ekleyin:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Adım 6: Belgeyi Kaydet

Son olarak OneNote belgesini kaydedin:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Çözüm

Tebrikler! Aspose.Note for Java'yı kullanarak OneNote belgeleri oluşturmayı ve bunlara resim eklemeyi başarıyla öğrendiniz. Bu adımları izleyerek Java uygulamalarınızdaki OneNote dosyalarını verimli bir şekilde yönetebilir ve değiştirebilirsiniz.

## SSS'ler

### S1: Aspose.Note for Java belgelerini nerede bulabilirim?

 A1: Belgelere erişebilirsiniz[Burada](https://reference.aspose.com/note/java/).

### S2: Aspose.Note for Java'yı nasıl indirebilirim?

 Cevap2: Aspose.Note for Java'yı şu adresten indirebilirsiniz:[indirme sayfası](https://releases.aspose.com/note/java/).

### S3: Aspose.Note for Java'nın ücretsiz deneme sürümü mevcut mu?

 C3: Evet, ücretsiz deneme sürümünü alabilirsiniz.[İnternet sitesi](https://releases.aspose.com/).

### S4: Aspose.Note for Java desteğini nereden alabilirim?

 Cevap4: Destek için şu adresi ziyaret edin:[Aspose.Note forumu](https://forum.aspose.com/c/note/28).

### S5: Aspose.Note for Java için geçici bir lisans alabilir miyim?

 Cevap5: Evet, geçici lisans talep edebilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

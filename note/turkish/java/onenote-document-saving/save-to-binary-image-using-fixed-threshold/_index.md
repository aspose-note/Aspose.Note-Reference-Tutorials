---
title: OneNote'ta Sabit Eşiği Kullanarak İkili Görüntüye Kaydetme
linktitle: OneNote'ta Sabit Eşiği Kullanarak İkili Görüntüye Kaydetme
second_title: Aspose.Note Java API'si
description: Aspose.Note Java ile sabit eşiği kullanarak Microsoft OneNote belgelerini ikili görüntüler olarak zahmetsizce kaydedin. OneNote dosya işleme yeteneklerinizi yükseltin.
weight: 14
url: /tr/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Sabit Eşiği Kullanarak İkili Görüntüye Kaydetme

## giriiş

Aspose.Note for Java, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir API'dir. Bu eğitimde, bir belgenin sabit bir eşik kullanarak ikili görüntü olarak nasıl kaydedileceğini inceleyeceğiz. Bunu başarmak için aşağıdaki adımları izleyin.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2.  Aspose.Note for Java kütüphanesi indirildi. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).
3. Java programlamanın temel bilgisi.

## Paketleri İçe Aktar

Öncelikle gerekli paketleri Java dosyanıza aktarın.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 1. Adım: Belgeyi Yükleyin

Aspose.Note API'sini kullanarak OneNote belgesini yükleyin.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: İkilileştirme Seçeneklerini Ayarlayın

Belgeyi ikili görüntü olarak kaydetmek için ikilileştirme seçeneklerini tanımlayın.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## 3. Adım: Görüntü Kaydetme Seçeneklerini Ayarlayın

Renk modu ve ikilileştirme seçenekleri de dahil olmak üzere görüntü kaydetme seçeneklerini ayarlayın.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Adım 4: Belgeyi Kaydedin

Belgeyi belirtilen seçeneklerle ikili görüntü olarak kaydedin.

```java
oneFile.save(dataDir, options);
```

## Çözüm

Bu eğitimde Aspose.Note for Java'da sabit bir eşik kullanarak bir belgeyi ikili görüntü olarak nasıl kaydedeceğimizi öğrendik. Bu adımları izleyerek OneNote dosyalarını program aracılığıyla kolayca değiştirebilirsiniz.

## SSS'ler

### S1: İkilileştirme için eşik değerini ayarlayabilir miyim?

 A1: Evet, eşik değerini ihtiyaçlarınıza göre değiştirerek ayarlayabilirsiniz.`setBinarizationThreshold()` yöntem parametresi.

### S2: Aspose.Note for Java, Microsoft OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note for Java, Microsoft OneNote'un 2010, 2013 ve 2016 dahil olmak üzere çeşitli sürümlerini destekler.

### S3: İşlenebilecek belgelerin boyutunda herhangi bir sınırlama var mı?

Cevap3: Aspose.Note for Java'nın işlenebilecek belge boyutu konusunda herhangi bir sınırlaması yoktur, bu da büyük dosyaları verimli bir şekilde yönetmenize olanak tanır.

### S4: Birden fazla OneNote belgesini aynı anda dönüştürebilir miyim?

C4: Evet, her dosya üzerinde yineleyerek ve gerekli işlemleri uygulayarak birden fazla OneNote belgesini toplu olarak işleyebilirsiniz.

### S5: Aspose.Note for Java için teknik destek mevcut mu?

 A5: Evet, teknik destek şu adresten mevcuttur:[Aspose.Note forumu](https://forum.aspose.com/c/note/28)Soru sorabileceğiniz ve uzmanlardan yardım alabileceğiniz yer.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

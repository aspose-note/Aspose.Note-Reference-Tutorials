---
title: Java kullanarak OneNote'tan Görüntü Bilgisi Alma
linktitle: Java kullanarak OneNote'tan Görüntü Bilgisi Alma
second_title: Aspose.Note Java API'si
description: Java'daki OneNote belgelerinden görüntü bilgilerini çıkarın! Resim boyutlarını, dosya adlarını ve daha fazlasını alın. Kolay adımlar ve kod örnekleri dahildir. #OneNote #Java #Aspose
weight: 15
url: /tr/java/onenote-hyperlinks-images/get-image-info/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java kullanarak OneNote'tan Görüntü Bilgisi Alma

## giriiş

Java geliştirme alanında, çeşitli belge formatlarından bilgi çıkarmak yaygın bir görevdir. Popüler bir not alma platformu olan OneNote, genellikle metnin yanında resimler de içerir. Java kullanarak OneNote dosyalarından görüntü bilgilerini programlı bir şekilde almak, belge işleme iş akışlarını kolaylaştırabilir. Bu eğitimde Aspose.Note for Java kullanarak OneNote belgelerinden görüntü ayrıntılarının nasıl çıkarılacağını inceleyeceğiz.

## Önkoşullar

Uygulamaya geçmeden önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

### 1. Java Geliştirme Kiti (JDK)

Sisteminizde Java Development Kit'in (JDK) kurulu olduğundan emin olun. En son JDK'yı şuradan indirip yükleyebilirsiniz:[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Java Kütüphanesi için Aspose.Note

 Aspose.Note for Java kütüphanesini indirin ve projenize ekleyin. Kütüphaneyi adresinden temin edebilirsiniz.[indirme sayfası](https://releases.aspose.com/note/java/).

### 3. OneNote Belgesi

Görüntüleri içeren örnek bir OneNote belgesi hazırlayın. Bu belge, görüntü bilgilerini programlı olarak çıkarmak için kullanılacaktır.

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Aspose.Note for Java'dan içe aktarın:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Yukarıdaki kodu adım adım talimatlara ayıralım:

## 1. Adım: Belge Dizinini Ayarlayın

```java
String dataDir = "Your Document Directory";
```

 Yer değiştirmek`"Your Document Directory"` OneNote belgenizin yolu ile birlikte.

## Adım 2: Belgeyi Yükleyin

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Aspose.Note for Java kütüphanesini kullanarak OneNote belgesini yükleyin. Belgenize doğru yolu girdiğinizden emin olun.

## 3. Adım: Tüm Görselleri Alın

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Yüklenen OneNote belgesindeki tüm görüntüleri alın.

## Adım 4: Toplam Görüntü Sayısını Yazdırın

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Belgede bulunan toplam görüntü sayısını yazdırın.

## Adım 5: Görüntü Bilgilerini Geçirin ve Yazdırın

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Her bir görüntü için görüntü listesini ve genişlik, yükseklik, orijinal boyutlar, dosya adı ve son değiştirilme zamanı gibi yazdırma ayrıntılarını yineleyin.

## Çözüm

Bu eğitimde özetlenen adımları izleyerek, Aspose.Note for Java kütüphanesinin yardımıyla Java kullanarak OneNote belgelerinden görüntü bilgilerini etkili bir şekilde alabilirsiniz. Bu işlevselliği uygulamalarınıza entegre etmek, belge işlemeyle ilgili görevleri otomatikleştirerek verimliliği ve üretkenliği artırabilir.

## SSS'ler

### S1: Aspose.Note for Java, OneNote dışındaki diğer belge formatlarını işleyebilir mi?

Cevap1: Evet, Aspose.Note for Java; OneNote, PDF ve Microsoft Word gibi çeşitli belge formatlarını destekler.

### S2: Aspose.Note for Java hem kişisel hem de ticari kullanıma uygun mudur?

C2: Evet, Aspose.Note for Java'yı hem kişisel hem de ticari amaçlarla kullanabilirsiniz.

### S3: Aspose.Note for Java teknik destek sunuyor mu?

 C3: Evet, teknik desteğe aşağıdaki Aspose forumlarından ulaşılabilir:[Burada](https://forum.aspose.com/c/note/28).

### S4: Satın almadan önce Aspose.Note for Java'yı deneyebilir miyim?

 Cevap4: Evet, Java için Aspose.Note'nın ücretsiz deneme sürümünü şuradan keşfedebilirsiniz:[Aspose.Note for Java](https://releases.aspose.com/note/java/).

### S5: Aspose.Note for Java için nasıl geçici lisans alabilirim?
 
 Cevap 5: Şuradan geçici bir lisans alabilirsiniz:[Geçici lisans/](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

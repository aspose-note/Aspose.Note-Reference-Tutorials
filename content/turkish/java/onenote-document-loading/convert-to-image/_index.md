---
title: OneNote Belgesini Görüntüye Dönüştürme - Java
linktitle: OneNote Belgesini Görüntüye Dönüştürme - Java
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'u görüntüye dönüştürmeyi öğrenin. Kolay adımları izleyin, belgeyi yükleyin, seçenekleri başlatın ve PNG olarak kaydedin.
type: docs
weight: 14
url: /tr/java/onenote-document-loading/convert-to-image/
---
## giriiş

Bu eğitimde, OneNote belgesini görüntüye dönüştürmek için Aspose.Note for Java'yı kullanma sürecinde size rehberlik edeceğiz. Her adımı takip edilmesi kolay talimatlara ayıracağız.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2.  Aspose.Note for Java kütüphanesi. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktar

Öncelikle gerekli paketleri Java kodunuza aktarın:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Şimdi sağlanan örnek kodu birden çok adıma ayıralım:

## 1. Adım: Belge Dizinini Ayarlayın

OneNote belgenizin bulunduğu dizini tanımlayın:

```java
String dataDir = "Your Document Directory";
```

 Yer değiştirmek`"Your Document Directory"` OneNote belgenizin yolu ile birlikte.

## Adım 2: Belgeyi Yükleyin

OneNote belgesini Aspose.Note'a yükleyin:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Emin olmak`"Sample1.one"` OneNote belge dosyanızın adıyla eşleşir.

## 3. Adım: ImageSaveOptions'ı başlatın

 Başlat`ImageSaveOptions` kaydetme biçimini belirtmek için nesne:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Burada belgeyi PNG görüntüsü olarak kaydediyoruz. Gerekirse JPEG veya BMP gibi diğer formatları seçebilirsiniz.

## Adım 4: Belgeyi Görüntü Olarak Kaydetme

Yüklenen belgeyi resim olarak kaydedin:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Bu satır, belgeyi belirtilen seçeneklerle PNG görüntüsü olarak kaydeder.

## Adım 5: Onayı Yazdırın

Dosyanın kaydedildiğini onaylamak için bir mesaj yazdırın:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Bu satır, başarılı dönüştürme ve kaydedilen görüntü dosyasının konumu hakkında sizi bilgilendirir.

## Çözüm

Yukarıda özetlenen adımları izleyerek, Aspose.Note for Java'yı kullanarak bir OneNote belgesini zahmetsizce bir görüntüye dönüştürebilirsiniz. Java uygulamalarınızda belge dönüştürme işlemlerini gerçekleştirmenin basit ve etkili bir yoludur.

## SSS'ler

### S1: Tek seferde birden fazla OneNote belgesini dönüştürebilir miyim?

Cevap1: Evet, bir belge listesinde dolaşabilir ve her belge için dönüştürme işlemini gerçekleştirebilirsiniz.

### S2: Aspose.Note görsellerin dışında diğer çıktı formatlarını da destekliyor mu?

Cevap2: Evet, Aspose.Note PDF, HTML ve Microsoft Word formatları gibi çeşitli çıktı formatlarını destekler.

### S3: Aspose.Note, OneNote dosyalarının tüm sürümleriyle uyumlu mudur?

Cevap3: Aspose.Note, Microsoft OneNote'un farklı sürümlerinde oluşturulan OneNote dosyalarıyla uyumluluk sunar.

### S4: Çıktı görüntülerinin çözünürlüğünü özelleştirebilir miyim?

Cevap4: Evet, Aspose.Note'ta bulunan seçenekleri kullanarak çözünürlüğü ve diğer parametreleri ayarlayabilirsiniz.

### S5: Aspose.Note belge dönüştürme için internet bağlantısı gerektiriyor mu?

Cevap5: Hayır, Aspose.Note internet bağlantısına ihtiyaç duymadan yerel olarak çalışır.
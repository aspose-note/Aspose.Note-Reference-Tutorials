---
date: 2025-12-21
description: Aspose.Note kullanarak Java’da görüntü boyutlarını nasıl alacağınızı
  öğrenin. OneNote dosyalarından sadece birkaç adımda genişlik, yükseklik, dosya adı
  ve daha fazlasını çıkarın.
linktitle: Get Image Dimensions Java from OneNote
second_title: Aspose.Note Java API
title: OneNote'tan Java ile Görüntü Boyutlarını Al
url: /tr/java/onenote-hyperlinks-images/get-image-info/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'tan Java ile Görüntü Boyutlarını Al

## Giriş

OneNote defterlerinden **get image dimensions java** almanız gerekiyorsa, doğru yerdesiniz. Birçok otomasyon senaryosunda—rapor oluşturma, içerik taşıma veya analiz—her resmin genişliğini, yüksekliğini, orijinal boyutunu ve dosya adını defteri manuel olarak açmadan bilmek istersiniz. Bu öğretici, bu bilgileri Aspose.Note for Java kullanarak programlı bir şekilde çıkarmanıza rehberlik eder.

## Hızlı Yanıtlar
- **Kod ne yapıyor?** Bir OneNote dosyasındaki tüm görüntüleri alır ve boyutlarını, orijinal boyutunu, dosya adını ve değiştirilme tarihini yazdırır.  
- **Hangi kütüphane gerekli?** Aspose.Note for Java.  
- **Lisans gerekir mi?** Test için geçici bir lisans çalışır; üretim için tam lisans gereklidir.  
- **Kaç satır kod?** Yaklaşık 30 satır, net, yeniden kullanılabilir adımlara bölünmüş.  
- **Tipik çalışma süresi?** Birkaç düzine görüntülü standart bir defter için milisaniyeler.

## Önkoşullar

Uygulamaya geçmeden önce, aşağıdaki önkoşulların karşılandığından emin olun:

### 1. Java Development Kit (JDK)

Sisteminizde Java Development Kit (JDK) yüklü olduğundan emin olun. En son JDK'yı [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) indirebilir ve kurabilirsiniz.

### 2. Aspose.Note for Java Kütüphanesi

Aspose.Note for Java kütüphanesini projenize indirin ve ekleyin. Kütüphaneyi [indirme sayfasından](https://releases.aspose.com/note/java/) edinebilirsiniz.

### 3. OneNote Belgesi

Görüntüler içeren örnek bir OneNote belgesi hazırlayın. Bu belge, görüntü bilgilerini programlı olarak çıkarmak için kullanılacak.

## Paketleri İçe Aktarın

Başlamak için, Aspose.Note for Java'dan gerekli paketleri içe aktarın:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Yukarıdaki kodu adım adım talimatlara ayıralım:

## OneNote'tan Java ile görüntü boyutlarını nasıl alırsınız

### Adım 1: Belge Dizini Ayarla

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini OneNote belgenizin yoluyla değiştirin.

### Adım 2: Belgeyi Yükle

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Aspose.Note for Java kütüphanesini kullanarak OneNote belgesini yükleyin. Belgenizin doğru yolunu sağladığınızdan emin olun.

### Adım 3: Tüm Görüntüleri Al

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Yüklenmiş OneNote belgesinden tüm görüntüleri alın.

### Adım 4: Toplam Görüntü Sayısını Yazdır

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Belgede bulunan toplam görüntü sayısını yazdırın.

### Adım 5: Gezin ve Görüntü Bilgilerini Yazdır

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

Görüntü listesini döngüye alarak her bir görüntü için genişlik, yükseklik, orijinal boyutlar, dosya adı ve son değiştirilme zamanı gibi detayları yazdırın.

## Java kullanarak OneNote'tan görüntüleri neden çıkarmalısınız?

- **Otomasyon:** Defterlerin manuel incelenmesini ortadan kaldırır.  
- **Veri Analitiği:** Görüntü meta verilerini raporlama hatlarına besler.  
- **Göç:** İçeriği diğer platformlara taşırken görüntü özelliklerini korur.  
- **Performans:** İhtiyacınız olan sadece meta verileri alır, ağır dosya ayrıştırmayı önler.

## Yaygın Tuzaklar ve İpuçları

- **Yanlış yol:** `dataDir`'in uygun dosya ayırıcıyla (`/` veya `\`) bittiğini iki kez kontrol edin.  
- **Lisans sorunları:** Geçerli bir lisans olmadan Aspose.Note değerlendirme uyarıları verebilir.  
- **Büyük defterler:** Binlerce görüntülü defterler için belleği azaltmak amacıyla işleme partiler halinde yapılmasını düşünün.

## Sıkça Sorulan Sorular

### S1: Aspose.Note for Java OneNote dışındaki diğer belge formatlarını işleyebilir mi?

**C1:** Evet, Aspose.Note for Java OneNote, PDF ve Microsoft Word dahil çeşitli belge formatlarını destekler.

### S2: Aspose.Note for Java kişisel ve ticari kullanım için uygun mu?

**C2:** Evet, Aspose.Note for Java'ı hem kişisel hem de ticari amaçlarla kullanabilirsiniz.

### S3: Aspose.Note for Java teknik destek sunuyor mu?

**C3:** Evet, teknik destek Aspose forumları üzerinden [burada](https://forum.aspose.com/c/note/28) mevcuttur.

### S4: Satın almadan önce Aspose.Note for Java'ı deneyebilir miyim?

**C4:** Evet, Aspose.Note for Java'ın ücretsiz deneme sürümünü [Aspose.Note for Java](https://releases.aspose.com/note/java/) adresinden keşfedebilirsiniz.

### S5: Aspose.Note for Java için geçici bir lisans nasıl alabilirim?

**C5:** Geçici bir lisansı [Temporary license/](https://purchase.aspose.com/temporary-license/) adresinden edinebilirsiniz.

## Sonuç

Bu öğreticide belirtilen adımları izleyerek, Aspose.Note for Java kullanarak OneNote belgelerinden etkili bir şekilde **get image dimensions java** alabilirsiniz. Bu işlevi uygulamalarınıza entegre etmek, belge işleme ile ilgili görevleri otomatikleştirerek verimliliği ve üretkenliği artırabilir.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose  

---
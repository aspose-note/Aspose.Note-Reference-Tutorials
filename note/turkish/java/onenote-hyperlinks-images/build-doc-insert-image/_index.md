---
date: 2025-12-20
description: Aspose.Note for Java kullanarak OneNote'a resim eklemeyi öğrenin. OneNote
  belgeleri oluşturmak ve programlı olarak resim eklemek için adım adım rehber.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Java kullanarak OneNote'a resim ekleme – Belge oluşturma ve resim ekleme
url: /tr/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile OneNote’a Resim Ekleme – Belge Oluşturma ve Görsel Yerleştirme

## Giriş

Bu öğreticide **Java Aspose.Note API** kullanarak **OneNote’a resim eklemeyi** öğreneceksiniz. Sıfırdan bir OneNote belgesi oluşturma, bir görsel ekleme ve sonucu PDF olarak kaydetme adımlarını göstereceğiz. Raporlama aracı geliştiriyor, not alma süreçlerini otomatikleştiriyor ya da programlı olarak grafik eklemeniz gerekiyorsa, bu rehber net ve uygulamalı bir yol sunar.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java.
- **Herhangi bir resim formatı ekleyebilir miyim?** JPEG, PNG, BMP, GIF ve daha fazlası desteklenir.
- **Hangi çıktı formatları mevcut?** OneNote, PDF, XPS, HTML vb. olarak kaydedebilirsiniz.
- **Üretim ortamında lisans gerekli mi?** Evet, deneme dışı kullanım için ticari lisans gerekir.
- **Kod platformlar arası mı?** Kesinlikle – Java Windows, Linux ve macOS’ta çalışır.

## “OneNote’a resim ekleme” nedir?
OneNote’a resim eklemek, bir resim dosyasını programlı olarak OneNote sayfasına gömerek metin, başlık veya diğer öğelerle birlikte görünmesini sağlamaktır. Aspose.Note API, OneNote dosya formatını soyutlayarak içeriğe odaklanmanızı, XML yapısını yönetmenizi gerektirmez.

## Neden Java ile OneNote’a resim ekleyelim?
- **Otomasyon:** Toplantı tutanaklarını otomatik olarak ekran görüntüleriyle oluşturun.
- **Tutarlılık:** Her sayfanın aynı düzen ve marka kimliğine sahip olmasını sağlayın.
- **Entegrasyon:** Diğer sistemlerden gelen verileri (ör. grafikler) doğrudan OneNote defterlerine ekleyin.
- **Platform bağımsızlığı:** Java, aynı kodu herhangi bir sunucu ya da masaüstü ortamında çalıştırmanıza olanak tanır.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – herhangi bir güncel sürüm (8 veya üzeri).  
2. **Aspose.Note for Java kütüphanesi** – [web sitesinden](https://releases.aspose.com/note/java/) indirin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir Java uyumlu editör.  

## Paketleri İçe Aktarma

Java kaynak dosyanıza gerekli sınıfları aşağıdaki gibi ekleyin:

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

## Adım‑Adım Kılavuz

### Adım 1: Belgeyi Oluşturma

Yeni bir OneNote belgesi ve içeriğin yer alacağı bir sayfa konteyneri oluşturun.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Adım 2: Outline’ı Başlatma

*Outline*, metin ve görseller gibi öğeleri tutan bir kapsayıcı görevi görür. İçeriğin sol‑üst köşeden başlaması için ofsetleri sıfıra ayarlarız.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Adım 3: Görseli Yükleme ve Hizalama

Eklemek istediğiniz resmi yükleyin ve sayfanın sağ tarafına hizalayın. İşte **OneNote’a resim ekleme** işleminin gerçekleştiği adım.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Adım 4: Görseli Outline Elementine Bağlama

Görseli bir `OutlineElement` içine sarın. Bu adım, görsel nesnesini belgenin outline hiyerarşisine bağlar.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Adım 5: Belge Yapısını Oluşturma

Outline elementini outline’a ekleyin, ardından outline’ı sayfaya, son olarak da sayfayı belgeye ekleyin.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Adım 6: OneNote Belgesini Kaydetme

Belgeyi diske kalıcı olarak yazın. Bu örnekte PDF’ye dışa aktarıyoruz, ancak `SaveFormat`’ı değiştirerek yerel OneNote dosyası (`.one`) olarak da kaydedebilirsiniz.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|------|
| **Görsel görünmüyor** | Yanlış dosya yolu veya desteklenmeyen format. | `dataDir`’in doğru klasöre işaret ettiğini doğrulayın ve desteklenen bir resim türü (JPEG, PNG vb.) kullanın. |
| **Belge boş PDF olarak kaydediliyor** | Outline ofsetleri hatalı ayarlanmış. | `setVerticalOffset(0)` ve `setHorizontalOffset(0)` çağrılarının yapıldığından emin olun veya ofsetleri sayfa sınırları içinde olacak şekilde ayarlayın. |
| **Kaydetme sırasında IOException** | Hedef klasör mevcut değil ya da yazma izni yok. | Klasörü önceden oluşturun veya programı gerekli izinlerle çalıştırın. |

## Sık Sorulan Sorular

**S1: Aspose.Note for Java dokümantasyonuna nereden ulaşabilirim?**  
C1: Dokümantasyona [buradan](https://reference.aspose.com/note/java/) erişebilirsiniz.

**S2: Aspose.Note for Java’yı nasıl indirebilirim?**  
C2: Aspose.Note for Java’yı [indirme sayfasından](https://releases.aspose.com/note/java/) indirebilirsiniz.

**S3: Aspose.Note for Java için ücretsiz deneme mevcut mu?**  
C3: Evet, ücretsiz deneme sürümünü [web sitesinden](https://releases.aspose.com/) alabilirsiniz.

**S4: Aspose.Note for Java için destek nasıl alınır?**  
C4: Destek için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

**S5: Aspose.Note for Java için geçici bir lisans alabilir miyim?**  
C5: Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) talep edebilirsiniz.

---

**Son Güncelleme:** 2025-12-20  
**Test Edilen Sürüm:** Aspose.Note for Java 24.12 (en yeni)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
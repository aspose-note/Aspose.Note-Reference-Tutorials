---
date: 2025-12-17
description: Aspose.Note for Java kullanarak bir belgeyi gri tonlamalı PNG görüntüsü
  olarak kaydederek OneNote dışa aktarmayı öğrenin. OneNote belgesini yükleme ve gri
  tonlamalı görüntü oluşturma adımlarını içerir.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u Gri Tonlu Görüntü Olarak Nasıl Dışa Aktarılır – Aspose.Note
url: /tr/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Gri Tonlamalı Görüntü Kaydetme - Aspose.Note

## Giriş

Bu öğreticide, **how to export onenote** işlemini Aspose.Note for Java kullanarak bir belgeyi gri tonlamalı bir görüntü olarak kaydetmekle göstereceğiz. Gri tonlamalı görüntüler, yalnızca gri tonlarından oluşan tek renkli resimlerdir ve baskı, arşivleme veya dosya boyutunu küçültme gibi durumlarda faydalı olabilir. OneNote belgesini yükleme, **gri tonlamalı bir görüntü oluşturmak** için kaydetme seçeneklerini yapılandırma ve sonunda **belgeyi PNG olarak kaydetme** adımlarını birlikte inceleyeceğiz.

## Hızlı Yanıtlar
- **“how to export onenote” ne anlama geliyor?** Bu, bir OneNote dosyasını programlı olarak başka bir formata, örneğin bir görüntüye dönüştürmeyi ifade eder.  
- **Gri tonlamalı çıktı için hangi format en iyisidir?** PNG, kayıpsız kaliteyi korur ve gri tonlama renk modunu desteklediği için iyi bir seçimdir.  
- **Bir lisansa ihtiyacım var mı?** Üretim kullanımı için geçerli bir Aspose.Note lisansı gereklidir; test amaçlı geçici bir deneme lisansı mevcuttur.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri önerilir.  
- **Görüntü boyutunu değiştirebilir miyim?** Evet, kaydetmeden önce `ImageSaveOptions` özellikleri olan `Resolution` veya `PageSize` gibi değerleri ayarlayabilirsiniz.

## “how to export onenote” nedir?
OneNote dışa aktarma, bir OneNote `.one` dosyasını programlı olarak PDF, HTML veya bir görüntü gibi başka bir temsile dönüştürmeyi ifade eder. Bu rehberde, **gri tonlamalı PNG** görüntüsüne dışa aktarmaya odaklanacağız; bu, dokümantasyon veya baskı iş akışları için yaygın bir gereksinimdir.

## Neden OneNote'u gri tonlamalı bir görüntü olarak dışa aktarıyorsunuz?
- **Dosya boyutu azalır** – Gri tonlamalı PNG'ler genellikle tam renkli görüntülerden daha küçüktür.  
- **Okunabilirlik artar** – Baskı raporları için gri tonlama genellikle daha net bir kontrast sağlar.  
- **Uyumluluk** – PNG, tarayıcılar, editörler ve mobil cihazlar arasında geniş çapta desteklenir.  

## Önkoşullar

Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

1. Sisteminizde Java Development Kit (JDK) yüklü olmalı.  
2. Aspose.Note for Java kütüphanesi. İndirmek için [buraya](https://releases.aspose.com/note/java/) tıklayın.  
3. Java programlamaya temel bir anlayış.

## Paketleri İçe Aktar

Başlamak için gerekli paketleri içe aktarın:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Adım 1: OneNote Belgesini Yükleyin

İlk olarak, **onenote belgesini** Aspose.Note içine **yükleyin**. `"Your Document Directory"` ifadesini yerel klasör yolunuzla ve `"Aspose.one"` ifadesini OneNote dosyanızın adıyla değiştirin.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: Çıktı Yolu ve Seçenekleri Belirleyin

Gri tonlamalı görüntünün çıkış yolunu tanımlayın ve kaydetme seçeneklerini belirtin. `ColorMode` değerini `GrayScale` olarak ayarlayacak ve **belgeyi png olarak kaydet** formatını kullanacağız.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Adım 3: Belgeyi Kaydedin

Son olarak, yapılandırılmış seçenekleri kullanarak belgeyi gri tonlamalı bir PNG görüntüsü olarak kaydedin.

```java
oneFile.save(dataDir, options);
```

## Yaygın Sorunlar ve Çözümler
- **FileNotFoundException** – `dataDir` değişkeninin doğru klasöre işaret ettiğini ve `.one` dosyasının mevcut olduğunu doğrulayın.  
- **LicenseException** – `save` metodunu çağırmadan önce geçerli bir Aspose.Note lisansı uyguladığınızdan emin olun.  
- **Düşük çözünürlüklü çıktı** – Gerekirse DPI'yi artırmak için `options.setResolution(300)` gibi bir ayar yapın.

## Sık Sorulan Sorular

**S1: Gri tonlamalı görüntüyü farklı bir formatta kaydedebilir miyim?**  
C1: Evet, `ImageSaveOptions` yapıcısındaki `SaveFormat` parametresini `Jpeg`, `Bmp` vb. olarak değiştirmeniz yeterlidir.

**S2: Aspose.Note tüm OneNote belge sürümleriyle uyumlu mu?**  
C2: Aspose.Note, Microsoft OneNote 2010 ve sonraki sürümlerini destekler.

**S3: Aspose.Note kullanmak için lisansa ihtiyaç var mı?**  
C3: Üretim ortamı için geçerli bir lisans gereklidir; değerlendirme amacıyla geçici bir deneme lisansı alınabilir.

**S4: Belgeyi görüntü olarak kaydetmeden önce başka yönlerini de değiştirebilir miyim?**  
C4: Kesinlikle! Aspose.Note, bölümler, sayfalar ve içerik üzerinde dışa aktarmadan önce düzenleme yapmanıza olanak tanıyan kapsamlı bir API sunar.

**S5: Sorun yaşarsam nereden destek alabilirim?**  
C5: Aspose.Note forumunda [burada](https://forum.aspose.com/c/note/28/) destek bulabilirsiniz.

## Sonuç

Artık **how to export onenote** işlemini bir OneNote dosyasını yükleyerek, **gri tonlamalı bir görüntü oluşturmak** için kaydetme seçeneklerini yapılandırarak ve **belgeyi PNG olarak kaydederek** nasıl yapacağınızı öğrendiniz. Bu teknik, OneNote defterlerinden hafif, baskıya hazır görseller üretmek için kullanışlıdır. Projenizin ihtiyaçlarına göre diğer `ColorMode` ayarlarını veya görüntü formatlarını denemekten çekinmeyin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---
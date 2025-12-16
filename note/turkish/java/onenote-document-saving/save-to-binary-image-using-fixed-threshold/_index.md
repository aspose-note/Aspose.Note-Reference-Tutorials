---
date: 2025-12-13
description: Aspose.Note Java ile OneNote’u PNG’ye dönüştürmek için eşik ayarını nasıl
  yapacağınızı öğrenin, Java görüntü ikilileştirme kullanarak siyah‑beyaz OneNote
  görüntüleri oluşturun.
linktitle: Save to Binary Image Using Fixed Threshold in OneNote
second_title: Aspose.Note Java API
title: OneNote'u İkili Görüntü Olarak Kaydederken Eşiği Nasıl Ayarlarsınız
url: /tr/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u İkili Görüntü Olarak Kaydederken Eşiğiınız

## Introduction

Bu öğreticide **eşiği nasıl ayarlayacağınızı** keşfedecek ve bir Microsoft OneNote sayfasını yüksek kontrastlı, siyah‑beyaz PNG görüntüsü olarak dışa aktaracaksınız. Sabit eşik değerini ayarlayarak dönüşüm üzerinde hassas kontrol elde eder, OCR ön işleme veya belge arşivleme gibi senaryolar için mükemmel bir sonuç elde edersiniz. Aspose.Note Java API'sını kullanarak her adımı adım adım göstereceğiz, böylece güvenilir **image binarization Java** teknikleriyle **OneNote'u PNG'ye dönüştürebilirsiniz**.

## Quick Answers
- **“adjust threshold” ne anlama geliyor?** Renkli bir görüntüyü siyah‑beyaza dönüştürürken kullanılan piksel yoğunluğu kesim noktasını ayarlar.
- **Hangi format üretiliyor?** Herhangi bir görüntü görüntüleyicisiyle açılabilen bir PNG dosyası.
- **Eşik değerini değiştirebilir miyim?** Evet – `setBinarizationThreshold()` çağrısını değiştirin.
- **Lisans gerekiyor mu?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.
- **Bu, tüm OneNote sürümleriyle uyumlu mu?** Aspose.Note, OneNote 2010, 2013, 2016 ve sonrası sürümleri destekler.

## Prerequisites

Başlamadan önce şunların yüklü olduğundan emin olun:

1. Java Development Kit (JDK) kurulmuş.
2. [buradan](https://releases.aspose.com/note/java/) indirilen Aspose.Note for Java kütüphanesi.
3. Java sözdizimine temel aşinalık.

## Import Packages

İlk olarak, gerekli sınıfları Java kaynak dosyanıza içe aktarın.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Load the Document

İşlemek istediğiniz OneNote dosyasını yükleyin.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Step 2: Set Binarization Options

**image binarization Java** ayarlarını tanımlayın ve kullanmak istediğiniz sabit eşiği belirtin.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

> **Pro tip:** Belirli belgeniz için en uygun noktayı bulmak amacıyla 0‑255 arasındaki eş değerleriyle deney yapın. Daha düşük değerler daha açık görüntüler, daha yüksek değerler daha koyu çıktı verir.

## Step 3: Set Image Save Options

Görüntü formatını, renk modunu yapılandırın ve binarizasyon seçeneklerini ekleyin.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

`ColorMode.BlackAndWhite` ayarı, son dosyanın bir **black and white OneNote** görüntüsü olmasını sağlar.

## Step 4: Save the Document

Önceden tanımlanan seçeneklerle kaydetme işlemini yürütün.

```java
oneFile.save(dataDir, options);
```

Kodu çalıştırdıktan sonra, çıktı klasörünüzde `SaveToBinaryImageUsingFixedThreshold_out.png` adlı bir PNG dosyası bulacaksınız; bu dosya daha fazla işleme veya arşivleme için hazırdır.

## Conclusion

**eşiği nasıl ayarlayacağınızı** gösterdik; Aspose.Note for Java kullanarak OneNote dosyasından temiz, yüksek kontrastlı bir PNG üretmek artık mümkün. **image binarization Java** seçeneklerini ustalaşarak **OneNote'u PNG'ye dönüştürebilir** ve OCR, baskı veya dijital koruma için **black and white OneNote** varlıkları oluşturabilirsiniz.

## Frequently Asked Questions

**S: Eşiği çok düşük ayarlarsam ne olur?**  
C: Oluşan görüntü yıkanmış görünebilir; birçok gri ton korunur ve net siyah‑beyaz kontrastı elde edilemez.

**S: Farklı bir binarizasyon yöntemi kullanabilir miyim?**  
C: Evet, Aspose.Note aynı zamanda adaptif eşikleme destekler; sadece `BinarizationMethod.FixedThreshold` yerine `BinarizationMethod.Adaptive` kullanın.

**S: JPEG gibi başka formatlara doğrudan dışa aktarım mümkün mü?**  
C: Kesinlikle—`ImageSaveOptions` yapıcısında `SaveFormat.Png` yerine `SaveFormat.Jpeg` olarak değiştirin.

**S: Şifre korumalı OneNote dosyalarını nasıl yönetirim?**  
C: Binarizasyon adımlarına geçmeden önce şifre dizesini kabul eden uygun aşırı yüklemeyi kullanarak belgeyi yükleyin.

**S: Bu yaklaşım Linux/macOS'ta çalışır mı?**  
C: Aspose.Note Java kütüphanesi platform bağımsızdır; uyumlu bir JDK ile aynı kod herhangi bir işletim sisteminde çalışır.

---

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.Note for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
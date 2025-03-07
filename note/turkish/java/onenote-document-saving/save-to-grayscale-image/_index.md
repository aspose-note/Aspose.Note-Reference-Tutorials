---
title: OneNote'ta Gri Tonlamalı Görüntüye Kaydetme - Aspose.Note
linktitle: OneNote'ta Gri Tonlamalı Görüntüye Kaydetme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java kullanarak bir belgeyi OneNote'ta gri tonlamalı görüntü olarak nasıl kaydedeceğinizi öğrenin. Microsoft OneNote belgelerini program aracılığıyla kolayca yönetin.
weight: 17
url: /tr/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Gri Tonlamalı Görüntüye Kaydetme - Aspose.Note

## giriiş

Bu eğitimde, Aspose.Note for Java kullanarak bir belgeyi OneNote'ta gri tonlamalı görüntü olarak nasıl kaydedeceğimizi keşfedeceğiz. Gri tonlamalı görüntüler, renk bilgilerinin yalnızca grinin tonlarıyla temsil edildiği tek renkli görüntülerdir. Aspose.Note, Microsoft OneNote belgelerinin programlı olarak değiştirilmesine olanak tanıyan güçlü bir Java API'sidir.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2.  Aspose.Note for Java kütüphanesi. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).
3. Java programlamanın temel anlayışı.

## Paketleri İçe Aktar

Başlamak için gerekli paketleri içe aktarın:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 1. Adım: Belgeyi Yükleyin

 İlk önce belgeyi Aspose.Note'a yükleyin. Yer değiştirmek`"Your Document Directory"` belge dizininizin yolu ile ve`"Aspose.one"` OneNote belgenizin adıyla birlikte.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: Çıkış Yolunu ve Seçeneklerini Ayarlayın

Gri tonlamalı görüntünün çıktı yolunu tanımlayın ve kaydetme seçeneklerini belirtin. Renk modunu gri tonlamaya ayarlayacağız.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 3. Adım: Belgeyi Kaydedin

Son olarak belirtilen seçenekleri kullanarak belgeyi gri tonlamalı görüntü olarak kaydedin.

```java
oneFile.save(dataDir, options);
```

## Çözüm

Tebrikler! Aspose.Note for Java kullanarak bir belgeyi OneNote'ta gri tonlamalı görüntü olarak nasıl kaydedeceğinizi başarıyla öğrendiniz. Bu, gri tonlamalı görüntülerin gerekli olduğu çeşitli uygulamalar için inanılmaz derecede yararlı olabilir.

## SSS'ler

### S1: Gri tonlamalı görüntüyü farklı bir formatta kaydedebilir miyim?

 A1: Evet, yapabilirsin. Basitçe değiştirin`SaveFormat` parametresi`ImageSaveOptions` yapıcıyı istediğiniz formata getirin.

### S2: Aspose.Note, OneNote belgelerinin tüm sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note, Microsoft OneNote 2010 ve üstünü destekler.

### S3: Aspose.Note'u kullanmak için lisans gerekiyor mu?

Cevap3: Evet, Aspose.Note'u üretim ortamlarında kullanmak için geçerli bir lisansa ihtiyacınız var. Ancak test amaçlı olarak geçici bir lisans alabilirsiniz.

### S4: Belgeyi resim olarak kaydetmeden önce belgenin diğer yönlerini değiştirebilir miyim?

Cevap4: Kesinlikle! Aspose.Note, OneNote belgelerini programlı olarak düzenlemek için çok çeşitli özellikler sunar.

### S5: Sorunlarla karşılaşırsam nereden destek bulabilirim?

Cevap5: Aspose.Note forumunda destek bulabilirsiniz[Burada](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

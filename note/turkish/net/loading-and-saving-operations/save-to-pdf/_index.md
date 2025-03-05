---
title: Aspose.Note'ta PDF'ye kaydet
linktitle: Aspose.Note'ta PDF'ye kaydet
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak Microsoft OneNote belgelerini PDF formatında nasıl kaydedeceğinizi öğrenin. Letter ve A4 sayfa düzenleri için kod örnekleri içeren adım adım eğitim.
type: docs
weight: 26
url: /tr/net/loading-and-saving-operations/save-to-pdf/
---
## giriiş

Bu eğitimde, Aspose.Note for .NET'i kullanarak belgeleri PDF formatında nasıl kaydedeceğimizi inceleyeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasını sağlayan güçlü bir kitaplıktır. Önkoşulları ele alacağız, ad alanlarını içe aktaracağız ve belgeleri çeşitli sayfa düzenlerinde PDF'ye kaydetmek için adım adım kılavuzlar sunacağız.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Sisteminizde Visual Studio yüklü.
-  Aspose.Note for .NET kütüphanesi indirildi ve kuruldu. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/net/).
- Temel C# programlama dili bilgisi.

## Ad Alanlarını İçe Aktar

Öncelikle gerekli ad alanlarını C# kodumuza aktaralım:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Artık önkoşulları ele aldığımıza ve ad alanlarını içe aktardığımıza göre, belgeleri farklı sayfa düzenlerinde PDF'ye kaydetmeye devam edelim.

## 1. Adım: Mektup Sayfası Ayarlarını kullanarak PDF'ye kaydedin


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Belgeler dizininin yolu.
    string dataDir = "Your Document Directory";

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Belgeyi kaydedin.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Açıklama:

- OneNote belgesini Aspose.Note'a yüklüyoruz.
- Kaydedilen PDF dosyasının hedef yolunu tanımlayın.
-  Belgeyi kullanarak PDF'ye kaydedin`PdfSaveOptions` ile`PageSettings` ayarlanır`Letter`.

## Adım 2: Yükseklik Sınırı Olmadan A4 Sayfa Ayarlarını kullanarak PDF'ye kaydedin

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Belgeler dizininin yolu.
    string dataDir = "Your Document Directory";

    // Belgeyi Aspose.Note'a yükleyin.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Belgeyi kaydedin.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Açıklama:

- Önceki adıma benzer şekilde OneNote belgesini Aspose.Note'a yüklüyoruz.
- Kaydedilen PDF dosyasının hedef yolunu tanımlayın.
-  Belgeyi kullanarak PDF'ye kaydedin`PdfSaveOptions` ile`PageSettings` ayarlanır`A4NoHeightLimit`.

## Çözüm

Bu eğitimde Aspose.Note for .NET kullanarak belgeleri PDF formatında nasıl kaydedeceğimizi öğrendik. İki farklı sayfa düzenini ele aldık: Letter ve yükseklik sınırı olmayan A4. Aspose.Note ile geliştiriciler OneNote dosyalarını programlı olarak kolayca yönetebilir, böylece belge yönetimi görevlerinde esneklik ve verimlilik sağlanır.

## SSS'ler

### S1: Aspose.Note karmaşık OneNote dosyalarını işleyebilir mi?

Cevap1: Evet, Aspose.Note, karmaşık OneNote dosyalarını etkili bir şekilde yönetmek için çeşitli özellikleri ve işlevleri destekler.

### S2: Aspose.Note ticari projeler için uygun mudur?

 Cevap2: Kesinlikle Aspose.Note ticari projelerde rahatlıkla kullanılabilir. Lisans satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).

### S3: Aspose.Note ücretsiz deneme sunuyor mu?

 Cevap3: Evet, Aspose.Note'u ücretsiz deneme sürümüyle keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.Note belgelerini nerede bulabilirim?

 Cevap4: Ayrıntılı belgeleri bulabilirsiniz[Burada](https://reference.aspose.com/note/net/).

### S5: Daha fazla yardıma mı ihtiyacınız var?

 Cevap5: Aspose.Note forumunda soru sormaktan veya destek almaktan çekinmeyin[Burada](https://forum.aspose.com/c/note/28).
---
title: Aspose.Note for .NET ile Karanlık Tema Dönüşümü
linktitle: Aspose.Note'ta Metne Koyu Tema Uygula
second_title: Aspose.Note .NET API'si
description: OneNote belgelerinizi Aspose.Note for .NET ile dönüştürün! Şık bir karanlık temayı zahmetsizce uygulayın. Hemen indirin ve not alma deneyiminizi geliştirin.
type: docs
weight: 11
url: /tr/net/text-manipulation/apply-dark-theme-text/
---
## giriiş
Aspose.Note for .NET'te metne koyu tema uygulamayla ilgili adım adım kılavuzumuza hoş geldiniz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir .NET API'sidir. Bu eğitimde, metne koyu bir tema uygulayarak OneNote belgelerinize nasıl şık ve modern bir görünüm kazandıracağınızı keşfedeceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
-  Aspose.Note for .NET: Aspose.Note for .NET'in kurulu olduğundan emin olun. Değilse, adresinden indirebilirsiniz.[Aspose.Note belgeleri](https://reference.aspose.com/note/net/).
- Geliştirme Ortamı: Visual Studio gibi tercih ettiğiniz .NET geliştirme ortamını kurun.
- Belge Dizini: OneNote belgenizin bulunduğu dizini hazırlayın.
## Ad Alanlarını İçe Aktar
.NET projenize Aspose.Note ile çalışmak için gerekli ad alanlarını içe aktarın:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## 1. Adım: OneNote Belgesini Yükleyin
Aşağıdaki kodu kullanarak OneNote belgenizi Aspose.Note'a yükleyin:
```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";
// Belgeyi Aspose.Note'a yükleyin.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Adım 2: Arka Plan Rengini Ayarlayın
Her sayfanın arka plan rengini siyah olarak ayarlayın:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## 3. Adım: Metin Rengini Ayarlayın
Daha iyi görünürlük için metnin yazı tipi rengini beyaza ayarlayın:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Adım 4: Belgeyi Kaydedin
Değiştirilen OneNote belgesini PDF olarak kaydedin:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Çözüm
Tebrikler! Aspose.Note belgenizdeki metne başarıyla karanlık bir tema uyguladınız. Bu basit ama etkili geliştirme, OneNote dosyalarınıza daha karmaşık bir görünüm kazandırabilir.
## Sıkça Sorulan Sorular
### OneNote belgemin belirli bölümlerine koyu bir tema uygulayabilir miyim?
Evet, kodu, belgenizdeki belirli sayfaları veya bölümleri hedefleyecek şekilde özelleştirebilirsiniz.
### Aspose.Note, PDF'nin yanı sıra diğer dışa aktarma formatlarını da destekliyor mu?
Kesinlikle! Aspose.Note, görüntüler ve Microsoft Word de dahil olmak üzere çeşitli dışa aktarma formatlarını destekler.
### Aspose.Note'un işleyebileceği belge boyutunun bir sınırı var mı?
Aspose.Note farklı boyutlardaki belgeleri işleyebilir ve performansı verimlilik için optimize edilmiştir.
### Koyu temayı uyguladıktan sonra orijinal temaya dönebilir miyim?
Evet, tercihlerinize göre temalar arasında geçiş yapmak için kodu değiştirebilirsiniz.
### Aspose.Note ile ilgili sorgular için nereden destek alabilirim?
 Herhangi bir yardım için şu adresi ziyaret edin:[Aspose.Note forumu](https://forum.aspose.com/c/note/28) veya keşfedin[dokümantasyon](https://reference.aspose.com/note/net/).
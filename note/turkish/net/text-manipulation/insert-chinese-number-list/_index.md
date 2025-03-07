---
title: Aspose.Note Metnine Çince Numara Listesi Ekle
linktitle: Aspose.Note Metnine Çince Numara Listesi Ekle
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET belgelerine Çince sayı listelerini zahmetsizce nasıl ekleyeceğinizi öğrenin. Bu adım adım kılavuzla belge biçimlendirme becerilerinizi geliştirin.
weight: 20
url: /tr/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note Metnine Çince Numara Listesi Ekle

## giriiş
Aspose.Note for .NET becerilerinizi, Çince sayı listelerini belgelerinize dahil ederek geliştirmek mi istiyorsunuz? Eğer öyleyse, doğru yerdesiniz! Bu eğitimde, Aspose.Note for .NET'i kullanarak Çince sayı listeleri ekleme sürecinde size yol göstereceğiz. Bu güçlü kitaplık, OneNote belgelerini sorunsuz bir şekilde değiştirmenize olanak tanır.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
- Temel C# programlama bilgisi.
-  Aspose.Note for .NET kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/note/net/).
## Ad Alanlarını İçe Aktar
Başlamak için gerekli ad alanlarını projenize aktarın:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1. Adım: OneNote Belgesini Başlatın
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 2. Adım: OneNote Sayfasını Başlatın
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## 3. Adım: Metin Stili Ayarlarını Uygulayın
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Adım 4: Anahat Öğeleri Oluşturun
Şimdi Çince sayı listeleriyle üç anahat öğesi oluşturalım:
### Adım 4.1: İlk Unsur
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Adım 4.2: İkinci Unsur
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Adım 4.3: Üçüncü Unsur
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Adım 5: Anahat'a Öğeler Ekleme
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Adım 6: Anahattı Sayfaya Ekle
```csharp
page.AppendChildLast(outline);
```
## Adım 7: Sayfayı Belgeye Ekle
```csharp
doc.AppendChildLast(page);
```
## Adım 8: OneNote Belgesini Kaydetme
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Tebrikler! .NET kitaplığını kullanarak Aspose.Note belgenize Çince sayı listelerini başarıyla eklediniz.
## Çözüm
Bu eğitimde, Çince sayı listelerini Aspose.Note for .NET belgelerinize adım adım dahil etme sürecini ele aldık. Bu tekniklerle belge biçimlendirme becerilerinizi geliştirin ve içeriğinizi daha ilgi çekici hale getirin.
## SSS
### S: Çince numara listelerinin formatını özelleştirebilir miyim?
 C: Evet, parametreleri ayarlayarak biçimlendirmeyi özelleştirebilirsiniz.`NumberList` yapıcı.
### S: Aspose.Note .NET'in en son sürümüyle uyumlu mu?
C: Evet, Aspose.Note, .NET'in en son sürümlerini destekleyecek şekilde düzenli olarak güncellenmektedir.
### S: Ek örnekleri ve belgeleri nerede bulabilirim?
C: Kapsamlı olanı keşfedin[Aspose.Note belgeleri](https://reference.aspose.com/note/net/).
### S: Aspose.Note için nasıl geçici lisans alabilirim?
 C: Geçici bir lisans alın[Burada](https://purchase.aspose.com/temporary-license/).
### S: Nereden yardım alabilirim veya Aspose.Note ile ilgili soruları tartışabilirim?
 C: Ziyaret edin[Aspose.Note destek forumu](https://forum.aspose.com/c/note/28) topluluk desteği için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

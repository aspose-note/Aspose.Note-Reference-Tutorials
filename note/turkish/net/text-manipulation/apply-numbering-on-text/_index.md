---
title: Aspose.Note'ta Metne Numaralandırma Uygula
linktitle: Aspose.Note'ta Metne Numaralandırma Uygula
second_title: Aspose.Note .NET API'si
description: Bu kapsamlı eğitimle Aspose.Note for .NET'te metin numaralandırmanın nasıl uygulanacağını öğrenin. Belge biçimlendirmenizi zahmetsizce geliştirin.
type: docs
weight: 12
url: /tr/net/text-manipulation/apply-numbering-on-text/
---
## giriiş
Aspose.Note for .NET, C# uygulamalarında belge manipülasyonu için güçlü araçlar sağlar. Bu eğitimde Aspose.Note'u kullanarak metne numaralandırma uygulama sürecini inceleyeceğiz. Belge biçimlendirmenizi zahmetsizce geliştirmek için bu adım adım talimatları izleyin.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
- C# programlama dilinin temel anlayışı.
-  Aspose.Note for .NET kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/note/net/).
- Visual Studio gibi entegre bir geliştirme ortamı (IDE).
## Ad Alanlarını İçe Aktar
Başlamak için C# projenize gerekli ad alanlarını içe aktardığınızdan emin olun:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1. Adım: Belgenizi Ayarlayın
Yeni bir belge oluşturarak ve gerekli nesneleri başlatarak başlayın:
```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";
//Document sınıfının bir nesnesini oluşturun
Document doc = new Document();
// Sayfa sınıfı nesnesini başlat
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Outline sınıfı nesnesini başlat
Outline outline = new Outline(doc);
```
## Adım 2: Varsayılan Stili Tanımlayın
ParagraphStyle sınıfını kullanarak metniniz için varsayılan stili ayarlayın:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 3. Adım: Numaralandırmayı Uygulayın
OutlineElement sınıfı nesnelerini başlatın ve her öğeye numaralandırma uygulayın:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 4. Adım: Anahat Öğelerini Ekleyin
Anahat öğelerini ana hatta ekleyin:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Adım 5: Belgeyi Kaydedin
OneNote belgesini uygulanan numaralandırmayla kaydedin:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Çözüm
Tebrikler! Aspose.Note for .NET'te metne numaralandırmanın nasıl uygulanacağını başarıyla öğrendiniz. Zahmetsizce görsel olarak çekici belgeler oluşturmak için farklı biçimlendirme seçeneklerini deneyin.
## SSS'ler
### 1. Numaralandırma formatını özelleştirebilir miyim?
Evet, NumberList sınıfı numaralandırma biçimini tercihlerinize göre özelleştirmenize olanak tanır.
### 2. Başka biçimlendirme seçenekleri mevcut mu?
Aspose.Note, yazı tipi stili, renk ve daha fazlasını içeren çok çeşitli formatlama seçenekleri sunar.
### 3. Aspose.Note Visual Studio ile uyumlu mu?
Kesinlikle! Aspose.Note, sorunsuz bir geliştirme deneyimi için Visual Studio ile sorunsuz bir şekilde bütünleşir.
### 4. Satın almadan önce Aspose.Note'u deneyebilir miyim?
 Kesinlikle! Ücretsiz denemeyi keşfedebilirsiniz[Burada](https://releases.aspose.com/).
### 5. Aspose.Note için nereden destek alabilirim?
 Herhangi bir yardım veya soru için şu adresi ziyaret edin:[Aspose.Note forumu](https://forum.aspose.com/c/note/28).
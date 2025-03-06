---
title: Aspose.Note'u kullanarak Kök ve Alt Sayfaları Olan Belgeler Oluşturun
linktitle: Aspose.Note'u kullanarak Kök ve Alt Sayfaları Olan Belgeler Oluşturun
second_title: Aspose.Note .NET API'si
description: Hiyerarşik yapılara sahip dinamik OneNote belgeleri oluşturmak için Aspose.Note for .NET'i nasıl kullanacağınızı öğrenin.
weight: 11
url: /tr/net/note-manipulation/create-documents-root-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note'u kullanarak Kök ve Alt Sayfaları Olan Belgeler Oluşturun

## giriiş

Aspose.Note for .NET'i kullanarak kök ve alt sayfalarla belgeler oluşturma eğitimimize hoş geldiniz! Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan, OneNote belgelerinin oluşturulmasına, değiştirilmesine ve dönüştürülmesine olanak tanıyan güçlü bir kitaplıktır.

Bu eğitimde size kök ve alt sayfalarla bir OneNote belgesi oluşturma sürecinde adım adım yol göstereceğiz. Aspose.Note for .NET'i kullanarak ayrıntılı açıklamalar ve kod parçacıkları sunacağız, böylece takip etmenizi ve kendi projelerinizde uygulamanızı kolaylaştıracağız.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Visual Studio: .NET kodunu yazmak ve derlemek için sisteminizde Visual Studio'nun yüklü olması gerekir.
2.  Aspose.Note for .NET: Aspose.Note for .NET'i şu adresten indirip yükleyin:[indirme sayfası](https://releases.aspose.com/note/net/).
3. Temel C# Bilgisi: Kod örneklerini anlamak ve uygulamak için C# programlama diline aşinalık gerekir.

Artık her şeyi ayarladığınıza göre, öğreticiye geçelim!

## Ad Alanlarını İçe Aktar

Öncelikle gerekli namespace’leri projemize aktaralım:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## 1. Adım: Belge Nesnesini Başlatın

```csharp
//Document sınıfının bir nesnesini oluşturun
Document doc = new Document();
```

## Adım 2: Kök Sayfa ve Alt Sayfalar Oluşturun

```csharp
// Page sınıfı nesnelerini başlatın ve düzeylerini ayarlayın
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Sayfa 1 için:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Sayfa 2 için:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Sayfa 3 için:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## 4. Adım: Belgeye Sayfa Ekleme

```csharp
// OneNote Belgesine sayfa ekleme
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Adım 5: Belgeyi Kaydet

```csharp
// OneNote belgesini kaydet
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Çözüm

Tebrikler! Aspose.Note for .NET'i kullanarak kök ve alt sayfalara sahip belgeler oluşturmayı başarıyla öğrendiniz. Artık bu bilgiyi uygulamalarınızda dinamik olarak karmaşık OneNote belgeleri oluşturmak için kullanabilirsiniz.

## SSS'ler

### S1: Aspose.Note büyük OneNote belgelerini işleyebilir mi?

Cevap1: Evet, Aspose.Note büyük OneNote belgelerini performanstan ödün vermeden verimli bir şekilde işleyecek şekilde tasarlanmıştır.

### S2: Aspose.Note .NET Core ile uyumlu mu?

C2: Evet, Aspose.Note geleneksel .NET Framework'ün yanı sıra .NET Core'u da destekler.

### S3: OneNote belgelerini Aspose.Note'u kullanarak diğer formatlara dönüştürebilir miyim?

Cevap3: Aspose.Note kesinlikle PDF, DOCX, HTML ve daha fazlasını içeren çeşitli formatlara dönüştürme yetenekleri sağlar.

### S4: Aspose.Note bulut entegrasyonu sunuyor mu?

Cevap4: Aspose.Note öncelikle şirket içi geliştirmeye odaklanır, ancak bunu uygun kurulumla bulut ortamlarında da kullanabilirsiniz.

### S5: Aspose.Note için teknik destek mevcut mu?

C5: Evet, Aspose, soru sorabileceğiniz ve yardım alabileceğiniz forumları aracılığıyla özel teknik destek sağlıyor.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

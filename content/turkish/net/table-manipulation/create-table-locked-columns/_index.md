---
title: Aspose.Note'u kullanarak Kilitli Sütunlu Tablo Oluşturma
linktitle: Aspose.Note'u kullanarak Kilitli Sütunlu Tablo Oluşturma
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak kilitli sütunlara sahip tablolar oluşturmayı öğrenin. Verimli belge işleme görevleri için adım adım kılavuz.
type: docs
weight: 12
url: /tr/net/table-manipulation/create-table-locked-columns/
---
## giriiş

Kilitli sütunlara sahip tablolar oluşturmak, belge işleme uygulamalarında yaygın bir gereksinimdir. Aspose.Note for .NET, bu görevi verimli bir şekilde gerçekleştirmek için güçlü araçlar sağlar. Bu eğitimde, Aspose.Note for .NET'i kullanarak kilitli sütunlara sahip bir tablo oluşturma sürecinde size adım adım rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- C# programlama dilinin temel anlayışı.
- Sisteminizde Visual Studio yüklü.
-  Aspose.Note for .NET kuruldu. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/net/).
- Belge işleme kavramlarına aşinalık.

## Ad Alanlarını İçe Aktar

Öncelikle gerekli ad alanlarını projenize aktarmanız gerekir:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## 1. Adım: Belge Nesnesini Başlatın

Document sınıfının bir nesnesini oluşturarak başlayın:

```csharp
Document doc = new Document();
```

## Adım 2: Sayfa Nesnesini Başlatın

Page sınıfı nesnesini başlatın:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 3. Adım: TableRow Nesnelerini Başlatın

Tablo için TableRow nesneleri oluşturun:

```csharp
TableRow row1 = new TableRow(doc);
TableRow row2 = new TableRow(doc);
```

## Adım 4: TableCell Nesnelerini Başlatın

TableCell nesneleri oluşturun ve her hücre için metin içeriğini ayarlayın:

```csharp
TableCell cell11 = new TableCell(doc);
cell11.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Small text"));

TableCell cell21 = new TableCell(doc);
cell21.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Long text with several words and spaces."));
```

## Adım 5: Tablo Nesnesini Başlatın

Table sınıfı nesnesini başlatın ve sütun genişliği ve kilitli genişlik gibi özellikleri ayarlayın:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70, LockedWidth = true } }
};
```

## Adım 6: Tabloya Satır Ekleme

Başlatılan satırları tabloya ekleyin:

```csharp
table.AppendChildLast(row1);
table.AppendChildLast(row2);
```

## Adım 7: Tabloyu Outline'a Ekle

Tablo düğümünü OutlineElement'e ekleyin:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
```

## Adım 8: Sayfaya Anahat Ekle

Anahat düğümünü sayfaya ekleyin:

```csharp
page.AppendChildLast(outline);
```

## Adım 9: Belgeyi Kaydet

Belgeyi kaydedin:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable with locked columns created successfully.\nFile saved at " + dataDir);
```

Bu adımları izledikten sonra Aspose.Note for .NET'i kullanarak kilitli sütunlara sahip bir tabloyu başarıyla oluşturacaksınız.

## Çözüm

Bu eğitimde Aspose.Note for .NET kullanarak kilitli sütunlara sahip bir tablonun nasıl oluşturulacağını öğrendik. Bu adımları izleyerek, belgelerinizdeki tabloları özel gereksinimlerinizi karşılayacak şekilde etkili bir şekilde değiştirebilirsiniz.

## SSS'ler

### S1: Tablonun görünümünü daha da özelleştirebilir miyim?

Cevap1: Evet, Aspose.Note for .NET tarafından sağlanan özellikleri kullanarak tablonun kenarlıklar, hücre formatlaması ve daha fazlası gibi çeşitli yönlerini özelleştirebilirsiniz.

### S2: Aspose.Note for .NET büyük ölçekli belge işleme görevlerine uygun mu?

A2: Kesinlikle! Aspose.Note for .NET, büyük ölçekli belge işleme görevlerini verimli bir şekilde gerçekleştirmek, yüksek performans ve güvenilirlik sağlamak üzere tasarlanmıştır.

### S3: Aspose.Note for .NET'i diğer .NET çerçeveleriyle entegre edebilir miyim?

C3: Evet, Aspose.Note for .NET diğer .NET çerçeveleriyle sorunsuz bir şekilde bütünleşerek belge işleme yeteneklerini uygulamalarınıza dahil etmenizi kolaylaştırır.

### S4: Aspose.Note for .NET için teknik destek mevcut mu?

 C4: Evet, teknik desteğe şu adresten erişebilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28) Karşılaşabileceğiniz her türlü soru veya sorunda size yardımcı olacak uzmanların bulunduğu yer.

### S5: Satın almadan önce Aspose.Note for .NET'i deneyebilir miyim?

 Cevap5: Evet, Aspose.Note for .NET'in ücretsiz deneme sürümünü şu adresten indirebilirsiniz:[Burada](https://releases.aspose.com/)özelliklerini ve gereksinimlerinize uygunluğunu değerlendirmek.
---
title: Aspose.Note'ta Etiketli Tablo Düğümü Ekleme
linktitle: Aspose.Note'ta Etiketli Tablo Düğümü Ekleme
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'te etiketli tabloları nasıl ekleyeceğinizi öğrenin. Belge işleme becerilerinizi programlı olarak geliştirin.
type: docs
weight: 11
url: /tr/net/tag-management/add-table-node-tag/
---
## giriiş

Bu eğitimde, Aspose.Note for .NET'i kullanarak etiketli bir tablo düğümü ekleme sürecinde size rehberlik edeceğiz. Bunu başarmak için aşağıdaki adımları izleyin.

## Ad Alanlarını İçe Aktar

Başlamadan önce Aspose.Note ile çalışmak için gerekli ad alanlarını içe aktardığınızdan emin olun:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Önkoşullar

Devam etmeden önce aşağıdaki önkoşulları oluşturduğunuzdan emin olun:

1.  Kurulum: Aspose.Note for .NET kütüphanesini şuradan indirip yükleyin:[Burada](https://releases.aspose.com/note/net/).
2.  Lisans: Bir lisans edinin veya kullanın[geçici lisans](https://purchase.aspose.com/temporary-license/) kütüphaneyi kullanmak için.
3. Geliştirme Ortamı: Visual Studio gibi uyumlu bir geliştirme ortamı kurun.

## Adım 1: Belge ve Sayfa Nesnelerini Başlatın

 Bir örneğini oluşturarak başlayın`Document` sınıf ve bir başlatma`Page` nesne:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Adım 2: Tablo, Satır ve Hücre Nesneleri Oluşturun

 Başlat`Table`, `TableRow` , Ve`TableCell` nesneler:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## 3. Adım: İçeriği Hücreye Ekleme

 kullanarak hücreye içerik ekleyin.`AppendChildLast` yöntem:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Adım 4: Tablo Düğümünü Başlatın

 Başlat`Table` belirtilen özelliklere sahip nesne:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Adım 5: Tabloya Satır Ekleme

Satır düğümünü tabloya ekleyin:

```csharp
table.AppendChildLast(row);
```

## Adım 6: Tablo Düğümüne Etiket Ekleme

Tablo düğümü için bir etiket ekleyin:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Adım 7: Anahat Öğesine Tablo Düğümü Ekleme

 Oluşturduğunuz bir`Outline` Ve`OutlineElement` tablo düğümünü eklemek için:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Adım 8: Belgeyi Kaydet

OneNote belgesini kaydedin:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Bu adımları izledikten sonra Aspose.Note for .NET'i kullanarak etiketli bir tablo düğümünü başarıyla eklemiş olmalısınız.

## Çözüm

Bu eğitimde Aspose.Note for .NET'te etiketli bir tablo düğümü ekleme sürecini ele aldık. Bu adımları izleyerek OneNote belgelerini programlı bir şekilde verimli bir şekilde yönetebilir ve belge yönetimi yeteneklerinizi geliştirebilirsiniz.

## SSS'ler

### S1: Aspose.Note .NET'in tüm sürümleriyle uyumlu mu?

Cevap1: Aspose.Note for .NET, .NET Core ve .NET Standard dahil olmak üzere .NET Framework 2.0 ve üstünü destekler.

### S2: Lisans satın almadan önce Aspose.Note'u deneyebilir miyim?

 C2: Evet, Aspose.Note'un ücretsiz deneme sürümünü şu adresten edinebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.Note için geçici lisansı nasıl edinebilirim?

 Cevap 3: Geçici lisansı şu adresten alabilirsiniz:[bu bağlantı](https://purchase.aspose.com/temporary-license/)30 gün süreyle geçerlidir.

### S4: Aspose.Note belge şifrelemeyi destekliyor mu?

Cevap4: Evet, Aspose.Note, veri güvenliğini sağlamak amacıyla OneNote belgelerinin şifrelenmesine yönelik destek sağlar.

### S5: Aspose.Note kullanıcıları için teknik destek mevcut mu?

 Cevap5: Evet, teknik destek Aspose forumları aracılığıyla sağlanıyor[Burada](https://forum.aspose.com/c/note/28)uzmanlardan yardım alabileceğiniz yer.
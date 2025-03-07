---
title: Aspose.Note ile Tablo Oluşturun
linktitle: Aspose.Note ile Tablo Oluşturun
second_title: Aspose.Note .NET API'si
description: Aspose.Note for .NET'i kullanarak zengin metin içerikli yapılandırılmış tabloları nasıl oluşturacağınızı öğrenin. Belge organizasyonunu ve okunabilirliğini zahmetsizce geliştirin.
weight: 11
url: /tr/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note ile Tablo Oluşturun

## giriiş

Tablolar, bilgilerin yapılandırılmış sunumuna olanak tanıyan, belgelerin temel bileşenleridir. Aspose.Note for .NET, tabloları zahmetsizce oluşturmak için güçlü araçlar sağlar. Bu eğitimde Aspose.Note'u kullanarak zengin metin içerikli tablolar oluşturma sürecinde size rehberlik edeceğiz.

## Önkoşullar

Aspose.Note for .NET ile tablo kompozisyonuna dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Ortam Kurulumu: .NET Framework veya .NET Core ile uygun bir geliştirme ortamına sahip olduğunuzdan emin olun.
2.  Kurulum: Aspose.Note for .NET'i aşağıdaki adresten indirip yükleyin:[İnternet sitesi](https://releases.aspose.com/note/net/).
3. Temel Bilgi: C# programlama ve belge işlemenin temel kavramlarına aşina olun.

## Ad Alanlarını İçe Aktar

Tablo oluşturmaya başlamadan önce gerekli ad alanlarını içe aktardığınızdan emin olun:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Sağlanan örneği yönetilebilir adımlara ayıralım:

## 1. Adım: Belge Dizinini Ayarlayın

Tabloyu oluşturmadan önce belgenin kaydedileceği dizini tanımlayın.

```csharp
string dataDir = "Your Document Directory";
```

## Adım 2: Başlık Metni Oluşturun

Başlık metnini yazı tipi boyutu ve kalınlık gibi belirli stillerle tanımlayın.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## 3. Adım: Sayfa ve Anahat Oluşturun

İçeriği yapılandırmak için bir sayfa ve bir taslak başlatın.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## 4. Adım: Özet Metni Ekleyin

Tablodan önce bir özet metni ekleyin.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Adım 5: Tablo Oluşturun

Verileri satırlar ve sütunlar halinde düzenlemek için bir tablo başlatın.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Adım 6: Başlık Satırını Ekle

Tabloyu, sütun başlıklarını içeren bir başlık satırıyla doldurun.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Adım 7: Boş Satırları Ekleyin

Veri eklemeye hazırlanmak için boş satırlar ekleyin.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Adım 8: İletişim Bilgilerini Ekleyin

'Kişiler' sütununu şablon içeriğiyle doldurun.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Adım 9: Belgeyi Kaydedin

Oluşturulan tablo belgesini kaydedin.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Adım 10: Onay

Başarılı belge kompozisyonunu onaylayın.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Çözüm

Bu eğitimde Aspose.Note for .NET kullanarak zengin metin içerikli tabloların nasıl oluşturulacağını araştırdık. Bu adım adım talimatları izleyerek belgelerinizde verimli bir şekilde yapılandırılmış tablolar oluşturabilir, okunabilirliği ve düzeni geliştirebilirsiniz.

## SSS'ler

### S1: Tablo öğelerinin stilini özelleştirebilir miyim?
   
Cevap1: Evet, yazı tipi boyutu, renk ve hizalama gibi çeşitli özellikleri gereksinimlerinize uyacak şekilde özelleştirebilirsiniz.

### S2: Aspose.Note diğer .NET kitaplıklarıyla uyumlu mu?
   
Cevap2: Aspose.Note, diğer .NET kitaplıklarıyla sorunsuz bir şekilde bütünleşerek belge işlemede kapsamlı esneklik sunar.

### S3: Aspose.Note tabloların farklı formatlara aktarılmasını destekliyor mu?
   
Cevap3: Kesinlikle Aspose.Note, tabloları PDF, DOCX ve HTML gibi çeşitli formatlara aktarmanıza olanak tanır.

### S4: Tabloları dinamik olarak harici kaynaklardan gelen verilerle doldurabilir miyim?
   
C4: Evet, veritabanlarından, API'lerden veya kullanıcı girişlerinden veri alarak tabloları dinamik olarak doldurabilirsiniz.

### S5: Aspose.Note kullanıcıları için teknik destek mevcut mu?
   
C5: Evet, Aspose, forumları ve özel destek kanalları aracılığıyla kapsamlı teknik destek sağlıyor.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

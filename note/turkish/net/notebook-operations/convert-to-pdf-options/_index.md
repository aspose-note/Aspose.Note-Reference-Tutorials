---
title: Aspose Note .NET'teki Seçeneklerle Not Defterlerini PDF'ye Dönüştürün
linktitle: Aspose Note .NET'teki Seçeneklerle Not Defterlerini PDF'ye Dönüştürün
second_title: Aspose.Note .NET API'si
description: Özelleştirilebilir seçeneklerle Aspose.Note for .NET kitaplığını kullanarak Microsoft OneNote not defterlerini PDF formatına nasıl dönüştüreceğinizi öğrenin.
weight: 16
url: /tr/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose Note .NET'teki Seçeneklerle Not Defterlerini PDF'ye Dönüştürün

## giriiş

Bu eğitimde, Aspose.Note for .NET kütüphanesini kullanarak not defterlerini PDF formatına dönüştürme sürecini anlatacağız. Aspose.Note for .NET, Microsoft OneNote dosyalarıyla programlı olarak çalışmak için güçlü bir dizi özellik sağlar.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

### 1. .NET Kütüphanesi için Aspose.Note
 Aspose.Note for .NET kitaplığını indirip yüklediğinizden emin olun. adresinden indirebilirsiniz.[İnternet sitesi](https://releases.aspose.com/note/net/).

### 2. Geliştirme Ortamı
Gerekli .NET çerçevesinin kurulu olduğu Visual Studio gibi bir geliştirme ortamına sahip olmanız gerekir.

## Ad Alanlarını İçe Aktar

Aspose.Note for .NET'i projemizde kullanmaya başlamadan önce gerekli ad alanlarını içe aktaralım:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Şimdi not defterlerini PDF'ye dönüştürme sürecini seçeneklerle birlikte birden fazla adıma ayıralım:

## 1. Adım: Dizüstü Bilgisayarı Yükleyin

Öncelikle PDF dosyasına dönüştürmek istediğimiz OneNote not defterini yüklememiz gerekiyor.

```csharp
// Belgeler dizininin yolu.
string dataDir = "Your Document Directory";

// OneNote Not Defteri Yükleme
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 2. Adım: PDF Kaydetme Seçeneklerini Belirleyin

Daha sonra not defterini PDF dosyası olarak kaydetme seçeneklerini belirleyeceğiz. Sayfa bölme algoritması, kenar boşlukları ve sayfa boyutu gibi çeşitli ayarları özelleştirebiliriz.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## 3. Adım: Not Defterini PDF olarak kaydedin

Şimdi belirtilen seçenekleri kullanarak not defterini PDF dosyası olarak kaydedeceğiz.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Not Defterini Kaydet
notebook.Save(dataDir, notebookSaveOptions);
```

## 4. Adım: Dönüşümü Doğrulayın

Son olarak dönüşümün başarılı olduğunu doğrulayalım ve PDF dosyasının kaydedildiği konumu yazdıralım.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Çözüm

Bu eğitimde, Aspose.Note for .NET kütüphanesini kullanarak OneNote not defterlerini PDF formatına nasıl dönüştüreceğimizi öğrendik. Yukarıda özetlenen adımları takip ederek bu işlevselliği .NET uygulamalarınıza kolayca entegre edebilirsiniz.

## SSS'ler

### S1: Aspose.Note for .NET, Microsoft OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap1: Evet, Aspose.Note for .NET, .one ve .onetoc2 formatları da dahil olmak üzere Microsoft OneNote'un çeşitli sürümlerini destekler.

### S2: PDF çıktısının görünümünü özelleştirebilir miyim?

Cevap2: Evet, PDF çıktısının görünümünü özelleştirmek için sayfa boyutu, kenar boşlukları ve sayfa bölme algoritması gibi çeşitli seçenekleri belirleyebilirsiniz.

### S3: Aspose.Note for .NET diğer dosya formatları için destek sağlıyor mu?

Cevap3: Evet, Aspose.Note for .NET resimler, HTML ve Microsoft Word belgeleri gibi diğer çeşitli formatlara dönüştürmeyi destekler.

### S4: Aspose.Note for .NET'in ücretsiz deneme sürümü mevcut mu?

Cevap4: Evet, satın almadan önce özelliklerini değerlendirmek için Aspose.Note for .NET'in ücretsiz deneme sürümünü web sitesinden indirebilirsiniz.

### S5: Aspose.Note for .NET için nasıl teknik destek alabilirim?

 Cevap5: Aspose.Note for .NET için teknik destek almak için şu adresi ziyaret edebilirsiniz:[Aspose.Note forumu](https://forum.aspose.com/c/note/28) veya doğrudan Aspose destek ekibiyle iletişime geçin.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

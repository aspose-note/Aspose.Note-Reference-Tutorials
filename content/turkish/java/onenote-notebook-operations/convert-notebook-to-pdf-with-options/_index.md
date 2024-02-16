---
title: OneNote'taki Seçeneklerle Not Defterini PDF'ye Dönüştürme - Aspose.Note
linktitle: OneNote'taki Seçeneklerle Not Defterini PDF'ye Dönüştürme - Aspose.Note
second_title: Aspose.Note Java API'si
description: OneNote not defterlerini kolaylıkla özelleştirin ve PDF'ye aktarın! Aspose.Note for Java ağır yükün üstesinden gelir. Adım adım kılavuz dahil! #OneNote #Java #Aspose
type: docs
weight: 17
url: /tr/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---
## giriiş

Bu eğitimde Aspose.Note for Java'yı kullanarak not defterlerini kişiselleştirilebilir seçeneklerle PDF'ye dönüştürme dünyasını derinlemesine inceleyeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote belgelerini programlı olarak değiştirmelerine olanak tanıyan güçlü bir Java API'sidir. Defterleri PDF formatına dönüştürmek çeşitli uygulamalarda yaygın bir gereksinimdir ve Aspose.Note ile bu görev kolaylaştırılmış ve verimli hale gelir.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun.
2. Aspose.Note for Java: Aspose.Note for Java'yı şu adresten indirip yükleyin:[İndirme: {link](https://releases.aspose.com/note/java/).
3. IDE (Entegre Geliştirme Ortamı): Java geliştirme için tercih ettiğiniz IDE'yi seçin. IntelliJ IDEA, Eclipse veya NetBeans popüler seçimlerdir.

## Paketleri İçe Aktar

Öncelikle gerekli paketleri Java projenize aktarmanız gerekir. Bu paketler, OneNote belgeleriyle çalışmak için gereken sınıfları ve yöntemleri sağlar.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## 1. Adım: OneNote Not Defterini yükleyin

Bir not defterini PDF'ye dönüştürmek için önce OneNote not defterini yüklemeniz gerekir. Not defteri dosyasının yolunun doğru şekilde belirtildiğinden emin olun.

```java
String dataDir = "Your Document Directory";
// OneNote Not Defteri Yükleme
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 2. Adım: PDF Kaydetme Seçeneklerini Belirleyin

Aspose.Note, PDF çıktısını özelleştirmek için çeşitli seçenekler sunar. Sayfa bölme algoritmaları, üstbilgi/altbilgi ayarları ve daha fazlası gibi seçenekleri belirleyebilirsiniz.

```java
// PDF kaydetme seçeneklerini belirtin
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## 3. Adım: Not Defterini PDF olarak kaydedin

Not defterini yükledikten ve kaydetme seçeneklerini belirledikten sonra not defterini PDF dosyası olarak kaydetmenin zamanı geldi.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Not Defterini Kaydet
notebook.save(dataDir, notebookSaveOptions);
```

## Çözüm

Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote not defterlerini PDF formatına nasıl dönüştürebileceğimizi araştırdık. Bu basit adımları izleyerek Java uygulamalarınızdaki belge dönüştürme işlemlerini verimli bir şekilde gerçekleştirebilirsiniz.

---

## SSS'ler

### S1: PDF çıktısının görünümünü özelleştirebilir miyim?

Cevap1: Evet, Aspose.Note, PDF çıktısını özelleştirmek için üstbilgi/altbilgi ayarları, sayfa bölme algoritmaları ve daha fazlası dahil olmak üzere çeşitli seçenekler sunar.

### S2: Aspose.Note, OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note, Microsoft OneNote 2010 ve sonraki sürümlerini destekler.

### S3: Aspose.Note ücretsiz deneme sunuyor mu?

 Cevap3: Evet, Aspose.Note'un ücretsiz deneme sürümünü şu adresten indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S4: Aspose.Note belgelerini nerede bulabilirim?

 Cevap4: Aspose.Note için kapsamlı belgeler bulabilirsiniz.[Burada](https://reference.aspose.com/note/java/).

### S5: Aspose.Note için nasıl destek alabilirim?

 Cevap5: Her türlü teknik yardım veya sorunuz için Aspose.Note destek forumunu ziyaret edebilirsiniz.[Burada](https://forum.aspose.com/c/note/28).
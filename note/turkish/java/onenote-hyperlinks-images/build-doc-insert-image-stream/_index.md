---
date: 2025-12-21
description: Aspose.Note for Java kullanarak OneNote belgesi oluşturmayı ve resimleri
  sorunsuz bir şekilde eklemeyi öğrenin. Java geliştiricileri için adım adım rehber.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Java ile OneNote belgesi nasıl oluşturulur – Belge oluşturma ve akışla resim
  ekleme
url: /tr/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile OneNote belgesi oluşturma – Belge Oluştur ve Akış ile Resim Ekle

## Introduction

Hoş geldiniz! Bu öğreticide **Java ile OneNote belgesi oluşturacak** ve bir görüntü akışı kullanarak resim eklemeyi öğreneceksiniz. Her adımı adım adım gösterecek, her parçanın neden önemli olduğunu açıklayacak ve gerçek projelerde tekniği uygulamanız için pratik ipuçları vereceğiz. Sonunda, OneNote sayfalarını programlı olarak oluşturabilecek ve resimleri tam istediğiniz yere yerleştirebileceksiniz.

## Quick Answers
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java  
- **Akıştan resim ekleyebilir miyim?** Yes – just pass an `InputStream` to the `Image` constructor.  
- **Hangi formata dışa aktarabilirim?** Any format supported by Aspose.Note, e.g., PDF, DOCX, HTML.  
- **Geliştirme için lisansa ihtiyacım var mı?** A free temporary license works for evaluation; a full license is required for production.  
- **Gerekli Java sürümü nedir?** Java 8 or higher.

## “Java ile OneNote belgesi oluşturma” nedir?

Java'da bir OneNote belgesi oluşturmak, Aspose.Note API'sini kullanarak bir not defteri yapısını—sayfalar, taslaklar ve öğeler—programlı olarak inşa etmek anlamına gelir; OneNote masaüstü istemcisini açmadan. Bu yaklaşım, otomatik rapor oluşturma, notların toplu işlenmesi veya OneNote içeriğini daha büyük Java uygulamalarına entegre etme için idealdir.

## Java ile OneNote belgesi oluşturmak için Aspose.Note for Java neden kullanılmalı?

- **Tam kontrol** sayfa düzeni, taslak konumlandırması ve öğe stilinde.  
- **COM etkileşimi yok** – Java'yı destekleyen herhangi bir işletim sisteminde çalışır.  
- **Zengin dışa aktarma seçenekleri** – aynı belgeyi tek bir çağrı ile PDF, DOCX, HTML vb. formatlara dönüştürebilirsiniz.  
- **Akış dostu** – görüntüleri doğrudan bellekten, ağdan veya bulut depolamadan yükleyebilirsiniz.

## Prerequisites

Başlamadan önce, aşağıdakilerin kurulu olduğundan emin olun:

### Java Development Kit (JDK)

Makinenizde yüklü bir JDK (8 veya daha yeni bir sürüm).

### Aspose.Note for Java Library

Kütüphaneyi resmi Aspose sürüm sayfasından indirin: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### IDE Setup

Sevdiğiniz IDE'yi (IntelliJ IDEA, Eclipse, VS Code) Aspose.Note JAR dosyalarını proje sınıf yoluna ekleyecek şekilde yapılandırın.

## Import Packages

Başlamak için gerekli Java ve Aspose.Note sınıflarını içe aktarın. Bu içe aktarmalar belge oluşturma, sayfa işleme, taslak yönetimi ve resim ekleme erişimi sağlar.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step 1: Set Up Document Directory

Kaynak resimlerinizi içeren ve çıktı dosyasının kaydedileceği klasörü tanımlayın. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Create Document Object

Yeni bir `Document` örneği oluşturun. Bu nesne, oluşturduğunuz OneNote not defterini temsil eder.

```java
Document doc = new Document();
```

## Step 3: Initialize Page Object

Bu not defteri sayfası için tüm taslakları ve öğeleri tutacak bir `Page` oluşturun.

```java
Page page = new Page();
```

## Step 4: Create Outline

`Outline`, konumlandırılmış öğeler için bir kapsayıcı görevi görür. Burada taslağı sayfada konumlandırmak için dikey ve yatay offset değerlerini ayarlıyoruz.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Step 5: Create Outline Element

`OutlineElement`, ekleyeceğimiz resmi barındıracak.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Step 6: Load Image Stream

Resim dosyasını bir akış olarak açın. Akış kullanmak, resmi dosya sisteminden, ağdan veya veritabanından önce diske kaydetmeden okumanıza olanak tanır.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Step 7: Insert Image

Bir `Image` nesnesi oluşturun. İlk argüman daha sonra bir akış sağladığınızda `null` olabilir, ancak basitlik açısından burada dosya yolunu referans alıyor ve hizalamasını sayfanın sağ tarafına ayarlıyoruz.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Step 8: Append Image to Outline Element

Resmi, sayfanın görsel hiyerarşisinin bir parçası haline gelmesi için taslak öğesine ekleyin.

```java
outlineElem1.appendChildLast(image);
```

## Step 9: Append Outline Element to Outline

Şimdi resmi içeren taslak öğesini taslak kapsayıcısına bağlayın.

```java
outline1.appendChildLast(outlineElem1);
```

## Step 10: Append Outline to Page

Taslağı sayfaya yerleştirin.

```java
page.appendChildLast(outline1);
```

## Step 11: Append Page to Document

Tamamen oluşturulmuş sayfayı belge nesnesine ekleyin.

```java
doc.appendChildLast(page);
```

## Step 12: Save Document

Son olarak, ihtiyacınız olan formatta OneNote belgesini kaydedin. Bu örnekte PDF olarak dışa aktarıyoruz, ancak Aspose.Note tarafından desteklenen herhangi bir formatı seçebilirsiniz.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Bu adımları izleyerek başarıyla **Java ile OneNote belgesi oluşturmuş** ve bir giriş akışı kullanarak bir resmi gömmüş oldunuz.

## Common Pitfalls & Tips

- **Stream not closed** – In a production scenario, always close the `InputStream` in a `finally` block or use try‑with‑resources.  
- **Incorrect file path** – Double‑check that `dataDir` ends with the appropriate separator (`/` or `\`).  
- **Image alignment** – If the image appears off‑screen, adjust the outline’s `VerticalOffset`/`HorizontalOffset` values.  
- **License exceptions** – Using the evaluation version may add a watermark to the output; apply a valid license to remove it.

## Frequently Asked Questions

### Q1: Is Aspose.Note for Java compatible with all versions of OneNote?

A1: Aspose.Note for Java supports various OneNote file formats, ensuring compatibility across desktop, online, and mobile versions.

### Q2: Can I customize the appearance of inserted images in OneNote documents using Aspose.Note for Java?

A2: Yes, you can modify alignment, size, rotation, and even apply cropping by using the corresponding properties on the `Image` object.

### Q3: Does Aspose.Note for Java provide support for other document formats besides PDF?

A3: Absolutely. The API can export to DOCX, HTML, XPS, and several other formats, giving you flexibility in how you share or archive your notes.

### Q4: Where can I find additional resources and support for Aspose.Note for Java?

A4: The official Aspose website offers extensive documentation, code examples, forums, and temporary licenses for evaluation.

### Q5: Is there a trial version available for Aspose.Note for Java?

A5: Yes, you can download a free trial from the Aspose release page to explore all features before purchasing.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
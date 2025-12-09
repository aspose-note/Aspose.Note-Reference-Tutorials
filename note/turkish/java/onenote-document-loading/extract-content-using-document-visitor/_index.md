---
date: 2025-12-04
description: Aspose.Note kullanarak Java’da OneNote dosyalarından resimleri nasıl
  çıkaracağınızı ve OneNote’u metne nasıl dönüştüreceğinizi öğrenin. Kod örnekleriyle
  adım adım rehber.
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Belge Ziyaretçisi Kullanarak OneNote'tan Görselleri Çıkarma - Java
url: /tr/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'tan Görüntüleri Document Visitor Kullanarak Çıkarma - Java

## Introduction

Aspose.Note for Java, Java'da temel `.one` dosyasını okumanın yanı sıra **OneNote** defterlerinden görüntüleri **çıkarmayı** kolaylaştırır. Bu öğreticide, bir OneNote dosyasını nasıl yükleyeceğinizi, özel bir `DocumentVisitor` ile yapısını nasıl dolaşacağınızı ve hem görüntüleri hem de düz metni nasıl çıkaracağınızı gösteren eksiksiz, uygulamalı bir örnek üzerinden sizi yönlendireceğiz. Sonunda, yalnızca metin içeriğine ihtiyacınız varsa **OneNote'u metne dönüştürmeyi** de öğreneceksiniz.

## Quick Answers
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java (aşağıdaki indirme bağlantısı).  
- **Sadece görüntüleri çıkarabilir miyim?** Evet – bir `DocumentVisitor` içinde `VisitImageStart` metodunu uygulayın.  
- **Java'da .one dosyasını nasıl okurum?** `new Document(path, new LoadOptions())` kullanın.  
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için ticari bir lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** JDK 8 ve üzeri.

## Prerequisites

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Java Development Kit (JDK) 8 veya daha yeni bir sürüm yüklü.  
2. Aspose.Note for Java kütüphanesini indirdiniz. **[buradan](https://releases.aspose.com/note/java/)** indirebilirsiniz.  
3. Görüntüleri çıkarmak veya metne dönüştürmek istediğiniz bir OneNote belgesi (`.one` dosyası).

## Import Packages

İlk olarak, Aspose.Note API'sinden gerekli sınıfları içe aktarın.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Step 1: Set Up a Custom Document Visitor

`DocumentVisitor` sınıfını genişleten bir sınıf oluşturun. Bu sınıf, OneNote belgesindeki her düğüm için çağrılacak ve **OneNote'tan görüntüleri çıkarmanıza** ve isteğe bağlı olarak metin toplamanıza olanak tanıyacak.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Step 2: Implement Visitor Methods

İlgilendiğiniz düğüm tipleri için geçersiz kılmalar ekleyin. Aşağıda zengin metin, görüntüler, başlıklar, sayfalar, anahatlar ve anahat öğeleri ele alıyoruz. Görüntü çıkarma işlemi `VisitImageStart` metodunda gerçekleşir.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Why implement these methods?

- **OneNote'tan görüntüleri çıkarmak:** `VisitImageStart` ham görüntü baytlarına doğrudan erişim sağlar.  
- **OneNote'u metne dönüştürmek:** `VisitRichTextStart` metin içeriğini toplar ve basit bir **OneNote'u metne dönüştür** işlemini mümkün kılar.  
- **.one dosyasını Java'da okumak:** Ziyaretçi deseni, temel `.one` dosya yapısını soyutlar, böylece ikili formatı kendiniz ayrıştırmanız gerekmez.

## Step 3: Run the Visitor from Your Main Method

`.one` dosyasını yükleyin, ziyaretçinizi örnekleyin ve dolaşımı başlatın.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Common Use Cases

- **Otomatik raporlama:** Bir OneNote toplantı defterinden görüntü ve metni çekerek PDF veya HTML özeti oluşturun.  
- **İçerik taşıma:** Eski OneNote arşivlerini indeksleme veya arama motoru alımı için düz metin dosyalarına dönüştürün.  
- **Dijital varlık çıkarma:** Gömülü ekran görüntülerini, diyagramları veya fotoğrafları diğer uygulamalarda yeniden kullanmak üzere toplayın.

## Troubleshooting & Tips

- **Büyük defterler:** Bellek sorunlarıyla karşılaşırsanız, `VisitPageStart` kontrol ederek sayfaları tek tek işleyin ve yalnızca gerektiğinde sayfa‑seviyesi kaynakları yükleyin.  
- **Görüntü formatları:** `Image` nesnesi ham baytları döndürür; kaydetmeden önce formatı (PNG, JPEG) tespit etmeniz gerekebilir.  
- **Lisans hataları:** Üretimde belgeyi yüklemeden önce Aspose lisansını ayarladığınızdan emin olun (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`).

## Frequently Asked Questions

**S: OneNote belgesinden belirli içerik türlerini çıkarabilir miyim?**  
C: Evet – yalnızca ihtiyacınız olan ziyaretçi metodlarını geçersiz kılarak (ör. görüntüler için `VisitImageStart`, metin için `VisitRichTextStart`) yapabilirsiniz.

**S: Aspose.Note for Java, farklı OneNote belge sürümleriyle uyumlu mu?**  
C: Kesinlikle. Kütüphane tüm ana OneNote dosya sürümlerini destekler, bu yüzden kaynak OneNote sürümünden bağımsız olarak **.one dosyasını Java'da okuyabilirsiniz**.

**S: Bu çıkarma sürecini Java uygulamama entegre edebilir miyim?**  
C: Evet. Ziyaretçi deseni herhangi bir Java kod tabanında sorunsuz çalışır; sadece kütüphane JAR'ını ekleyin ve yukarıdaki örneği çağırın.

**S: Aspose.Note for Java, karmaşık OneNote belgelerini işlemek için destek sağlıyor mu?**  
C: Sağlıyor. İç içe anahatlar, gömülü medya ve özel veriler tümü ziyaretçi API'si aracılığıyla erişilebilir.

**S: İşlenebilecek OneNote belgesinin boyutu konusunda bir sınırlama var mı?**  
C: Katı bir sınır yoktur, ancak çok büyük defterler daha fazla yığın (heap) belleği gerektirebilir; bunları sayfa sayfa işlemek mantıklı olabilir.

**S: Çıkarılan metni düz metin dosyasına nasıl dönüştürürüm?**  
C: `myConverter.GetText()` bir `String` döndürdükten sonra, standart Java I/O kullanarak dosyaya yazın (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Son Güncelleme:** 2025-12-04  
**Test Edilen Versiyon:** Aspose.Note for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
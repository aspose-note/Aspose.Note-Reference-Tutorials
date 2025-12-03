---
date: 2025-12-03
description: Aspose.Note for Java kullanarak OneNote'u metne nasıl dönüştüreceğinizi
  öğrenin. Metin çıkarma, resim çıkarma ve OneNote dosyalarını nasıl okuyacağınızı
  kapsayan adım adım rehber.
language: tr
linktitle: Convert OneNote to Text with Document Visitor – Java
second_title: Aspose.Note Java API
title: Document Visitor ile OneNote'u Metne Dönüştür – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u Metne Dönüştürme – Document Visitor – Java

## Giriş

Bu öğreticide Aspose.Note for Java'nın Document Visitor'ını kullanarak **OneNote'u metne nasıl dönüştüreceğinizi** öğreneceksiniz. OneNote dosyalarını programlı olarak okumanız, düz metin içeriğini çıkarmanız ya da gömülü resimleri almanız gerekse, Document Visitor .one belgesindeki her düğüm üzerinde ayrıntılı kontrol sağlar.

## Hızlı Yanıtlar
- **“OneNote'u metne dönüştürmek” ne anlama geliyor?** .one dosyasından düz metin temsili (ve isteğe bağlı olarak resimler) çıkarmak demektir.  
- **Bu konuda hangi kütüphane yardımcı olur?** Aspose.Note for Java `DocumentVisitor` API'sini sağlar.  
- **Lisans gerekli mi?** Değerlendirme için ücretsiz deneme çalışır; üretim için ücretli lisans gerekir.  
- **Resimleri de çıkarabilir miyim?** Evet – resimleri almak için `VisitImageStart` metodunu uygulayın.  
- **Önkoşullar nelerdir?** Java JDK 8+, Aspose.Note for Java JAR ve işlenecek bir .one dosyası.

## “OneNote'u metne dönüştürmek” nedir?
OneNote'u metne dönüştürmek, bir OneNote (.one) dosyasını programlı olarak okuyup metin içeriğini, başlıkları ve diğer öğeleri orijinal OneNote arayüzü olmadan elde etmek anlamına gelir. Bu, arama indeksleme, raporlama veya içeriği diğer platformlara taşıma gibi senaryolar için faydalıdır.

## Neden Document Visitor'ı **OneNote dosyalarını okumak** için kullanmalısınız?
The Document Visitor follows the Visitor design pattern, allowing you to walk through every element (pages, outlines, images, rich‑text runs, etc.) in a OneNote document. Compared with loading the whole document into memory and parsing it manually, the visitor approach is:

* **Bellek‑verimli** – düğümleri tek tek işler.  
* **Genişletilebilir** – herhangi bir düğüm türü için özel mantık ekleyebilirsiniz (ör. resimleri çıkarmak).  
* **Doğru** – orijinal hiyerarşiyi korur, gizli içeriği kaçırmadığınızdan emin olur.

## Önkoşullar

1. **Java Development Kit (JDK) 8 veya üzeri** yüklü.  
2. **Aspose.Note for Java** kütüphanesini resmi siteden indirin – [buradan indirin](https://releases.aspose.com/note/java/).  
3. Metne dönüştürmek istediğiniz bir **OneNote belgesi** (`.one` dosyası).

## Adım 1: Paketleri İçe Aktarın

First, import the classes you’ll need to work with Aspose.Note for Java.

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

## Adım 2: Document Visitor Sınıfını Kurun

Create a class that extends `DocumentVisitor`. This custom visitor will collect text, count nodes, and (if you wish) store images.

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

## Adım 3: Visitor Metodlarını Uygulayın  

Here we implement the callbacks for the node types we care about. The methods increment a node counter and, for `RichText`, append the actual text to our `StringBuilder`. You can also add logic to **extract images from OneNote** by handling `VisitImageStart`.

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
    // Pro tip: you can save the image stream here if you need to extract images.
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

## Adım 4: Ana Metot – Visitor'ı Çalıştırın

The `main` method loads a OneNote file, creates an instance of our custom visitor, and starts the traversal. After visiting, we print the extracted text and the total node count.

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
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## Yaygın Kullanım Senaryoları – **OneNote'tan resim çıkarmak**

* **Arama indeksleme** – OneNote defterlerini tam metin arama motorları için düz metne dönüştürün.  
* **İçerik taşıma** – Notları bir CMS veya dokümantasyon portalına taşıyın.  
* **Veri analitiği** – Doğal dil işleme veya görüntü analizi için metin ve resimleri çıkarın.  

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **.one dosyası okunurken NullPointerException** | Dosya yolunun (`dataDir`) bir yol ayırıcı (`/` veya `\\`) ile bittiğinden ve dosyanın mevcut olduğundan emin olun. |
| **Resimler çıkarılmıyor** | `VisitImageStart` içinde `image.getImageData()`'yı bir dosyaya veya akışa yazmak için mantık ekleyin. |
| **Büyük defterler yüksek bellek kullanımı oluşturur** | Belgeyi sayfa sayfa işleyin veya mümkünse akış API'lerini kullanın. |

## Sıkça Sorulan Sorular

**S: OneNote belgesinden belirli içerik türlerini çıkarabilir miyim?**  
C: Evet, sadece ihtiyacınız olan visitor metodlarını uygulayarak (ör. metin için `VisitRichTextStart`, resimler için `VisitImageStart`).

**S: Aspose.Note for Java farklı OneNote dosya sürümleriyle uyumlu mu?**  
C: Kesinlikle. Kütüphane, Microsoft OneNote'un son sürümleriyle oluşturulan .one dosyalarını destekler.

**S: Bu çıkarma sürecini Java uygulamama entegre edebilir miyim?**  
C: Evet. Gösterilen kod, doğrudan herhangi bir Java projesine yerleştirilebilecek bağımsız bir örnektir.

**S: Aspose.Note for Java karmaşık OneNote yapılarıyla başa çıkabilir mi?**  
C: Evet. Visitor deseni, hiyerarşiyi kaybetmeden iç içe geçmiş taslakları, grupları ve gömülü nesneleri dolaşmanıza olanak tanır.

**S: İşlenebilecek OneNote belgesinin boyutu için bir sınırlama var mı?**  
C: Katı bir sınırlama yoktur, ancak çok büyük defterler daha fazla yığın belleği gerektirebilir; bunları artımlı olarak işlemeyi düşünün.

**S: OneNote'tan nasıl resim çıkarırım?**  
C: `VisitImageStart` metodunu uygulayarak `image.getImageData()`'ya erişin ve baytları bir dosyaya yazın.

---

**Last Updated:** 2025-12-03  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
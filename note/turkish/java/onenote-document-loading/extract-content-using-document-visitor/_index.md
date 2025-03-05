---
title: Belge Ziyaretçisini kullanarak OneNote İçeriğini Çıkarma - Java
linktitle: Belge Ziyaretçisini kullanarak OneNote İçeriğini Çıkarma - Java
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak Java'daki OneNote belgelerinden içeriği nasıl çıkaracağınızı öğrenin. Sağlanan kod örnekleriyle adım adım eğitim.
type: docs
weight: 21
url: /tr/java/onenote-document-loading/extract-content-using-document-visitor/
---
## giriiş

Aspose.Note for Java, OneNote belgelerinden içerik çıkarmak için güçlü özellikler sunar. Bu öğreticide, Java'daki Belge Ziyaretçisini kullanarak OneNote belgesinden içerik çıkarma sürecinde size yol göstereceğiz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde Java Geliştirme Kiti (JDK) yüklü.
2.  Aspose.Note for Java kütüphanesi indirildi. İndirebilirsin[Burada](https://releases.aspose.com/note/java/).
3. İçeriğin ayıklanacağı bir OneNote belgesi (.one uzantılı).

## Paketleri İçe Aktar

Öncelikle Aspose.Note for Java ile çalışmak için gerekli paketleri içe aktarmanız gerekir.

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

## 1. Adım: Belge Ziyaretçi Sınıfını Ayarlayın

genişleten bir sınıf oluşturun.`DocumentVisitor` Java için Aspose.Note tarafından sağlanan sınıf. Bu sınıf, belgenin farklı düğümlerini ziyaret etmeyi ele alacaktır.

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
    
    // Burada başka yöntemler de uygulanacak
}
```

## 2. Adım: Ziyaretçi Yöntemlerini Uygulayın

Belgede işlemek istediğiniz farklı düğüm türleri için ziyaretçi yöntemlerini uygulayın. Bu örnekte RichText, Document, Page, Title, Image, OutlineGroup, Outline ve OutlineElement düğümleri için yöntemler uygulayacağız.

```java
// Farklı düğüm türleri için ziyaretçi yöntemleri

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

## Adım 3: Ana Yöntem

Ana yöntemde OneNote belgesini yükleyin, özel Belge Ziyaretçisi sınıfınızın bir örneğini oluşturun ve ziyaretçinin ziyaret sürecini başlatmasını kabul edin.

```java
public static void main(String[] args) throws IOException {
    // Dönüştürmek istediğimiz belgeyi açın.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // DocumentVisitor sınıfından miras alan bir nesne oluşturun.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Ziyaret sürecini başlatmak için ziyaretçiyi kabul edin.
    doc.accept(myConverter);
    
    // İşlemin sonucunu alın.
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## Çözüm

Bu eğitimde Aspose.Note for Java'yı kullanarak bir OneNote belgesinden nasıl içerik çıkaracağınızı öğrendiniz. Özel bir Belge Ziyaretçisi sınıfı uygulayarak ve belgenin farklı düğümlerini ziyaret ederek, gereksinimlerinize göre içeriği etkili bir şekilde çıkarabilir ve işleyebilirsiniz.

## SSS'ler

### S1: OneNote belgesinden belirli içerik türlerini çıkarabilir miyim?

Cevap1: Evet, farklı düğüm türleri için belirli ziyaretçi yöntemleri uygulayarak metin, resim, başlık vb. içerikleri seçerek çıkarabilirsiniz.

### S2: Aspose.Note for Java, OneNote belgelerinin farklı sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note for Java, OneNote belgelerinin çeşitli sürümlerini destekleyerek içeriğin uyumluluğunu ve sorunsuz şekilde çıkarılmasını sağlar.

### S3: Bu çıkarma işlemini Java uygulamama entegre edebilir miyim?

Cevap3: Kesinlikle, verilen eğitimi takip ederek içerik çıkarma sürecini Java uygulamalarınıza kolayca entegre edebilirsiniz.

### S4: Aspose.Note for Java, karmaşık OneNote belgelerinin işlenmesi için destek sağlıyor mu?

Cevap4: Evet, Aspose.Note for Java, OneNote belgeleri içindeki karmaşık yapıların ve içeriğin işlenmesi için kapsamlı destek sunar.

### S5: Aspose.Note for Java kullanılarak işlenebilecek OneNote belgesinin boyutunda herhangi bir sınır var mı?

Cevap5: Aspose.Note for Java, çeşitli boyutlardaki OneNote belgelerini verimli bir şekilde işleyecek ve büyük belgelerde bile en iyi performansı sağlayacak şekilde tasarlanmıştır.
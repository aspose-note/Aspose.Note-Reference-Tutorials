---
date: 2026-02-10
description: Aspose.Note for Java ile OneNote'u metne dönüştürmeyi ve resimleri çıkarmayı
  öğrenin. Rehber, .one dosyasını Java ile nasıl okuyacağınızı ve OneNote metin çıkarımını
  nasıl gerçekleştireceğinizi gösterir.
linktitle: Convert OneNote to Text and Extract Images using Document Visitor - Java
second_title: Aspose.Note Java API
title: OneNote'u Metne Dönüştür ve Görselleri Belge Ziyaretçisi ile Çıkar - Java
url: /tr/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u Metne Dönüştürme ve Document Visitor Kullanarak Görüntüleri Çıkarma - Java

## Giriş

Aspose.Note for Java, **OneNote'u metne dönüştürmeyi** ve aynı zamanda **OneNote'tan görüntüleri çıkarmayı** kolaylaştırır. Bu öğreticide, bir OneNote dosyasını nasıl yükleyeceğinizi, özel bir `DocumentVisitor` ile yapısını nasıl dolaşacağınızı ve hem görüntüleri hem de düz metni nasıl çıkaracağınızı adım adım göstereceğiz. Sonunda **.one dosyasını java** projelerinde nasıl okuyacağınızı ve bu yaklaşımın otomatik içerik taşıma veya raporlama için neden ideal olduğunu da öğreneceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java (aşağıdaki indirme bağlantısı).  
- **Sadece görüntüleri çıkarabilir miyim?** Evet – bir `DocumentVisitor` içinde `VisitImageStart` metodunu uygulayın.  
- **Java'da .one dosyasını nasıl okurum?** `new Document(path, new LoadOptions())` kullanın.  
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için ticari bir lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** JDK 8 ve üzeri.

## OneNote'u Metne Dönüştürme Nedir?

OneNote'u metne dönüştürmek, bir `.one` defterindeki ham metin içeriğini çıkarmak ve bunu düz Unicode metni olarak kaydetmek anlamına gelir. Bu, aranabilir arşivlere, hafif veri akışlarına veya orijinal OneNote biçimlendirmesi olmadan basit özetlere ihtiyaç duyduğunuzda faydalıdır.

## Neden Aspose.Note'un Document Visitor'ını OneNote metin çıkarımı için kullanmalıyız?

- **İnce ayarlı kontrol:** Visitor deseni, hangi düğümleri (sayfalar, anahatlar, görüntüler, zengin metin) işlemek istediğinizi tam olarak belirlemenizi sağlar.  
- **Performans:** Tüm belgeyi tek bir blok olarak belleğe yüklemekten kaçınırsınız; her düğüm ihtiyaç duyulduğunda ziyaret edilir.  
- **Çok yönlülük:** Aynı visitor, görüntüleri, tabloları veya özel meta verileri çıkarmak için genişletilebilir ve **onenote'u metne dönüştürme** ve **görüntüleri çıkarma** görevleri için tek durak çözüm sunar.

## Ön Koşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

1. Java Development Kit (JDK) 8 veya daha yeni bir sürüm yüklü.  
2. Aspose.Note for Java kütüphanesini indirdiniz. **[buradan](https://releases.aspose.com/note/java/)** indirebilirsiniz.  
3. Görüntüleri çıkarmak ya da metne dönüştürmek istediğiniz bir OneNote belgesi (`.one` dosyası).

## Paketleri İçe Aktarma

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

## Adım 1: Özel Bir Document Visitor Oluşturun

`DocumentVisitor` sınıfını genişleten bir sınıf oluşturun. Bu sınıf, OneNote belgesindeki her düğüm için çağrılacak ve **OneNote görüntülerini çıkarmanıza** ve isteğe bağlı olarak metin toplamanıza olanak tanır.

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

## Adım 2: Visitor Metodlarını Uygulayın

İlgilendiğiniz düğüm tipleri için geçersiz kılmalar ekleyin. Aşağıda zengin metin, görüntüler, başlıklar, sayfalar, anahatlar ve anahat öğeleri işleniyor. Görüntü çıkarımının gerçekleştiği yer `VisitImageStart` metodudur.

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

### Bu metodları neden uygulamalısınız?

- **OneNote'tan görüntü çıkarma:** `VisitImageStart` size ham görüntü baytlarına doğrudan erişim sağlar.  
- **OneNote'u metne dönüştürme:** `VisitRichTextStart` metin içeriğini toplar ve basit bir **OneNote'u metne dönüştürme** işlemi sağlar.  
- **.one dosyasını Java'da okuma:** Visitor deseni, alttaki `.one` dosya yapısını soyutlar, böylece ikili formatı kendiniz ayrıştırmanız gerekmez.

## Adım 3: Visitor'ı Ana Metodunuzdan Çalıştırın

`.one` dosyasını yükleyin, visitor'ınızı örnekleyin ve gezintiye başlayın.

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

## Yaygın Kullanım Senaryoları

- **Otomatik raporlama:** Bir OneNote toplantı defterinden görüntü ve metni çekerek PDF veya HTML özeti oluşturun.  
- **İçerik taşıma:** Eski OneNote arşivlerini indeksleme veya arama motoru alımı için düz metin dosyalarına dönüştürün.  
- **Dijital varlık çıkarma:** Gömülü ekran görüntülerini, diyagramları veya fotoğrafları diğer uygulamalarda yeniden kullanmak üzere toplayın.  

## Sorun Giderme ve İpuçları

- **Büyük defterler:** Bellek sorunlarıyla karşılaşırsanız, `VisitPageStart` kontrol ederek sayfaları tek tek işleyin ve sayfa‑seviyesi kaynakları yalnızca gerektiğinde yükleyin.  
- **Görüntü formatları:** `Image` nesnesi ham baytları döndürür; kaydetmeden önce formatı (PNG, JPEG) tespit etmeniz gerekebilir.  
- **Lisans hataları:** Üretimde belgeyi yüklemeden önce Aspose lisansını ayarladığınızdan emin olun (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`).  
- **Görüntüleri verimli çıkarma:** Sadece belirli görüntü türlerine ihtiyacınız varsa, `VisitImageStart` içinde düğümleri boyut veya formata göre filtreleyin.  

## Sıkça Sorulan Sorular

**S: OneNote belgesinden belirli türde içerik çıkarabilir miyim?**  
C: Evet – sadece ihtiyacınız olan visitor metodlarını geçersiz kılarak (ör. görüntüler için `VisitImageStart`, metin için `VisitRichTextStart`) yapabilirsiniz.

**S: Aspose.Note for Java, farklı OneNote belge sürümleriyle uyumlu mu?**  
C: Kesinlikle. Kütüphane tüm büyük OneNote dosya sürümlerini destekler, bu yüzden kaynak OneNote sürümünden bağımsız olarak **.one dosyasını java** projelerinde güvenle okuyabilirsiniz.

**S: Bu çıkarım sürecini Java uygulamama entegre edebilir miyim?**  
C: Evet. Visitor deseni, herhangi bir Java kod tabanında sorunsuz çalışır; sadece kütüphane JAR'ını ekleyin ve yukarıdaki örneği çağırın.

**S: Aspose.Note for Java, karmaşık OneNote belgelerini işlemek için destek sağlıyor mu?**  
C: Sağlıyor. İç içe anahatlar, gömülü medya ve özel veriler visitor API aracılığıyla erişilebilir.

**S: İşlenebilecek OneNote belgesi boyutu konusunda bir sınırlama var mı?**  
C: Katı bir sınır yoktur, ancak çok büyük defterler daha fazla yığın belleği gerektirebilir; bunları sayfa sayfa işlemek mantıklı olabilir.

**S: Çıkarılan metni düz metin dosyasına nasıl dönüştürürüm?**  
C: `myConverter.GetText()` bir `String` döndürdükten sonra, standart Java I/O ile dosyaya yazın (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---

**Son Güncelleme:** 2026-02-10  
**Test Edilen Versiyon:** Aspose.Note for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
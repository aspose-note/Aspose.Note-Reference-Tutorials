---
date: 2026-01-23
description: Aspose.Note for Java ile OneNote'tan tablo metnini nasıl çıkaracağınızı
  öğrenin. Bu adım adım kılavuz, tablolardan metin nasıl çıkarılacağını ve hatta OneNote
  tablo metnini daha fazla işleme için nasıl dönüştürebileceğinizi gösterir.
linktitle: How to Extract Table Text from OneNote Using Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note Kullanarak OneNote'tan Tablo Metnini Nasıl Çıkarabilirsiniz
url: /tr/java/onenote-table-manipulation/extract-text-from-table/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'tan Aspose.Note Kullanarak Tablo Metni Nasıl Çıkarılır

## Giriş
Java uygulamanızda OneNote dosyalarıyla çalışıyorsanız, raporlama, veri analizi veya taşıma amaçları için tabloların içeriğini çıkarmanız sıkça gerekebilirisini** hızlı ve güvenilir bir şekilde Aspose.Note kütüphanesini kullanarak nasıl çıkaracağınızı öğreneceksiniz. `.one` adım göstere küt.Note for Java (en son sürüm).  
- **Lisans gerekli mi?** Test için geçici bir lisans yeterli; üretim için tam lisans gerekir.  
- **OneNote tablo metnini başka bir formata dönüştürebilir miyim?** Evet—çıkarılan dizeyi CSV, JSON veya ihtiyacınız olan herhangi bir formatta kaydedebilirsiniz.  
- sürer.

## “Tablo nasıl çıkarılır” OneNote bağlamında ne anlama geliyor?
Note tablo düğümünün her hücresinde depolanan metin içeriğini okuyup düz metin temsiline dönüştürmek anlamına gelir. Bu, **tabloların metnini çıkarmak** gerektiğinde raporlar oluşturmak veya veriyi başka sistemlere aktarmak gibi işlemler için faydalıdır.

## Tablo metni çıkarmak için Aspose.Note neden kullanılmalı?
- **OneNote dosya yapısı üzerinde tam kontrol**; Microsoft Office y, hazır:

amı** – JDK 8 veya üzeri yüklü ve yapılandırılmış.  
- **Aspose.Note Kütüphanesi** – resmi sürüm sayfasından en son JAR dosyasını indirin [burada](https://releases.aspose.com/note/java/).  
- **Örnek bir OneNote dosyası** (`Sample1.one`) kodunuzdan erişebileceğiniz bir klasöre yerleştirilmiş.

## Paketleri İçe Aktarma
Java projenizde aktarın. Bu blok değişmeden kalır:

```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.Table;
```

## Adım‑Adım Kılavuz

### Adım 1: Belgeyi Yükleyin
`.one` dosyanızın bulunduğu klasöre işaret edin ve bir `Document` örneği oluşturun.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document document = new Document(dataDir + "Sample1.one");
// Get a list of table nodes
List<Table> nodes = document.getChildNodes(Table.class);
// Load the document into Aspose.Note
Document document = new Document(dataDir + "Sample1.one");
```

> **İpucu:** `dataDir` yolunu mutlak tutun veya platform‑özel sorunları önlemek için `Paths.get()` kullanın.

### Adım 2: Tablo Düğümlerini Alın
Belgedeki tüm tablo düğümlerini alın. Bu, üzerinde döngü kurabileceğiniz bir koleksiyon sağlar.

```java
// Get a list of table nodes
List<Table> nodes = document.getChildNodes(Table.class);
```

### Adım 3: Tabloları Döngüyle İşleyin
Her tabloyu dolaşın ve indeksini yazdırın. Bu, belge birden fazla tablo içerdiğinde hangi tabloyu işlediğinizi belirlemenize yardımcı olur.

```java
for (int i = 0; i < nodes.size(); i++) {
    Table table = nodes.get(i);
    System.out.println("Table # " + i);
```

### Adım 4: Tablo Metnini Alın
Mevcut tablodan `RichText` nesnelerini çıkarın, metinlerini birleştirin ve bir `StringBuilder` içinde saklayın.

```java
// Retrieve text
List<RichText> textNodes = (List<RichText>) table.getChildNodes(RichText.class);
StringBuilder text = new StringBuilder();
for (RichText richText : textNodes) {
    text = text.append(richText.getText().toString());
}
```

> **Neden önemli:** `RichText` sınıfı biçimlendirmeyi yakalar, ancak `getText()` çağrısı, sonraki işleme veya dönüştürmeye ihtiyaç duyduğunuz düz dizeyi döndürür.

### Adım 5: Metni Yazdırın
Son olarak, çıkarılan metni konsola gösterin. Gerçek bir senaryoda bu dizeyi bir dosyaya, veritabanına yazabilir veya CSV’ye dönüştürebilirsiniz.

```java
// Print text on the output screen
System.out.println(text);
```

Bu adımları dikkatle izleyerek OneNote belgelerinizdeki **tabloların metnini** etkili bir şekilde çıkarabilirsiniz.

## Yaygın Sorunlar & Çözümler
| Sorun | Açıklama | Çözüm |
|-------|----------|------|
| `NullPointerException` `getChildNodes` çağrılırken | Belge hiçbir tablo içermiyor olabilir. | Döngü kurmadan önce `nodes.isEmpty()` kontrol edin. |
| ASCII olmayan karakterlerde kodlama sorunları | Aspose.Note Unicode döndürür, ancak konsol bunu desteklemeyebilir. | Konsarlayın (`System.out` sarm sürümü lisans ayarl uyumlu olacak şekildeasyon sağlar.

**S: Aspose.Note’u kişisel ve ticari projelerde kullanabilir miyim?**  
C: Evet, Aspose.Note’u kişisel ve ticari projelerde kullanabilirsiniz. Lisans detaylarını [burada](https://purchase.aspose.com/buy) inceleyin.

**S: Test amaçlı geçici bir lisansa ihtiyacım var mı?**  
C: Evet, değerlendirme için geçici bir lisans mevcuttur. [Bu bağlantıdan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

**S: Aspose.Note için topluluk desteği nerede bulunur?**  
C: Topluluk desteği [Aspose.Note forumlarında](https://forum.aspose.com/c/note/28) mevcuttur.

**S: Aspose.Note kütüphanesini nasıl satın alabilirim?**  
C: Kütüphaneyi doğrudan [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-23  
**Test Edilen Vers
---
date: 2026-02-28
description: Aspose.Note for Java kullanarak OneNote dosyalarından etiketleri nasıl
  çıkaracağınızı öğrenin. Bu öğreticide OneNote dosyasını nasıl yükleyeceğiniz, OneNote
  etiketlerini nasıl alacağınız ve OneNote etiketlerini verimli bir şekilde nasıl
  değiştireceğiniz gösterilmektedir.
linktitle: How to Extract Tags from OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note ile OneNote'tan Etiketleri Nasıl Çıkarabilirsiniz
url: /tr/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'tan Etiketleri Nasıl Çıkarabilirsiniz Aspose.Note ile

## Giriş
OneNote belgesinden **etiketleri nasıl çıkaracağınızı** öğrenmeniz gerekiyorsa, doğru yerdesiniz. Bu rehberde bir OneNote dosyasını yükleme, OneNote etiketlerini alma ve hatta bu etiketleri Aspose.Note for Java kullanarak değiştirme sürecini adım adım inceleyeceğiz. Eğitimin sonunda etiket çıkarımını herhangi bir Java uygulamasına güvenle entegre edebileceksiniz.

## Hızlı Yanıtlar
- **OneNote dosyasını açmak için birincil sınıf nedir?** `Document`
- **Tüm RichText düğümlerini döndüren yöntem hangisidir?** `doc.getChildNodes(RichText.class)`
- **Bir NoteTag'in oluşturulma zamanını okuyabilir misiniz?** Evet, `noteTag.getCreationTime()` ile
- **Üretim kullanımı için lisansa ihtiyacım var mı?** Evet, geçerli bir Aspose.Note lisansı gereklidir
- **API, Java 8 ve üzeri sürümlerle uyumlu mu?** Kesinlikle, modern Java sürümlerini destekler

## OneNote'ta “etiketleri nasıl çıkaracağınız” nedir?
Etiketleri çıkarmak, OneNote'un paragraflara, onay kutularına veya diğer içerik öğelerine eklediği meta verileri (durum, etiket, simge ve zaman damgaları gibi) okumak anlamına gelir. Bu etiketler, `RichText` düğümleri içinde `NoteTag` nesneleri olarak depolanır.

## Etiket çıkarımı için neden Aspose.Note kullanmalı?
- **OneNote kurulumu gerekmez** – .one dosyalarıyla doğrudan çalışın.
- **Tam kontrol** – etiket özelliklerini programlı olarak alabilir, okuyabilir ve değiştirebilirsiniz.
- **Çapraz platform** – Java'yı destekleyen herhangi bir işletim sisteminde çalışır.

## Önkoşullar
- Java geliştirme ortamı (JDK 8+).
- Aspose.Note kütüphanesi [buradan](https://releases.aspose.com/note/java/) indirilebilir.
- Bilinen bir dizine yerleştirilmiş örnek bir OneNote belgesi (ör. `Sample1.one`).

## Paketleri İçe Aktarma
İhtiyacınız olan sınıfları içe aktararak başlayın. Bu importlar belge işleme, etiket arabirimleri ve zengin metin düğümlerine erişim sağlar.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## OneNote Dosyasını Nasıl Yükleyebilirsiniz
İlk adım, OneNote dosyasını bir `Document` nesnesine yüklemektir.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
```

> **Pro ipucu:** `dataDir` yolunu mutlak tutun veya yol hatalarını önlemek için `Paths.get(...)` kullanın.

## OneNote Etiketlerini Nasıl Alabilirsiniz
Belge yüklendikten sonra, tüm `RichText` düğümlerini alın. Her düğüm bir veya daha fazla etiket içerebilir.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## Her Düğüm Üzerinde Döngü
Her `RichText` düğümünü döngüye alarak etiketlerini inceleyin.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## NoteTag'leri Alın (OneNote Etiketlerini Nasıl Değiştirebilirsiniz)
Döngü içinde, bir etiketin `NoteTag` olup olmadığını kontrol edin. Eğer öyleyse, özelliklerini okuyabilir veya gerekirse değiştirebilirsiniz.

```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Retrieve properties
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
        // Example of modifying a property
        // noteTag.setLabel("Updated Label");
    }
}
```

> **Uyarı:** Bir etiketi değiştirmek temel belgeyi değiştirir. Değişiklik yaptıktan sonra belgeyi kaydetmeyi unutmayın.

## Sonuç
Artık **etiketleri nasıl çıkaracağınızı**, **OneNote dosyasını nasıl yükleyeceğinizi**, **OneNote etiketlerini nasıl alacağınızı** ve hatta Aspose.Note for Java kullanarak **OneNote etiketlerini nasıl değiştireceğinizi** biliyorsunuz. Bu kod parçacıklarını kendi projelerinize entegre ederek not analizi, raporlama veya taşıma görevlerini otomatikleştirebilirsiniz.

## SSS
### Aspose.Note tüm OneNote sürümleriyle uyumlu mu?
Aspose.Note, çeşitli OneNote dosya formatlarını destekler ve farklı sürümler arasında uyumluluk sağlar.

### Alınan NoteTag özelliklerini değiştirebilir miyim?
Evet, Aspose.Note, NoteTag özelliklerini programlı olarak değiştirmenize ve güncellemenize olanak tanır.

### Aspose.Note için bir deneme sürümü mevcut mu?
Kesinlikle! Ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### Aspose.Note for Java için kapsamlı belgeleri nerede bulabilirim?
Detaylı belgeleri [buradan](https://reference.aspose.com/note/java/) inceleyebilirsiniz.

### Herhangi bir sorun veya soruya destek nasıl alabilirim?
Aspose topluluğundan yardım almak için destek forumuna [buradan](https://forum.aspose.com/c/note/28) gidin.

## Sıkça Sorulan Sorular
**S:** *Şifre korumalı OneNote dosyalarından etiket çıkarabilir miyim?*  
**C:** Evet, `Document` nesnesini oluştururken şifreyi sağlayın.

**S:** *Etiketleri değiştirdikten sonra bir kaydetme yöntemi çağırmam gerekiyor mu?*  
**C:** Kesinlikle. Değişiklikleri kalıcı hale getirmek için `doc.save("UpdatedSample.one");` kullanın.

**S:** *Etiketleri durumuna göre filtrelemek mümkün mü?*  
**C:** `noteTag.getStatus()` metodunu döngü içinde kontrol ederek yalnızca istenen durumları işleyebilirsiniz.

**S:** *Bir RichText düğümünün etiketi yoksa ne olur?*  
**C:** `richText.getTags()` boş bir koleksiyon döndürür; döngü sadece atlar.

**S:** *Birden fazla OneNote dosyasını toplu işleyebilir miyim?*  
**C:** Yukarıdaki mantığı bir dosya yineleme rutinine sararak her belgeyi sırasıyla işleyebilirsiniz.

---

**Son Güncelleme:** 2026-02-28  
**Test Edilen:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
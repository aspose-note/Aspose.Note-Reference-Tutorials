---
date: 2026-03-08
description: Aspose.Note for Java kullanarak OneNote belgelerinden liste özelliklerini
  nasıl çıkaracağınızı öğrenin. Bu adım adım rehber, ihtiyacınız olan tam kodu ve
  ipuçlarını gösterir.
linktitle: How to Extract List Properties in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'ta Liste Özelliklerini Nasıl Çıkarılır - Aspose.Note
url: /tr/java/onenote-text-manipulation/get-list-properties/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Liste Özelliklerini Nasıl Çıkarılır - Aspose.Note

## Introduction
Bu öğreticide **liste özelliklerini nasıl çıkaracağınızı** Aspose.Note for Java ile bir OneNote dosyasından keşfedeceksiniz. Yazı tipi detaylarını, liste biçimlendirmesini veya stil niteliklerini okumanız gerekse, bu kılavuz belgeyi yüklemeden çıkarılan değerleri yazdırmaya kadar her adımı size gösterir. Sonunda, herhangi bir Java tabanlı belge‑işleme hattına entegre edilebilecek hazır bir kod parçacığına sahip olacaksınız.

## Quick Answers
- **“extract list” ne anlama geliyor?** OneNote taslağında saklanan numaralı veya madde işaretli listelerin biçimlendirme detaylarını (yazı tipi, boyut, renk, stil) okumak demektir.  
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java (en son sürüm).  
- **Test için lisansa ihtiyacım var mı?** Evet, üretim dışı çalıştırmalar için geçici bir lisans önerilir.  
- **Herhangi bir işletim sisteminde çalıştırabilir miyim?** Java API'si Windows, Linux ve macOS'ta çalışır.  
- **Uygulama ne kadar sürer?** Temel bir kurulum genellikle 10 dakikadan az sürer.

## What is “how to extract list” in the context of OneNote?
OneNote her liste öğesini bir `OutlineElement` olarak saklar ve bu öğe bir `NumberList` nesnesi içerebilir. Listeyi çıkarmak, bu nesnenin yazı tipi adı, boyutu, rengi ve biçimlendirme gibi özelliklerine programlı olarak erişmek anlamına gelir.

## Why use Aspose.Note for Java to extract list properties?
- **No COM interop** – Windows OneNote istemcisine ihtiyaç duymadan tamamen Java içinde çalışır.  
- **Full fidelity** – Özel yazı tipleri ve renkler dahil tüm biçimlendirme detaylarını korur.  
- **Cross‑platform** – Aynı kodu herhangi bir sunucu‑tarafı ortamda çalıştırabilirsiniz.  
- **Rich API** – Liste nesnelerine doğrudan erişim sağlar, böylece özellik çıkarımı basittir.

## Prerequisites
Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

- Aspose.Note for Java: En son sürümü **[buradan](https://releases.aspose.com/note/java/)** indirin.  
- Java geliştirme ortamı (JDK 8 veya üzeri).  
- Bilinen bir dizinde bulunan bir OneNote belgesi (ör. `Sample1.one`).

## Import Packages
İlk olarak, ihtiyacınız olan sınıfları içe aktarın. Bu, temel Aspose.Note işlevselliğine erişmenizi sağlar.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.OutlineElement;
```

Şimdi uygulamayı adım adım inceleyelim.

## How to extract list properties – Step‑by‑Step Guide

### Step 1: Load the OneNote Document
`.one` dosyasının doğru yolunu sağlayın ve bir `Document` örneği oluşturun.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Pro tip:** `FileNotFoundException` almamak için mutlak yollar kullanın veya proje kaynak klasörüne göre göreli bir yol yapılandırın.

### Step 2: Retrieve the collection of outline nodes
Her liste bir `OutlineElement` içinde bulunur. Belgeden tüm bu öğeleri çekin.

```java
// Retrieve a collection of nodes of the outline element
List<OutlineElement> nodes = oneFile.getChildNodes(OutlineElement.class);
```

### Step 3: Iterate through the nodes and locate lists
Her düğümü döngüye alın, bir `NumberList` içerip içermediğini kontrol edin. İçeriyorsa, daha sonra çıkarım için referansı saklayın.

```java
// Iterate through each node
for (OutlineElement node : nodes) {
    if (node.getNumberList() != null) {
        NumberList list = node.getNumberList();
        // Continue with further operations on list properties
    }
}
```

### Step 4: Extract the desired list properties
Döngü içinde artık `NumberList` sınıfı tarafından sunulan herhangi bir niteliği okuyabilirsiniz.

```java
// Retrieve font name
System.out.println("Font Name: " + list.getFont());
// Retrieve font length (character count)
System.out.println("Font Length: " + list.getFont());
// Retrieve font size
System.out.println("Font Size: " + list.getFontSize());
// Retrieve font color
System.out.println("Font Color: " + list.getFontColor());
// Retrieve format (e.g., decimal, lowerLetter)
System.out.println("Font format: " + list.getFormat());
// Check bold style
System.out.println("Is bold: " + list.isBold());
// Check italic style
System.out.println("Is italic: " + list.isItalic());
```

Konsol çıktısı her özelliği gösterecek, böylece liste stil bilgilerini kaydedebilir, analiz edebilir veya daha ileri işleyebilirsiniz.

## Common Issues & Troubleshooting
| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| `NullPointerException` on `list.getFont()` | Düğüm bir `NumberList` içermiyor. | Null kontrolü ekleyin (`if (node.getNumberList() != null)`). |
| No output appears | `dataDir` yanlış klasöre işaret ediyor. | Yolu doğrulayın ve `Sample1.one` dosyasının mevcut olduğundan emin olun. |
| Font color shows as `null` | Liste varsayılan tema rengini kullanıyor. | `list.getFontColor()` çağırın ve belge temasına bir yedekleme ekleyin. |

## Frequently Asked Questions

**Q: Aspose.Note farklı OneNote sürümleriyle uyumlu mu?**  
A: Evet, Aspose.Note eski 2007 sürümlerinden en yeni Office 365 sürümlerine kadar geniş bir OneNote dosya formatı yelpazesini destekler.

**Q: Hangi yazı tipi özelliklerinin alınacağını özelleştirebilir miyim?**  
A: Kesinlikle. İhtiyacınız olan getter'ları (ör. `getFontSize()` veya `isBold()`) çağırıp geri kalanını yok sayabilirsiniz.

**Q: Ek destek veya yardım nereden bulabilirim?**  
A: Her türlü soru ve sorun için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret ederek hızlı yardım alabilirsiniz.

**Q: Test için geçici bir lisansa ihtiyacım var mı?**  
A: Evet, değerlendirme amaçlı **[buradan](https://purchase.aspose.com/temporary-license/)** geçici bir lisans alabilirsiniz.

**Q: Aspose.Note for Java'yı satın almak istersem?**  
A: Ürünü **[buradan](https://purchase.aspose.com/buy)** satın alarak projelerinizde tam potansiyelini açabilirsiniz.

---

**Last Updated:** 2026-03-08  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
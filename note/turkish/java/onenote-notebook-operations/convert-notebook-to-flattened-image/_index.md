---
date: 2025-12-25
description: OneNote'u PNG'ye dönüştürmeyi Aspose.Note for Java ile öğrenin. Bu kılavuz,
  görüntü çözünürlüğünü ayarlamayı, bir not defterini düzleştirmeyi ve OneNote'u verimli
  bir şekilde resim olarak kaydetmeyi gösterir.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u PNG'ye Dönüştürme – Aspose.Note ile Defteri Görüntüye Düzleştirme
url: /tr/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Not Defterini Düzleştirilmiş Görüntüye Dönüştürme - Aspose.Note

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak bir bütün not defterini tek bir düzleştirilmiş görüntüye dönüştürerek **OneNote'u PNG'ye dönüştürmeyi** keşfedeceksiniz. Bu yaklaşım, bir not defterini statik bir resim olarak paylaşmanız, raporlara yerleştirmeniz veya görsel detayları kaybetmeden arşivlemeniz gerektiğinde mükemmeldir.

## Hızlı Yanıtlar
- **“flatten notebook” ne anlama geliyor?** Tüm sayfa öğelerini tek bir raster görüntüde birleştirir.  
- **Hangi format kullanılıyor?** PNG varsayılan olup kayıpsız kalite sağlar.  
- **DPI'yi değiştirebilir miyim?** Evet, `ImageSaveOptions` üzerinde `setResolution` kullanın.  
- **Lisans gerekli mi?** Değerlendirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Bu tüm işletim sistemlerinde destekleniyor mu?** Java API'si Java çalıştırabildiği her yerde çalışır.

## OneNote'u PNG'ye dönüştürmek nedir?

OneNote'u PNG'ye dönüştürmek, not defterindeki her sayfanın bitmap temsili oluşturur ve metin, çizimler ve gömülü nesneleri tek bir görüntü dosyasında korur. Bu, özellikle dokümantasyon, sunumlar veya uyumluluk arşivleri için faydalıdır.

## OneNote'u PNG'ye Aspose.Note ile neden dönüştürmeliyiz?

- **Full fidelity** – Tüm görsel öğeler korunur.  
- **Single‑file output** – Birden fazla sayfa dosyasını yönetmeye gerek yoktur.  
- **Customizable resolution** – Kalite gereksinimlerini karşılamak için DPI ayarlanabilir.  
- **No Office installation** – Microsoft OneNote'dan tamamen bağımsız çalışır.

## Ön Koşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Sisteminizde yüklü Java Development Kit (JDK).  
2. Aspose.Note for Java kütüphanesini indirmiş ve Java projenize eklemiş olun. Kütüphaneyi [buradan](https://releases.aspose.com/note/java/) indirebilirsiniz.  
3. Java programlama temelleri.

## Paketleri İçe Aktarma

Başlamak için, Aspose.Note for Java'dan gerekli paketleri içe aktarmanız gerekir:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Adım 1: Belge Dizinini Ayarlama

İlk olarak, not defteri dosyanızın bulunduğu dizini tanımlayın:

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini not defteri dosyanızın yoluyla değiştirin.

## Adım 2: Not Defterini Yükleme

Sonra, `Notebook` sınıfını kullanarak not defteri dosyasını yükleyin:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

`"test.onetoc2"` ifadesini not defteri dosyanızın adıyla değiştirin.

## Adım 3: Görüntü Kaydetme Seçeneklerini Ayarlama

Şimdi, not defterini görüntü olarak kaydetmek için seçenekleri ayarlayın. Kaydetme formatını PNG olarak belirleyecek ve çözünürlüğü 400 DPI olarak ayarlayacağız:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Çözünürlüğü gereksinimlerinize göre ayarlayabilirsiniz. Çıktı kalitesini kontrol etmek için **görüntü çözünürlüğünü ayarladığınız** yerdir.

## Adım 4: Not Defterini Düzleştirme

Tüm öğelerin tek bir görüntüde düzleştirildiğinden emin olmak için `flatten` seçeneğini `true` olarak ayarlayın:

```java
saveOptions.setFlatten(true);
```

`flatten` seçeneğini `true` olarak ayarlamak, oluşan PNG'nin not defterinizin tam düzenini korumasını sağlar.

## Adım 5: Görüntüyü Kaydetme

Son olarak, not defterini düzleştirilmiş bir görüntü olarak kaydedin:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

`"ExportImageasFlattenedNotebook_out.png"` ifadesini istediğiniz çıktı dosya adıyla değiştirin. Bu adım, **OneNote'u istediğiniz yerde paylaşabileceğiniz veya yerleştirebileceğiniz bir görüntü olarak kaydeder**.

## Yaygın Kullanım Senaryoları

- **Documentation:** Not defteri görüntüsünü teknik kılavuzlara veya kullanıcı rehberlerine yerleştirin.  
- **Presentations:** Yazı tipi veya nesne uyumluluğu konusunda endişe etmeden PowerPoint'te yüksek çözünürlüklü PNG slaytı kullanın.  
- **Archiving:** Uyumluluk denetimleri için not defterinin yalnızca okunabilir bir anlık görüntüsünü saklayın.

## Sorun Giderme İpuçları

- **File not found:** `dataDir` yolunu iki kez kontrol edin ve `.onetoc2` dosyasının mevcut olduğundan emin olun.  
- **Low quality image:** DPI'yi artırmak için `documentSaveOptions.setResolution(600);` ifadesini değiştirin.  
- **Missing elements:** `saveOptions.setFlatten(true);` seçeneğinin etkin olduğundan emin olun; aksi takdirde bazı katmanlar ayrı kalabilir.

## Sıkça Sorulan Sorular

**S1: Çıktı görüntüsünün çözünürlüğünü ayarlayabilir miyim?**  
C1: Evet, `setResolution` metod parametresini değiştirerek çözünürlüğü gereksinimlerinize göre ayarlayabilirsiniz.

**S2: Aspose.Note dışa aktarım için başka görüntü formatlarını destekliyor mu?**  
C2: Evet, Aspose.Note not defterlerini dışa aktarmak için PNG, JPEG, BMP vb. çeşitli görüntü formatlarını destekler.

**S3: Çıktı görüntüsünü daha da özelleştirebilir miyim?**  
C3: Evet, Aspose.Note sayfa boyutu, yönlendirme ve kalite ayarları gibi birçok özelleştirme seçeneği sunar.

**S4: Aspose.Note for Java için bir deneme sürümü mevcut mu?**  
C4: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

**S5: Aspose.Note for Java için destek nereden bulunabilir?**  
C5: Destek ve kaynakları Aspose.Note forumunda [burada](https://forum.aspose.com/c/note/28) bulabilirsiniz.

---

**Son Güncelleme:** 2025-12-25  
**Test Edilen Versiyon:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
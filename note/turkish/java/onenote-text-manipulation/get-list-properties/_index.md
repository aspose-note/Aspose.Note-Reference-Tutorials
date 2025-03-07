---
title: OneNote'ta Liste Özelliklerini Alma - Aspose.Note
linktitle: OneNote'ta Liste Özelliklerini Alma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı keşfedin ve OneNote belgelerindeki liste özelliklerini zahmetsizce alın. Bu güçlü Java kitaplığıyla belge işlemenizi geliştirin.
weight: 19
url: /tr/java/onenote-text-manipulation/get-list-properties/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Liste Özelliklerini Alma - Aspose.Note

## giriiş
OneNote belgelerindeki liste özelliklerini almak ve analiz etmek için Aspose.Note for Java'dan yararlanmaya yönelik bu kapsamlı eğitime hoş geldiniz. İster deneyimli bir geliştirici olun ister Aspose.Note'a yeni başlıyor olun, bu kılavuz süreç boyunca size yol gösterecek ve net bir anlayış sağlamak için her adımı parçalara ayıracaktır.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:
-  Aspose.Note for Java: En son sürümün kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/note/java/).
- Java Geliştirme Ortamı: Sisteminizde bir Java geliştirme ortamı kurun.
- OneNote Belgesi: Test için bir OneNote belgesini (örneğin, "Sample1.one") hazır bulundurun.
## Paketleri İçe Aktar
Gerekli paketleri Java projenize aktararak başlayın. Bu, Aspose.Note işlevlerini kodunuzda sorunsuz bir şekilde kullanabilmenizi sağlar.
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.OutlineElement;
```

Şimdi, örneğin her adımını adım adım kılavuza ayıralım.

## 1. Adım: OneNote Belgesini Yükleyin

```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";

// Belgeyi Aspose.Note'a yükleyin
Document oneFile = new Document(dataDir + "Sample1.one");
```

OneNote belgenizin doğru yolunu girdiğinizden emin olun. Bu adım Aspose.Note kütüphanesini belgenizle başlatır.

## 2. Adım: Düğüm Koleksiyonunu Alın

```java
// Anahat öğesinin koleksiyon düğümlerini alın
List<OutlineElement> nodes = oneFile.getChildNodes(OutlineElement.class);
```

Burada, OneNote belgesindeki anahat öğelerini temsil eden bir düğüm koleksiyonunu alıyoruz.

## Adım 3: Düğümler Üzerinden Yineleme Yapın

```java
// Her düğümde yineleme
for (OutlineElement node : nodes) {
    if (node.getNumberList() != null) {
        NumberList list = node.getNumberList();
        // Liste özelliklerinde daha fazla işlem yapmaya devam edin
    }
}
```

Bu döngü, her anahat öğesi düğümü boyunca yinelenir ve bir sayı listesi içerip içermediğini kontrol eder. Doğruysa liste özelliklerinin çıkarılmasıyla devam eder.

## Adım 4: Liste Özelliklerini Çıkarın

```java
// Yazı tipi adını al
System.out.println("Font Name: " + list.getFont());
// Yazı tipi uzunluğunu al
System.out.println("Font Length: " + list.getFont());
// Yazı tipi boyutunu al
System.out.println("Font Size: " + list.getFontSize());
// Yazı tipi rengini al
System.out.println("Font Color: " + list.getFontColor());
// Formatı al
System.out.println("Font format: " + list.getFormat());
// Kalın olarak kontrol edin
System.out.println("Is bold: " + list.isBold());
// İtalik kontrol edin
System.out.println("Is italic: " + list.isItalic());
```

Bu satırlar yazı tipi adı, yazı tipi uzunluğu, yazı tipi boyutu, yazı tipi rengi, formatı ve stili (kalın veya italik) gibi çeşitli liste özelliklerini çıkarır.

## Çözüm
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'ta liste özelliklerinin nasıl alınacağını başarıyla keşfettiniz. Bu kılavuz sizi belge işleme yeteneklerinizi geliştirecek bilgilerle donattı. Farklı belgelerle denemeler yapın ve kodu özel gereksinimlerinize uyacak şekilde uyarlayın.
## SSS
### Aspose.Note farklı OneNote sürümleriyle uyumlu mu?
Aspose.Note, çeşitli OneNote sürümlerini destekleyerek farklı belge formatları arasında uyumluluk sağlar.
### OneNote belgelerinden alınan yazı tipi özelliklerini özelleştirebilir miyim?
Evet, kodu ihtiyaçlarınıza uyacak şekilde değiştirebilir ve belirli yazı tipi özelliklerini seçerek alabilirsiniz.
### Nerede ek destek veya yardım bulabilirim?
 Sorularınız veya sorunlarınız için şu adresi ziyaret edin:[Aspose.Note forumu](https://forum.aspose.com/c/note/28) hızlı yardım için.
### Test için geçici bir lisansa ihtiyacım var mı?
 Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/) test amaçlı.
### Aspose.Note for Java'yı satın almak istersem ne olur?
 Ürünü satın alabilirsiniz[Burada](https://purchase.aspose.com/buy)Projeleriniz için tüm potansiyelini açığa çıkarmak için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

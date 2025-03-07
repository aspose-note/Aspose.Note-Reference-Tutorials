---
title: OneNote'ta Düğüm Etiketlerini Alma - Aspose.Note
linktitle: OneNote'ta Düğüm Etiketlerini Alma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java ile OneNote'un sırlarını ortaya çıkarın. Bu kılavuz, düğüm etiketlerini zahmetsizce çıkarmanızı sağlar. Belge manipülasyonunun geleceğine dalın!
weight: 15
url: /tr/java/onenote-tag-operations/get-node-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Düğüm Etiketlerini Alma - Aspose.Note

## giriiş
Aspose.Note for Java dünyasına hoş geldiniz! OneNote belgelerinden bilgi yönetimi ve çıkarılması konusunda derinlemesine bilgi edinmek istiyorsanız doğru yerdesiniz. Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote'ta düğüm etiketleri alma sürecinde size rehberlik edeceğiz. Sonunda, bu güçlü Java API'nin tüm potansiyelinden yararlanacak bilgiyle donatılmış olacaksınız.
## Önkoşullar
Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:
- Java Geliştirme Ortamı: Sisteminizde çalışan bir Java geliştirme ortamının kurulu olduğundan emin olun.
-  Aspose.Note Kütüphanesi: Aspose.Note kütüphanesini şuradan indirip yükleyin:[Burada](https://releases.aspose.com/note/java/).
- OneNote Belgesi: Test ve keşif için hazır bir OneNote belgesi (örneğin, "Sample1.one") bulundurun.
## Paketleri İçe Aktar
Gerekli paketleri Java projenize aktararak başlayın. Bu paketler, Aspose.Note'u kullanarak OneNote belgeleriyle etkileşim kurmak için gereken araçları sağlayacaktır.
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```
Şimdi OneNote'ta düğüm etiketleri alma sürecini takip edilmesi kolay adımlara ayıralım:
## 1. Adım: OneNote Belgesini Yükleyin
```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";
// Belgeyi Aspose.Note'a yükleyin
Document doc = new Document(dataDir + "Sample1.one");
// Tüm RichText düğümlerini alın
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Belgeyi Aspose.Note'a yükleyin
Document doc = new Document(dataDir + "Sample1.one");
```
Aspose.Note belgesinin yüklendiğinden ve daha sonraki işlemlere hazır olduğundan emin olun.
## Adım 2: RichText Düğümlerini Alın
```java
// Tüm RichText düğümlerini alın
List<RichText> nodes = doc.getChildNodes(RichText.class);
```
Yüklenen OneNote belgesinden tüm RichText düğümlerini çıkarın. Bu düğümler ilgilendiğimiz bilgileri içerir.
## Adım 3: Her Düğümde Yineleme Yapın
```java
// Her düğümde yineleme
for (RichText richText : nodes) {
    // Her düğümü burada işleyin
}
```
İçeriğine erişmek ve analiz etmek için her RichText düğümünde döngü yapın.
## 4. Adım: Not Etiketlerini Alın
```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Özellikleri al
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
    }
}
```
Her RichText düğümü için NoteTag'leri kontrol edin ve özelliklerini alın. Bu adım, tamamlanma süresi, oluşturma süresi, yazı tipi rengi, durum, etiket, simge ve vurgulama gibi ayrıntıları ortaya çıkarır.
## Çözüm
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'tan düğüm etiketlerini ayıklamanın karmaşık ortamında başarıyla gezindiniz. Bu bilgiyle donanmış olarak artık bu işlevselliği Java uygulamalarınıza sorunsuz bir şekilde entegre edebilirsiniz.
## SSS
### Aspose.Note, OneNote'un tüm sürümleriyle uyumlu mu?
Aspose.Note, çeşitli OneNote dosya formatlarını destekleyerek farklı sürümler arasında uyumluluk sağlar.
### Alınan NoteTag özelliklerini değiştirebilir miyim?
Evet, Aspose.Note, NoteTag özelliklerini programlı olarak değiştirmenize ve güncellemenize olanak tanır.
### Aspose.Note'un deneme sürümü mevcut mu?
 Kesinlikle! Ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
### Aspose.Note for Java'nın kapsamlı belgelerini nerede bulabilirim?
 Ayrıntılı belgeleri inceleyin[Burada](https://reference.aspose.com/note/java/).
### Herhangi bir sorun veya soru için nasıl destek alabilirim?
 Destek forumuna gidin[Burada](https://forum.aspose.com/c/note/28) Aspose topluluğundan yardım için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

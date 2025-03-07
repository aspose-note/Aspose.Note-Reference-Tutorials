---
title: OneNote'ta Outlook Görevini Alma - Aspose.Note
linktitle: OneNote'ta Outlook Görevini Alma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Outlook görevlerini OneNote'tan zahmetsizce çıkarma konusunda Aspose.Note for Java'nın gücünü keşfedin. Adım adım kılavuzumuzu takip edin ve belge işleme yeteneklerinizi geliştirin.
weight: 10
url: /tr/java/task-and-outlook-integration/get-outlook-task/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Outlook Görevini Alma - Aspose.Note

## giriiş
OneNote'ta Outlook görevlerini sorunsuz bir şekilde almak için Aspose.Note for Java'yı kullanmayla ilgili kapsamlı kılavuzumuza hoş geldiniz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla zahmetsizce çalışmasına olanak tanıyan güçlü bir Java API'sidir. Bu öğreticide, Outlook görevlerini bir OneNote belgesinden adım adım çıkarma sürecinde size yol göstereceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.
-  Aspose.Note Kütüphanesi: Aspose.Note for Java kütüphanesini indirip yükleyin. Kütüphaneyi bulabilirsiniz[Burada](https://releases.aspose.com/note/java/).
## Paketleri İçe Aktar
Başlamak için gerekli paketleri Java projenize aktarın. Kodunuza aşağıdaki satırları ekleyin:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;

```
Şimdi süreci yönetilebilir adımlara ayıralım:
## 1. Adım: Belge Dizininizi Kurun
OneNote belgenizin bulunduğu dizini tanımlayın:
```java
String dataDir = "Your Document Directory";
```
## 2. Adım: OneNote Belgesini Yükleyin
Aspose.Note'u kullanarak OneNote belgesini yükleyin:
```java
Document doc = new Document(dataDir + "Sample1.one");
```
## 3. Adım: Tüm RichText Düğümlerini Alın
Belgedeki tüm RichText düğümlerini alın:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## Adım 4: Her Düğümde Yineleme Yapın
Her RichText düğümünü yineleyin ve NoteTask etiketlerini kontrol edin:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Özellikleri al
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```
## Çözüm
Tebrikler! OneNote'ta Outlook görevlerini almak için Aspose.Note for Java'yı nasıl kullanacağınızı başarıyla öğrendiniz. Bu güçlü API, süreci basitleştirerek verimli ve geliştirici dostu hale getirir.
## SSS
### Aspose.Note, OneNote'un tüm sürümleriyle uyumlu mu?
Aspose.Note, Microsoft OneNote 2010 ve sonraki sürümlerini destekler.
### Aspose.Note'u hem kişisel hem de ticari projeler için kullanabilir miyim?
 Evet, Aspose.Note hem kişisel hem de ticari projeler için kullanılabilir. Ziyaret etmek[Burada](https://purchase.aspose.com/buy) Lisanslama seçeneklerini keşfetmek için.
### Aspose.Note'un ücretsiz deneme sürümü mevcut mu?
 Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
### Aspose.Note için nasıl destek alabilirim?
 Ziyaret edin[Aspose.Note Forumu](https://forum.aspose.com/c/note/28) topluluk desteği için. Ek yardım için bir satın almayı düşünün.[geçici lisans](https://purchase.aspose.com/temporary-license/).
### Test için herhangi bir örnek OneNote belgesi var mı?
 Örnek belgeleri Aspose.Note belgelerinde bulabilirsiniz.[Burada](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

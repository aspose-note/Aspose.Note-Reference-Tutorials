---
title: OneNote'ta Outlook Görevini Alma - Aspose.Note
linktitle: OneNote'ta Outlook Görevini Alma - Aspose.Note
second_title: Aspose.Note Java API'si
description: OneNote belgelerinden Outlook Görevi ayrıntılarını zahmetsizce çıkarma konusunda Aspose.Note for Java'nın potansiyelini keşfedin. Bu sağlam kitaplıkla Java gelişiminizi geliştirin.
type: docs
weight: 10
url: /tr/java/onenote-text-manipulation/get-outlook-task/
---
## giriiş
Java geliştiricilerinin Microsoft OneNote dosyalarıyla sorunsuz bir şekilde çalışmasını sağlayan güçlü bir araç olan Aspose.Note for Java dünyasına hoş geldiniz. Bu adım adım kılavuzda, Aspose.Note for Java'yı kullanarak Outlook Görev bilgilerini OneNote belgesinden çıkarma sürecinde size yol göstereceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
- Java Geliştirme Kiti (JDK): Sisteminizde Java'nın kurulu olduğundan emin olun.
-  Aspose.Note for Java: Aspose.Note kütüphanesini şuradan indirip yükleyin:[indirme sayfası](https://releases.aspose.com/note/java/).
## Paketleri İçe Aktar
Gerekli paketleri Java projenize aktararak başlayın. Java dosyanızın başına aşağıdaki satırları ekleyin:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```
## 1. Adım: Projenizi Kurun
Yeni bir Java projesi oluşturun ve Aspose.Note kütüphanesini projenizin bağımlılıklarına ekleyin. Proje yapınızın düzenli olduğundan ve belgeleriniz için özel bir dizininizin olduğundan emin olun.
## 2. Adım: OneNote Belgesini Yükleyin
OneNote belgenizi Aspose.Note'a yüklemek için aşağıdaki kodu kullanın:
```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```
"Belge Dizininiz"i OneNote belgenizin yolu ile değiştirdiğinizden emin olun.
## 3. Adım: RichText Düğümlerini Alın
Aşağıdaki kodu kullanarak tüm RichText düğümlerini belgeden çıkarın:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## Adım 4: Her Düğümde Yineleme Yapın
Her RichText düğümünde döngü yapın ve bir NoteTask etiketi içerip içermediğini belirleyin:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // NoteTask'ı işlemek için kodunuz
        }
    }
}
```
## Adım 5: Görev Özelliklerini Alın
NoteTask'ın Tamamlanma Zamanı, Oluşturulma Zamanı, Son Tarih, Durum ve Simge gibi çeşitli özelliklerini alın ve yazdırın:
```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```
Belgedeki tüm NoteTask düğümleri için bu işlemi tekrarlayın.
## Çözüm
Tebrikler! Bir OneNote belgesinden Outlook Görev bilgilerini çıkarmak için Aspose.Note for Java'yı nasıl kullanacağınızı başarıyla öğrendiniz. Bu güçlü kitaplık, Microsoft OneNote dosyalarıyla çalışan Java geliştiricileri için bir olasılıklar dünyasının kapılarını açar.
## SSS
### S: Aspose.Note for Java'yı diğer Java çerçeveleriyle birlikte kullanabilir miyim?
C: Evet, Aspose.Note for Java çeşitli Java çerçeveleriyle uyumludur ve entegrasyonda esneklik sağlar.
### S: Aspose.Note for Java'nın ücretsiz deneme sürümü mevcut mu?
 C: Evet, Aspose.Note for Java'nın ücretsiz deneme sürümünü keşfedebilirsiniz[Burada](https://releases.aspose.com/).
### S: Aspose.Note for Java desteğini nasıl alabilirim?
 C: Ziyaret edin[Aspose.Note Forumu](https://forum.aspose.com/c/note/28) topluluk desteği için veya premium destek seçeneklerini keşfedin.
### S: Aspose.Note for Java'nın ayrıntılı belgelerini nerede bulabilirim?
 C: Bkz.[Java belgeleri için Aspose.Note](https://reference.aspose.com/note/java/) derinlemesine bilgi için.
### S: Aspose.Note for Java için nasıl geçici lisans edinebilirim?
 C: Geçici lisansınızı alın[Burada](https://purchase.aspose.com/temporary-license/).
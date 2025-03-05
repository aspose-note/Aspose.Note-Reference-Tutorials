---
title: OneNote'ta Tablodan Metin Çıkarma - Aspose.Note
linktitle: OneNote'ta Tablodan Metin Çıkarma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'taki tablolardan metni zahmetsizce nasıl çıkaracağınızı öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
type: docs
weight: 14
url: /tr/java/onenote-table-manipulation/extract-text-from-table/
---
## giriiş
Java geliştirme alanında Aspose.Note, OneNote belgelerini yönetmek için güçlü bir araç olarak öne çıkıyor. Dikkate değer özelliklerinden biri, tablolardan metni zahmetsizce çıkarma yeteneğidir. Bu eğitim, kusursuz bir deneyim sağlamak için her adımı parçalara ayırarak süreç boyunca size rehberlik edecektir.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdakilerin yerinde olduğundan emin olun:
- Java Geliştirme Ortamı: Sisteminizde bir Java geliştirme ortamı kurun.
-  Aspose.Note Kütüphanesi: Aspose.Note kütüphanesini indirin ve yükleyin. Gerekli paketleri bulabilirsiniz[Burada](https://releases.aspose.com/note/java/).
## Paketleri İçe Aktar
İşlevlerinden yararlanmak için Java projenizde Aspose.Note paketlerini içe aktarın. İşte bir örnek:
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.Table;
```
## 1. Adım: Belgeyi Yükleyin
```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";
// Belgeyi Aspose.Note'a yükleyin
Document document = new Document(dataDir + "Sample1.one");
// Tablo düğümlerinin listesini alın
List<Table> nodes = document.getChildNodes(Table.class);
// Belgeyi Aspose.Note'a yükleyin
Document document = new Document(dataDir + "Sample1.one");
```
## Adım 2: Tablo Düğümlerini Alın
```java
// Tablo düğümlerinin listesini alın
List<Table> nodes = document.getChildNodes(Table.class);
```
## Adım 3: Tablolarda Yineleme Yapın
```java
for (int i = 0; i < nodes.size(); i++) {
    Table table = nodes.get(i);
    System.out.println("Table # " + i);
```
## Adım 4: Tablodan Metni Alın
```java
// Metni al
List<RichText> textNodes = (List<RichText>) table.getChildNodes(RichText.class);
StringBuilder text = new StringBuilder();
for (RichText richText : textNodes) {
    text = text.append(richText.getText().toString());
}
```
## Adım 5: Metni Yazdır
```java
// Çıkış ekranındaki metni yazdırın
System.out.println(text);
```
OneNote belgelerinizdeki tablolardan metni etkili bir şekilde çıkarmak için bu adımları özenle izleyin.
## Çözüm
Aspose.Note for Java'yı geliştirme araç setinize dahil ederek OneNote belgelerindeki tablolardan metni sorunsuz bir şekilde çıkarabilirsiniz. Bu eğitimde, bu özelliği zahmetsizce uygulayabilmenizi sağlayan ayrıntılı bir kılavuz sağlanmıştır.
## SSS
### Aspose.Note en son Java sürümleriyle uyumlu mu?
Evet, Aspose.Note en son Java sürümleriyle uyumlu olacak şekilde tasarlanmıştır ve sorunsuz entegrasyon sağlar.
### Aspose.Note'u hem kişisel hem de ticari projeler için kullanabilir miyim?
 Evet, Aspose.Note hem kişisel hem de ticari projeler için kullanılabilir. Lisans ayrıntılarını kontrol edin[Burada](https://purchase.aspose.com/buy).
### Test amacıyla geçici bir lisansa ihtiyacım var mı?
 Evet, test etmek için geçici bir lisans alabilirsiniz.[bu bağlantı](https://purchase.aspose.com/temporary-license/).
### Aspose.Note için topluluk desteğini nerede bulabilirim?
 Topluluk desteğini şu adreste bulabilirsiniz:[Aspose.Note forumları](https://forum.aspose.com/c/note/28).
### Aspose.Note kütüphanesini nasıl satın alabilirim?
 Kütüphaneyi satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).
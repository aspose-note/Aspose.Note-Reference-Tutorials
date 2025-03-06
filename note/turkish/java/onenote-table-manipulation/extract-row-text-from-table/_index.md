---
title: OneNote Belgesindeki Tablodan Satır Metnini Çıkarma - Aspose.Note
linktitle: OneNote Belgesindeki Tablodan Satır Metnini Çıkarma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java ile OneNote tablolarından satır metinlerini zahmetsizce çıkarmayı öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
weight: 13
url: /tr/java/onenote-table-manipulation/extract-row-text-from-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Belgesindeki Tablodan Satır Metnini Çıkarma - Aspose.Note

## giriiş
Aspose.Note for Java kullanarak OneNote belgelerindeki tablolardan satır metni çıkarmaya yönelik bu kapsamlı eğitime hoş geldiniz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla sorunsuz bir şekilde çalışmasını sağlayan güçlü bir Java kitaplığıdır. Bu öğreticide, OneNote belgelerinizdeki tablolardan satır metnini verimli bir şekilde nasıl çıkaracağınızı göstererek süreç boyunca size adım adım rehberlik edeceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
-  Aspose.Note for Java Library: Aspose.Note for Java kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[İndirme: {link](https://releases.aspose.com/note/java/).
- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.
- OneNote Belgesi: Satır metnini çıkarmak istediğiniz tabloları içeren örnek bir OneNote belgesi (örneğin, "Sample1.one") hazırlayın.
## Paketleri İçe Aktar
Java projenizde gerekli Aspose.Note paketlerini içe aktarın. Bu, OneNote belgeleriyle çalışmak için gereken sınıflara ve yöntemlere erişebilmenizi sağlar.
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## 1. Adım: Belge Dizinini Ayarlayın
```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";
```
## 2. Adım: OneNote Belgesini Yükleyin
```java
// Belgeyi Aspose.Note'a yükleyin.
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## 3. Adım: Tablo Düğümlerini Alın
```java
// Tablo düğümlerinin listesini alın
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## Adım 4: Tablolar ve Satırlar Arasında Yineleme Yapın
```java
// Satır sayısını ayarla
int rowCount = 0;
for (Table table : nodes) {
    // Tablo satırları arasında yineleme
    for (TableRow row : table) {
        rowCount++;
        // Metni al
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // Çıkış ekranındaki metni yazdırın
        System.out.println(text);
    }
}
```
OneNote belgenizdeki her tablo için bu adımları tekrarlayın; satır metnini başarıyla ayıklayın.
## Çözüm
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote belgelerindeki tablolardan satır metnini nasıl çıkaracağınızı öğrendiniz. Bu eğitim, Aspose.Note'un güçlü özelliklerinden Java uygulamalarınızda yararlanmanız için bir temel sağlar.
## Sıkça Sorulan Sorular
### Aspose.Note, Microsoft OneNote'un en son sürümüyle uyumlu mu?
 Aspose.Note, en son sürümler de dahil olmak üzere çeşitli OneNote sürümlerini destekler. Bakın[dokümantasyon](https://reference.aspose.com/note/java/) uyumluluk ayrıntıları için.
### Satın almadan önce Aspose.Note for Java'yı deneyebilir miyim?
Evet, Aspose.Note'un ücretsiz deneme sürümünü şuradan keşfedebilirsiniz:[bu bağlantı](https://releases.aspose.com/).
### Nerede ek destek ve yardım bulabilirim?
 Ziyaret edin[Aspose.Note forumu](https://forum.aspose.com/c/note/28) topluluk desteği ve tartışmalar için.
### Aspose.Note için geçici lisansı nasıl edinebilirim?
 Şuradan geçici bir lisans alın:[bu bağlantı](https://purchase.aspose.com/temporary-license/).
### Aspose.Note for Java'yı kullanmak için herhangi bir özel sistem gereksinimi var mı?
Ayrıntılı sistem gereksinimleri için belgelere bakın.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

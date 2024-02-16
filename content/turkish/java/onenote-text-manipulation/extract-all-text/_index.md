---
title: OneNote'taki Tüm Metni Çıkart - Aspose.Note
linktitle: OneNote'taki Tüm Metni Çıkart - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'tan nasıl metin çıkaracağınızı öğrenin. Sorunsuz metin çıkarma için adım adım talimatlar içeren kapsamlı bir kılavuz.
type: docs
weight: 15
url: /tr/java/onenote-text-manipulation/extract-all-text/
---
## giriiş
Aspose.Note for Java'yı kullanarak OneNote'taki tüm metni çıkarmaya ilişkin adım adım kılavuzumuza hoş geldiniz. Aspose.Note, Microsoft OneNote dosyalarıyla sorunsuz bir şekilde çalışmanıza olanak tanıyan güçlü bir Java kitaplığıdır. Bu eğitimde, size sürecin ayrıntılı bir açıklamasını sunarak metin çıkarma konusuna odaklanacağız.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
1. Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.
2.  Aspose.Note for Java Kütüphanesi: Aspose.Note for Java kütüphanesini şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/note/java/).
3. Metin Çıkarılacak Belge: Belirlediğiniz belge dizininizde örnek bir OneNote belgesi (örneğin, "Sample1.one") hazır bulundurun.
## Paketleri İçe Aktar
Aspose.Note işlevselliğini kullanmak için Java projenize gerekli paketleri ekleyin. Paketleri içe aktarmak için örnek kod pasajını burada bulabilirsiniz:
```java
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.RichText;
```
Şimdi yukarıdaki kodu adım adım kılavuza ayıralım:
## 1. Adım: Belge Dizini Yolunu Ayarlayın
Java kodunda belge dizininizin yolunu tanımlayın:
```java
String dataDir = "Your Document Directory";
```
## 2. Adım: OneNote Belgesini Yükleyin
Aspose.Note'u kullanarak OneNote belgesini yükleyin:
```java
Document oneFile = new Document(dataDir + "Sample1.one");
```
## 3. Adım: Metin Düğümlerini Alın
Yüklenen belgeden metin düğümlerini alın:
```java
List<RichText> textNodes = (List<RichText>) oneFile.getChildNodes(RichText.class);
```
## Adım 4: Metni Çıkarın
Çıkarılan metni depolamak için bir StringBuilder oluşturun:
```java
StringBuilder text = new StringBuilder();
for (RichText richText : textNodes) {
    text = text.append(richText.getText().toString());
}
```
## Adım 5: Metni Yazdır
Çıkarılan metni çıktı ekranına yazdırın:
```java
System.out.println(text)
```
Herhangi bir OneNote belgesi için bu adımları tekrarlayın; Aspose.Note for Java, tüm metni verimli bir şekilde çıkaracaktır.
## Çözüm
Bu kılavuzda, bir OneNote belgesindeki tüm metni çıkarmak için Aspose.Note for Java'nın nasıl kullanılacağını araştırdık. Aspose.Note, basitliği ve güçlü özellikleriyle süreci kolaylaştırarak metin çıkarmayı sorunsuz hale getirir.
## Sıkça Sorulan Sorular

### S: Parola korumalı OneNote dosyalarından metin çıkarabilir miyim?
C: Şu an itibariyle Aspose.Note for Java, parola korumalı OneNote dosyalarından metin çıkarmayı desteklemiyor.
### S: Aspose.Note for Java, OneNote'un tüm sürümleriyle uyumlu mudur?
C: Aspose.Note for Java, Microsoft OneNote 2010 ve sonraki sürümlerini destekler.
### S: Aspose.Note for Java için nasıl geçici lisans alabilirim?
 C: Geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).
### S: Metin ayıklama için OneNote dosyalarının boyutunda herhangi bir sınırlama var mı?
C: Aspose.Note for Java, büyük OneNote dosyalarını verimli bir şekilde işlemek için tasarlanmıştır, ancak çok büyük dosyalar performansı etkileyebilir.
### S: Ek desteği veya topluluk tartışmalarını nerede bulabilirim?
 C: Ziyaret edin[Aspose.Note forumu](https://forum.aspose.com/c/note/28) Destek ve tartışmalar için.
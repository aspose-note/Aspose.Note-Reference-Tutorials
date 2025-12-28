---
date: 2025-12-28
description: Aspose.Note for Java का उपयोग करके पूर्ण नियंत्रण के साथ OneNote को PDF
  में निर्यात करना सीखें। इसमें OneNote नोटबुक को PDF में निर्यात करने के विकल्प और
  नोटबुक को PDF में बदलने के लिए जावा गाइड शामिल है।
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: विकल्पों के साथ OneNote को PDF में निर्यात कैसे करें – Aspose.Note का उपयोग
  करके नोटबुक को PDF में बदलें
url: /hi/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote को PDF में विकल्पों के साथ निर्यात करने का तरीका – Aspose.Note Java API

## परिचय

इस ट्यूटोरियल में आप **OneNote को PDF में निर्यात करने** का तरीका सीखेंगे, जिसमें Aspose.Note for Java का उपयोग करके अनुकूलन योग्य विकल्प उपलब्ध हैं। OneNote नोटबुक को PDF में बदलना अक्सर आवश्यक होता है—चाहे आप मीटिंग नोट्स साझा करना चाहते हों, दस्तावेज़ों को संग्रहित करना चाहते हों, या प्रिंट करने योग्य रिपोर्ट बनाना चाहते हों। Aspose.Note के साथ प्रक्रिया सीधी, पूरी तरह प्रोग्रामेबल, और उत्पन्न PDF पर सूक्ष्म नियंत्रण प्रदान करती है।

## त्वरित उत्तर
- **API क्या करता है?** यह OneNote नोटबुक को लोड करता है और वैकल्पिक सेटिंग्स के साथ उसे PDF के रूप में सहेजता है।  
- **कौन सी भाषा उपयोग की गई है?** Java – सर्वर‑साइड या डेस्कटॉप एप्लिकेशन के लिए उपयुक्त।  
- **क्या लाइसेंस की आवश्यकता है?** विकास के लिए मुफ्त ट्रायल काम करता है; उत्पादन के लिए व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं पेज लेआउट नियंत्रित कर सकता हूँ?** हाँ, आप पेज‑स्प्लिटिंग एल्गोरिदम, हेडर, फुटर और अधिक सेट कर सकते हैं।  
- **क्या कोड नमूना चलाने योग्य है?** बिल्कुल – बस प्लेसहोल्डर पाथ को अपनी नोटबुक के स्थान से बदलें।

## “OneNote को PDF में निर्यात करने” का अर्थ क्या है?

OneNote को PDF में निर्यात करना मतलब मूल OneNote नोटबुक (`*.onetoc2` और संबंधित सेक्शन फ़ाइलें) को एक पोर्टेबल, फिक्स्ड‑लेआउट PDF दस्तावेज़ में बदलना है। यह रूपांतरण फ़ॉर्मेटिंग, इमेजेज़ और एम्बेडेड ऑब्जेक्ट्स को संरक्षित रखता है, जबकि सामग्री को किसी भी डिवाइस पर OneNote की आवश्यकता के बिना देखा जा सकता है।

## Aspose.Note for Java क्यों उपयोग करें?

- **Microsoft Office पर निर्भरता नहीं** – Java चलाने वाले किसी भी प्लेटफ़ॉर्म पर काम करता है।  
- **समृद्ध PDF विकल्प** – पेज स्प्लिटिंग, हेडर/फुटर, और ऑब्जेक्ट हैंडलिंग को नियंत्रित करें।  
- **उच्च फ़िडेलिटी** – PDF आउटपुट मूल OneNote की उपस्थिति के बहुत करीब होता है।  
- **स्केलेबल** – हजारों नोटबुक की बैच प्रोसेसिंग के लिए उपयुक्त।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

1. **Java Development Kit (JDK)** – संस्करण 8 या उससे ऊपर।  
2. **Aspose.Note for Java** – इसे [download link](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **एक IDE** – IntelliJ IDEA, Eclipse, या NetBeans (आपकी पसंद)।  
4. **एक OneNote नोटबुक** जिसे आप बदलना चाहते हैं (उदा., `Notizbuch öffnen.onetoc2`)।

## पैकेज इम्पोर्ट करें

सबसे पहले उन क्लासेज़ को इम्पोर्ट करें जो नोटबुक हैंडलिंग और PDF सेविंग फ़ंक्शनैलिटी प्रदान करती हैं।

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## चरण 1: OneNote नोटबुक लोड करें

डिस्क से नोटबुक फ़ाइल लोड करें। `Your Document Directory` को उस वास्तविक फ़ोल्डर से बदलें जिसमें आपकी `.onetoc2` फ़ाइल मौजूद है।

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## चरण 2: PDF सेव ऑप्शन निर्दिष्ट करें

यहाँ आप परिभाषित करते हैं कि PDF कैसे जेनरेट किया जाएगा। उदाहरण में पेज‑स्प्लिटिंग एल्गोरिदम सेट किया गया है जो ठोस ऑब्जेक्ट्स को एक साथ रखता है, जो डायग्राम या टेबल्स के लिए उपयोगी है जिन्हें एक ही पेज पर रहना चाहिए।

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## चरण 3: नोटबुक को PDF के रूप में सहेजें

अंत में, नोटबुक को PDF फ़ाइल के रूप में लिखें। आउटपुट पाथ कोई भी स्थान हो सकता है जो आप पसंद करें।

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| **फ़ाइल नहीं मिली** | गलत `dataDir` या फ़ाइलनाम। | पाथ को दोबारा जाँचें और सुनिश्चित करें कि नोटबुक फ़ाइल मौजूद है। |
| **फ़ॉन्ट्स गायब** | PDF रेंडरिंग को OneNote के समान फ़ॉन्ट्स चाहिए होते हैं। | सर्वर पर आवश्यक फ़ॉन्ट्स इंस्टॉल करें या अतिरिक्त Aspose विकल्पों के माध्यम से उन्हें एम्बेड करें। |
| **बड़ी नोटबुक्स से OutOfMemoryError** | पूरी नोटबुक मेमोरी में लोड होती है। | सेक्शन‑वाइज़ प्रोसेस करें या JVM हीप साइज बढ़ाएँ (`-Xmx`)। |

## निष्कर्ष

हमने **OneNote को PDF में निर्यात करने** का तरीका Aspose.Note for Java का उपयोग करके दिखाया, जिसमें नोटबुक लोड करना, PDF विकल्प कॉन्फ़िगर करना, और परिणाम सहेजना शामिल है। इन चरणों का पालन करके आप किसी भी Java एप्लिकेशन—डेस्कटॉप टूल, वेब सर्विस, या बैच‑प्रोसेसिंग बैकएंड—में नोटबुक‑से‑PDF रूपांतरण को एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं PDF आउटपुट की उपस्थिति को कस्टमाइज़ कर सकता हूँ?

A1: हाँ, Aspose.Note विभिन्न विकल्प प्रदान करता है जैसे हेडर/फुटर सेटिंग्स, पेज स्प्लिटिंग एल्गोरिदम, आदि।

### Q2: क्या Aspose.Note सभी OneNote संस्करणों के साथ संगत है?

A2: Aspose.Note Microsoft OneNote 2010 और उसके बाद के संस्करणों को सपोर्ट करता है।

### Q3: क्या Aspose.Note का मुफ्त ट्रायल उपलब्ध है?

A3: हाँ, आप Aspose.Note का मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

### Q4: Aspose.Note की दस्तावेज़ीकरण कहाँ मिल सकती है?

A4: आप Aspose.Note की व्यापक दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/note/java/) पा सकते हैं।

### Q5: Aspose.Note के लिए समर्थन कैसे प्राप्त करें?

A5: किसी भी तकनीकी सहायता या प्रश्नों के लिए आप Aspose.Note सपोर्ट फ़ोरम [यहाँ](https://forum.aspose.com/c/note/28) पर जा सकते हैं।

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: मैं OneNote नोटबुक को बिना इमेजेज़ खोए PDF में कैसे निर्यात करूँ?**  
उत्तर: सुनिश्चित करें कि `KeepSolidObjectsAlgorithm` सेट है (जैसा दिखाया गया है) और स्रोत नोटबुक की इमेज फ़ाइलें उसी डायरेक्टरी में उपलब्ध हों।

**प्रश्न: क्या मैं एक ही रन में कई नोटबुक्स को बैच में बदल सकता हूँ?**  
उत्तर: हाँ। नोटबुक पाथ की सूची पर लूप चलाएँ, प्रत्येक के लिए `Notebook` इंस्टैंसिएट करें, समान `NotebookPdfSaveOptions` लागू करें, और `save()` कॉल करें।

**प्रश्न: क्या रूपांतरण के दौरान PDF मेटाडेटा (लेखक, शीर्षक) सेट करना संभव है?**  
उत्तर: `PdfSaveOptions.setMetadata()` का उपयोग करके सहेजने से पहले लेखक, शीर्षक, विषय और कीवर्ड निर्धारित करें।

**प्रश्न: क्या API पासवर्ड‑प्रोटेक्टेड PDFs को सपोर्ट करता है?**  
उत्तर: आप अन्य विकल्पों को कॉन्फ़िगर करने के बाद `PdfSaveOptions` पर `setEncryptionPassword()` सेट करके पासवर्ड लगा सकते हैं।

**प्रश्न: इस ट्यूटोरियल में कौन सा Aspose.Note संस्करण उपयोग किया गया था?**  
उत्तर: कोड को Aspose.Note for Java 23.12 के साथ परीक्षण किया गया था।

---

**अंतिम अपडेट:** 2025-12-28  
**परीक्षित संस्करण:** Aspose.Note for Java 23.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
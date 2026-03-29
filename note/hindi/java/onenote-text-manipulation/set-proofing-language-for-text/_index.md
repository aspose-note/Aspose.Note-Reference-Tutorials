---
date: 2026-03-29
description: Aspose.Note for Java का उपयोग करके OneNote में टेक्स्ट की भाषा कैसे सेट
  करें, सीखें। यह चरण‑दर‑चरण गाइड आपको दिखाता है कि OneNote दस्तावेज़ कैसे बनाएं,
  टेक्स्ट की भाषा बदलें, और OneNote फ़ाइल को प्रभावी ढंग से सहेजें।
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote में टेक्स्ट की भाषा कैसे सेट करें – Aspose.Note
url: /hi/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में टेक्स्ट के लिए भाषा कैसे सेट करें – Aspose.Note

## परिचय
यदि आपको OneNote नोटबुक के भीतर विशिष्ट टेक्स्ट के टुकड़ों के लिए **भाषा कैसे सेट करें** की आवश्यकता है, तो Aspose.Note for Java इसे सरल बनाता है। इस ट्यूटोरियल में आप सीखेंगे कि OneNote दस्तावेज़ कैसे बनाएं, व्यक्तिगत शब्दों या वाक्यांशों के लिए टेक्स्ट भाषा कैसे बदलें, और अंत में सही प्रूफ़िंग भाषा लागू करके OneNote फ़ाइल को सहेजें। अंत तक आप समझेंगे कि भाषा सेट करना स्पेल‑चेकिंग और स्थानीयकरण के लिए क्यों महत्वपूर्ण है, और आपके पास चलाने योग्य कोड नमूना होगा।

## त्वरित उत्तर
- **“भाषा सेट करना” क्या प्रभावित करता है?** यह OneNote को बताता है कि स्पेल‑चेक और व्याकरण के लिए कौन सा प्रूफ़िंग शब्दकोश उपयोग करना है।  
- **क्या मैं एक ही नोट में विभिन्न भाषाएँ सेट कर सकता हूँ?** हाँ, आप प्रत्येक टेक्स्ट रन को एक भाषा असाइन कर सकते हैं।  
- **क्या मुझे Aspose.Note के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **कौन से Java संस्करण समर्थित हैं?** Aspose.Note for Java Java 8 और उसके बाद के संस्करणों को समर्थन देता है।  
- **क्या आउटपुट .one फ़ाइल है?** हाँ, दस्तावेज़ OneNote *.one* फ़ाइल के रूप में सहेजा जाता है।

## पूर्वापेक्षाएँ
कोड में डुबकी लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java विकास वातावरण** – JDK 8 या उससे ऊपर स्थापित और कॉन्फ़िगर किया हुआ।  
2. **Aspose.Note for Java लाइब्रेरी** – लाइब्रेरी को [download link](https://releases.aspose.com/note/java/) से डाउनलोड और इंस्टॉल करें।  
3. **डॉक्यूमेंट डायरेक्टरी** – अपने मशीन पर एक फ़ोल्डर बनाएं जहाँ उत्पन्न OneNote फ़ाइल सहेजी जाएगी।

## OneNote में टेक्स्ट के लिए भाषा क्यों सेट करें?
प्रूफ़िंग भाषा सेट करने से यह सुनिश्चित होता है कि स्पेल‑चेक, व्याकरण सुझाव, और खोज अनुक्रमण मल्टीभाषी सामग्री के लिए सही ढंग से काम करें। यह विशेष रूप से उपयोगी है:

- **वैश्विक टीमें** जो एक ही नोटबुक पर सहयोग करती हैं।  
- **स्थानीयकृत दस्तावेज़ीकरण** जहाँ प्रत्येक अनुभाग अलग भाषा में हो सकता है।  
- **डेटा‑चालित एप्लिकेशन** जो विश्व भर के उपयोगकर्ताओं के लिए प्रोग्रामेटिक रूप से नोट्स उत्पन्न करते हैं।

## पैकेज आयात करें
आवश्यक Aspose.Note क्लासेस और Java यूटिलिटीज़ को आयात करके शुरू करें।

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## चरण 1: दस्तावेज़ और पृष्ठ सेट करें
एक नया OneNote दस्तावेज़ और एक पृष्ठ बनाएं जो आपकी सामग्री रखेगा। यह चरण **create OneNote document** को भी दर्शाता है।

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## चरण 2: रूपरेखा और रूपरेखा तत्व बनाएं
रूपरेखा नोटबुक सामग्री का कंटेनर है। यहाँ हम वह संरचना बनाते हैं जो बाद में भाषा‑विशिष्ट टेक्स्ट रखेगी।

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## चरण 3: भाषा सेटिंग्स के साथ रिच टेक्स्ट जोड़ें
अब हम प्रत्येक टेक्स्ट सेगमेंट में एक विशिष्ट `Locale` के साथ `TextStyle` संलग्न करके **टेक्स्ट भाषा बदलते** हैं। यह **set language for text** को दर्शाता है।

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## चरण 4: तत्वों को व्यवस्थित करें और सहेजें
रूपरेखा पदानुक्रम को एकत्रित करें, इसे पृष्ठ से संलग्न करें, और अंत में भाषा सेटिंग्स लागू करके **OneNote फ़ाइल सहेजें**।

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## सामान्य जाल और सुझाव
- **Locale फ़ॉर्मेट** – IETF BCP‑47 टैग (जैसे `en-US`, `de-DE`) का उपयोग करें। गलत टैग दस्तावेज़ की भाषा पर डिफ़ॉल्ट हो जाएगा।  
- **फ़ाइल पाथ** – सुनिश्चित करें कि `dataDir` एक मौजूदा फ़ोल्डर की ओर इशारा करता है; अन्यथा `document.save` एक `IOException` फेंकेगा।  
- **प्रो टिप:** यदि आपको पूरे पैराग्राफ की भाषा सेट करनी है, तो प्रत्येक `append` कॉल के बजाय `ParagraphStyle` पर `TextStyle` लागू करें।

## निष्कर्ष
आपने अभी Aspose.Note for Java का उपयोग करके OneNote नोटबुक में व्यक्तिगत टेक्स्ट अंशों के लिए **भाषा कैसे सेट करें** सीखा है। यह क्षमता आपको प्रोग्रामेटिक रूप से **OneNote दस्तावेज़ बनाना**, **टेक्स्ट भाषा बदलना**, और सटीक प्रूफ़िंग मेटाडेटा के साथ **OneNote फ़ाइल सहेजना** सक्षम करती है।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं उदाहरण में उल्लेखित नहीं की गई अन्य भाषाओं के लिए प्रूफ़िंग भाषा सेट कर सकता हूँ?**  
A: बिल्कुल! इच्छित `Locale.forLanguageTag("xx-XX")` के साथ अतिरिक्त `append` कॉल जोड़ें।

**Q: क्या Aspose.Note for Java नवीनतम Java संस्करणों के साथ संगत है?**  
A: हाँ, लाइब्रेरी नियमित रूप से अपडेट की जाती है ताकि नवीनतम Java रिलीज़ को समर्थन मिल सके।

**Q: भाषा‑सेटिंग प्रक्रिया के दौरान त्रुटियों को कैसे संभालूँ?**  
A: `save` ऑपरेशन को `try‑catch` ब्लॉक में लपेटें ताकि `IOException` या `AsposeException` को पकड़ सकें।

**Q: क्या मैं इस कोड को वेब एप्लिकेशन में एकीकृत कर सकता हूँ?**  
A: निश्चित रूप से। बस Aspose.Note JAR को अपने वेब प्रोजेक्ट के क्लासपाथ में शामिल करें और सुनिश्चित करें कि सर्वर को लक्ष्य डायरेक्टरी में लिखने की अनुमति हो।

**Q: Aspose.Note for Java के अतिरिक्त उदाहरण और दस्तावेज़ीकरण कहाँ मिल सकते हैं?**  
A: पूरी API सूची और नमूना प्रोजेक्ट्स के लिए [documentation](https://reference.aspose.com/note/java/) देखें।

---

**अंतिम अपडेट:** 2026-03-29  
**परीक्षण किया गया:** Aspose.Note for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-03-05
description: Aspose.Note for Java की Image Save Options का उपयोग करके OneNote दस्तावेज़ों
  को BMP इमेज में निर्यात करना सीखें। साथ ही देखें कि OneNote को PDF में कैसे बदलें
  या OneNote को PNG के रूप में कैसे सहेजें।
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: इमेज सेव विकल्पों का उपयोग करके वननोट को BMP इमेज में निर्यात कैसे करें
url: /hi/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Image Save Options का उपयोग करके OneNote को BMP इमेज में निर्यात कैसे करें

## OneNote को BMP इमेज में निर्यात करने का तरीका

Aspose.Note for Java एक शक्तिशाली लाइब्रेरी है जो Java डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है। **इस ट्यूटोरियल में आप सीखेंगे कि OneNote दस्तावेज़ों को BMP इमेज में कैसे निर्यात किया जाए** Aspose.Note for Java की Image Save Options सुविधा का उपयोग करके। हम प्रत्येक चरण को विस्तार से देखेंगे, यह बताएँगे कि आप अन्य फ़ॉर्मैट की तुलना में BMP क्यों चुन सकते हैं, और यह दिखाएँगे कि इस क्षमता को अपने एप्लिकेशन में कैसे एकीकृत किया जाए।

## त्वरित उत्तर
- **Image Save Options क्लास क्या करता है?** यह आपको OneNote पेज को परिवर्तित करते समय आउटपुट इमेज फ़ॉर्मैट (BMP, PNG, JPEG, आदि) निर्दिष्ट करने की अनुमति देता है।  
- **क्या मुझे सैंपल चलाने के लिए लाइसेंस चाहिए?** एक फ्री ट्रायल मूल्यांकन के लिए काम करता है, लेकिन प्रोडक्शन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **क्या मैं OneNote पेज को BMP के बजाय PDF या PNG में बदल सकता हूँ?** हां – बस `SaveFormat` एन्नुम को बदलें (उदाहरण के लिए, `SaveFormat.Pdf` या `SaveFormat.Png`)।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण पूरी तरह समर्थित हैं।  
- **क्या बड़े दस्तावेज़ों के लिए कोई विशेष हैंडलिंग है?** उच्च मेमोरी उपयोग से बचने के लिए आप आउटपुट को स्ट्रीम कर सकते हैं।

## Aspose.Note में “Image Save Options” क्या है?
`ImageSaveOptions` क्लास यह नियंत्रित करने के लिए सूक्ष्म नियंत्रण प्रदान करता है कि OneNote पेज रास्टर इमेज के रूप में कैसे रेंडर होते हैं। आप इमेज फ़ॉर्मैट, रिज़ॉल्यूशन, कलर डेप्थ आदि सेट कर सकते हैं। यह लचीलापन लेगेसी सिस्टम (BMP) या आधुनिक वेब परिदृश्यों (PNG/JPEG) के लिए **OneNote पेज इमेज निर्यात** करना आसान बनाता है।  

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

1. Java प्रोग्रामिंग भाषा का बुनियादी ज्ञान।  
2. आपके मशीन पर JDK (Java Development Kit) स्थापित हो।  
3. Eclipse या IntelliJ IDEA जैसे IDE।  
4. Aspose.Note for Java लाइब्रेरी – इसे [यहाँ](https://releases.aspose.com/note/java/) से डाउनलोड करें।

## पैकेज आयात करें

पहले, आवश्यक Aspose.Note क्लासेज़ और मानक Java I/O यूटिलिटीज़ आयात करें:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## चरण 1: OneNote दस्तावेज़ लोड करें

यहाँ हम उस फ़ोल्डर की ओर इशारा करते हैं जिसमें स्रोत OneNote फ़ाइल (`Aspose.one`) है और इसे एक `Document` ऑब्जेक्ट में लोड करते हैं। यह ऑब्जेक्ट आपको नोटबुक के भीतर पेज, सेक्शन और अन्य तत्वों तक पूर्ण पहुँच प्रदान करता है।

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## चरण 2: दस्तावेज़ को BMP इमेज के रूप में सहेजें

हम आउटपुट फ़ाइल नाम को जोड़ते हैं, फिर `save` को कॉल करते हैं जिसमें **BMP** (`SaveFormat.Bmp`) के लिए कॉन्फ़िगर किया गया `ImageSaveOptions` इंस्टेंस होता है।  
यदि आप **OneNote पेज को PNG** के रूप में सहेजना चाहते हैं, तो बस `SaveFormat.Bmp` को `SaveFormat.Png` से बदल दें। इसी प्रकार, `SaveFormat.Pdf` आपको **OneNote को PDF** में परिवर्तित करने की सुविधा देता है।

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## BMP क्यों चुनें?
- **Lossless quality** – BMP कच्चा पिक्सेल डेटा संग्रहीत करता है, जिससे मूल पेज की सटीक उपस्थिति बनी रहती है।  
- **Compatibility** – पुराने Windows एप्लिकेशन अक्सर BMP फ़ाइलों की आवश्यकता रखते हैं।  
- **Simplicity** – कोई संपीड़न आर्टिफैक्ट नहीं होते, जिससे यह आगे की इमेज प्रोसेसिंग के लिए आदर्श बनता है।

## सामान्य समस्याएँ और सुझाव

- **File path errors** – सुनिश्चित करें कि `dataDir` उचित फ़ाइल सेपरेटर (`/` या `\`) के साथ समाप्त हो।  
- **Large notebooks** – बहुत बड़े OneNote फ़ाइलों के लिए, मेमोरी उपयोग कम रखने हेतु प्रत्येक पेज को अलग-अलग सहेजने पर विचार करें।  
- **License exceptions** – वैध लाइसेंस के बिना कोड चलाने पर उत्पन्न इमेज में वॉटरमार्क जुड़ जाएगा।

## निष्कर्ष

इस गाइड में हमने Aspose.Note for Java के `ImageSaveOptions` का उपयोग करके **OneNote को BMP इमेज में निर्यात करने** का प्रदर्शन किया। `SaveFormat` एन्नुम को बदलकर आप PNG, JPEG, PDF या अन्य समर्थित फ़ॉर्मैट भी बना सकते हैं, जिससे किसी भी डाउनस्ट्रीम परिदृश्य के लिए OneNote सामग्री निर्यात करने का लचीला तरीका मिलता है।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं OneNote दस्तावेज़ों को BMP के अलावा अन्य इमेज फ़ॉर्मैट में सहेज सकता हूँ?**  
A: हाँ, आप `ImageSaveOptions` को `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif`, या `SaveFormat.Tiff` के साथ उपयोग करके उन फ़ॉर्मैट में निर्यात कर सकते हैं।

**Q2: क्या Aspose.Note for Java विभिन्न दस्तावेज़ फ़ॉर्मैटों के बीच रूपांतरण का समर्थन करता है?**  
A: बिल्कुल। इमेज फ़ॉर्मैट के अलावा, आप उपयुक्त `SaveFormat` का उपयोग करके OneNote फ़ाइलों को PDF, DOCX, HTML और अन्य फ़ॉर्मैट में बदल सकते हैं।

**Q3: क्या Aspose.Note for Java नवीनतम OneNote संस्करणों के साथ संगत है?**  
A: हाँ, लाइब्रेरी को नियमित रूप से अपडेट किया जाता है ताकि यह नवीनतम OneNote रिलीज़ के साथ सिंक में रहे।

**Q4: क्या मैं OneNote दस्तावेज़ों की सामग्री को प्रोग्रामेटिकली बदल सकता हूँ?**  
A: हाँ, आप API के माध्यम से पेज, सेक्शन और रिच कंटेंट (टेक्स्ट, इमेज, टेबल) को जोड़, संपादित या हटाकर बदल सकते हैं।

**Q5: क्या Aspose.Note for Java तकनीकी समर्थन प्रदान करता है?**  
A: हाँ, Aspose तकनीकी समर्थन और एक समर्पित फ़ोरम प्रदान करता है। सहायता के लिए [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) पर जाएँ।

---

**अंतिम अपडेट:** 2026-03-05  
**परीक्षित संस्करण:** Aspose.Note for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
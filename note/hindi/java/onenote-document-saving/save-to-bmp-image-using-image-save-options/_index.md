---
date: 2025-12-16
description: Aspose.Note for Java की इमेज सेव विकल्पों का उपयोग करके OneNote दस्तावेज़ों
  को BMP इमेज में कैसे सहेजें, सीखें। साथ ही देखें कि OneNote को PDF या PNG में कैसे
  सहेजा जा सकता है।
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: इमेज सेव विकल्पों का उपयोग करके वननोट को BMP इमेज के रूप में कैसे सहेजें
url: /hi/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# इमेज सेव ऑप्शन्स का उपयोग करके OneNote को BMP इमेज के रूप में कैसे सहेजें

## परिचय

Aspose.Note for Java एक शक्तिशाली लाइब्रेरी है जो Java डेवलपर्स को प्रोग्रामेटिक रूप से Microsoft OneNote फ़ाइलों के साथ काम करने में सक्षम बनाती है। **इस ट्यूटोरियल में आप सीखेंगे कि Aspose.Note for Java की Image Save Options सुविधा का उपयोग करके OneNote दस्तावेज़ों को BMP इमेज में कैसे सहेजा जाए**। हम प्रत्येक चरण को विस्तार से दिखाएंगे, यह समझाएंगे कि आप अन्य फ़ॉर्मेट की तुलना में BMP क्यों चुन सकते हैं, और यह दिखाएंगे कि इस क्षमता को अपने एप्लिकेशन में कैसे एकीकृत किया जाए।

## त्वरित उत्तर
- **Image Save Options क्लास क्या करती है?** यह OneNote पेज को कन्वर्ट करते समय आउटपुट इमेज फ़ॉर्मेट (BMP, PNG, JPEG आदि) निर्दिष्ट करने की अनुमति देती है।  
- **क्या सैंपल चलाने के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए एक फ्री ट्रायल काम करता है, लेकिन प्रोडक्शन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **क्या मैं BMP के बजाय PDF या PNG में OneNote पेज को कन्वर्ट कर सकता हूँ?** हाँ – केवल `SaveFormat` एन्नुम को बदलें (उदाहरण के लिए `SaveFormat.Pdf` या `SaveFormat.Png`)।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण पूरी तरह सपोर्टेड हैं।  
- **क्या बड़े दस्तावेज़ों के लिए कोई विशेष हैंडलिंग है?** आप आउटपुट को स्ट्रीम करके उच्च मेमोरी खपत से बच सकते हैं।

## Aspose.Note में “Image Save Options” क्या है?
`ImageSaveOptions` क्लास OneNote पेजों को रास्टर इमेज के रूप में रेंडर करने पर सूक्ष्म नियंत्रण प्रदान करती है। आप इमेज फ़ॉर्मेट, रिज़ॉल्यूशन, कलर डेप्थ आदि सेट कर सकते हैं। यह लचीलापन लेगेसी सिस्टम के लिए BMP फ़ाइलें या वेब उपयोग के लिए PNG/JPEG फ़ाइलें जनरेट करना आसान बनाता है।

## आवश्यकताएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

1. Java प्रोग्रामिंग भाषा का बुनियादी ज्ञान।  
2. आपके मशीन पर JDK (Java Development Kit) स्थापित हो।  
3. Eclipse या IntelliJ IDEA जैसे IDE।  
4. Aspose.Note for Java लाइब्रेरी – इसे [यहाँ](https://releases.aspose.com/note/java/) से डाउनलोड करें।

## पैकेज इम्पोर्ट करें

पहले आवश्यक Aspose.Note क्लासेज़ और मानक Java I/O यूटिलिटीज़ इम्पोर्ट करें:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## चरण 1: OneNote दस्तावेज़ लोड करें

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

यहाँ हम उस फ़ोल्डर की ओर इशारा करते हैं जिसमें स्रोत OneNote फ़ाइल (`Aspose.one`) मौजूद है और इसे `Document` ऑब्जेक्ट में लोड करते हैं। यह ऑब्जेक्ट आपको नोटबुक के पेज, सेक्शन और अन्य तत्वों तक पूर्ण पहुँच देता है।

## चरण 2: दस्तावेज़ को BMP इमेज के रूप में सहेजें

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

हम आउटपुट फ़ाइल नाम को जोड़ते हैं, फिर `ImageSaveOptions` इंस्टेंस को **BMP** (`SaveFormat.Bmp`) के लिए कॉन्फ़िगर करके `save` कॉल करते हैं।  
यदि आप **OneNote पेज को PNG** में सहेजना चाहते हैं, तो बस `SaveFormat.Bmp` को `SaveFormat.Png` से बदल दें। इसी तरह, `SaveFormat.Pdf` आपको **OneNote को PDF** में कन्वर्ट करने की सुविधा देता है।

## BMP क्यों चुनें?
- **लॉसलेस क्वालिटी** – BMP कच्चा पिक्सेल डेटा स्टोर करता है, जिससे मूल पेज की सटीक उपस्थिति बनी रहती है।  
- **कम्पैटिबिलिटी** – पुराने Windows एप्लिकेशन अक्सर BMP फ़ाइलों की आवश्यकता रखते हैं।  
- **सरलता** – कोई कम्प्रेशन आर्टिफैक्ट नहीं, जिससे आगे की इमेज प्रोसेसिंग आसान होती है।

## सामान्य समस्याएँ एवं टिप्स

- **फ़ाइल पाथ त्रुटियाँ** – सुनिश्चित करें कि `dataDir` उचित फ़ाइल सेपरेटर (`/` या `\`) के साथ समाप्त हो।  
- **बड़े नोटबुक** – बहुत बड़े OneNote फ़ाइलों के लिए, मेमोरी उपयोग कम रखने हेतु प्रत्येक पेज को अलग‑अलग सहेजने पर विचार करें।  
- **लाइसेंस अपवाद** – वैध लाइसेंस के बिना कोड चलाने पर उत्पन्न इमेज में वॉटरमार्क जुड़ जाएगा।

## निष्कर्ष

इस गाइड में हमने Aspose.Note for Java की `ImageSaveOptions` का उपयोग करके **OneNote दस्तावेज़ों को BMP इमेज में कैसे सहेजें** दिखाया। `SaveFormat` एन्नुम को बदलकर आप PNG, JPEG, PDF या अन्य समर्थित फ़ॉर्मेट भी जनरेट कर सकते हैं, जिससे OneNote कंटेंट को किसी भी डाउनस्ट्रीम परिदृश्य के लिए निर्यात करने का लचीला तरीका मिलता है।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं OneNote दस्तावेज़ों को BMP के अलावा अन्य इमेज फ़ॉर्मेट में सहेज सकता हूँ?**  
A: हाँ, आप `ImageSaveOptions` के साथ `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` या `SaveFormat.Tiff` का उपयोग करके इन फ़ॉर्मेट में एक्सपोर्ट कर सकते हैं।

**Q2: क्या Aspose.Note for Java विभिन्न दस्तावेज़ फ़ॉर्मेट के बीच कन्वर्ज़न सपोर्ट करता है?**  
A: बिल्कुल। इमेज फ़ॉर्मेट के अलावा, आप उचित `SaveFormat` का उपयोग करके OneNote फ़ाइलों को PDF, DOCX, HTML आदि में भी कन्वर्ट कर सकते हैं।

**Q3: क्या Aspose.Note for Java नवीनतम OneNote संस्करणों के साथ संगत है?**  
A: हाँ, लाइब्रेरी को नियमित रूप से अपडेट किया जाता है ताकि यह नवीनतम OneNote रिलीज़ के साथ सिंक में रहे।

**Q4: क्या मैं प्रोग्रामेटिक रूप से OneNote दस्तावेज़ों की सामग्री को बदल सकता हूँ?**  
A: हाँ, आप API के माध्यम से पेज, सेक्शन और रिच कंटेंट (टेक्स्ट, इमेज, टेबल) को जोड़, संपादित या हटाने का कार्य कर सकते हैं।

**Q5: क्या Aspose.Note for Java तकनीकी समर्थन प्रदान करता है?**  
A: हाँ, Aspose तकनीकी समर्थन और एक समर्पित फ़ोरम प्रदान करता है। सहायता के लिए [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) देखें।

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**अंतिम अपडेट:** 2025-12-16  
**परीक्षित संस्करण:** Aspose.Note for Java 24.12  
**लेखक:** Aspose  

---
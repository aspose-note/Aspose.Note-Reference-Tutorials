---
date: 2026-02-07
description: Aspose.Note for Java का उपयोग करके OneNote को HTML के रूप में सहेजते
  समय फ़ॉन्ट निर्यात करना सीखें। यह गाइड आपको दिखाता है कि प्रोग्रामेटिक रूप से OneNote
  कैसे बनाएं और फ़ॉन्ट, CSS, तथा छवियों को एम्बेड करें।
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNote को HTML के रूप में सहेजते समय फ़ॉन्ट कैसे निर्यात करें – Java
url: /hi/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote को HTML के रूप में सहेजते समय फ़ॉन्ट्स को एक्सपोर्ट कैसे करें – Java

## परिचय

## त्वरित उत्तर
- **एक्सपोर्ट को कौन सी लाइब्रेरी संभालती है?** Aspose.Note for Java  
- **क्या फ़ॉन्ट्स को HTML में एम्बेड किया जा सकता है?** हाँ – `ExportFonts` को `ExportEmbedded` सेट करें  
- **क्या उत्पादन के लिए लाइसेंस की आवश्यकता है?** व्यावसायिक उपयोग के लिए एक वैध Aspose.Note लाइसेंस आवश्यक है  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर  
- **क्या संसाधनों को अलग फ़ाइलों में सहेजा जा सकता है?** बिल्कुल – `ResourceExportType` को तदनुसार कॉन्फ़िगर करें  

## OneNote HTML रूपांतरण के संदर्भ में “फ़ॉन्ट्स को एक्सपोर्ट कैसे करें” क्या है?
जब आप OneNote नोटबुक को HTML में बदलते हैं, तो दृश्य रूप CSS, छवियों, और विशेष रूप से मूल पृष्ठों में उपयोग किए गए फ़ॉन्ट्स पर निर्भर करता है। **फ़ॉन्ट्स को एक्सपोर्ट करना** का मतलब है फ़ॉन्ट फ़ाइलों (जैसे, TTF) को सीधे HTML पैकेज में एम्बेड करना ताकि ब्राउज़र टेक्स्ट को ठीक उसी तरह रेंडर कर सके जैसा वह OneNote में दिखता है, भले ही अंतिम उपयोगकर्ता के पास वह फ़ॉन्ट स्थानीय रूप से स्थापित न हो।

## प्रोग्रामेटिक रूप से OneNote क्यों बनाएं और उसे HTML के रूप में सहेजें?
- **ऑटोमेशन:** OneNote से रिपोर्ट, दस्तावेज़, या नॉलेज‑बेस लेख उत्पन्न करें बिना मैन्युअल कॉपी‑पेस्ट के।  
- **संगतता:** लेआउट, स्टाइलिंग, और कस्टम फ़ॉन्ट्स को विभिन्न डिवाइसों पर संरक्षित रखें।  
- **पोर्टेबिलिटी:** HTML सार्वभौमिक रूप से देखा जा सकता है—OneNote क्लाइंट की आवश्यकता नहीं।  

## पूर्वापेक्षाएँ
1. Java Development Kit (JDK) 8 या नया स्थापित हो।  
2. Aspose.Note for Java लाइब्रेरी – [यहाँ](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. लोड करने के लिए एक नमूना OneNote फ़ाइल (`.one`), या आप प्रोग्रामेटिक रूप से नई फ़ाइल बना सकते हैं।  

## पैकेज इम्पोर्ट करें
पहले, आवश्यक क्लासेस को अपने Java प्रोजेक्ट में इम्पोर्ट करें:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## OneNote को HTML के रूप में सहेजते समय फ़ॉन्ट्स को कैसे एक्सपोर्ट करें?
नीचे एक चरण‑दर‑चरण गाइड है जो आपको **फ़ॉन्ट्स को एक्सपोर्ट करने** और अन्य संसाधनों को दिखाता है।

### चरण 1: प्रोग्रामेटिक रूप से OneNote दस्तावेज़ बनाएं  
```java
Document document = new Document("Path_to_your_sample_one_file");
```

यह पंक्ति मौजूदा `.one` फ़ाइल को लोड करती है। यदि आपको **प्रोग्रामेटिक रूप से OneNote बनाना** है, तो आप एक नया `Document` ऑब्जेक्ट बना सकते हैं और API के माध्यम से सेक्शन/पेज जोड़ सकते हैं (यहाँ फ़ॉन्ट्स को एक्सपोर्ट करने पर ध्यान केंद्रित रखने के लिए नहीं दिखाया गया है)।

### चरण 2: एम्बेडेड फ़ॉन्ट्स के साथ मेमोरी स्ट्रीम में सहेजें  
```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` Aspose.Note को **फ़ॉन्ट्स को सीधे HTML पैकेज में एक्सपोर्ट** करने के लिए बताता है।  
- `setFontFaceTypes(FontFaceType.Ttf)` यह सुनिश्चित करता है कि TrueType फ़ॉन्ट्स उपयोग किए जाएँ, जो ब्राउज़र में व्यापक समर्थन रखते हैं।

### चरण 3: अलग संसाधन फ़ाइलों के साथ HTML के रूप में सहेजें (फ़ॉन्ट्स अभी भी एक्सपोर्ट हो रहे हैं)  
```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

भले ही CSS और छवियां एम्बेडेड हों, यदि आप आसान कैशिंग के लिए अलग फ़ाइलें चाहते हैं तो आप `ResourceExportType` को `ExportExternal` बदल सकते हैं। मुख्य भाग—**फ़ॉन्ट्स को एक्सपोर्ट करना**—अभी भी वही रहता है।

### चरण 4: प्रत्येक संसाधन को कहाँ संग्रहीत किया जाए, इसे नियंत्रित करने के लिए कॉलबैक्स का उपयोग करें  
```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

`UserSavingCallbacks` क्लास (आपको `ICssSavingCallback`, `IImageSavingCallback`, और `IFontSavingCallback` को इम्प्लीमेंट करना होगा) आपको फ़ोल्डर संरचना पर पूर्ण नियंत्रण देता है, जिससे आप फ़ॉन्ट्स को एक समर्पित `fonts` डायरेक्टरी में रख सकते हैं जबकि **फ़ॉन्ट्स को सही ढंग से एक्सपोर्ट** किया जा रहा है।

## OneNote को HTML में बदलते समय कस्टम फ़ॉन्ट्स को कैसे एम्बेड करें
कस्टम फ़ॉन्ट्स को एम्बेड करने से यह सुनिश्चित होता है कि HTML रेंडरिंग मूल OneNote लेआउट से मेल खाती है, भले ही डिवाइस में वह फ़ॉन्ट स्थापित न हो। `ExportEmbedded` को `FontFaceType.Ttf` के साथ उपयोग करने पर, TrueType फ़ाइलें base‑64 एन्कोड हो जाती हैं और उत्पन्न CSS में सीधे सम्मिलित हो जाती हैं, जिससे बाहरी फ़ॉन्ट होस्टिंग की आवश्यकता समाप्त हो जाती है।

## ResourceExportType का उपयोग करके संसाधन एक्सपोर्ट को नियंत्रित करना
`ResourceExportType` आपको यह तय करने देता है कि CSS, छवियां, और फ़ॉन्ट्स **HTML फ़ाइल के अंदर** (`ExportEmbedded`) संग्रहीत हों या **बाहरी** फ़ाइलों (`ExportExternal`) के रूप में सहेजे जाएँ। एकल‑फ़ाइल समाधान के लिए `ExportEmbedded` चुनें, या बड़े एसेट्स के लिए ब्राउज़र कैशिंग का उपयोग करने हेतु `ExportExternal` चुनें।

## HTML एक्सपोर्ट के लिए प्रोग्रामेटिक रूप से OneNote बनाना
यदि आप शून्य से शुरू करते हैं, तो आप पूरी तरह कोड में OneNote दस्तावेज़ बना सकते हैं, सेक्शन, पेज, और रिच टेक्स्ट जोड़ सकते हैं, और फिर ऊपर दिखाए गए समान `HtmlSaveOptions` लागू कर सकते हैं। यह आपको डेटा जेनरेशन से लेकर एम्बेडेड कस्टम फ़ॉन्ट्स वाले पूर्ण स्टाइल्ड HTML आउटपुट तक एंड‑टू‑एंड ऑटोमेशन देता है।

## सामान्य समस्याएँ और टिप्स
- **आउटपुट में फ़ॉन्ट्स गायब:** सुनिश्चित करें कि `setExportFonts(ResourceExportType.ExportEmbedded)` सेट है और स्रोत OneNote फ़ाइल वास्तव में एम्बेडेड फ़ॉन्ट्स का उपयोग करती है।  
- **बड़े HTML फ़ाइलें:** फ़ॉन्ट्स को एम्बेड करने से आकार बढ़ सकता है। यदि बैंडविड्थ समस्या है, तो `ExportFonts` को `ExportExternal` में बदलें और फ़ॉन्ट्स को CDN पर होस्ट करें।  
- **कॉलबैक इम्प्लीमेंटेशन त्रुटियां:** सुनिश्चित करें कि आपके कॉलबैक क्लासेस स्ट्रीम को सही ढंग से लिखते हैं और संसाधनों को बंद करते हैं ताकि फ़ाइल भ्रष्ट न हो।  

## अक्सर पूछे जाने वाले प्रश्न
**प्रश्न:** क्या मैं एक साथ कई OneNote दस्तावेज़ों को HTML में बदल सकता हूँ?  
**उत्तर:** हाँ, प्रत्येक `Document` इंस्टेंस पर लूप करें और समान `HtmlSaveOptions` लागू करें।  

**प्रश्न:** क्या Aspose.Note for Java HTML के अलावा अन्य आउटपुट फ़ॉर्मेट्स को सपोर्ट करता है?  
**उत्तर:** बिल्कुल। आप उपयुक्त सेव विकल्पों का उपयोग करके PDF, DOCX, PNG, JPEG, और अधिक में एक्सपोर्ट कर सकते हैं।  

**प्रश्न:** क्या Aspose.Note for Java के लिए ट्रायल संस्करण उपलब्ध है?  
**उत्तर:** हाँ, [यहाँ](https://releases.aspose.com/) से एक मुफ्त ट्रायल डाउनलोड करें।  

**प्रश्न:** मैं Aspose.Note for Java के लिए समर्थन कहाँ प्राप्त कर सकता हूँ?  
**उत्तर:** समुदाय और आधिकारिक सहायता के लिए [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) पर जाएँ।  

**प्रश्न:** मैं Aspose.Note for Java का लाइसेंस कैसे खरीद सकता हूँ?  
**उत्तर:** लाइसेंस [Aspose वेबसाइट](https://purchase.aspose.com/buy) पर उपलब्ध हैं।  

## निष्कर्ष
अब आप जानते हैं कि Aspose.Note for Java का उपयोग करके **OneNote को HTML के रूप में सहेजते समय फ़ॉन्ट्स को कैसे एक्सपोर्ट करें**। `HtmlSaveOptions` को कॉन्फ़िगर करके और वैकल्पिक रूप से कॉलबैक्स का उपयोग करके, आप अपने OneNote पृष्ठों की सटीक रूपरेखा—कस्टम फ़ॉन्ट्स सहित—वेब पर प्रदान करते समय संरक्षित रख सकते हैं। अपने प्रोजेक्ट की प्रदर्शन और स्टोरेज आवश्यकताओं के अनुसार विभिन्न `ResourceExportType` सेटिंग्स के साथ प्रयोग करने में संकोच न करें।

---

**अंतिम अपडेट:** 2026-02-07  
**परीक्षित संस्करण:** Aspose.Note for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
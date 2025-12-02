---
date: 2025-12-02
description: Aspose.Note for Java का उपयोग करके OneNote को HTML के रूप में सहेजते
  समय फ़ॉन्ट निर्यात करना सीखें। यह गाइड आपको प्रोग्रामेटिक रूप से OneNote बनाने और
  फ़ॉन्ट, CSS, तथा छवियों को एम्बेड करने का तरीका दिखाता है।
language: hi
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: वननोट को HTML के रूप में सहेजते समय फ़ॉन्ट्स को कैसे निर्यात करें – जावा
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote को HTML के रूप में सहेजते समय फ़ॉन्ट निर्यात कैसे करें – Java

## परिचय

इस ट्यूटोरियल में आप **फ़ॉन्ट निर्यात कैसे करें** जब आप **OneNote को HTML के रूप में सहेजते** हैं, Aspose.Note for Java का उपयोग करके जानेंगे। हम प्रोग्रामेटिक रूप से OneNote दस्तावेज़ बनाने, HTML सहेजने के विकल्पों को कॉन्फ़िगर करने, और आवश्यक फ़ॉन्ट फ़ाइलों को एम्बेड करने की प्रक्रिया से गुजरेंगे ताकि परिणामी HTML मूल OneNote पृष्ठों जैसा ही दिखे। यह तरीका तब बिल्कुल उपयुक्त है जब आपको OneNote सामग्री की दृश्य सटीकता को वेब‑फ़्रेंडली फ़ॉर्मेट में संरक्षित रखना हो।

## त्वरित उत्तर
- **निर्यात को संभालने वाली लाइब्रेरी कौन सी है?** Aspose.Note for Java  
- **क्या फ़ॉन्ट को HTML में एम्बेड किया जा सकता है?** हाँ – `ExportFonts` को `ExportEmbedded` सेट करें  
- **क्या उत्पादन के लिए लाइसेंस की आवश्यकता है?** व्यावसायिक उपयोग के लिए एक वैध Aspose.Note लाइसेंस आवश्यक है  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर  
- **क्या संसाधनों को अलग फ़ाइलों में सहेजना संभव है?** बिल्कुल – `ResourceExportType` को तदनुसार कॉन्फ़िगर करें  

## OneNote HTML रूपांतरण के संदर्भ में “फ़ॉन्ट निर्यात कैसे करें” क्या है?

जब आप OneNote नोटबुक को HTML में बदलते हैं, तो दृश्य रूप CSS, इमेज और विशेष रूप से मूल पृष्ठों में उपयोग किए गए फ़ॉन्ट पर निर्भर करता है। **फ़ॉन्ट निर्यात** का अर्थ है फ़ॉन्ट फ़ाइलों (जैसे TTF) को सीधे HTML पैकेज में एम्बेड करना ताकि ब्राउज़र टेक्स्ट को ठीक उसी तरह रेंडर कर सके जैसा OneNote में दिखता है, भले ही अंतिम उपयोगकर्ता के पास ये फ़ॉन्ट स्थानीय रूप से इंस्टॉल न हों।

## प्रोग्रामेटिक रूप से OneNote क्यों बनाएं और इसे HTML के रूप में सहेजें?

- **ऑटोमेशन:** OneNote से रिपोर्ट, दस्तावेज़ या ज्ञान‑आधार लेख उत्पन्न करें बिना मैन्युअल कॉपी‑पेस्ट के।  
- **संगति:** लेआउट, स्टाइलिंग और कस्टम फ़ॉन्ट को विभिन्न डिवाइसों पर बनाए रखें।  
- **पोर्टेबिलिटी:** HTML सार्वभौमिक रूप से देखा जा सकता है—OneNote क्लाइंट की आवश्यकता नहीं।  

## पूर्वापेक्षाएँ

1. Java Development Kit (JDK) 8 या नया स्थापित हो।  
2. Aspose.Note for Java लाइब्रेरी – [यहाँ](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. लोड करने के लिए एक नमूना OneNote फ़ाइल (`.one`), या आप प्रोग्रामेटिक रूप से नई फ़ाइल बना सकते हैं।  

## इम्पोर्ट पैकेज

सबसे पहले, आवश्यक क्लासेज़ को अपने Java प्रोजेक्ट में इम्पोर्ट करें:

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

## OneNote को HTML के रूप में सहेजते समय फ़ॉन्ट कैसे निर्यात करें?

नीचे एक चरण‑दर‑चरण गाइड है जो आपको **फ़ॉन्ट निर्यात** और अन्य संसाधनों को दिखाता है।

### चरण 1: प्रोग्रामेटिक रूप से OneNote दस्तावेज़ बनाएं  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

यह पंक्ति मौजूदा `.one` फ़ाइल को लोड करती है। यदि आपको **प्रोग्रामेटिक रूप से OneNote बनाना** है, तो आप एक नया `Document` ऑब्जेक्ट इंस्टैंशिएट कर सकते हैं और API के माध्यम से सेक्शन/पेज जोड़ सकते हैं (फ़ॉन्ट निर्यात पर ध्यान केंद्रित रखने के लिए यहाँ नहीं दिखाया गया है)।

### चरण 2: एम्बेडेड फ़ॉन्ट के साथ मेमोरी स्ट्रीम में सहेजें  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` Aspose.Note को **फ़ॉन्ट निर्यात** सीधे HTML पैकेज में करने के लिए बताता है।  
- `setFontFaceTypes(FontFaceType.Ttf)` सुनिश्चित करता है कि TrueType फ़ॉन्ट उपयोग किए जाएँ, जो अधिकांश ब्राउज़र में समर्थित हैं।

### चरण 3: अलग संसाधन फ़ाइलों के साथ HTML के रूप में सहेजें (फ़ॉन्ट निर्यात अभी भी सक्रिय है)

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

भले ही CSS और इमेज एम्बेडेड हों, आप `ResourceExportType` को `ExportExternal` में बदल सकते हैं यदि आप आसान कैशिंग के लिए अलग फ़ाइलें पसंद करते हैं। मुख्य भाग—**फ़ॉन्ट निर्यात**—अभी भी वही रहता है।

### चरण 4: प्रत्येक संसाधन को कहाँ संग्रहीत किया जाए, इसे नियंत्रित करने के लिए कॉलबैक का उपयोग करें

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

`UserSavingCallbacks` क्लास (आपको `ICssSavingCallback`, `IImageSavingCallback`, और `IFontSavingCallback` को इम्प्लीमेंट करना होगा) आपको फ़ोल्डर संरचना पर पूर्ण नियंत्रण देती है, जिससे आप फ़ॉन्ट को एक समर्पित `fonts` डायरेक्टरी में रख सकते हैं जबकि फिर भी **फ़ॉन्ट निर्यात** सही ढंग से हो रहा हो।

## सामान्य समस्याएँ और सुझाव

- **आउटपुट में फ़ॉन्ट गायब हैं:** सुनिश्चित करें कि `setExportFonts(ResourceExportType.ExportEmbedded)` सेट है और स्रोत OneNote फ़ाइल वास्तव में एम्बेडेड फ़ॉन्ट का उपयोग करती है।  
- **बड़े HTML फ़ाइलें:** फ़ॉन्ट एम्बेड करने से आकार बढ़ सकता है। यदि बैंडविड्थ समस्या है, तो `ExportFonts` को `ExportExternal` में बदलें और फ़ॉन्ट को CDN पर होस्ट करें।  
- **कॉलबैक इम्प्लीमेंटेशन त्रुटियाँ:** सुनिश्चित करें कि आपके कॉलबैक क्लास सही ढंग से स्ट्रीम लिखते हैं और संसाधनों को बंद करते हैं ताकि फ़ाइल भ्रष्ट न हो।  

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं एक साथ कई OneNote दस्तावेज़ों को HTML में बदल सकता हूँ?**  
A: हाँ, प्रत्येक `Document` इंस्टेंस पर लूप करें और समान `HtmlSaveOptions` लागू करें।  

**Q: क्या Aspose.Note for Java HTML के अलावा अन्य आउटपुट फ़ॉर्मेट का समर्थन करता है?**  
A: बिल्कुल। आप उपयुक्त सहेजने के विकल्पों का उपयोग करके PDF, DOCX, PNG, JPEG और अधिक फ़ॉर्मेट में निर्यात कर सकते हैं।  

**Q: क्या Aspose.Note for Java के लिए कोई ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, [यहाँ](https://releases.aspose.com/) से एक मुफ्त ट्रायल डाउनलोड करें।  

**Q: Aspose.Note for Java के लिए समर्थन कहाँ प्राप्त कर सकता हूँ?**  
A: समुदाय और आधिकारिक सहायता के लिए [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) देखें।  

**Q: Aspose.Note for Java के लिए लाइसेंस कैसे खरीदूँ?**  
A: लाइसेंस [Aspose वेबसाइट](https://purchase.aspose.com/buy) पर उपलब्ध हैं।  

## निष्कर्ष

आप अब जानते हैं **फ़ॉन्ट निर्यात** कैसे करें जबकि आप **OneNote को HTML के रूप में सहेजते** हैं Aspose.Note for Java का उपयोग करके। `HtmlSaveOptions` को कॉन्फ़िगर करके और वैकल्पिक रूप से कॉलबैक का उपयोग करके, आप अपने OneNote पृष्ठों की सटीक लुक—कस्टम फ़ॉन्ट सहित—वेब पर डिलीवर कर सकते हैं। विभिन्न `ResourceExportType` सेटिंग्स के साथ प्रयोग करें ताकि आपके प्रोजेक्ट की प्रदर्शन और स्टोरेज आवश्यकताओं के अनुसार अनुकूलित किया जा सके।

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

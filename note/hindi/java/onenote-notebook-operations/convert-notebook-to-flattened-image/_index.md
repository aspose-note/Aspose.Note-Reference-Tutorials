---
date: 2025-12-25
description: Aspose.Note for Java का उपयोग करके OneNote को PNG में बदलना सीखें। यह
  गाइड दिखाता है कि कैसे इमेज रेज़ोल्यूशन सेट करें, नोटबुक को फ्लैटन करें, और OneNote
  को प्रभावी ढंग से इमेज के रूप में सहेजें।
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: OneNote को PNG में कैसे बदलें – Aspose.Note के साथ नोटबुक को इमेज में फ्लैटन
  करें
url: /hi/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में नोटबुक को फ्लैटेड इमेज में परिवर्तित करें - Aspose.Note

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि कैसे **OneNote को PNG में परिवर्तित** किया जाए, जिसमें पूरी नोटबुक को Aspose.Note for Java का उपयोग करके एक ही फ्लैटेड इमेज में बदला जाता है। यह तरीका तब उत्तम है जब आपको नोटबुक को स्थिर चित्र के रूप में साझा करना हो, रिपोर्ट में एम्बेड करना हो, या बिना किसी दृश्य विवरण के खोए इसे आर्काइव करना हो।

## त्वरित उत्तर
- **flatten notebook** का क्या अर्थ है? यह सभी पृष्ठ तत्वों को एक रास्टर इमेज में मिलाता है।  
- **कौन सा फॉर्मेट उपयोग किया जाता है?** PNG डिफ़ॉल्ट है, जो लॉस‑लेस क्वालिटी देता है।  
- **क्या मैं DPI बदल सकता हूँ?** हाँ, `ImageSaveOptions` पर `setResolution` का उपयोग करें।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या यह सभी OS पर समर्थित है?** Java API जहाँ भी Java चलता है, वहाँ चलता है।

## OneNote को PNG में परिवर्तित करना क्या है?

OneNote को PNG में परिवर्तित करने से नोटबुक के प्रत्येक पृष्ठ की बिटमैप प्रतिनिधित्व बनती है, जिसमें टेक्स्ट, ड्रॉइंग और एम्बेडेड ऑब्जेक्ट्स एक ही इमेज फ़ाइल में संरक्षित रहते हैं। यह विशेष रूप से दस्तावेज़ीकरण, प्रस्तुतियों, या अनुपालन आर्काइव के लिए उपयोगी है।

## Aspose.Note के साथ OneNote को PNG में क्यों परिवर्तित करें?

- **पूर्ण सटीकता** – सभी दृश्य तत्व बरकरार रहते हैं।  
- **एकल‑फ़ाइल आउटपुट** – कई पृष्ठ फ़ाइलों को प्रबंधित करने की आवश्यकता नहीं।  
- **कस्टमाइज़ेबल रिज़ॉल्यूशन** – गुणवत्ता आवश्यकताओं को पूरा करने के लिए DPI समायोजित करें।  
- **कोई Office इंस्टॉलेशन नहीं** – Microsoft OneNote से पूरी तरह स्वतंत्र रूप से काम करता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर Java Development Kit (JDK) स्थापित हो।  
2. Aspose.Note for Java लाइब्रेरी डाउनलोड करके अपने Java प्रोजेक्ट में सेट अप करें। आप लाइब्रेरी [यहाँ](https://releases.aspose.com/note/java/) से डाउनलोड कर सकते हैं।  
3. Java प्रोग्रामिंग का बुनियादी ज्ञान।

## पैकेज इम्पोर्ट करें

शुरू करने के लिए, आपको Aspose.Note for Java से आवश्यक पैकेज इम्पोर्ट करने होंगे:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## चरण 1: दस्तावेज़ डायरेक्टरी सेट करें

सबसे पहले, उस डायरेक्टरी को परिभाषित करें जहाँ आपका नोटबुक फ़ाइल स्थित है:

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को अपने नोटबुक फ़ाइल के पथ से बदलें।

## चरण 2: नोटबुक लोड करें

अगला, `Notebook` क्लास का उपयोग करके नोटबुक फ़ाइल लोड करें:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

`"test.onetoc2"` को अपने नोटबुक फ़ाइल के नाम से बदलना सुनिश्चित करें।

## चरण 3: इमेज सेव ऑप्शन सेट करें

अब, नोटबुक को इमेज के रूप में सेव करने के विकल्प सेट करें। हम सेव फॉर्मेट को PNG निर्धारित करेंगे और रिज़ॉल्यूशन को 400 DPI सेट करेंगे:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

आप अपनी आवश्यकताओं के अनुसार रिज़ॉल्यूशन समायोजित कर सकते हैं। यहाँ आप आउटपुट क्वालिटी को नियंत्रित करने के लिए **इमेज रिज़ॉल्यूशन सेट** करते हैं।

## चरण 4: नोटबुक को फ्लैट करें

सभी तत्वों को एक ही इमेज में फ्लैट करने के लिए, `flatten` विकल्प को `true` सेट करें:

```java
saveOptions.setFlatten(true);
```

`flatten` को `true` सेट करने से यह सुनिश्चित होता है कि परिणामी PNG आपके नोटबुक के सटीक लेआउट को बनाए रखता है।

## चरण 5: इमेज सेव करें

अंत में, नोटबुक को फ्लैटेड इमेज के रूप में सेव करें:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

`"ExportImageasFlattenedNotebook_out.png"` को अपनी इच्छित आउटपुट फ़ाइल नाम से बदलें। यह चरण **OneNote को इमेज के रूप में सेव** करता है जिसे आप कहीं भी साझा या एम्बेड कर सकते हैं।

## सामान्य उपयोग केस

- **दस्तावेज़ीकरण:** तकनीकी मैनुअल या उपयोगकर्ता गाइड में नोटबुक इमेज एम्बेड करें।  
- **प्रस्तुतियाँ:** फ़ॉन्ट या ऑब्जेक्ट संगतता की चिंता किए बिना PowerPoint में हाई‑रेज़ॉल्यूशन PNG स्लाइड का उपयोग करें।  
- **आर्काइविंग:** अनुपालन ऑडिट के लिए नोटबुक का रीड‑ओनली स्नैपशॉट संग्रहित करें।

## समस्या निवारण टिप्स

- **फ़ाइल नहीं मिली:** `dataDir` पाथ को दोबारा जांचें और सुनिश्चित करें कि `.onetoc2` फ़ाइल मौजूद है।  
- **कम क्वालिटी इमेज:** DPI बढ़ाने के लिए `documentSaveOptions.setResolution(600);` बदलें।  
- **गायब तत्व:** सुनिश्चित करें कि `saveOptions.setFlatten(true);` सक्षम है; अन्यथा कुछ लेयर अलग रह सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं आउटपुट इमेज का रिज़ॉल्यूशन समायोजित कर सकता हूँ?**  
A1: हाँ, आप `setResolution` मेथड पैरामीटर को बदलकर अपनी आवश्यकताओं के अनुसार रिज़ॉल्यूशन समायोजित कर सकते हैं।

**Q2: क्या Aspose.Note निर्यात के लिए अन्य इमेज फॉर्मेट्स का समर्थन करता है?**  
A2: हाँ, Aspose.Note नोटबुक निर्यात के लिए PNG, JPEG, BMP आदि जैसे विभिन्न इमेज फॉर्मेट्स का समर्थन करता है।

**Q3: क्या मैं आउटपुट इमेज को और कस्टमाइज़ कर सकता हूँ?**  
A3: हाँ, Aspose.Note आउटपुट इमेज को कस्टमाइज़ करने के लिए विस्तृत विकल्प प्रदान करता है, जिसमें पेज साइज, ओरिएंटेशन, और क्वालिटी सेटिंग्स शामिल हैं।

**Q4: क्या Aspose.Note for Java के लिए ट्रायल वर्ज़न उपलब्ध है?**  
A4: हाँ, आप एक मुफ्त ट्रायल वर्ज़न [यहाँ](https://releases.aspose.com/) से प्राप्त कर सकते हैं।

**Q5: Aspose.Note for Java के लिए समर्थन कहाँ मिल सकता है?**  
A5: आप Aspose.Note फ़ोरम पर समर्थन और संसाधन [यहाँ](https://forum.aspose.com/c/note/28) पा सकते हैं।

---

**अंतिम अपडेट:** 2025-12-25  
**परीक्षण किया गया:** Aspose.Note for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
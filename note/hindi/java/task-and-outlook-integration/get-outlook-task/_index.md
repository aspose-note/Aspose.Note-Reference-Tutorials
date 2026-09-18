---
date: 2026-04-01
description: Aspose.Note for Java का उपयोग करके Outlook से OneNote में कार्य निकालना
  सीखें। कार्य विवरण को जल्दी प्राप्त करने के लिए इस चरण‑दर‑चरण गाइड का पालन करें।
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: Outlook कार्य OneNote में प्राप्त करें - Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note के साथ OneNote में Outlook कार्यों को निकालने का तरीका
url: /hi/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में Outlook कार्य प्राप्त करें - Aspose.Note

## परिचय
Aspose.Note for Java का उपयोग करके OneNote नोटबुक में Outlook से **कार्य निकालने का तरीका** पर हमारा व्यापक मार्गदर्शक में आपका स्वागत है। चाहे आप माइग्रेशन टूल बना रहे हों, रिपोर्ट जनरेट कर रहे हों, या केवल कार्य डेटा को सिंक करने की आवश्यकता हो, यह ट्यूटोरियल आपको हर चरण में ले जाता है— OneNote फ़ाइल लोड करने से लेकर प्रत्येक Outlook कार्य की प्रॉपर्टीज़ पढ़ने तक। अंत तक, आपके पास एक तैयार‑उपयोग कोड स्निपेट होगा जिसे आप अपने प्रोजेक्ट्स में अनुकूलित कर सकते हैं।

## त्वरित उत्तर
- **यह ट्यूटोरियल क्या कवर करता है?** Aspose.Note for Java के साथ OneNote दस्तावेज़ से Outlook कार्य विवरण निकालना।  
- **कौन सा API उपयोग किया गया है?** Aspose.Note Java लाइब्रेरी।  
- **क्या मुझे लाइसेंस की आवश्यकता है?** विकास के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** पर्यावरण सेट अप होने के बाद लगभग 10‑15 मिनट।  
- **क्या मैं कई नोटबुक्स प्रोसेस कर सकता हूँ?** हाँ—फ़ाइलों पर लूप करें और वही लॉजिक पुन: उपयोग करें।

## कार्य निष्कर्षण क्या है?
कार्य निष्कर्षण का मतलब है संरचित कार्य जानकारी (जैसे नियत तिथियां, स्थिति, और आइकन) को पढ़ना जो Outlook OneNote पृष्ठों के अंदर `NoteTask` टैग के रूप में संग्रहीत करता है। यह मैन्युअल कॉपी किए बिना कार्य मेटाडेटा तक प्रोग्रामेटिक पहुंच सक्षम करता है।

## Java के लिए Aspose.Note का उपयोग क्यों करें?
- **Microsoft Office की आवश्यकता नहीं** – Java रनटाइम वाले किसी भी प्लेटफ़ॉर्म पर काम करता है।  
- **पूर्ण सटीकता** – सभी OneNote तत्वों को संरक्षित रखता है जबकि आपको टैग्स तक सीधी पहुंच देता है।  
- **उच्च प्रदर्शन** – बड़े नोटबुक्स और बैच प्रोसेसिंग के लिए अनुकूलित।  

## पूर्वापेक्षाएँ
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित तैयार हैं:

- **Java विकास पर्यावरण** – JDK 8 या नया स्थापित और कॉन्फ़िगर किया हुआ।  
- **Aspose.Note लाइब्रेरी** – आधिकारिक साइट से नवीनतम Java पैकेज डाउनलोड करें [here](https://releases.aspose.com/note/java/).  
- **एक नमूना OneNote फ़ाइल** – ट्यूटोरियल `Sample1.one` का उपयोग करता है; आप इसे किसी भी नोटबुक से बदल सकते हैं जिसमें Outlook कार्य हों।

## पैकेज आयात करें
अपने Java क्लास में आवश्यक इम्पोर्ट जोड़ें। ये क्लासेज़ आपको दस्तावेज़ मॉडल और Outlook‑विशिष्ट `NoteTask` टैग तक पहुंच देती हैं।

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## क्रमिक मार्गदर्शिका

### चरण 1: अपने दस्तावेज़ निर्देशिका को सेट करें
उस फ़ोल्डर को परिभाषित करें जिसमें आपका OneNote फ़ाइल है। पूर्ण या सापेक्ष पाथ का उपयोग काम करता है, लेकिन पठनीयता के लिए पाथ स्ट्रिंग को साफ रखें।

```java
String dataDir = "Your Document Directory";
```

### चरण 2: OneNote दस्तावेज़ लोड करें
`Document` इंस्टेंस बनाएं `.one` फ़ाइल की ओर इशारा करके। Aspose.Note फ़ाइल को एक DOM‑समान संरचना में पार्स करता है जिसे आप ट्रैवर्स कर सकते हैं।

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### चरण 3: सभी RichText नोड्स प्राप्त करें
Outlook कार्य `RichText` तत्वों के अंदर संग्रहीत होते हैं। प्रत्येक `RichText` नोड को प्राप्त करें ताकि आप उसके टैग्स की जांच कर सकें।

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### चरण 4: प्रत्येक नोड पर इटररेट करें
प्रत्येक `RichText` नोड पर लूप करें, उसके टैग्स की जांच करें, और जब आप `NoteTask` से मिलें तो कार्रवाई करें। नीचे दिया गया कोड प्रत्येक कार्य के सबसे उपयोगी प्रॉपर्टीज़ को प्रिंट करता है।

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**Pro tip:** यदि आपको केवल प्रॉपर्टीज़ का एक उपसमुच्चय चाहिए, तो बड़े नोटबुक्स को प्रोसेस करते समय प्रदर्शन सुधारने के लिए अन्य को छोड़ सकते हैं।

### सामान्य समस्याएँ और समाधान
- **कोई कार्य नहीं मिला:** सुनिश्चित करें कि OneNote पेज में वास्तव में Outlook कार्य हैं। वे छोटे Outlook आइकन वाले चेक‑बॉक्स के रूप में दिखते हैं।  
- **Null मान:** कुछ कार्य फ़ील्ड्स (जैसे `CompletedTime`) `null` हो सकते हैं यदि कार्य पूर्ण नहीं हुआ है। प्रिंट करने से पहले `null` की जाँच करके `NullPointerException` से बचें।  
- **फ़ाइल नहीं मिली:** सुनिश्चित करें कि `dataDir` आपके OS के लिए उपयुक्त पाथ सेपरेटर (`/` या `\\`) के साथ समाप्त हो।

## निष्कर्ष
बधाई हो! आपने Aspose.Note Java API का उपयोग करके OneNote में Outlook से **कार्य निकालने का तरीका** सीख लिया है। यह दृष्टिकोण आपको कार्य डेटा पर पूर्ण प्रोग्रामेटिक नियंत्रण देता है, जिससे कस्टम रिपोर्टिंग टूल्स, डेटाबेस, या अन्य व्यावसायिक वर्कफ़्लो के साथ एकीकरण संभव होता है।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.Note सभी संस्करणों के OneNote के साथ संगत है?**  
A: Aspose.Note Microsoft OneNote 2010 और बाद के संस्करणों का समर्थन करता है।

**Q: क्या मैं Aspose.Note को व्यक्तिगत और व्यावसायिक दोनों प्रोजेक्ट्स के लिए उपयोग कर सकता हूँ?**  
A: हाँ, Aspose.Note को व्यक्तिगत और व्यावसायिक दोनों प्रोजेक्ट्स के लिए उपयोग किया जा सकता है। लाइसेंस विकल्पों को देखने के लिए [here](https://purchase.aspose.com/buy) पर जाएँ।

**Q: क्या Aspose.Note के लिए मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप मुफ्त ट्रायल [here](https://releases.aspose.com/) पर एक्सेस कर सकते हैं।

**Q: मैं Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूँ?**  
A: समुदाय समर्थन के लिए [Aspose.Note Forum](https://forum.aspose.com/c/note/28) पर जाएँ। अतिरिक्त सहायता के लिए, एक [temporary license](https://purchase.aspose.com/temporary-license/) खरीदने पर विचार करें।

**Q: क्या परीक्षण के लिए कोई नमूना OneNote दस्तावेज़ उपलब्ध हैं?**  
A: आप Aspose.Note दस्तावेज़ीकरण में नमूना दस्तावेज़ [here](https://reference.aspose.com/note/java/) पर पा सकते हैं।

---

**अंतिम अपडेट:** 2026-04-01  
**परीक्षण किया गया:** Aspose.Note for Java 24.12 (latest at time of writing)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
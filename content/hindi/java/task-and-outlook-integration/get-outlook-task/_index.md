---
title: OneNote में आउटलुक कार्य प्राप्त करें - Aspose.Note
linktitle: OneNote में आउटलुक कार्य प्राप्त करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: OneNote से Outlook कार्यों को सहजता से निकालने में Java के लिए Aspose.Note की शक्ति का अन्वेषण करें। हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें और अपनी दस्तावेज़ प्रसंस्करण क्षमताओं को बढ़ाएं।
type: docs
weight: 10
url: /hi/java/task-and-outlook-integration/get-outlook-task/
---
## परिचय
OneNote में Outlook कार्यों को निर्बाध रूप से पुनर्प्राप्त करने के लिए Java के लिए Aspose.Note का उपयोग करने पर हमारी व्यापक मार्गदर्शिका में आपका स्वागत है। Aspose.Note एक शक्तिशाली जावा एपीआई है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ सहजता से काम करने की अनुमति देता है। इस ट्यूटोरियल में, हम आपको OneNote दस्तावेज़ से चरण दर चरण आउटलुक कार्यों को निकालने की प्रक्रिया के बारे में बताएंगे।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
- जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।
-  Aspose.Note लाइब्रेरी: जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड और इंस्टॉल करें। आप पुस्तकालय पा सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
## पैकेज आयात करें
आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। अपने कोड में निम्नलिखित पंक्तियाँ जोड़ें:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;

```
अब, आइए इस प्रक्रिया को प्रबंधनीय चरणों में विभाजित करें:
## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें
उस निर्देशिका को परिभाषित करें जहाँ आपका OneNote दस्तावेज़ स्थित है:
```java
String dataDir = "Your Document Directory";
```
## चरण 2: OneNote दस्तावेज़ लोड करें
Aspose.Note का उपयोग करके OneNote दस्तावेज़ लोड करें:
```java
Document doc = new Document(dataDir + "Sample1.one");
```
## चरण 3: सभी रिचटेक्स्ट नोड्स प्राप्त करें
दस्तावेज़ से सभी रिचटेक्स्ट नोड्स पुनर्प्राप्त करें:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## चरण 4: प्रत्येक नोड के माध्यम से पुनरावृति करें
प्रत्येक रिचटेक्स्ट नोड के माध्यम से पुनरावृति करें और नोटटास्क टैग की जांच करें:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // गुण पुनः प्राप्त करें
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```
## निष्कर्ष
बधाई हो! आपने OneNote में Outlook कार्यों को पुनः प्राप्त करने के लिए Java के लिए Aspose.Note का उपयोग करना सफलतापूर्वक सीख लिया है। यह शक्तिशाली एपीआई प्रक्रिया को सरल बनाती है, जिससे यह कुशल और डेवलपर-अनुकूल बन जाती है।
## पूछे जाने वाले प्रश्न
### क्या Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?
Aspose.Note Microsoft OneNote 2010 और बाद के संस्करणों का समर्थन करता है।
### क्या मैं व्यक्तिगत और व्यावसायिक दोनों परियोजनाओं के लिए Aspose.Note का उपयोग कर सकता हूँ?
 हां, Aspose.Note का उपयोग व्यक्तिगत और व्यावसायिक दोनों परियोजनाओं के लिए किया जा सकता है। मिलने जाना[यहाँ](https://purchase.aspose.com/buy) लाइसेंसिंग विकल्पों का पता लगाने के लिए।
### क्या Aspose.Note के लिए कोई निःशुल्क परीक्षण उपलब्ध है?
 हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मैं Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूँ?
 दौरा करना[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) सामुदायिक समर्थन के लिए. अतिरिक्त सहायता के लिए, खरीदने पर विचार करें[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/).
### क्या परीक्षण के लिए कोई नमूना OneNote दस्तावेज़ उपलब्ध हैं?
 आप Aspose.Note दस्तावेज़ में नमूना दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/note/java/).
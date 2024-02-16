---
title: OneNote दस्तावेज़ में तालिका से पंक्ति पाठ निकालें - Aspose.Note
linktitle: OneNote दस्तावेज़ में तालिका से पंक्ति पाठ निकालें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note के साथ OneNote तालिकाओं से पंक्ति पाठ को आसानी से निकालना सीखें। निर्बाध एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 13
url: /hi/java/onenote-table-manipulation/extract-row-text-from-table/
---
## परिचय
जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में तालिकाओं से पंक्ति पाठ निकालने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। Aspose.Note एक शक्तिशाली जावा लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ निर्बाध रूप से काम करने में सक्षम बनाती है। इस ट्यूटोरियल में, हम चरण-दर-चरण प्रक्रिया के माध्यम से आपका मार्गदर्शन करेंगे, यह प्रदर्शित करते हुए कि आपके OneNote दस्तावेज़ों में तालिकाओं से पंक्ति पाठ को कुशलतापूर्वक कैसे निकाला जाए।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
-  जावा लाइब्रेरी के लिए Aspose.Note: सुनिश्चित करें कि आपके पास जावा लाइब्रेरी के लिए Aspose.Note स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[लिंक को डाउनलोड करें](https://releases.aspose.com/note/java/).
- जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।
- OneNote दस्तावेज़: एक नमूना OneNote दस्तावेज़ तैयार करें (उदाहरण के लिए, "Sample1.one") जिसमें वे तालिकाएँ हों जिनसे आप पंक्ति पाठ निकालना चाहते हैं।
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में, आवश्यक Aspose.Note पैकेज आयात करें। यह सुनिश्चित करता है कि आपके पास OneNote दस्तावेज़ों के साथ काम करने के लिए आवश्यक कक्षाओं और विधियों तक पहुंच है।
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## चरण 1: दस्तावेज़ निर्देशिका सेट करें
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
```
## चरण 2: OneNote दस्तावेज़ लोड करें
```java
// दस्तावेज़ को Aspose.Note में लोड करें।
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## चरण 3: टेबल नोड्स प्राप्त करें
```java
// तालिका नोड्स की एक सूची प्राप्त करें
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## चरण 4: तालिकाओं और पंक्तियों के माध्यम से पुनरावृति करें
```java
// पंक्ति संख्या निर्धारित करें
int rowCount = 0;
for (Table table : nodes) {
    // तालिका पंक्तियों के माध्यम से पुनरावृति करें
    for (TableRow row : table) {
        rowCount++;
        // पाठ पुनः प्राप्त करें
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // आउटपुट स्क्रीन पर टेक्स्ट प्रिंट करें
        System.out.println(text);
    }
}
```
अपने OneNote दस्तावेज़ में प्रत्येक तालिका के लिए इन चरणों को दोहराएँ, और आप पंक्ति पाठ को सफलतापूर्वक निकाल लेंगे।
## निष्कर्ष
बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में तालिकाओं से पंक्ति पाठ निकालना सीख लिया है। यह ट्यूटोरियल आपके जावा अनुप्रयोगों में Aspose.Note की शक्तिशाली क्षमताओं का लाभ उठाने के लिए एक आधार प्रदान करता है।
## अक्सर पूछे जाने वाले प्रश्नों
### क्या Aspose.Note Microsoft OneNote के नवीनतम संस्करण के साथ संगत है?
 Aspose.Note नवीनतम सहित विभिन्न OneNote संस्करणों का समर्थन करता है। को देखें[प्रलेखन](https://reference.aspose.com/note/java/) अनुकूलता विवरण के लिए.
### क्या मैं खरीदने से पहले जावा के लिए Aspose.Note आज़मा सकता हूँ?
हां, आप यहां Aspose.Note का निःशुल्क परीक्षण देख सकते हैं[इस लिंक](https://releases.aspose.com/).
### मुझे अतिरिक्त सहायता और सहायता कहां मिल सकती है?
 दौरा करना[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) सामुदायिक समर्थन और चर्चा के लिए।
### मैं Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
 से अस्थायी लाइसेंस प्राप्त करें[इस लिंक](https://purchase.aspose.com/temporary-license/).
### क्या Java के लिए Aspose.Note का उपयोग करने के लिए कोई विशिष्ट सिस्टम आवश्यकताएँ हैं?
विस्तृत सिस्टम आवश्यकताओं के लिए दस्तावेज़ देखें।
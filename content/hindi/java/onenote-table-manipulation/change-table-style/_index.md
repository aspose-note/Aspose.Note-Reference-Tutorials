---
title: OneNote में तालिका शैली बदलें - Aspose.Note
linktitle: OneNote में तालिका शैली बदलें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note के साथ अपनी OneNote तालिकाओं को सहजता से बढ़ाएं। तालिका शैलियाँ बदलने के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें। अभी लाइब्रेरी डाउनलोड करें!
type: docs
weight: 10
url: /hi/java/onenote-table-manipulation/change-table-style/
---
## परिचय
Java के लिए Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को OneNote फ़ाइलों में आसानी से हेरफेर करने की अनुमति देती है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में तालिका शैली को बदलने पर ध्यान केंद्रित करेंगे। अपनी तालिकाओं की दृश्य अपील बढ़ाने के लिए चरण-दर-चरण मार्गदर्शिका का पालन करें।
## आवश्यक शर्तें
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित स्थान हैं:
- जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।
-  जावा लाइब्रेरी के लिए Aspose.Note: जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[डाउनलोड पेज](https://releases.aspose.com/note/java/).
- दस्तावेज़ निर्देशिका: अपने OneNote दस्तावेज़ों को संग्रहीत करने के लिए एक निर्देशिका तैयार करें।
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में, Aspose.Note के साथ काम करने के लिए आवश्यक पैकेज आयात करें:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## चरण 1: दस्तावेज़ सेट करें
OneNote दस्तावेज़ को Aspose.Note में लोड करें और तालिका नोड्स की सूची पुनः प्राप्त करें
```java
// दस्तावेज़ सेट करें और तालिका नोड्स की सूची प्राप्त करें
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## चरण 2: पंक्ति शैलियाँ सेट करें
हेडर के बाद पहली पंक्ति को हाइलाइट करने सहित, प्रत्येक पंक्ति के लिए शैली सेट करते हुए, प्रत्येक तालिका में पुनरावृत्ति करें।

```java
// दस्तावेज़ में प्रत्येक तालिका के लिए पंक्ति शैलियाँ सेट करें
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // सिर के बाद पहली पंक्ति को हाइलाइट करें।
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## setRowStyle विधि
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```
## चरण 3: दस्तावेज़ सहेजें
संशोधित दस्तावेज़ को नई तालिका शैलियों के साथ सहेजें।
इन चरणों का पालन करके, आप Java के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में तालिका शैली को आसानी से बदल सकते हैं।

```java
// संशोधित दस्तावेज़ सहेजें
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## निष्कर्ष
Java के लिए Aspose.Note OneNote फ़ाइलों में हेरफेर करने की प्रक्रिया को सरल बनाता है। लाइब्रेरी की क्षमताओं का लाभ उठाकर, आप अपनी तालिकाओं की दृश्य प्रस्तुति को आसानी से बढ़ा सकते हैं।

## पूछे जाने वाले प्रश्न
### मैं जावा के लिए Aspose.Note के लिए दस्तावेज़ कहाँ पा सकता हूँ?
 दौरा करना[प्रलेखन](https://reference.aspose.com/note/java/) व्यापक मार्गदर्शन के लिए.
### मैं जावा के लिए Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 इसका पीछा करो[जोड़ना](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस प्राप्त करने के लिए.
### क्या Java के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?
 हां, आप यहां से नि:शुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).
### जावा के लिए Aspose.Note के लिए मुझे समर्थन कहाँ से मिल सकता है?
 शामिल होना[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) समुदाय से सहायता लेने के लिए.
### मैं जावा के लिए Aspose.Note कैसे खरीदूं?
 आप लाइब्रेरी खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
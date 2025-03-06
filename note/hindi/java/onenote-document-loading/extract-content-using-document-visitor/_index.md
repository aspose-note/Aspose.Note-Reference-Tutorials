---
title: दस्तावेज़ विज़िटर - जावा का उपयोग करके OneNote सामग्री निकालें
linktitle: दस्तावेज़ विज़िटर - जावा का उपयोग करके OneNote सामग्री निकालें
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके जावा में OneNote दस्तावेज़ों से सामग्री निकालने का तरीका जानें। कोड उदाहरणों के साथ चरण-दर-चरण ट्यूटोरियल प्रदान किया गया।
weight: 21
url: /hi/java/onenote-document-loading/extract-content-using-document-visitor/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# दस्तावेज़ विज़िटर - जावा का उपयोग करके OneNote सामग्री निकालें

## परिचय

Java के लिए Aspose.Note OneNote दस्तावेज़ों से सामग्री निकालने के लिए शक्तिशाली सुविधाएँ प्रदान करता है। इस ट्यूटोरियल में, हम जावा में दस्तावेज़ विज़िटर का उपयोग करके OneNote दस्तावेज़ से सामग्री निकालने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
3. सामग्री निकालने के लिए एक OneNote दस्तावेज़ (एक्सटेंशन .one के साथ)।

## पैकेज आयात करें

सबसे पहले, आपको Java के लिए Aspose.Note के साथ काम करने के लिए आवश्यक पैकेज आयात करने होंगे।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## चरण 1: दस्तावेज़ विज़िटर क्लास सेट करें

एक क्लास बनाएं जो इसका विस्तार करे`DocumentVisitor` जावा के लिए Aspose.Note द्वारा प्रदान की गई कक्षा। यह वर्ग दस्तावेज़ के विभिन्न नोड्स पर जाकर काम करेगा।

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // अन्य तरीकों को यहां लागू किया जाएगा
}
```

## चरण 2: विज़िटर विधियाँ लागू करें

विभिन्न प्रकार के नोड्स के लिए विज़िटर विधियों को लागू करें जिन्हें आप दस्तावेज़ में संसाधित करना चाहते हैं। इस उदाहरण में, हम रिचटेक्स्ट, दस्तावेज़, पेज, शीर्षक, छवि, आउटलाइनग्रुप, आउटलाइन और आउटलाइनएलिमेंट नोड्स के लिए तरीकों को लागू करेंगे।

```java
// विभिन्न प्रकार के नोड्स के लिए विज़िटर विधियाँ

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

## चरण 3: मुख्य विधि

मुख्य विधि में, OneNote दस्तावेज़ को लोड करें, अपने कस्टम दस्तावेज़ विज़िटर वर्ग का एक उदाहरण बनाएं, और विज़िटर को विज़िट प्रक्रिया शुरू करने के लिए स्वीकार करें।

```java
public static void main(String[] args) throws IOException {
    // वह दस्तावेज़ खोलें जिसे हम कनवर्ट करना चाहते हैं।
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // एक ऑब्जेक्ट बनाएं जो DocumentVisitor वर्ग से प्राप्त हो।
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // विजिटिंग प्रक्रिया शुरू करने के लिए विजिटर को स्वीकार करें।
    doc.accept(myConverter);
    
    // ऑपरेशन का परिणाम प्राप्त करें.
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## निष्कर्ष

इस ट्यूटोरियल में, आपने सीखा कि Java के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ से सामग्री कैसे निकाली जाए। एक कस्टम दस्तावेज़ विज़िटर वर्ग को लागू करके और दस्तावेज़ के विभिन्न नोड्स पर जाकर, आप अपनी आवश्यकताओं के अनुसार सामग्री को प्रभावी ढंग से निकाल और संसाधित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं OneNote दस्तावेज़ से विशिष्ट प्रकार की सामग्री निकाल सकता हूँ?

A1: हाँ, विभिन्न नोड प्रकारों के लिए विशिष्ट विज़िटर विधियों को कार्यान्वित करके, आप पाठ, चित्र, शीर्षक इत्यादि जैसी सामग्री को चुनिंदा रूप से निकाल सकते हैं।

### Q2: क्या जावा के लिए Aspose.Note OneNote दस्तावेज़ों के विभिन्न संस्करणों के साथ संगत है?

A2: Java के लिए Aspose.Note OneNote दस्तावेज़ों के विभिन्न संस्करणों का समर्थन करता है, जो सामग्री की अनुकूलता और सुचारू निष्कर्षण सुनिश्चित करता है।

### Q3: क्या मैं इस निष्कर्षण प्रक्रिया को अपने जावा एप्लिकेशन में एकीकृत कर सकता हूं?

उ3: बिल्कुल, आप दिए गए ट्यूटोरियल का पालन करके सामग्री निष्कर्षण प्रक्रिया को अपने जावा अनुप्रयोगों में आसानी से एकीकृत कर सकते हैं।

### Q4: क्या Java के लिए Aspose.Note जटिल OneNote दस्तावेज़ों को संभालने के लिए सहायता प्रदान करता है?

A4: हाँ, Java के लिए Aspose.Note OneNote दस्तावेज़ों के भीतर जटिल संरचनाओं और सामग्री को संभालने के लिए व्यापक समर्थन प्रदान करता है।

### Q5: क्या OneNote दस्तावेज़ के आकार की कोई सीमा है जिसे Java के लिए Aspose.Note का उपयोग करके संसाधित किया जा सकता है?

A5: Java के लिए Aspose.Note को विभिन्न आकारों के OneNote दस्तावेज़ों को कुशलतापूर्वक संभालने के लिए डिज़ाइन किया गया है, जो बड़े दस्तावेज़ों के साथ भी इष्टतम प्रदर्शन सुनिश्चित करता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

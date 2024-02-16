---
title: Aspose.Note में टैग के साथ प्रोजेक्ट खोलें और बंद करें
linktitle: Aspose.Note में टैग के साथ प्रोजेक्ट खोलें और बंद करें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके प्रोग्रामेटिक रूप से Microsoft OneNote फ़ाइलों में हेरफेर करना सीखें। टैग के साथ कुशलतापूर्वक प्रोजेक्ट खोलें और बंद करें।
type: docs
weight: 15
url: /hi/net/tag-management/open-close-projects-tags/
---
## परिचय

इस ट्यूटोरियल में, हम सीखेंगे कि टैग के साथ प्रोजेक्ट खोलने और बंद करने के लिए .NET के लिए Aspose.Note का उपयोग कैसे करें। Aspose.Note एक शक्तिशाली एपीआई है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देता है, जिससे दस्तावेज़ों के भीतर टेक्स्ट, छवियों और टैग में हेरफेर करने जैसे कार्यों को सक्षम किया जा सकता है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपने निम्नलिखित पूर्वापेक्षाएँ स्थापित कर ली हैं:

## नामस्थान आयात करें

```csharp
using System.IO;
using System.Linq;
```

आइए अब प्रत्येक उदाहरण को कई चरणों में तोड़ें:

## चरण 1: दस्तावेज़ लोड करें

सबसे पहले, हमें दस्तावेज़ को Aspose.Note में लोड करना होगा।

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## चरण 2: प्रोजेक्ट सी आइटम बंद करें

अब, 'प्रोजेक्ट सी' से संबंधित सभी चेकबॉक्स आइटम बंद करें।

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## चरण 3: बंद प्रोजेक्ट सी नोट्स सहेजें

संशोधित दस्तावेज़ को बंद 'प्रोजेक्ट सी' आइटम के साथ सहेजें।

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## चरण 4: प्रोजेक्ट सी आइटम खोलें

इसके बाद, 'प्रोजेक्ट सी' से संबंधित सभी चेकबॉक्स आइटम खोलें।

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## चरण 5: ओपन प्रोजेक्ट सी नोट्स सहेजें

संशोधित दस्तावेज़ को खुले हुए 'प्रोजेक्ट सी' आइटम के साथ सहेजें।

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

अब आपने सीख लिया है कि .NET का उपयोग करके Aspose.Note में टैग के साथ प्रोजेक्ट कैसे खोलें और बंद करें।

## निष्कर्ष

.NET के लिए Aspose.Note OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से हेरफेर करने का एक सुविधाजनक तरीका प्रदान करता है। इस ट्यूटोरियल का अनुसरण करके, आप टैग का उपयोग करके आइटम खोलकर और बंद करके अपनी परियोजनाओं को कुशलतापूर्वक प्रबंधित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A1: Aspose.Note Microsoft OneNote 2010 और नए संस्करणों का समर्थन करता है।

### Q2: क्या मैं व्यावसायिक परियोजनाओं के लिए Aspose.Note का उपयोग कर सकता हूँ?

 उ2: हां, आप व्यक्तिगत और व्यावसायिक दोनों परियोजनाओं के लिए Aspose.Note का उपयोग कर सकते हैं। मिलने जाना[यहाँ](https://purchase.aspose.com/buy) लाइसेंस खरीदने के लिए.

### Q3: क्या Aspose.Note निःशुल्क परीक्षण की पेशकश करता है?

 उ3: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मुझे Aspose.Note के लिए दस्तावेज़ कहां मिल सकते हैं?

 A4: आप दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/note/net/).

### Q5: मुझे Aspose.Note के लिए समर्थन कहाँ से मिल सकता है?

 A5: समर्थन के लिए, आप Aspose.Note पर जा सकते हैं[मंच](https://forum.aspose.com/c/note/28).
---
title: Aspose.Note टेक्स्ट में हाल के सभी परिवर्तनों को हाइलाइट करें
linktitle: Aspose.Note टेक्स्ट में हाल के सभी परिवर्तनों को हाइलाइट करें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note के साथ अपने नोट दस्तावेज़ों को बेहतर बनाएं! इस चरण-दर-चरण ट्यूटोरियल के साथ सीखें कि टेक्स्ट में हाल के परिवर्तनों को कैसे उजागर करें।
weight: 19
url: /hi/net/text-manipulation/highlight-recent-changes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note टेक्स्ट में हाल के सभी परिवर्तनों को हाइलाइट करें

## परिचय
क्या आप .NET का उपयोग करके अपने नोट दस्तावेज़ों में गतिशील और दृश्य रूप से आकर्षक सुविधाएँ जोड़ना चाह रहे हैं? .NET के लिए Aspose.Note एक शक्तिशाली समाधान है जो आपको अपनी नोट फ़ाइलों में निर्बाध रूप से हेरफेर करने और बढ़ाने की अनुमति देता है। इस ट्यूटोरियल में, हम एक विशिष्ट पहलू पर गौर करेंगे: Aspose.Note टेक्स्ट में हाल के सभी परिवर्तनों पर प्रकाश डालना।
## आवश्यक शर्तें
इससे पहले कि हम इस यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
-  .NET के लिए Aspose.Note: सुनिश्चित करें कि आपके पास Aspose.Note लाइब्रेरी स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[.NET दस्तावेज़ीकरण के लिए Aspose.Note](https://reference.aspose.com/note/net/).
- विकास परिवेश: विज़ुअल स्टूडियो जैसी आईडीई सहित एक .NET विकास परिवेश स्थापित करें।
- नमूना दस्तावेज़: एक नोट दस्तावेज़ तैयार करें (इस मामले में, "Aspose.one") जिसमें वह टेक्स्ट हो जिसे आप हाइलाइट करना चाहते हैं।
## नामस्थान आयात करें
आरंभ करने के लिए, अपने .NET प्रोजेक्ट में आवश्यक नामस्थान आयात करें:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## चरण 1: दस्तावेज़ लोड करें
नोट दस्तावेज़ को Aspose.Note में लोड करके प्रारंभ करें:
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## चरण 2: हाल के परिवर्तनों को पहचानें
इसके बाद, पिछले सप्ताह के भीतर संशोधित रिचटेक्स्ट नोड्स की पहचान करें:
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## चरण 3: हाइलाइट रंग सेट करें
अब, पहचाने गए नोड्स और टेक्स्ट रन के लिए हाइलाइट रंग सेट करें:
```csharp
foreach (var node in richTextNodes)
{
    // पैराग्राफ़ के लिए हाइलाइट रंग सेट करें
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    // प्रत्येक टेक्स्ट रन के लिए हाइलाइट रंग सेट करें
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## चरण 4: संशोधित दस्तावेज़ सहेजें
हाइलाइट किए गए हालिया परिवर्तनों के साथ दस्तावेज़ को सहेजें:
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## चरण 5: सफलता संदेश प्रदर्शित करें
अंत में, उपयोगकर्ता को सूचित करने के लिए एक सफलता संदेश प्रदर्शित करें:
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## निष्कर्ष
इस ट्यूटोरियल में, हमने पता लगाया कि नोट दस्तावेज़ के भीतर पाठ में सभी हालिया परिवर्तनों को उजागर करने के लिए .NET के लिए Aspose.Note का उपयोग कैसे करें। यह सुविधा दस्तावेज़ दृश्यता को बढ़ाती है और नोट फ़ाइलों के साथ काम करने के लिए आपके टूलकिट में एक मूल्यवान अतिरिक्त है।
## पूछे जाने वाले प्रश्न
### क्या मैं विभिन्न समयावधियों के लिए अलग-अलग हाइलाइट रंग लागू कर सकता हूँ?
हां, आप अपनी विशिष्ट आवश्यकताओं के आधार पर अलग-अलग हाइलाइट रंग सेट करने के लिए कोड को कस्टमाइज़ कर सकते हैं।
### क्या Aspose.Note नवीनतम .NET फ्रेमवर्क के साथ संगत है?
नवीनतम .NET फ्रेमवर्क के साथ अनुकूलता सुनिश्चित करने के लिए Aspose.Note नियमित रूप से अपनी लाइब्रेरी को अपडेट करता है।
### इस सुविधा को लागू करते समय मैं त्रुटियों से कैसे निपट सकता हूँ?
आप अपवादों को संभालने और एक सहज उपयोगकर्ता अनुभव प्रदान करने के लिए ट्राई-कैच ब्लॉक को शामिल कर सकते हैं।
### क्या Aspose.Note अन्य टेक्स्ट फ़ॉर्मेटिंग सुविधाओं का समर्थन करता है?
बिल्कुल! Aspose.Note टेक्स्ट फ़ॉर्मेटिंग के लिए सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है, जिसमें फ़ॉन्ट शैलियाँ, आकार और बहुत कुछ शामिल हैं।
### क्या मैं इस समाधान को वेब एप्लिकेशन में एकीकृत कर सकता हूँ?
हाँ, आप दस्तावेज़ प्रसंस्करण क्षमताओं को बढ़ाने के लिए .NET के लिए Aspose.Note को वेब अनुप्रयोगों में एकीकृत कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

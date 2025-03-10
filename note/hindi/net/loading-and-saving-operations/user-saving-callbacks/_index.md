---
title: Aspose.Note में उपयोगकर्ता-सेविंग कॉलबैक
linktitle: Aspose.Note में उपयोगकर्ता-सेविंग कॉलबैक
second_title: Aspose.Note .NET API
description: फ़ॉन्ट, सीएसएस और छवियों को सहेजने को अनुकूलित करने के लिए .NET के लिए Aspose.Note में उपयोगकर्ता-बचत कॉलबैक को कार्यान्वित करने का तरीका जानें।
weight: 31
url: /hi/net/loading-and-saving-operations/user-saving-callbacks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note में उपयोगकर्ता-सेविंग कॉलबैक

## परिचय

इस ट्यूटोरियल में, हम यह पता लगाएंगे कि .NET के लिए Aspose.Note में उपयोगकर्ता-बचत कॉलबैक कैसे लागू करें। ये कॉलबैक आपको विभिन्न चरणों में हस्तक्षेप करने के लिए हुक प्रदान करके बचत प्रक्रिया को अनुकूलित करने की अनुमति देते हैं, जैसे कि फ़ॉन्ट, सीएसएस स्टाइलशीट और छवियों को सहेजना। इन कॉलबैक का उपयोग करके, आप अपनी विशिष्ट आवश्यकताओं के अनुरूप बचत व्यवहार को तैयार कर सकते हैं, आउटपुट पर लचीलेपन और नियंत्रण को बढ़ा सकते हैं।

## आवश्यक शर्तें

Aspose.Note में उपयोगकर्ता-बचत कॉलबैक के कार्यान्वयन में उतरने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

1.  .NET SDK के लिए Aspose.Note: .NET SDK के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें।[डाउनलोड पेज](https://releases.aspose.com/note/net/).
   
2. विकास परिवेश: एक उपयुक्त विकास परिवेश स्थापित करें, जैसे विज़ुअल स्टूडियो या कोई अन्य .NET विकास परिवेश।

## नामस्थान आयात करें

आरंभ करने के लिए, Aspose.Note लाइब्रेरी से आवश्यक कक्षाओं और विधियों तक पहुँचने के लिए अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करना सुनिश्चित करें:

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

अब, आइए उपयोगकर्ता-बचत कॉलबैक के कार्यान्वयन को कई चरणों में विभाजित करें:

## चरण 1: कॉलबैक गुणों को परिभाषित करें

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

यहां, हम रूट फ़ोल्डर, सीएसएस फ़ोल्डर, फ़ॉन्ट फ़ोल्डर, छवि फ़ोल्डर और अन्य प्रासंगिक सेटिंग्स निर्दिष्ट करने के लिए विभिन्न गुणों को परिभाषित करते हैं।

## चरण 2: फ़ॉन्ट सेविंग कॉलबैक लागू करें

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 इस चरण में, हम इसे लागू करते हैं`FontSaving` फ़ॉन्ट की बचत को संभालने के लिए कॉलबैक विधि। यह निर्दिष्ट फ़ॉन्ट फ़ोल्डर में एक संसाधन बनाता है और तदनुसार स्ट्रीम और यूआरआई निर्दिष्ट करता है।

## चरण 3: सीएसएस सेविंग कॉलबैक लागू करें

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 यहां, हम परिभाषित करते हैं`CssSaving` सीएसएस स्टाइलशीट की बचत को प्रबंधित करने के लिए कॉलबैक विधि। यह निर्दिष्ट सीएसएस फ़ोल्डर में एक संसाधन बनाता है और तदनुसार स्ट्रीम, यूआरआई और अन्य गुणों को सेट करता है।

## चरण 4: इमेज सेविंग कॉलबैक लागू करें

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 अंत में, हम इसे लागू करते हैं`ImageSaving` छवियों की बचत को संभालने के लिए कॉलबैक विधि। पिछले चरणों के समान, यह निर्दिष्ट छवि फ़ोल्डर में एक संसाधन बनाता है और स्ट्रीम और यूआरआई निर्दिष्ट करता है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा है कि .NET के लिए Aspose.Note में उपयोगकर्ता-बचत कॉलबैक कैसे लागू करें। दिए गए चरणों का पालन करके, आप फ़ॉन्ट, सीएसएस स्टाइलशीट और छवियों के लिए बचत प्रक्रिया को अनुकूलित कर सकते हैं, जिससे आउटपुट पर अधिक लचीलेपन और नियंत्रण की अनुमति मिलती है।

## पूछे जाने वाले प्रश्न

### Q1: क्या मैं बचत प्रक्रिया के अन्य पहलुओं को अनुकूलित करने के लिए इन कॉलबैक का उपयोग कर सकता हूँ?

A1: हाँ, आप अपनी आवश्यकताओं के अनुसार बचत प्रक्रिया के विभिन्न पहलुओं को अनुकूलित करने के लिए इन कॉलबैक को बढ़ा सकते हैं या अतिरिक्त लागू कर सकते हैं।

### Q2: क्या .NET के लिए Aspose.Note अन्य .NET फ्रेमवर्क के साथ संगत है?

A2: हां, .NET के लिए Aspose.Note .NET कोर और .NET मानक सहित विभिन्न .NET फ्रेमवर्क के साथ संगत है।

### Q3: मैं बचत प्रक्रिया के दौरान त्रुटियों या अपवादों को कैसे संभाल सकता हूँ?

A3: आप होने वाली किसी भी त्रुटि या अपवाद को शालीनता से संभालने के लिए प्रत्येक कॉलबैक विधि के भीतर त्रुटि प्रबंधन तंत्र को शामिल कर सकते हैं।

### Q4: क्या इन कॉलबैक का उपयोग करते समय कोई प्रदर्शन संबंधी विचार हैं?

उ4: हालांकि ये कॉलबैक लचीलापन प्रदान करते हैं, सुनिश्चित करें कि इन्हें किसी भी प्रदर्शन ओवरहेड से बचने के लिए कुशलतापूर्वक लागू किया जाता है, खासकर बड़े दस्तावेज़ों या संसाधनों से निपटते समय।

### Q5: क्या मैं उपयोगकर्ता इनपुट या अन्य स्थितियों के आधार पर बचत व्यवहार को गतिशील रूप से बदल सकता हूँ?

A5: हाँ, आप विभिन्न कारकों के आधार पर बचत व्यवहार को गतिशील रूप से समायोजित करने के लिए कॉलबैक विधियों के भीतर सशर्त तर्क को शामिल कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

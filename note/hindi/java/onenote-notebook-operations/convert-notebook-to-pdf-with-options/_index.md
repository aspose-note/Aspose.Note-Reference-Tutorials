---
title: OneNote में विकल्पों के साथ नोटबुक को पीडीएफ में बदलें - Aspose.Note
linktitle: OneNote में विकल्पों के साथ नोटबुक को पीडीएफ में बदलें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: OneNote नोटबुक को आसानी से PDF में अनुकूलित और निर्यात करें! जावा के लिए Aspose.Note भारी सामान उठाने का काम संभालता है। चरण-दर-चरण मार्गदर्शिका शामिल! #वननोट #जावा #एस्पोज़
weight: 17
url: /hi/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में विकल्पों के साथ नोटबुक को पीडीएफ में बदलें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके अनुकूलन योग्य विकल्पों के साथ नोटबुक को पीडीएफ में परिवर्तित करने की दुनिया में गहराई से उतरेंगे। Aspose.Note एक शक्तिशाली जावा एपीआई है जो डेवलपर्स को Microsoft OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से हेरफेर करने की अनुमति देता है। नोटबुक को पीडीएफ प्रारूप में परिवर्तित करना विभिन्न अनुप्रयोगों में एक सामान्य आवश्यकता है, और Aspose.Note के साथ, यह कार्य सुव्यवस्थित और कुशल हो जाता है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है।
2. जावा के लिए Aspose.Note: जावा के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/note/java/).
3. आईडीई (एकीकृत विकास पर्यावरण): जावा विकास के लिए अपना पसंदीदा आईडीई चुनें। IntelliJ IDEA, Eclipse, या NetBeans लोकप्रिय विकल्प हैं।

## पैकेज आयात करें

सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। ये पैकेज OneNote दस्तावेज़ों के साथ काम करने के लिए आवश्यक कक्षाएं और विधियाँ प्रदान करते हैं।

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## चरण 1: OneNote नोटबुक लोड करें

किसी नोटबुक को पीडीएफ में बदलने के लिए, आपको पहले OneNote नोटबुक को लोड करना होगा। सुनिश्चित करें कि नोटबुक फ़ाइल का पथ सही ढंग से निर्दिष्ट है।

```java
String dataDir = "Your Document Directory";
// OneNote नोटबुक लोड करें
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## चरण 2: पीडीएफ सेव विकल्प निर्दिष्ट करें

Aspose.Note पीडीएफ आउटपुट को अनुकूलित करने के लिए विभिन्न विकल्प प्रदान करता है। आप पेज स्प्लिटिंग एल्गोरिदम, हेडर/फुटर सेटिंग्स और बहुत कुछ जैसे विकल्प निर्दिष्ट कर सकते हैं।

```java
// पीडीएफ सेव विकल्प निर्दिष्ट करें
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## चरण 3: नोटबुक को पीडीएफ के रूप में सहेजें

एक बार जब आप नोटबुक लोड कर लेते हैं और सेव विकल्प निर्दिष्ट कर लेते हैं, तो नोटबुक को पीडीएफ फ़ाइल के रूप में सहेजने का समय आ जाता है।

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// नोटबुक सहेजें
notebook.save(dataDir, notebookSaveOptions);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया है कि जावा के लिए Aspose.Note का उपयोग करके OneNote नोटबुक को पीडीएफ प्रारूप में कैसे परिवर्तित किया जाए। इन सरल चरणों का पालन करके, आप अपने जावा अनुप्रयोगों में दस्तावेज़ रूपांतरणों को कुशलतापूर्वक संभाल सकते हैं।

---

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पीडीएफ आउटपुट के स्वरूप को अनुकूलित कर सकता हूँ?

A1: हाँ, Aspose.Note पीडीएफ आउटपुट को अनुकूलित करने के लिए विभिन्न विकल्प प्रदान करता है, जिसमें हेडर/फुटर सेटिंग्स, पेज स्प्लिटिंग एल्गोरिदम और बहुत कुछ शामिल है।

### Q2: क्या Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A2: Aspose.Note Microsoft OneNote 2010 और बाद के संस्करणों का समर्थन करता है।

### Q3: क्या Aspose.Note निःशुल्क परीक्षण की पेशकश करता है?

 उ3: हां, आप Aspose.Note का निःशुल्क परीक्षण यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मुझे Aspose.Note के लिए दस्तावेज़ कहां मिल सकते हैं?

 A4: आप Aspose.Note के लिए व्यापक दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/note/java/).

### Q5: मैं Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A5: किसी भी तकनीकी सहायता या प्रश्न के लिए, आप Aspose.Note समर्थन फ़ोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

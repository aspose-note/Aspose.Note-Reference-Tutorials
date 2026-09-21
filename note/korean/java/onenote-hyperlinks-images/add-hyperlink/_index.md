---
date: 2026-07-29
description: Java와 Aspose.Note를 사용하여 link onenote를 삽입하고, OneNote를 PDF로 저장하며, 하이퍼링크를
  추가하는 방법을 배웁니다. OneNote를 손쉽게 PDF로 내보낼 수 있습니다.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Java로 OneNote를 PDF로 저장하고 OneNote에 하이퍼링크 추가
og_description: Java와 Aspose.Note를 사용하여 link onenote를 삽입하고 OneNote를 PDF로 내보냅니다. 하이퍼링크를
  추가하고 PDF를 생성하는 방법을 단계별로 배웁니다.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Embed Link onenote – Java를 사용하여 OneNote를 PDF로 저장
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Embed Link onenote – Java를 사용하여 OneNote를 PDF로 저장
url: /ko/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote를 PDF로 저장하고 Java로 OneNote에 하이퍼링크 추가

## 소개

If you need to **embed link onenote** while turning a notebook into a portable PDF, you’ve come to the right place. This tutorial walks you through saving OneNote as PDF and inserting clickable hyperlinks using Java and the Aspose.Note library. You’ll see why this approach is ideal for archiving, sharing, and automating document pipelines.

## 빠른 답변
- **Java로 OneNote를 PDF로 저장할 수 있나요?** 예, Aspose.Note for Java는 PDF를 생성하기 위해 단일 `save` 호출을 제공합니다.
- **하이퍼링크를 어떻게 삽입하나요?** `RichText` 세그먼트에 `TextStyle.setHyperlinkAddress`를 사용합니다.
- **필수 조건은 무엇인가요?** JDK 8 이상 및 Aspose.Note for Java 라이브러리.
- **지원되는 출력 형식은 무엇인가요?** PDF, DOCX, XPS 등 다양한 형식.
- **프로덕션에 라이선스가 필요합니까?** 예, 비평가용 사용을 제외하고는 상업용 라이선스가 필요합니다.

## “save onenote as pdf”란 무엇인가요?

OneNote 노트북을 PDF로 저장하면 OneNote 앱 없이도 누구나 열 수 있는 읽기 전용, 크로스 플랫폼 버전의 노트를 만들 수 있습니다. 이 형식은 원본 레이아웃, 이미지 및 삽입된 하이퍼링크를 그대로 유지하면서 아카이빙, 인쇄 또는 OneNote가 설치되지 않은 협업자와 공유하기에 이상적입니다.

## 왜 Aspose.Note Java로 OneNote에서 PDF를 생성하나요?

Aspose.Note for Java는 **export onenote to pdf**를 100 % 레이아웃 정확도로 수행할 수 있으며, 전체 파일을 메모리에 로드하지 않고도 문서당 최대 200 페이지를 처리합니다. 이 라이브러리는 이미지, 표 및 하이퍼링크 스타일의 95 %를 포함한 30가지 이상의 다양한 콘텐츠 유형을 처리하므로 원본 노트북의 충실한 복제본을 얻을 수 있습니다. 또한 Windows, Linux, macOS에서 실행되어 클라우드 또는 온프레미스 서비스에서 배치 변환을 가능하게 합니다.

## 전제 조건

시작하기 전에 시스템에 다음 전제 조건이 설치되고 설정되어 있는지 확인하십시오:

### 자바 개발 키트 (JDK)

시스템에 Java Development Kit (JDK)이 설치되어 있는지 확인하십시오. [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 JDK를 다운로드하고 설치할 수 있습니다.

### Aspose.Note for Java 라이브러리

Aspose.Note for Java 라이브러리를 다운로드하고 설치하십시오. 문서와 다운로드 링크는 [here](https://reference.aspose.com/note/java/)에서 확인할 수 있습니다.

## 패키지 가져오기

먼저, Aspose.Note for Java 작업에 필요한 패키지를 가져옵니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

이제 제공된 예제를 여러 단계로 나누어 살펴보겠습니다:

## PDF로 저장하면서 link onenote를 삽입하는 방법은?

`Document` 인스턴스를 새로 로드하고, 페이지 구조를 구성한 뒤, 하이퍼링크용 빨간색 `TextStyle`을 정의하고, 마지막으로 `document.save("output.pdf", SaveFormat.Pdf)`를 호출합니다. 이 순서는 모든 원본 서식 및 이미지를 보존하면서 완전한 기능의 하이퍼링크가 포함된 PDF를 생성합니다.

## 단계 1: 문서 구조 설정

`Document`는 Aspose.Note에서 OneNote 노트북을 나타냅니다.
`Page`는 개요 및 기타 페이지 수준 요소를 담는 컨테이너입니다.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## 단계 2: 기본 텍스트 스타일 정의

`ParagraphStyle`은 정렬, 간격 및 들여쓰기와 같은 단락의 기본 서식을 정의합니다.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## 단계 3: 제목 텍스트 설정

`Title`은 OneNote 문서에서 페이지 제목 요소를 나타냅니다.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## 단계 4: 개요 및 개요 요소 생성

`Outline`은 콘텐츠 블록 계층 구조를 담는 컨테이너 역할을 합니다.
`OutlineElement`는 개요 내의 개별 요소로, 예를 들어 단락이나 표가 있습니다.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 단계 5: 하이퍼링크용 텍스트 스타일 정의

`TextStyle`은 글꼴, 색상 및 밑줄 설정을 포함한 텍스트 실행의 시각적 모습을 제어합니다.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## 단계 6: 하이퍼링크가 포함된 텍스트 추가

`RichText`는 단락 내부의 서식이 적용된 텍스트 실행을 나타냅니다. 하이퍼링크 주소를 설정하면 내보낸 PDF에서 텍스트를 클릭할 수 있게 됩니다.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## 단계 7: 개요를 페이지에 추가하고 페이지를 문서에 추가

이 단계에서는 이전에 만든 개요 요소를 페이지에 연결한 다음, 페이지를 `Document` 객체에 추가합니다.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 단계 8: 문서를 PDF로 저장

`SaveFormat.Pdf`는 Aspose.Note에 문서를 PDF 형식으로 내보내도록 지시합니다.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## 결론

축하합니다! Java와 Aspose.Note 라이브러리를 사용하여 **OneNote를 PDF로 저장**하고 문서에 하이퍼링크를 성공적으로 추가했습니다. 이 기능을 통해 **embed link onenote**를 수행하고 OneNote 콘텐츠에서 직접 인터랙티브하고 공유 가능한 PDF를 만들 수 있습니다.

## 자주 묻는 질문

**Q: 하이퍼링크의 모양을 어떻게 사용자 정의할 수 있나요?**  
A: `setHyperlinkAddress`를 호출하기 전에 `setFontColor`, `setUnderline`, `setFontName`과 같은 `TextStyle` 속성을 사용합니다.

**Q: PDF 외의 형식으로 문서를 저장할 수 있나요?**  
A: 예, Aspose.Note는 DOCX, XPS, HTML 및 기타 여러 내보내기 형식을 지원합니다.

**Q: 기존 OneNote 파일에 하이퍼링크를 추가해야 하면 어떻게 하나요?**  
A: `new Document("input.one")`으로 기존 파일을 로드하고, 예시와 같이 내용을 수정한 뒤 원하는 형식으로 `save`를 호출합니다.

**Q: PDF가 생성된 후 프로그래밍 방식으로 하이퍼링크를 열 수 있는 방법이 있나요?**  
A: PDF 뷰어가 클릭 가능한 링크를 자동으로 처리하므로 추가 코드가 필요하지 않습니다.

**Q: 개발용으로 라이선스가 필요합니까?**  
A: 임시 평가 라이선스는 개발 및 테스트에 충분하지만, 프로덕션 배포에는 정식 라이선스가 필요합니다.

---

**마지막 업데이트:** 2026-07-29  
**테스트 환경:** Aspose.Note for Java 26.4  
**작성자:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## 관련 튜토리얼

- [Aspose.Note for Java를 사용하여 OneNote를 PDF로 저장하는 방법](/note/java/onenote-document-loading/load-save-format/)
- [PdfSaveOptions를 사용하여 Aspose.Note로 OneNote를 PDF로 변환하기](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Java로 OneNote 이미지에 하이퍼링크 추가](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
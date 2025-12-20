---
date: 2025-12-20
description: Java와 Aspose.Note 라이브러리를 사용하여 OneNote를 PDF로 저장하고 OneNote에 하이퍼링크를 추가하는
  방법을 배워보세요. OneNote에서 PDF를 손쉽게 생성합니다.
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: Java를 사용하여 OneNote를 PDF로 저장하고 OneNote에 하이퍼링크 추가
url: /ko/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java로 OneNote를 PDF로 저장하고 하이퍼링크 추가하기

## 소개

OneNote 문서에 하이퍼링크를 추가하면서 동시에 PDF로 저장하면 노트의 인터랙티브성이 크게 향상되고 공유가 쉬워집니다. 이 튜토리얼에서는 **OneNote를 PDF로 저장하는 방법**과 Java 및 Aspose.Note 라이브러리를 사용해 클릭 가능한 링크를 삽입하는 방법을 배웁니다. 함께 단계별로 진행해 보세요!

## 빠른 답변
- **Java로 OneNote를 PDF로 저장할 수 있나요?** 예, Aspose.Note for Java는 PDF를 생성하기 위한 단일 `save` 호출을 제공합니다.
- **하이퍼링크는 어떻게 삽입하나요?** `RichText` 세그먼트에 `TextStyle.setHyperlinkAddress`를 사용합니다.
- **필수 사전 조건은 무엇인가요?** JDK 8 이상 및 Aspose.Note for Java 라이브러리.
- **지원되는 출력 형식은 무엇인가요?** PDF, DOCX, XPS 등 다양한 형식.
- **프로덕션에서 라이선스가 필요한가요?** 예, 평가용이 아닌 경우 상업용 라이선스가 필요합니다.

## “save onenote as pdf”란?

OneNote 노트북을 PDF로 저장하면 OneNote 앱 없이도 모든 장치에서 열 수 있는 휴대용 읽기 전용 버전이 만들어집니다. 이는 아카이브, 인쇄 또는 OneNote를 사용하지 않는 사용자와 공유할 때 특히 유용합니다.

## 왜 Aspose.Note Java로 OneNote에서 PDF를 생성하나요?

- **전체 충실도:** 서식, 이미지 및 하이퍼링크를 그대로 유지합니다.
- **프로그래밍 제어:** 백엔드 서비스에서 배치 변환을 자동화할 수 있습니다.
- **크로스‑플랫폼:** Windows, Linux, macOS에서 동작합니다.
- **강력한 API:** 저장하기 전에 콘텐츠를 쉽게 추가하거나 수정할 수 있습니다.

## 사전 요구 사항

시작하기 전에 아래 항목들이 시스템에 설치되고 설정되어 있는지 확인하세요.

### Java Development Kit (JDK)

시스템에 Java Development Kit (JDK)가 설치되어 있는지 확인하십시오. JDK는 [Oracle 웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드하고 설치할 수 있습니다.

### Aspose.Note for Java Library

Aspose.Note for Java 라이브러리를 다운로드하고 설치하십시오. 문서와 다운로드 링크는 [여기](https://reference.aspose.com/note/java/)에서 확인할 수 있습니다.

## 패키지 가져오기

Aspose.Note for Java를 사용하기 위해 필요한 패키지를 가져옵니다.

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

## 단계 1: 문서 구조 설정

새 문서와 콘텐츠가 들어갈 페이지를 먼저 생성합니다.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## 단계 2: 기본 텍스트 스타일 정의

대부분의 텍스트 요소에 적용될 기본 단락 스타일을 정의합니다.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## 단계 3: 제목 텍스트 설정

페이지의 제목을 만들고 기본 스타일을 적용합니다.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## 단계 4: 개요 및 개요 요소 만들기

개요는 단락 및 기타 요소를 담는 컨테이너 역할을 합니다.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 단계 5: 하이퍼링크용 텍스트 스타일 정의

여기서는 클릭 가능한 부분에 사용할 빨간색 스타일을 정의합니다.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## 단계 6: 하이퍼링크가 있는 텍스트 추가

이제 일반 텍스트와 하이퍼링크를 혼합한 `RichText` 객체를 만듭니다.  
`setHyperlinkAddress` 메서드는 Aspose.Note에 해당 세그먼트가 클릭 가능하도록 알려줍니다.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## 단계 7: 개요를 페이지에, 페이지를 문서에 추가

개요 요소를 개요에, 개요를 페이지에, 마지막으로 페이지를 문서에 연결합니다.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 단계 8: 문서를 PDF로 저장

마지막 단계는 OneNote 문서를 PDF 파일로 저장하는 것입니다. 여기서 핵심 키워드 **save onenote as pdf**가 사용됩니다.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## 결론

축하합니다! Java와 Aspose.Note 라이브러리를 사용해 **OneNote를 PDF로 저장**하고 문서에 하이퍼링크를 성공적으로 추가했습니다. 이 기능을 통해 OneNote 콘텐츠에서 직접 인터랙티브하고 공유 가능한 PDF를 만들 수 있습니다.

## FAQ

### Q1: Aspose.Note가 모든 Java 버전과 호환되나요?

A1: 예, Aspose.Note for Java는 JDK 8 이상을 포함한 모든 주요 Java 버전을 지원합니다.

### Q2: Aspose.Note를 사용하여 하나의 문서에 여러 하이퍼링크를 추가할 수 있나요?

A2: 물론입니다! OneNote 문서 내에서 필요에 따라 원하는 만큼 하이퍼링크를 추가할 수 있습니다.

### Q3: Aspose.Note가 다른 프로그래밍 언어도 지원하나요?

A3: 네, Aspose.Note는 .NET, Python, Android 등 다양한 프로그래밍 언어용 라이브러리를 제공합니다.

### Q4: Aspose.Note를 기존 Java 프로젝트에 쉽게 통합할 수 있나요?

A4: 예, Aspose.Note를 Java 프로젝트에 통합하는 과정은 간단하고 문서화가 잘 되어 있어 빠르게 시작할 수 있습니다.

### Q5: Aspose.Note 사용에 대한 추가 도움과 리소스는 어디서 찾을 수 있나요?

A5: 자세한 문서, 튜토리얼 및 커뮤니티 지원은 [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 확인할 수 있습니다.

## 자주 묻는 질문

**Q: 하이퍼링크의 외관을 어떻게 커스터마이즈하나요?**  
A: `setHyperlinkAddress`를 호출하기 전에 `TextStyle`의 `setFontColor`, `setUnderline`, `setFontName` 등 속성을 사용하면 됩니다.

**Q: PDF 외에 다른 형식으로 문서를 저장할 수 있나요?**  
A: 예, Aspose.Note는 DOCX, XPS, HTML 등 여러 다른 내보내기 형식을 지원합니다.

**Q: 기존 OneNote 파일에 하이퍼링크를 추가하려면 어떻게 해야 하나요?**  
A: `new Document("input.one")`으로 기존 파일을 로드하고, 위 예시와 같이 내용을 수정한 뒤 원하는 형식으로 `save`하면 됩니다.

**Q: PDF 생성 후 프로그래밍 방식으로 하이퍼링크를 열 수 있는 방법이 있나요?**  
A: PDF 뷰어가 클릭 가능한 링크를 자동으로 처리하므로 별도의 코드는 필요하지 않습니다.

**Q: 개발용으로 라이선스가 필요한가요?**  
A: 개발 및 테스트 단계에서는 임시 평가 라이선스로 충분하지만, 프로덕션 배포 시에는 정식 라이선스가 필요합니다.

**Last Updated:** 2025-12-20  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2025-12-09
description: Aspose.Note for Java를 사용하여 Java에서 서식이 지정된 리치 텍스트가 포함된 OneNote를 PDF로 저장하는
  방법을 배워보세요. 원활한 문서 자동화를 위한 단계별 가이드를 따라하세요.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Java에서 서식이 적용된 리치 텍스트로 OneNote를 PDF로 저장
url: /ko/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 서식이 적용된 리치 텍스트로 OneNote를 PDF로 저장하기

## Introduction

리치 텍스트 서식을 유지하면서 **OneNote를 PDF로 저장**해야 한다면, 바로 여기가 정답입니다. 이 튜토리얼에서는 OneNote 문서를 만들고, 사용자 정의 스타일을 적용한 뒤, Aspose.Note for Java를 사용해 직접 PDF로 내보내는 과정을 단계별로 안내합니다. 끝까지 따라오면 어떤 Java 프로젝트에도 삽입해 깔끔한 OneNote‑to‑PDF 변환을 자동화할 수 있는 재사용 가능한 코드 스니펫을 얻게 됩니다.

## Quick Answers
- **이 튜토리얼은 무엇을 가르치나요?** 스타일이 적용된 텍스트로 OneNote 문서를 만들고 PDF로 저장하는 방법.  
- **필요한 라이브러리는?** Aspose.Note for Java (공식 사이트에서 다운로드 가능).  
- **라이선스가 필요합니까?** 테스트용 임시 라이선스는 사용할 수 있지만, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **어떤 IDE를 사용할 수 있나요?** IntelliJ IDEA, Eclipse, NetBeans 등 모든 Java IDE.  
- **출력 형식을 변경할 수 있나요?** 예, Aspose.Note는 PDF, HTML, PNG 등 다양한 형식을 지원합니다.

## What is “save onenote as pdf”?
OneNote를 PDF로 저장한다는 것은 텍스트, 이미지 및 서식을 포함한 OneNote 페이지 구조를 정적인 PDF 파일로 변환하는 것으로, OneNote 없이도 모든 플랫폼에서 볼 수 있습니다.

## Why format rich text java?
Java에서 직접 리치 텍스트 서식트, 색상, 스타일)을 적용하면 수동 편집 없이도 전문적이고 브랜드 가이드라인에 맞는 문서를 생성할 수 있습니다.

## Prerequisites

1. **Java Development Kit (JDK)** – 최신 버전(8 이상) 중 하나.  
2. **Aspose.Note for Java JAR** – [download 링크](https://releases.aspose.com/note/java/)에서 다운로드합니다.  
3. **IDE** – IntelliJ IDEA, Eclipse 또는 선호하는 편집기.  

## Import Packages

먼저, Java 프로젝트에 필요한 패키지를 import해야 합니다. Java 파일의 시작 부분에 다음 import 구문을 추가하세요:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Step 1: Set Up Document and Page

먼저 `Document`와 `Page` 객체를 초기화해 보겠습니다:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Step 2: Create Title with Formatting

이제 서식이 적용된 제목을 만들어 보겠습니다:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Step 3: Create Rich Text with Formatting

다음으로 다양한 서식 스타일이 적용된 리치 텍스트를 만들어 보겠습니다:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Step 4: Add Elements to Page and Document

이제 제목과 리치 텍스트를 페이지와 개요 요소에 추가해 보겠습니다:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Step 5: Save Document

마지막으로, 만든 OneNote 문서를 PDF로 저장합니다:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **파일을 찾을 수 없음** | `dataDir`가 존재하는 폴더를 가리키고 쓰기 권한이 있는지 확인하세요. |
| **폰트 누락** | 참조한 폰트(예: *Calibri*)가 호스트 머신에 설치되어 있는지 확인하세요. |
| **라이선스 적용 안 됨** | `Document`를 생성하기 전에 Aspose 라이선스를 로드하여 평가 워터마크를 방지하세요. |

## Frequently Asked Questions

**Q: 글꼴 스타일을 더 커스터마이즈할 수 있나요?**  
A: 예, `TextStyle` 및 `ParagraphStyle` 클래스를 통해 밑줄, 취소선, 텍스트 정렬 등 추가 속성을 조정할 수 있습니다.

**Q: Aspose.Note for Java가 모든 Java IDE와 호환되나요?**  
A: 물론입니다. IDE가 표준 Java 개발을 지원한다면, 프로젝트 클래스패스에 Aspose.Note JAR을 추가하면 됩니다.

**Q: 이 기능을 웹 애플리케이션에 통합할 수 있나요?**  
A: 예, 동일한 코드를 서블릿 기반 또는 Spring Boot 애플리케이션에서 사용할 수 있어 서버 측에서 동적인 OneNote‑to‑PDF 생성이 가능합니다.

**Q: Aspose.Note for Java 사용에 라이선스 요구사항이 있나요?**  
A: 프로덕션 사용에는 상용 라이선스가 필요합니다. 평가 및 테스트용으로 임시 라이선스를 제공하고 있습니다.

**Q: Aspose.Note for Java가 OneNote 외에 다른 문서 형식을 지원하나요?**  
A: PDF, HTML, PNG, JPEG 등 여러 내보내기 형식을 지원하므로 OneNote 페이지를 원하는 형식으로 변환할 수 있는 유연성을 제공합니다.

## Conclusion

이 가이드에서는 Aspose.Note for Java를 사용해 리치 텍스트 서식을 적용하면서 **OneNote를 PDF로 저장**하는 방법을 보여주었습니다. 단계별 지침을 따라 하면 깔끔한 OneNote 문서를 자동으로 생성하고 Java 기반 솔루션에서 PDF로 변환할 수 있습니다.

---

**마지막 업데이트:** 2025-12-09  
**테스트 환경:** Aspose.Note for Java 24.11 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
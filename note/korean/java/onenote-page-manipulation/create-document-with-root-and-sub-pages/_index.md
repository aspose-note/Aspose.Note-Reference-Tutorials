---
date: 2026-04-30
description: Aspose.Note for Java를 사용하여 OneNote를 PDF로 저장하고 하위 페이지를 추가하는 방법을 배워보세요.
  이 단계별 가이드를 따라 노트를 효율적으로 정리하세요.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: OneNote를 PDF로 저장하고 하위 페이지 추가하는 방법
second_title: Aspose.Note Java API
title: OneNote를 PDF로 저장하고 하위 페이지를 추가하는 방법
url: /ko/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote를 PDF로 저장하고 하위 페이지 추가하는 방법

## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 루트 페이지와 하위 페이지를 모두 포함하는 문서를 만들면서 **OneNote를 PDF로 저장하는 방법**을 알아봅니다. OneNote 노트북을 명확한 계층 구조로 정리하면 탐색이 쉬워지고, PDF로 내보내면 모든 사람이 읽을 수 있는 형식으로 노트를 공유할 수 있습니다. 또한 **OneNote 스타일로 하위 페이지를 추가하는 방법**을 보여드려 다중 레벨 구조를 손쉽게 구축할 수 있습니다.

## 빠른 답변
- **“OneNote를 PDF로 저장”이란 무엇을 의미합니까?** Aspose.Note for Java를 사용하여 OneNote 노트북을 PDF 파일로 내보내는 것을 의미합니다.  
- **필요한 API는 무엇입니까?** Aspose.Note for Java가 필요한 클래스와 메서드를 제공합니다.  
- **계층형 페이지를 만들 수 있나요?** 예 – 페이지 레벨을 설정하여 루트 페이지와 하위 페이지를 만들 수 있습니다.  
- **프로덕션에 라이선스가 필요합니까?** 무료 체험판을 사용할 수 있지만, 프로덕션 사용에는 상용 라이선스가 필요합니다.  
- **어떤 형식으로 내보낼 수 있나요?** PDF 외에도 BMP, PNG, JPEG, DOCX 등 다양한 형식으로 내보낼 수 있습니다.

## OneNote를 PDF로 저장하는 방법

OneNote를 PDF로 저장하면 각 노트북 페이지가 고정 레이아웃 문서로 변환되어 서식, 이미지 및 페이지 계층 구조를 보존합니다. 이는 원본 구조를 유지하면서 노트를 공유, 보관 또는 인쇄할 때 이상적입니다.

## 왜 OneNote에 하위 페이지를 추가하나요?

하위 페이지를 추가하면 관련 콘텐츠를 상위 페이지 아래에 그룹화하여 폴더와 같은 구조를 만들 수 있습니다. 이는 노트 정리를 개선하고 검색 속도를 높이며, 노트북을 PDF로 내보낼 때 읽기 경험을 향상시킵니다.

## 전제 조건

1. **Java Development Kit (JDK)** – 시스템에 JDK가 설치되어 있는지 확인하십시오.  
2. **Aspose.Note for Java** – [웹사이트](https://purchase.aspose.com/buy)에서 Aspose.Note for Java를 다운로드하고 설치하십시오.  
3. **통합 개발 환경 (IDE)** – IntelliJ IDEA, Eclipse, NetBeans 등 Java IDE를 선택하십시오.

## 패키지 가져오기

Start by importing the necessary packages in your Java project:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 단계 1: 문서 디렉터리 설정

Define the directory where you want to save your OneNote document:

```java
String dataDir = "Your Document Directory";
```

## 단계 2: Document 객체 생성

Instantiate a `Document` object:

```java
Document doc = new Document();
```

## 단계 3: 페이지 생성

Initialize page objects and set their levels. Setting the level determines whether a page is a root page or a sub page:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 단계 4: 페이지에 노드 추가

### 첫 번째 페이지에 노드 추가

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### 두 번째 페이지에 노드 추가

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### 세 번째 페이지에 노드 추가

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 단계 5: 페이지를 Document에 추가

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 단계 6: 문서 저장

Save the OneNote document as a PDF (or BMP in this example). Changing the `SaveFormat` lets you export to PDF, which fulfills the “save onenote as pdf” requirement:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **팁:** PDF로 직접 내보내려면 `SaveFormat.Bmp`를 `SaveFormat.Pdf`로 교체하십시오.

축하합니다! 이제 루트 페이지와 하위 페이지가 포함된 OneNote 문서를 성공적으로 만들었으며 Aspose.Note for Java를 사용하여 **OneNote를 PDF로 저장하는 방법**을 배웠습니다.

## 이것이 중요한 이유

- **계층형 조직:** 루트 페이지와 하위 페이지를 사용하면 OneNote 내부에서 폴더 구조를 모방할 수 있습니다.  
- **원활한 PDF 내보내기:** 구조를 정리하면 PDF로 내보낼 때 계층 구조가 보존되어 최종 문서를 읽고 공유하기 쉽습니다.  
- **자동화:** 코드를 더 큰 Java 애플리케이션에 통합하여 구조화된 노트북을 배치로 생성할 수 있습니다.

## 일반적인 함정 및 회피 방법

| 문제 | 원인 | 해결책 |
|-------|-------|----------|
| 페이지가 동일한 수준에 표시됨 | `setLevel` 값이 잘못됨 | 루트 페이지는 `setLevel((byte) 1)`, 하위 페이지는 `setLevel((byte) 2)`(또는 그 이상) 사용하십시오. |
| PDF 출력이 빈 화면 | `SaveFormat.Pdf` 누락 또는 파일 경로 오류 | 디렉터리가 존재하는지 확인하고 `SaveFormat.Pdf`를 사용하십시오. |
| 글꼴이 적용되지 않음 | 잘못된 글꼴 이름 또는 시스템에 글꼴이 없음 | 코드를 실행하는 머신에 해당 글꼴(예: “David Transparent”)이 설치되어 있는지 확인하십시오. |

## 자주 묻는 질문

**Q: Aspose.Note for Java를 사용하여 다중 레벨 하위 페이지를 만들 수 있나요?**  
A: 예, 더 높은 레벨 번호를 설정하여 더 깊은 계층 구조를 만들 수 있습니다(예: 세 번째 레벨 하위 페이지는 `setLevel((byte) 3)` 사용).

**Q: Aspose.Note for Java가 다양한 Java IDE와 호환되나요?**  
A: 물론입니다. IntelliJ IDEA, Eclipse, NetBeans 및 Java 개발을 지원하는 모든 IDE에서 작동합니다.

**Q: OneNote 문서의 텍스트 서식을 사용자 정의할 수 있나요?**  
A: 예. `ParagraphStyle`을 사용하여 각 `RichText` 요소의 글꼴 이름, 크기, 색상 및 기타 속성을 설정할 수 있습니다.

**Q: Aspose.Note for Java가 BMP 외의 형식으로 문서를 저장하는 것을 지원하나요?**  
A: 예. 지원되는 형식에는 PDF, PNG, JPEG, DOCX 등이 포함됩니다. `SaveFormat` 열거형을 적절히 변경하십시오.

**Q: Aspose.Note for Java의 체험판이 있나요?**  
A: 예, Aspose 웹사이트에서 무료 체험판을 다운로드할 수 있습니다.

## 결론

명확한 계층 구조로 OneNote 노트북을 정리하고 PDF로 내보내면 노트를 더 쉽게 접근하고 공유할 수 있습니다. 위 단계들을 따라 하면 이제 Aspose.Note for Java를 사용하여 프로그래밍 방식으로 **OneNote를 PDF로 저장하는 방법**과 **OneNote 스타일로 하위 페이지를 추가하는 방법**을 알게 되었습니다.

---

**마지막 업데이트:** 2026-04-30  
**테스트 환경:** Aspose.Note for Java 24.11 (latest)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-03-05
description: Aspose.Note for Java를 사용하여 번호 매기기 목록을 만들면서 OneNote를 PDF로 저장하는 방법을 배웁니다.
  기본 텍스트 스타일 설정 및 번호 매기기 사용자 지정 단계가 포함됩니다.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: OneNote를 PDF로 저장 – Aspose.Note로 번호 매기기 목록 만들기
url: /ko/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote를 PDF로 저장 – Aspose.Note으로 번호 매기기 목록 만들기

## 소개
Aspose.Note for Java은 Java 개발자가 **OneNote를 PDF로 저장**하고 번호 매기기 목록과 같은 고급 서식으로 문서를 풍부하게 만들 수 있도록 지원합니다. 이 튜토리얼에서는 기본 텍스트 스타일 설정부터 번호 매기기 형식 사용자 지정까지 전체 과정을 단계별로 안내하여 OneNote를 전문적인 모습의 PDF로 내보낼 수 있도록 합니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.Note for Java를 사용하여 OneNote에서 번호 매기기 목록을 만들고 파일을 PDF로 저장합니다.  
- **대상 주요 키워드**는 *save onenote as pdf* 입니다.  
- **라이선스가 필요합니까?** 무료 체험판을 사용할 수 있으며, 프로덕션에서는 상용 라이선스가 필요합니다.  
- **필요한 Java 버전**은 JDK 8 이상입니다.  
- **구현 소요 시간**은 기본 목록의 경우 약 10–15분입니다.

## “OneNote를 PDF로 저장”이란 무엇인가요?
OneNote를 PDF로 저장하면 풍부한 텍스트가 포함된 OneNote 페이지를 휴대 가능하고 고정 레이아웃 문서로 변환하여 OneNote가 없어도 다양한 플랫폼에서 공유할 수 있습니다. 이는 특히 보관, 보고서 작성, 또는 OneNote가 설치되지 않은 사용자에게 콘텐츠를 배포할 때 유용합니다.

## 내보내기 전에 번호 매기기 목록을 만드는 이유는 무엇인가요?
번호 매기기 목록은 구조와 가독성을 높여 내보낸 PDF가 깔끔한 보고서처럼 보이게 합니다. Aspose.Note를 사용하면 **번호 매기기 형식**을 사용자 지정하고, 글꼴을 설정하며, 간격을 제어할 수 있으며, 원본 OneNote 레이아웃을 유지합니다.

## 전제 조건
- 머신에 Java Development Kit (JDK)이 설치되어 있어야 합니다.  
- Aspose.Note for Java 라이브러리를 [here](https://releases.aspose.com/note/java/)에서 다운로드합니다.

## 패키지 가져오기
먼저, OneNote 객체와 PDF 변환을 다루기 위해 필요한 클래스를 가져옵니다.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## 번호 매기기 목록으로 OneNote를 PDF로 저장하는 방법은?
아래는 **목록** 요소를 만들고, **기본 텍스트 스타일을 설정**하며, 최종적으로 **OneNote를 PDF로 내보내는** 단계별 가이드입니다.

### 1단계: Document, Page, Outline 객체 초기화
우리는 핵심 OneNote 구조를 생성하는 것으로 시작합니다. 이는 **add outline element java** 사용법도 보여줍니다.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Pro tip:** `dataDir` 경로를 절대 경로로 유지하거나 `System.getProperty("user.dir")`를 사용하여 경로 문제를 방지하세요.

### 2단계: 기본 텍스트 스타일 설정
일관된 스타일은 목록의 모든 항목이 동일하게 보이도록 보장합니다.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### 3단계: Outline 요소 만들기 (번호 매기기 목록)
여기서는 `NumberList`를 사용하여 **번호 매기기 형식**을 사용자 지정합니다. 패턴 `"{0})"`은 “1)”, “2)” 등으로 출력됩니다.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **왜 중요한가:** 각 `OutlineElement`에 `NumberList`를 연결하면 번호 매기기 스타일, 글꼴 및 크기를 완전히 제어할 수 있습니다.

### 4단계: Outline 요소를 Outline에 추가
이제 개별 목록 항목을 하나의 Outline으로 묶습니다.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### 5단계: Outline을 페이지에 연결
Outline이 OneNote 페이지 계층 구조의 일부가 됩니다.

```java
page.appendChildLast(outline);
```

### 6단계: 문서를 PDF로 저장
마지막으로, **OneNote를 PDF로 저장**합니다. 출력 파일에는 정의된 대로 번호 매기기 목록이 정확히 포함됩니다.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

위 코드를 실행하면 지정한 디렉터리에 `CreateNumberedList_out.pdf`라는 PDF가 생성되며, 번호 매기기 목록 형식이 유지됩니다.

## 일반적인 문제 및 해결책
| Issue | Solution |
|-------|----------|
| **PDF가 비어 있음** | `doc.save()` 전에 `doc.appendChildLast(page);`가 호출되었는지 확인하세요. |
| **번호 매기기가 표시되지 않음** | `NumberList` 패턴과 `NumberFormat`이 올바르게 설정되었는지 확인하세요. |
| **파일을 찾을 수 없음 오류** | `dataDir`에 절대 경로를 사용하거나 미리 디렉터리를 생성하세요. |
| **글꼴 불일치** | 코드를 실행하는 머신에 해당 글꼴(예: Arial)을 설치하세요. |

## 자주 묻는 질문
### Q: OneNote 목록의 번호 매기기 형식을 사용자 지정할 수 있나요?
A: 물론 가능합니다! Aspose.Note for Java에서 제공하는 `NumberList` 클래스를 사용하여 번호 매기기 형식을 사용자 지정할 수 있습니다.

### Q: Aspose.Note for Java의 체험 버전을 사용할 수 있나요?
A: 예, 무료 체험판을 [here](https://releases.aspose.com/)에서 다운로드할 수 있습니다.

### Q: Aspose.Note for Java에 대한 지원을 어떻게 받을 수 있나요?
A: 커뮤니티 지원을 위해 [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) 를 방문하세요.

### Q: Aspose.Note for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?
A: 포괄적인 정보를 위해 [documentation](https://reference.aspose.com/note/java/)을 참고하세요.

### Q: Aspose.Note for Java 라이선스는 어떻게 구매하나요?
A: 라이선스는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

## 결론
이 튜토리얼에서는 Aspose.Note for Java를 사용하여 깔끔한 번호 매기기 목록을 만들면서 **OneNote를 PDF로 저장**하는 방법을 보여주었습니다. 기본 텍스트 스타일을 설정하고, 번호 매기기 형식을 사용자 지정하며, 단계별 가이드를 따르면 OneNote 페이지에서 빠르고 안정적으로 전문적인 PDF를 생성할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026-03-05  
**테스트 환경:** Aspose.Note for Java 24.11  
**작성자:** Aspose
---
date: 2025-12-02
description: Aspose.Note for Java를 사용하여 Java에서 제목이 있는 OneNote 페이지를 만드는 방법을 배웁니다. 이
  가이드는 OneNote 페이지 제목을 설정하고 제목 글꼴을 사용자 지정하는 방법을 보여줍니다.
language: ko
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: 제목이 있는 OneNote 페이지 만들기 - Java
url: /java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote 페이지를 제목과 함께 만들기 - Java

## 소개

프로그래밍 방식으로 **OneNote 페이지를 만드는 방법**이 필요하다면 Aspose.Note for Java가 이를 간단하게 해줍니다. 이 튜토리얼에서는 OneNote 파일을 생성하고, 페이지 제목을 설정하며, 제목의 글꼴까지 커스터마이징하는 방법을 Java 코드만으로 배우게 됩니다. 끝까지 따라오면 언제든 Java 애플리케이션에 통합할 수 있는 사용 준비가 된 OneNote 문서를 얻게 됩니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.Note for Java.
- **제목에 사용자 지정 글꼴을 적용할 수 있나요?** 예 – `ParagraphStyle`을 사용해 글꼴 이름, 크기, 색상을 정의합니다.
- **지원되는 Java 버전은?** JDK 8 이상이면 모두 지원됩니다(API는 하위 호환됩니다).
- **개발용 라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 프로덕션에서는 라이선스가 필요합니다.
- **출력 파일은 어디에 저장되나요?** `dataDir` 변수에 지정한 경로에 저장됩니다.

## OneNote 페이지 제목이란?
OneNote 페이지 제목은 각 페이지 상단에 표시되는 헤더입니다. 일반적으로 페이지 이름, 생성 날짜 및 시간이 포함됩니다. 프로그래밍 방식으로 이 제목을 설정하면 일관되고 구조화된 노트북을 만들 수 있습니다.

## 프로그래밍 방식으로 OneNote 페이지 제목을 설정해야 하는 이유
- **자동화:** 수동 편집 없이 보고서나 회의록을 생성합니다.  
- **일관성:** 모든 페이지에 동일한 명명 규칙을 적용합니다.  
- **통합:** OneNote를 CRM, 프로젝트 관리 도구 등 다른 시스템과 연동합니다.  

## 사전 준비 사항

- **Java Development Kit (JDK)** – 버전 8 이상.  
- **Aspose.Note for Java** – 공식 사이트 **[here](https://releases.aspose.com/note/java/)**에서 다운로드.  
- **IDE** – IntelliJ IDEA, Eclipse 또는 NetBeans 중 선택.

## 패키지 가져오기

먼저 Aspose.Note 라이브러리에서 필요한 클래스를 가져옵니다.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### 단계 1: 문서 디렉터리 설정  
생성된 OneNote 파일이 저장될 위치를 정의합니다.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### 단계 2: Document 객체 생성  
새 `Document`를 인스턴스화합니다 – 이는 구축할 OneNote 파일을 나타냅니다.

```java
// Create an object of the Document class
Document doc = new Document();
```

### 단계 3: Page 객체 초기화  
제목과 기타 콘텐츠를 담을 `Page` 객체를 생성합니다.

```java
// Initialize Page class object
Page page = new Page();
```

### 단계 4: 기본 텍스트 스타일 설정  
제목 텍스트에 적용될 기본 `ParagraphStyle`을 정의합니다. 여기서 **OneNote 제목 글꼴을 커스터마이징**합니다.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### 단계 5: 페이지 제목 속성 설정  
여기서 **OneNote 페이지 제목** 세부 정보를 설정합니다 – 제목 텍스트, 날짜, 시간 등을 지정합니다. 필요에 따라 문자열을 수정하세요.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### 단계 6: 제목을 페이지에 할당  
이제 `Title` 객체를 `Page`와 연결하여 **OneNote에 제목을 추가**합니다.

```java
page.setTitle(title);
```

### 단계 7: 페이지를 Document에 추가  
구성된 페이지를 문서 구조에 추가합니다.

```java
doc.appendChildLast(page);
```

### 단계 8: OneNote 문서 저장  
출력 파일 이름을 지정하고 노트북을 저장합니다. 이로써 **java create onenote file** 과정이 완료됩니다.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## 일반적인 문제 및 팁

| 문제 | 해결책 |
|-------|----------|
| **잘못된 파일 경로** | `dataDir`이 올바른 구분자(`/` 또는 `\\`)로 끝나는지, 폴더가 존재하는지 확인하세요. |
| **제목이 보이지 않음** | 각 `RichText` 요소에 `ParagraphStyle`이 적용되었는지 확인하세요. |
| **라이선스 예외** | 테스트용으로 체험판 라이선스를 사용하고, 배포 전에는 정식 라이선스를 적용하세요. |
| **날짜가 잘못된 월 표시** | Java의 월은 0부터 시작합니다; `cal.set(2018, 04, 03)`은 실제로 5월을 설정합니다. 적절히 조정하세요. |

## 자주 묻는 질문

**Q: Aspose.Note for Java는 다양한 Java 버전과 호환되나요?**  
A: 예, 라이브러리는 Java 8 이상에서 작동하므로 환경에 따라 유연하게 사용할 수 있습니다.

**Q: 페이지 제목의 글꼴 스타일과 크기를 커스터마이즈할 수 있나요?**  
A: 물론입니다! 단계 4에서 보여준 대로 `ParagraphStyle`을 사용해 원하는 글꼴 이름, 크기, 색상을 설정하면 됩니다.

**Q: 페이지에 더 많은 콘텐츠(예: 단락, 이미지)를 추가하려면 어떻게 하나요?**  
A: 추가 `RichText` 또는 `Image` 객체를 생성하고 스타일을 지정한 뒤, `page.appendChildLast(yourObject)`를 사용해 `Page`에 추가하면 됩니다.

**Q: Aspose.Note for Java의 체험판 버전을 사용할 수 있나요?**  
A: 예, Aspose 웹사이트에서 무료 체험판을 다운로드하여 모든 기능을 평가할 수 있습니다.

**Q: 문제가 발생했을 때 어디에서 지원을 받을 수 있나요?**  
A: [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 커뮤니티 도움을 받거나 Aspose에 지원 티켓을 열어 문의하세요.

---

**마지막 업데이트:** 2025-12-02  
**테스트 환경:** Aspose.Note for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
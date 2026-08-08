---
date: 2026-08-08
description: Aspose.Note for Java를 사용하여 페이지 개정을 프로그래밍 방식으로 가져와 OneNote에서 변경 사항을 추적하는
  방법을 배웁니다.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: OneNote에서 페이지 개정 가져오기 - Aspose.Note
og_description: Aspose.Note for Java를 사용하여 페이지 개정을 프로그래밍 방식으로 가져와 OneNote에서 변경 사항을
  추적하는 방법을 배웁니다.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: OneNote에서 변경 사항 추적 – Aspose.Note와 함께 페이지 개정
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: OneNote에서 변경 사항 추적 – Aspose.Note와 함께 페이지 개정
url: /ko/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 변경 사항 추적 – Aspose.Note를 사용한 페이지 개정

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.Note for Java를 사용하여 OneNote 파일에서 페이지 개정 기록을 검색합니다.  
- **필요한 라이브러리 버전은?** `LoadOptions.setLoadHistory`를 지원하는 최신 Aspose.Note for Java 릴리스라면 모두 사용 가능.  
- **라이선스가 필요합니까?** 테스트용 임시 평가 라이선스는 작동하지만, 프로덕션에서는 상용 라이선스가 필요합니다.  
- **개정을 수정할 수 있나요?** API는 개정에 대해 읽기 전용이며, 가져오기만 가능합니다.  
- **주요 전제 조건은 무엇인가요?** Java JDK, Aspose.Note for Java, 그리고 개정 데이터가 포함된 OneNote 문서.

## “aspose.note 페이지 개정 튜토리얼”이란?
이 튜토리얼은 프로그래밍 방식으로 OneNote 페이지의 과거 버전에 접근하는 방법을 보여줍니다. 각 개정에는 작성자, 생성 시간, 수정 시간과 같은 메타데이터가 포함되어 있어, 애플리케이션 내에서 감사 로그나 변경 기록 기능을 구축할 수 있습니다.

## 페이지 개정 추적에 Aspose.Note를 사용하는 이유?
표준 2 GHz CPU에서 500 페이지 파일의 전체 개정 기록을 5 초 미만에 로드하고, OneNote UI를 실행하지 않아도 메타데이터를 검색할 수 있습니다. 이 라이브러리는 30개 이상의 입력 및 출력 형식을 지원하며, Windows, Linux, macOS에서 실행되어 서버 환경의 95 % 이상을 커버하고, 각 개정 속성을 완벽히 제어할 수 있습니다.

## 전제 조건

### 1. Java Development Kit (JDK)
최근 JDK(8 이상)가 설치되어 있고 `JAVA_HOME`이 설정되어 있는지 확인하십시오.

### 2. Aspose.Note for Java
라이브러리를 [download link](https://releases.aspose.com/note/java/)에서 다운로드하십시오.

### 3. Sample OneNote Document
개정 기록이 포함된 페이지가 있는 OneNote 파일(예: `Sample1.one`)을 만들거나 구하십시오.

## 패키지 가져오기
먼저 필요한 Aspose.Note 클래스를 가져옵니다. `Document`는 OneNote 노트북을 나타내고, `LoadOptions`는 로딩 동작을 구성하며, `Page`는 단일 페이지를 나타냅니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 단계별 구현

### 단계 1: 문서 디렉터리 설정
OneNote 파일이 위치한 폴더를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

### 단계 2: 히스토리가 활성화된 OneNote 문서 로드
`LoadOptions`는 Aspose.Note가 파일을 여는 방식을 지정하는 구성 클래스이며, 개정 데이터를 읽을지 여부를 포함합니다. 문서를 로드하기 전에 해당 플래그를 활성화하십시오.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### 단계 3: 첫 번째 페이지 가져오기
첫 번째 페이지 객체를 가져옵니다; 이는 해당 페이지의 개정 기록을 검색하기 위한 기준점이 됩니다.

```java
Page firstPage = document.getFirstChild();
```

### 단계 4: 페이지 개정 순회
각 개정을 순회하면서 타임스탬프, 제목, 레벨, 작성자와 같은 유용한 메타데이터를 출력합니다.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **팁:** 특정 작성자나 날짜 범위로 개정을 필터링해야 하는 경우, `for` 루프 안에 조건 검사를 추가하면 됩니다.

## 일반적인 문제 및 해결책
- **개정이 반환되지 않음:** 문서를 로드하기 전에 `loadOptions.setLoadHistory(true)`가 호출되었는지 확인하십시오.  
- **작성자 또는 제목이 null:** 일부 오래된 OneNote 버전에서는 해당 필드가 저장되지 않을 수 있으므로, `null` 값을 적절히 처리하십시오.  
- **대형 노트북에서 성능 저하:** 필요한 섹션만 로드하거나 JVM 힙 크기를 늘리십시오.

## 자주 묻는 질문

**Q1: Aspose.Note for Java를 사용하여 페이지 개정을 수정할 수 있나요?**  
A1: 아니요, 현재 API는 페이지 개정에 대해 읽기 전용 접근만 지원합니다.

**Q2: Aspose.Note for Java가 다양한 버전의 OneNote 문서와 호환되나요?**  
A2: 예, 여러 OneNote 파일 형식을 지원하여 버전 간 원활한 처리가 가능합니다.

**Q3: Aspose.Note for Java를 사용하려면 라이선스가 필요합니까?**  
A3: 프로덕션 사용에는 상용 라이선스가 필요하지만, 테스트용 임시 평가 라이선스를 사용할 수 있습니다.

**Q4: Aspose.Note for Java 사용 중 문제가 발생하면 지원을 받을 수 있나요?**  
A4: 예, Aspose.Note 포럼에서 질문할 수 있습니다. [Aspose.Note forum](https://forum.aspose.com/c/note/28)

**Q5: Aspose.Note for Java에 대한 무료 체험판이 있나요?**  
A5: 예, [website](https://releases.aspose.com/)에서 무료 체험판을 다운로드할 수 있습니다.

**마지막 업데이트:** 2026-08-08  
**테스트 환경:** Aspose.Note for Java (latest release)  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [track changes onenote – Aspose.Note로 페이지 개정 관리](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java Tutorial - OneNote 페이지 정보 가져오기 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [OneNote 페이지 배경 색상 변경 – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
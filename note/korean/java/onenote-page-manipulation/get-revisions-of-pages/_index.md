---
date: 2026-08-13
description: Aspose.Note for Java를 사용하여 OneNote 페이지 수정 시간을 가져오고 페이지 리비전을 검색하는 방법을
  배웁니다. 감사 및 문서 관리에 이상적입니다.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: OneNote 페이지 리비전 가져오기 - Aspose.Note
og_description: Aspose.Note for Java를 사용하여 OneNote 페이지 수정 시간을 가져오고 페이지 리비전을 검색하는 방법을
  배웁니다. 빠른 단계, 코드 스니펫 및 문제 해결.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Aspose.Note를 사용하여 OneNote 페이지 수정 시간 가져오기 – Java 튜토리얼
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Aspose.Note를 사용하여 OneNote 페이지 수정 시간 가져오기
url: /ko/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note를 사용하여 OneNote 페이지 수정 시간 가져오기

## 소개

이 튜토리얼에서는 **get onenote page modified** 타임스탬프를 가져오고 Aspose.Note for Java를 사용하여 OneNote 페이지의 전체 수정 내역을 추출하는 방법을 배웁니다. 감사 추적 기능, 변경 로그 뷰어를 구축하거나 대시보드에 최신 편집 날짜를 표시해야 할 경우, 이 가이드는 환경 설정부터 일반적인 함정 처리까지 모든 단계를 안내합니다.

## 빠른 답변
- **“get last modified time”은 무엇을 반환합니까?** OneNote 페이지에서 가장 최근 편집된 시간의 타임스탬프를 반환합니다.  
- **어떤 클래스가 수정 내역을 제공합니까?** `PageHistory`는 `Document.getPageHistory(Page)`를 통해 제공합니다.  
- **이 기능에 라이선스가 필요합니까?** 예, 프로덕션 사용을 위해서는 유효한 Aspose.Note 라이선스가 필요합니다.  
- **지원되는 Java 버전은 무엇입니까?** Java 8 이상 (JDK 8+).  
- **작성자별로 수정 내역을 필터링할 수 있습니까?** 각 `Page` 객체의 `Author` 속성을 읽어 자체 필터를 적용할 수 있습니다.

## OneNote에서 “get last modified time”이란?

수정된 마지막 시간은 각 OneNote 페이지에 메타데이터 속성으로 저장되어 가장 최근 편집 시점을 나타냅니다. Aspose.Note는 이 값을 `Page.getLastModifiedTime()` 메서드를 통해 노출하며, 이 메서드는 `java.util.Date` 객체를 반환하므로 애플리케이션 요구에 따라 포맷하거나 로그에 기록할 수 있습니다.

## 페이지 수정 내역을 가져와야 하는 이유

페이지 수정 내역을 가져오면 OneNote 페이지에 대한 모든 변경 사항에 대한 완전한 감사 추적을 제공하여 누가 언제 무엇을 편집했는지 추적할 수 있습니다. 이 기록은 버전 비교, 이전 상태 복원, 팀 간 협업 패턴 분석 등에 활용될 수 있어 규정 준수 및 품질 관리에 필수적입니다.

## 사전 요구 사항

- **Java Development Kit (JDK) 8 이상** – Oracle 웹사이트 또는 호환 가능한 공급업체에서 설치합니다.  
- **Aspose.Note for Java 라이브러리** – Aspose.Note Java 릴리스 페이지 **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)**에서 JAR를 다운로드하고 설치 가이드 **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**를 따릅니다.  

## 패키지 가져오기

`Document` 클래스는 메모리에 로드된 OneNote 노트북을 나타내며, `Page`와 `PageHistory`는 개별 페이지와 해당 수정 데이터를 접근할 수 있게 합니다.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(실제 import 문은 원본 코드 블록 수를 유지하기 위해 일반 텍스트로 표시됩니다.)*

## OneNote 페이지 수정 시간을 가져오는 방법

마지막 수정 타임스탬프를 얻으려면 먼저 OneNote 문서를 `Document` 객체에 로드한 뒤 원하는 `Page`를 선택합니다. 해당 페이지에서 `getLastModifiedTime()` 메서드를 호출하면 `java.util.Date`를 반환합니다. 이후 `SimpleDateFormat`을 사용해 날짜를 포맷하거나 UTC로 변환하여 시간대에 관계없이 일관된 보고를 할 수 있습니다.

## 단계 1: 문서 디렉터리 설정

OneNote 파일이 들어 있는 폴더를 정의합니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 단계 2: 문서 로드

전체 경로를 지정하여 `.one` 파일을 `Document` 인스턴스로 생성합니다.

```java
String dataDir = "Your Document Directory";
```

## 단계 3: 첫 번째 페이지 가져오기

문서의 페이지 컬렉션에서 첫 번째 `Page` 객체를 가져옵니다.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 단계 4: 페이지 수정 내역 가져오기

선택한 페이지에 대한 `PageHistory`를 얻습니다. 노트북이 한 번도 편집되지 않은 경우 이 호출은 `null`을 반환할 수 있습니다.

```java
Page firstPage = doc.getFirstChild();
```

## 단계 5: 페이지 수정 내역 순회

각 `Page` 수정 내역을 반복하면서 `Author`와 `LastModifiedTime`을 읽고 정보를 표시합니다.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## 일반적인 문제와 해결책
- **Null `PageHistory`** – 노트북에 실제로 수정 내역이 있는지 확인하십시오; 그렇지 않으면 `getPageHistory`가 `null`을 반환합니다.  
- **시간대 차이** – `getLastModifiedTime()`은 JVM의 기본 시간대를 사용합니다. 애플리케이션에서 표준 시간대가 필요하면 `SimpleDateFormat`으로 UTC로 변환하십시오.  
- **라이선스 미로드** – 유효한 라이선스가 없으면 Aspose.Note가 평가 모드로 실행되어 페이지 처리에 제한이 있습니다. 이 제한을 피하려면 애플리케이션 시작 시 라이선스 파일을 로드하십시오.

## 자주 묻는 질문

**Q1: Aspose.Note for Java를 사용하여 새로운 OneNote 문서를 만들 수 있나요?**  
A: 예, API를 통해 프로그래밍 방식으로 OneNote 노트북을 처음부터 생성, 편집 및 저장할 수 있습니다.

**Q2: Aspose.Note for Java가 다양한 버전의 OneNote 파일과 호환되나요?**  
A: 예, OneNote 2007‑2021 파일 형식을 지원하여 데스크톱 및 클라우드 환경 전반에 걸친 광범위한 호환성을 보장합니다.

**Q3: OneNote 문서를 내보낼 때 출력 형식을 사용자 정의할 수 있나요?**  
A: 물론입니다. PDF, HTML, PNG, SVG 등으로 내보낼 수 있으며 이미지 해상도와 글꼴 포함과 같은 옵션을 제어할 수 있습니다.

**Q4: Aspose.Note for Java를 상업적으로 사용하려면 라이선스가 필요합니까?**  
A: 예, 프로덕션 배포를 위해서는 상업용 라이선스가 필수입니다. 평가용 무료 체험판을 제공하고 있습니다.

**Q5: 문제가 발생했을 때 어디에서 도움을 받을 수 있나요?**  
A: Aspose.Note 커뮤니티 포럼 **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**을 방문하여 질문하고 경험을 공유하며 커뮤니티와 Aspose 엔지니어에게 도움을 받을 수 있습니다.

---

**마지막 업데이트:** 2026-08-13  
**테스트 환경:** Aspose.Note for Java 23.12 (작성 시 최신 버전)  
**작성자:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 관련 튜토리얼

- [Aspose Java 튜토리얼 - OneNote 페이지 정보 가져오기 - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note 페이지 수정 튜토리얼 – OneNote에서 페이지 수정 내역 가져오기](/note/java/onenote-page-manipulation/get-page-revisions/)
- [변경 사항 추적 onenote – Aspose.Note로 페이지 수정 관리](/note/java/onenote-page-manipulation/working-with-page-revisions/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
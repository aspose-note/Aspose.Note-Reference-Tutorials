---
date: 2026-01-10
description: Aspose.Note for Java를 사용하여 OneNote 페이지의 마지막 수정 시간과 수정 내역을 가져오는 방법을 배우세요.
  이를 Java 애플리케이션에 통합하여 효율적인 문서 관리를 구현하세요.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote 페이지의 마지막 수정 시간 가져오기 – Aspose.Note
url: /ko/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote 페이지 개정 가져오기 - Aspose.Note

## 소개

이 튜토리얼에서는 OneNote 문서 내부 페이지의 **마지막 수정 시간**을 가져오고 Aspose.Note for Java를 사용하여 전체 개정 기록을 검색하는 방법을 살펴봅니다. 문서 관리 시스템을 구축하거나, 변경 사항을 감사하거나, 페이지가 마지막으로 편집된 시점을 표시해야 할 경우, 이 가이드는 해당 정보를 프로그래밍 방식으로 추출하는 방법을 정확히 보여줍니다.

## 빠른 답변
- **“마지막 수정 시간 가져오기”가 반환하는 값은 무엇인가요?** OneNote 페이지에서 가장 최근에 편집된 시점의 타임스탬프입니다.  
- **어떤 클래스가 개정 기록을 제공하나요?** `Document.getPageHistory(Page)`를 통해 얻는 `PageHistory` 클래스입니다.  
- **이 기능을 사용하려면 라이선스가 필요합니까?** 예, 프로덕션 사용을 위해서는 유효한 Aspose.Note 라이선스가 필요합니다.  
- **지원되는 Java 버전은 무엇인가요?** Java 8 이상 (JDK 8+).  
- **작성자별로 개정을 필터링할 수 있나요?** 각 `Page` 객체의 `Author` 속성을 읽어 직접 필터링을 적용할 수 있습니다.

## OneNote에서 “마지막 수정 시간 가져오기”란 무엇인가요?

**마지막 수정 시간**은 각 페이지에 저장되는 메타데이터 필드로, 페이지가 가장 최근에 변경된 시점을 기록합니다. Aspose.Note는 `Page.getLastModifiedTime()` 메서드를 통해 이 값을 제공하므로 변경 날짜를 표시하거나 로그에 기록하기가 쉽습니다.

## 페이지 개정을 가져와야 하는 이유

- **감사 추적:** 누가 무엇을 언제 변경했는지 기록을 유지합니다.  
- **버전 비교:** 두 개정을 나란히 비교하는 기능을 구축합니다.  
- **사용자 협업 인사이트:** 공유 노트북에서의 편집 패턴을 파악합니다.  

## 사전 요구 사항

시작하기 전에 다음 항목이 준비되어 있는지 확인하십시오:

### Java Development Kit (JDK) 설치
Oracle 웹사이트 또는 선호하는 패키지 관리자를 통해 JDK 8 이상을 설치하십시오.

### Aspose.Note for Java 라이브러리
공식 사이트에서 라이브러리를 다운로드하십시오. 다운로드 링크는 **[here](https://releases.aspose.com/note/java/)** 에서 확인할 수 있습니다. 문서의 설치 안내는 **[here](https://reference.aspose.com/note/java/)** 를 참고하십시오.

## 패키지 가져오기

시작하려면 Java 프로젝트에 필요한 패키지를 가져오세요. 이 패키지들을 통해 Aspose.Note for Java가 제공하는 기능을 활용할 수 있습니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

이제 제공된 예제 코드를 여러 단계로 나누어 각 구성 요소와 기능을 이해해 보겠습니다.

## OneNote 페이지의 마지막 수정 시간 가져오기

### 단계 1: 문서 디렉터리 설정
OneNote 문서가 위치한 디렉터리를 정의하십시오.

```java
String dataDir = "Your Document Directory";
```

### 단계 2: 문서 로드
OneNote 문서를 Aspose.Note에 로드하십시오.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 단계 3: 첫 번째 페이지 가져오기
문서에서 첫 번째 페이지를 가져옵니다.

```java
Page firstPage = doc.getFirstChild();
```

### 단계 4: 페이지 개정 가져오기
페이지의 개정 기록을 가져옵니다.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### 단계 5: 페이지 개정 순회
페이지 개정 목록을 순회하면서 **마지막 수정 시간**을 포함한 관련 정보를 가져옵니다.

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

## 일반적인 문제 및 해결책
- **Null `PageHistory`**: 문서에 실제로 개정이 포함되어 있는지 확인하십시오; 그렇지 않으면 `getPageHistory`가 `null`을 반환할 수 있습니다.  
- **시간대 차이**: `getLastModifiedTime()`은 시스템 기본 시간대의 `java.util.Date`를 반환합니다. 필요에 따라 UTC로 변환하십시오.  
- **라이선스 미로드**: 유효한 라이선스가 없으면 Aspose.Note가 평가 모드로 동작하여 처리 가능한 페이지 수가 제한될 수 있습니다.

## 자주 묻는 질문

### Q1: Aspose.Note for Java를 사용해 새로운 OneNote 문서를 만들 수 있나요?
A1: 예, Aspose.Note for Java는 OneNote 문서를 프로그래밍 방식으로 생성, 읽기 및 조작하기 위한 포괄적인 지원을 제공합니다.

### Q2: Aspose.Note for Java가 다양한 버전의 OneNote 파일과 호환되나요?
A2: 예, Aspose.Note for Java는 다양한 Microsoft OneNote 파일 버전을 지원하여 여러 환경에서 호환성을 보장합니다.

### Q3: OneNote 문서를 내보낼 때 출력 형식을 맞춤 설정할 수 있나요?
A3: 물론입니다. Aspose.Note for Java는 PDF, HTML, 이미지 등 다양한 형식으로 OneNote 문서를 내보낼 때 맞춤 옵션을 제공하여 유연하게 처리할 수 있습니다.

### Q4: Aspose.Note for Java를 상업적으로 사용하려면 라이선스가 필요합니까?
A4: 예, Aspose.Note for Java를 상업적으로 사용하려면 유효한 라이선스가 필요합니다. 라이선스는 Aspose 웹사이트에서 구매할 수 있습니다.

### Q5: Aspose.Note for Java와 관련된 문제나 질문이 있을 때 어디에서 도움을 받을 수 있나요?
A5: 지원 및 도움을 원하시면 Aspose.Note 포럼 **[here](https://forum.aspose.com/c/note/28)** 를 방문하십시오. 여기서 질문을 하고, 경험을 공유하며, 다른 사용자 및 전문가와 소통할 수 있습니다.

---

**마지막 업데이트:** 2026-01-10  
**테스트 환경:** Aspose.Note for Java 23.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-01-10
description: Java용 Aspose.Note 페이지 개정 튜토리얼을 배우세요 – Aspose.Note를 사용하여 OneNote 페이지 개정을
  프로그래밍 방식으로 가져옵니다. 단계별 가이드를 따라하세요.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note 페이지 개정 튜토리얼 – OneNote에서 페이지 개정 가져오기
url: /ko/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 페이지 개정 가져오기 - Aspose.Note

OneNote는 강력한 필기 플랫폼이며, 변경 사항을 감사해야 할 때 **aspose.note page revisions tutorial**은 몇 줄의 Java 코드만으로 개정 기록을 가져오는 방법을 정확히 보여줍니다. 이 가이드에서는 환경 설정부터 각 개정의 세부 정보를 출력하는 방법까지 모든 과정을 단계별로 안내하므로 편집, 작성자 기여 및 타임스탬프를 손쉽게 추적할 수 있습니다.

## 빠른 답변
- **튜토리얼은 무엇을 다루나요?** Aspose.Note for Java를 사용하여 OneNote 파일에서 페이지 개정 기록을 가져옵니다.  
- **필요한 라이브러리 버전은?** `LoadOptions.setLoadHistory`를 지원하는 최신 Aspose.Note for Java 릴리스라면 모두 사용 가능합니다.  
- **라이선스가 필요합니까?** 테스트용 임시 평가 라이선스를 사용할 수 있지만, 프로덕션에서는 상업용 라이선스가 필요합니다.  
- **개정을 수정할 수 있나요?** API는 개정에 대해 읽기 전용이며, 조회만 가능합니다.  
- **주요 전제 조건은?** Java JDK, Aspose.Note for Java, 그리고 개정 데이터가 포함된 OneNote 문서가 필요합니다.

## “aspose.note page revisions tutorial”란 무엇인가요?
이 튜토리얼은 프로그래밍 방식으로 OneNote 페이지의 과거 버전에 접근하는 방법을 보여줍니다. 각 개정에는 작성자, 생성 시간, 수정 시간과 같은 메타데이터가 포함되어 있어 애플리케이션 내부에 감사 로그나 변경 로그 기능을 구현할 수 있습니다.

## 페이지 개정 추적에 Aspose.Note를 사용하는 이유
- **UI 의존 없음** – 코드만으로 동작하므로 백엔드 서비스에 최적입니다.  
- **크로스‑플랫폼** – Java는 Windows, Linux, macOS에서 실행됩니다.  
- **전체 제어** – OneNote를 직접 열지 않고도 모든 개정 속성을 조회할 수 있습니다.  
- **성능** – 개정 로딩이 최적화되어 있어 대용량 노트북도 빠르게 처리됩니다.

## 전제 조건

### 1. Java Development Kit (JDK)
최근 JDK(8 이상)가 설치되어 있고 `JAVA_HOME`이 설정되어 있는지 확인하십시오.

### 2. Aspose.Note for Java
라이브러리를 [download link](https://releases.aspose.com/note/java/)에서 다운로드하십시오.

### 3. Sample OneNote Document
개정 기록이 포함된 OneNote 파일(예: `Sample1.one`)을 만들거나 확보하십시오.

## Import Packages
먼저 필요한 Aspose.Note 클래스를 가져옵니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Step‑by‑Step Implementation

### Step 1: Set Up Document Directory
OneNote 파일이 위치한 폴더를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Load OneNote Document with History Enabled
`LoadOptions` 플래그를 활성화하여 개정 데이터를 가져옵니다.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Step 3: Get the First Page
첫 번째 페이지 객체를 가져옵니다. 이 객체가 개정 기록을 조회하는 기준점이 됩니다.

```java
Page firstPage = document.getFirstChild();
```

### Step 4: Iterate Through Page Revisions
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

> **Pro tip:** 특정 작성자나 날짜 범위로 개정을 필터링해야 하는 경우, `for` 루프 내부에 조건문을 추가하면 됩니다.

## Common Issues & Solutions
- **No revisions returned:** 문서를 로드하기 전에 `loadOptions.setLoadHistory(true)`가 호출되었는지 확인하십시오.  
- **Null author or title:** 일부 오래된 OneNote 버전에서는 해당 필드가 저장되지 않을 수 있으니 `null` 값을 적절히 처리하십시오.  
- **Performance lag on large notebooks:** 필요한 섹션만 로드하거나 JVM 힙 크기를 늘리십시오.

## Frequently Asked Questions

**Q1: Can I use Aspose.Note for Java to modify page revisions?**  
A1: No, the API currently supports only read‑only access to page revisions.

**Q2: Is Aspose.Note for Java compatible with different versions of OneNote documents?**  
A2: Yes, it works with various OneNote file formats, allowing seamless processing across versions.

**Q3: Does Aspose.Note for Java require a license to use?**  
A3: A commercial license is required for production use, but a temporary evaluation license is available for testing.

**Q4: Can I seek support if I encounter any issues while using Aspose.Note for Java?**  
A4: Yes, you can ask questions on the Aspose.Note forum [here](https://forum.aspose.com/c/note/28).

**Q5: Is there a free trial available for Aspose.Note for Java?**  
A5: Yes, you can download a free trial from the [website](https://releases.aspose.com/).

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
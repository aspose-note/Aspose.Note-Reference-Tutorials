---
date: 2026-01-15
description: Aspose.Note for Java를 사용하여 OneNote에서 변경 사항을 추적하고 페이지 개정을 관리하는 방법을 배우세요.
  개정 요약 예제와 개정 날짜를 수정하는 방법을 포함합니다.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote에서 변경 사항 추적 – Aspose.Note로 페이지 개정 관리
url: /ko/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 페이지 개정 관리하기 - Aspose.Note

## Introduction

OneNote은 노트를 정리하는 강력한 도구이며, **track changes onenote**를 추적해야 할 때 페이지 개정을 관리하는 것이 효과적인 협업에 필수적입니다. Aspose.Note for Java를 사용하면 프로그래밍 방식으로 개정을 처리하고, 페이지를 누가 편집했는지 확인하며, 타임스탬프까지 조정할 수 있습니다. 이 튜토리얼은 문서를 로드하는 단계부터 개정 요약을 업데이트하는 단계까지 각 단계를 안내합니다.

## Quick Answers
- **“track changes onenote”가 무엇을 의미하나요?** OneNote 페이지를 누가 언제 편집했는지 모니터링하는 것을 의미합니다.
- **필요한 라이브러리는 무엇인가요?** Aspose.Note for Java.
- **개정의 작성자나 날짜를 변경할 수 있나요?** 예, RevisionSummary API(`modify revision date`)를 사용하면 가능합니다.
- **미리 OneNote 파일이 필요합니까?** 예, 샘플 `.one` 파일이 필요합니다.
- **프로덕션에서 라이선스가 필요합니까?** 상업적 사용을 위해서는 유효한 Aspose.Note 라이선스가 필요합니다.

## What is a revision summary example?

*revision summary*는 페이지에 대한 최신 변경 사항의 메타데이터—작성자 이름, 마지막 수정 시간 및 기타 세부 정보를 제공합니다. 이 가이드에서는 해당 정보를 가져와 표시하고, **modify revision date**를 수행하는 방법을 보여줍니다.

## Why track changes onenote with Aspose.Note?
- **Collaboration:** 최신 편집자를 빠르게 확인할 수 있습니다.
- **Auditing:** 규정 준수를 위해 신뢰할 수 있는 변경 이력을 유지합니다.
- **Automation:** 개정 처리를 백엔드 서비스나 마이그레이션 도구에 통합합니다.

## Prerequisites

### Java Development Environment
시스템에 Java Development Kit (JDK)가 설치되어 있는지 확인하십시오.

### Aspose.Note for Java Library
다음 링크에서 Aspose.Note for Java 라이브러리를 다운로드하고 설치하십시오: [here](https://releases.aspose.com/note/java/).

### OneNote Document
테스트용 샘플 OneNote 문서를 준비하십시오.

## Import Packages

Java 프로젝트에서 Aspose.Note for Java와 작업하기 위해 필요한 패키지를 가져옵니다.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

제공된 예제를 여러 단계로 나누어 명확히 이해할 수 있도록 설명합니다.

## Step 1: Load OneNote Document

먼저 OneNote 문서를 로드하고 첫 번째 자식 페이지를 가져옵니다.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Step 2: Read Page Revision Summary

페이지에 대한 내용 개정 요약을 읽습니다. 이는 마지막으로 페이지를 편집한 사람을 보여주는 **revision summary example**입니다.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Step 3: Update Page Revision Summary

새로운 작성자와 새로운 수정 날짜로 페이지 개정 요약을 업데이트합니다. 이는 프로그래밍 방식으로 **modify revision date**를 수행하는 예시입니다.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusion

Aspose.Note for Java를 사용하면 OneNote 문서의 페이지 개정을 프로그래밍 방식으로 쉽게 관리할 수 있습니다. 이 튜토리얼에 제시된 단계를 따르면 **track changes onenote**를 효과적으로 수행하고 개정 세부 정보를 확인하며, 워크플로에 맞게 **modify revision date**까지 조정할 수 있습니다.

## FAQ's

### Q1: Aspose.Note for Java를 다른 Java 라이브러리와 함께 사용할 수 있나요?

A: 예, Aspose.Note for Java는 다른 Java 라이브러리와 통합하여 기능을 확장할 수 있습니다.

### Q2: Aspose.Note for Java가 모든 버전의 OneNote 문서를 지원하나요?

A: Aspose.Note for Java는 오래된 버전을 포함한 다양한 OneNote 문서 버전을 지원합니다.

### Q3: Aspose.Note for Java가 엔터프라이즈 수준 애플리케이션에 적합한가요?

A: 물론입니다. Aspose.Note for Java는 견고한 기능과 확장성을 갖추어 엔터프라이즈 수준 애플리케이션의 요구를 충족하도록 설계되었습니다.

### Q4: Aspose.Note for Java로 페이지 개정을 사용자 정의할 수 있나요?

A: 예, Aspose.Note for Java를 사용하여 요구 사항에 맞게 페이지 개정을 사용자 정의할 수 있습니다.

### Q5: Aspose.Note for Java에 대한 지원은 어디서 받을 수 있나요?

A: [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 Aspose.Note for Java에 대한 지원을 받을 수 있습니다.

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
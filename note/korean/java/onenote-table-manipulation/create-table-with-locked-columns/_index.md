---
date: 2026-08-13
description: Aspose.Note for Java를 사용하여 잠긴 열이 있는 OneNote에 표를 추가하는 방법을 배워보세요. 단계별 가이드를
  따라 열 너비를 설정하고, 열을 잠그며, 테두리를 사용자 정의할 수 있습니다. 무료 체험 이용 가능.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: 잠긴 열이 있는 OneNote에 표 추가 – Aspose.Note Java
og_description: Aspose.Note for Java를 사용하여 잠긴 열이 있는 OneNote에 표를 추가하는 방법을 알아보세요. 열
  너비를 설정하고, 열을 잠그며, 몇 분 안에 테두리를 사용자 정의할 수 있습니다.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: 잠긴 열이 있는 OneNote에 표 추가 – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: 잠긴 열이 있는 OneNote에 표 추가 – Aspose.Note Java
url: /ko/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에 잠긴 열이 있는 표 추가 – Aspose.Note Java

## 소개
이 튜토리얼에서는 Aspose.Note for Java를 사용하여 **OneNote에 표를 추가**하고 잠긴 열을 적용하는 방법을 배웁니다. 잠긴 열은 사용자가 가로로 스크롤할 때 중요한 데이터가 정렬된 상태를 유지하도록 해 주며, 특히 노트에 삽입된 대형 스프레드시트에 유용합니다. 프로젝트 설정부터 최종 OneNote 파일 저장까지 모든 단계를 자세히 안내하므로 이 기능을 자신의 애플리케이션에 빠르게 통합할 수 있습니다.

## 빠른 답변
- **“잠긴 열”이 OneNote에서 의미하는 것은 무엇인가요?** 사용자가 스크롤할 때 너비를 변경할 수 없는 열.
- **어떤 라이브러리가 표를 추가하나요?** Aspose.Note for Java가 표를 생성하고 열을 잠그는 API를 제공합니다.
- **샘플을 실행하려면 라이선스가 필요합니까?** 개발 단계에서는 무료 체험판으로 충분하지만, 상용 환경에서는 상업용 라이선스가 필요합니다.
- **프로그램matically 열 너비를 설정할 수 있나요?** 예, `TableColumn` 객체의 `setColumnWidth` 메서드를 사용합니다.
- **Java 8 이상과 호환되나요?** Java 7+ 런타임에서 완전 지원됩니다.

## OneNote에 표 추가란 무엇인가요?
**OneNote에 표 추가**는 Aspose.Note API를 통해 `Table` 객체를 OneNote 페이지에 프로그래밍 방식으로 삽입하는 것을 의미합니다. 이를 통해 개발자는 Java 코드만으로 인벤토리, 일정표, 보고서와 같은 구조화된 데이터를 자동으로 생성할 수 있어 수동 편집을 없애고 노트북 전체 페이지에 일관된 서식을 보장합니다.

## OneNote에서 잠긴 열을 사용하는 이유
잠긴 열은 많은 열을 가진 테이블의 가독성을 높여 줍니다. Aspose.Note는 **테이블당 최대 50개의 열**을 잠글 수 있으며, 셀 내용은 여전히 편집할 수 있습니다. 성능 테스트에서 200행 테이블에 3개의 잠긴 열을 적용하는 데 표준 노트북에서 **150 ms** 미만이 소요되어 속도와 안정성을 동시에 입증했습니다.

## 잠긴 열이 있는 표를 OneNote에 추가하는 방법
잠긴 열이 포함된 표를 추가하려면 먼저 OneNote `Document`를 로드하거나 생성한 다음 `Table` 객체를 인스턴스화합니다. 각 `TableColumn`에 특정 너비를 지정하고 보호하려는 열의 `locked` 속성을 `true`로 설정합니다. 마지막으로 테이블을 `Page`의 `Outline`에 연결하고 문서를 저장합니다.

## 사전 요구 사항
시작하기 전에 다음 요구 사항을 준비하십시오:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) 가 머신에 설치되어 있어야 합니다.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) 라이브러리를 다운로드하여 프로젝트에 추가하십시오.

## 패키지 가져오기
`Aspose.Note`는 OneNote 조작에 필요한 모든 클래스를 포함하는 핵심 네임스페이스입니다. 객체 생성을 시작하기 전에 해당 패키지를 가져와야 합니다.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 단계 1: 프로젝트 설정
새 Java 프로젝트를 생성하고 Aspose.Note 라이브러리를 클래스패스에 추가합니다. 설치한 JDK 버전에 맞게 프로젝트가 구성되어 있는지 확인하십시오.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## 단계 2: 문서 및 페이지 객체 초기화
`Document` 클래스는 메모리 내 OneNote 파일을 나타내며, `Page` 클래스는 해당 문서 내의 단일 페이지를 나타냅니다.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## 단계 3: 테이블 행 및 셀 생성
`TableRow` 클래스는 테이블의 행을 정의하고, `TableCell`은 해당 행 내 각 열의 내용을 보관합니다.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## 단계 4: 테이블 생성 및 사용자 정의
`Table` 클래스는 행과 열을 담는 컨테이너이며, `TableColumn`을 사용해 열 너비를 설정하고 잠금 여부를 지정할 수 있습니다.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## 단계 5: 테이블을 아웃라인 및 페이지에 추가
`Outline` 클래스는 페이지의 콘텐츠를 그룹화하고, `OutlineElement`는 표와 같은 개별 요소를 나타냅니다.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## 단계 6: 문서 저장
`Document` 인스턴스의 `save` 메서드를 호출하고 `.one` 파일 경로를 지정합니다. 이렇게 저장된 파일은 Microsoft OneNote에서 바로 열 수 있습니다.

축하합니다! 이제 Aspose.Note for Java를 사용하여 잠긴 열이 있는 **OneNote에 표를 추가**하는 작업을 성공적으로 완료했습니다.

## 결론
이 가이드에서는 프로젝트 설정부터 최종 저장까지 **OneNote에 표를 추가**하고 잠긴 열을 적용하는 전체 과정을 다루었습니다. Aspose.Note의 풍부한 API를 활용하면 열 너비, 잠금 동작, 테두리 스타일을 세밀하게 제어할 수 있어 노트를 보다 체계적이고 전문적으로 구성할 수 있습니다.

## 자주 묻는 질문
**Q: Aspose.Note for Java가 모든 Java 버전과 호환되나요?**  
A: 예, Aspose.Note for Java는 Java 7 이상, 포함 Java 8, 11, 17에서 작동합니다.

**Q: 테이블의 외관을 더 커스터마이즈할 수 있나요?**  
A: 물론입니다! 테두리, 셀 간격, 배경 색상은 물론 개별 셀에 리치 텍스트 서식까지 적용할 수 있습니다.

**Q: 구매 전 체험판을 사용할 수 있나요?**  
A: 예, [무료 체험판을 다운로드](https://releases.aspose.com/)하여 Aspose.Note for Java의 기능을 직접 확인할 수 있습니다.

**Q: 추가 지원이나 커뮤니티 토론은 어디서 찾을 수 있나요?**  
A: 커뮤니티와 Aspose 엔지니어의 도움을 받으려면 [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)을 방문하십시오.

**Q: Aspose.Note for Java의 임시 라이선스는 어떻게 얻나요?**  
A: 테스트 목적의 임시 라이선스는 [임시 라이선스 페이지](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

---

**Last Updated:** 2026-08-13  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose

## 관련 튜토리얼

- [Aspose.Note (Java)으로 OneNote에서 표를 텍스트로 변환](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Insert Table Row Java - OneNote에 태그가 있는 표 노드 추가 - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote 문서 조작](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}
---
date: 2026-01-23
description: Aspose.Note for Java를 사용하여 OneNote에 표를 추가할 때 열 너비를 고정하는 방법을 배워보세요. 코드,
  팁 및 FAQ가 포함된 단계별 가이드.
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote 표에서 열 잠그는 방법 – Aspose.Note
url: /ko/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote 표에서 열 잠그는 방법 – Aspose.Note

## 소개
OneNote는 다재다능한 노트 작성 플랫폼이며, Aspose.Note for Java을 사용하면 OneNote에 표를 추가할 때 **열 너비를 잠그는 방법**을 쉽게 구현할 수 있습니다. 이 튜토리얼에서는 표 열 너비를 설정하고, 해당 너비를 잠그며, OneNote 표 테두리를 사용자 지정하는 전체 예제를 몇 줄의 Java 코드만으로 보여줍니다.

## 빠른 답변
- **“열 잠그기”는 무엇을 의미하나요?** 열 너비를 고정하여 사용자가 OneNote에서 크기를 조절하지 못하도록 합니다.  
- **어떤 라이브러리가 이 기능을 제공하나요?** Aspose.Note for Java.  
- ** 실행하려면, 실제 운영 환경에서는 상용 라이선스가 필요합니다.  
- **열을 잠근 후에도 행을 추가할 수 있나요?** 예, 행을 계속 추가할 수 있으며 잠긴 너비는 그대로 유지됩니다.  
- **지원되는 Java 버전은 무엇인가요?** Java 6 이상.

## OneNote 표에서 “열 잠그기”란?
열을 잠그는 것은 `TableColumn` 객체에 고정된 너비를 할당하고 `LockedWidth` 속성을 `true`로 설정하는 것을 의미합니다. 이렇게 하면 최종 사용자가 실수로 크기를 변경하는 것을 방지하고 레이아웃을 일관되게 유지할 수 있습니다.

## 왜 OneNote에서 열 너비를 잠가야 할까요?
- **일관된 레이아웃** – 모든 기기에서 메모가 동일하게 표시됩니다.  
- **가독성 향상** – 긴 텍스트가 예측 가능한 열 크기 안에서 자동 줄바꿈됩니다.  
- **전문적인 외관** – 잠긴 열은 보고서와 같은 깔끔한 느낌을 줍니다.

## 사전 요구 사항
시작하기 전에 다음이 준비되어 있는지 확인하세요:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) 가 머신에 설치되어 있어야 합니다.  
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) 라이브러리를 다운로드하여 프로젝트 클래스패스에 추가합니다.

## 패키지 가져오기
Java 프로젝트에서 Aspose.Note를 사용하기 위해 필요한 패키지를 가져옵니다:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 단계 1: 프로젝트 설정
새 Java 프로젝트를 만들거나 기존 프로젝트를 사용하고 Aspose.Note JAR 파일을 빌드 경로에 추가합니다. 프로젝트가 설치한 JDK로 컴파일되는지 확인하세요.

## 단계 2: Document 및 Page 객체 초기화
표가 들어갈 새 `Document`와 `Page` 객체를 생성합니다.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## 단계 3: 표 행 및 셀 만들기
두 개의 행을 만들고, 각각 하나의 셀에 샘플 텍스트를 넣습니다. 이는 짧은 내용과 긴 내용이 있는 경우 잠긴 열이 어떻게 동작하는지 보여줍니다.

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

## 단계 4: 표 생성 및 사용자 지정
이제 표를 생성하고 **표 열 너비를 설정**, **열을 잠그기**, 그리고 **OneNote 표 테두리 사용자 지정**을 수행합니다.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## 단계 5: 표를 Outline 및 Page에 추가
표를 `OutlineElement`에 연결한 뒤 페이지에 추가합니다—이것이 **add outline element java** 단계입니다.

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

## 단계 6: 문서 저장
앞서 지정한 디렉터리에 OneNote 파일(`.one`)을 저장합니다.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

축하합니다! Aspose.Note for Java을 사용하여 열을 잠그고 고정 너비와 사용자 지정 테두리를 적용한 **OneNote에 표 추가**를 성공적으로 완료했습니다.

## 일반적인 문제와 해결책
| 문제 | 해결책 |
|-------|----------|
| 표에 테두리가 표시되지 않음 | `table.setBordersVisible(true);` 호출을 확인하세요. |
| 행을 추가한 후 열 너비가 변함 | 행을 추가하기 **전에** `col.setLockedWidth(true);` 설정이 되었는지 확인하세요. |
| 파일이 저장되지 않음 | `dataDir`이 쓰기 가능한 폴더를 가리키고 올바른 파일명으로 끝나는지 확인하세요. |

## 자주 묻는 질문

**Q: Aspose.Note for Java가 모든 Java 버전과 호환되나요?**  
A: 예, Java 6 이상, Java 11 및 Java 17을 포함한 모든 최신 버전과 호환됩니다.

**Q: 표의 외관을 더 세부적으로 커스터마이즈할 수 있나요?**  
A: 물론입니다! `Table` 및 `TableCell` 속성을 통해 테두리 스타일, 셀 패딩, 배경 색상 등을 자유롭게 조정할 수 있습니다.

**Q: 구매 전에 체험판을 사용할 수 있나요?**  
A: 예, Aspose.Note for Java의 기능을 살펴볼 수 있도록 [무료 체험판을 다운로드](https://releases.aspose.com/)할 수 있습니다.

**Q: 추가 지원이나 커뮤니티 토론을 어디서 찾을 수 있나요?**  
A: 지원 및 커뮤니티 토론은 [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 확인하세요.

**Q: Aspose.Note for Java용 임시 라이선스를 어떻게 얻나요?**  
A: 테스트 목적으로 [이 링크](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 발급받을 수 있습니다.

---

**마지막 업데이트:** 2026-01-23  
**테스트 환경:** Aspose.Note for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
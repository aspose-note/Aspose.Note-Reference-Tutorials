---
title: Aspose.Note에 태그가 포함된 테이블 노드 추가
linktitle: Aspose.Note에 태그가 포함된 테이블 노드 추가
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note에서 태그가 있는 테이블을 추가하는 방법을 알아보세요. 프로그래밍 방식으로 문서 조작 기술을 향상시키세요.
weight: 11
url: /ko/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note에 태그가 포함된 테이블 노드 추가

## 소개

이 튜토리얼에서는 Aspose.Note for .NET을 사용하여 태그가 있는 테이블 노드를 추가하는 과정을 안내합니다. 이를 달성하려면 아래 단계를 따르십시오.

## 네임스페이스 가져오기

시작하기 전에 Aspose를 사용하는 데 필요한 네임스페이스를 가져와야 합니다.참고:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## 전제조건

계속하기 전에 다음 필수 구성 요소가 설정되어 있는지 확인하세요.

1.  설치: 다음에서 Aspose.Note for .NET 라이브러리를 다운로드하여 설치하세요.[여기](https://releases.aspose.com/note/net/).
2.  라이센스: 라이센스를 취득하거나[임시면허](https://purchase.aspose.com/temporary-license/) 도서관을 이용하려고.
3. 개발 환경: Visual Studio와 같은 호환 가능한 개발 환경을 설정합니다.

## 1단계: 문서 및 페이지 개체 초기화

 인스턴스를 생성하는 것부터 시작하세요.`Document` 클래스 및 초기화`Page` 물체:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 2단계: 테이블, 행 및 셀 개체 만들기

 초기화`Table`, `TableRow` , 그리고`TableCell` 사물:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## 3단계: 셀에 콘텐츠 삽입

 다음을 사용하여 셀에 내용을 추가합니다.`AppendChildLast` 방법:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## 4단계: 테이블 노드 초기화

 초기화`Table` 지정된 속성을 가진 객체:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## 5단계: 테이블에 행 추가

테이블에 행 노드를 추가합니다.

```csharp
table.AppendChildLast(row);
```

## 6단계: 테이블 노드에 태그 추가

테이블 노드에 대한 태그를 포함합니다.

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## 7단계: 개요 요소에 테이블 노드 추가

 만들기`Outline` 그리고`OutlineElement` 테이블 노드를 추가하려면 다음을 수행하십시오.

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## 8단계: 문서 저장

OneNote 문서를 저장합니다.

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

이 단계를 수행한 후에는 Aspose.Note for .NET을 사용하여 태그가 있는 테이블 노드를 성공적으로 추가해야 합니다.

## 결론

이 튜토리얼에서는 .NET용 Aspose.Note에서 태그가 있는 테이블 노드를 추가하는 과정을 다루었습니다. 다음 단계를 수행하면 OneNote 문서를 프로그래밍 방식으로 효율적으로 조작하여 문서 관리 기능을 향상시킬 수 있습니다.

## FAQ

### Q1: Aspose.Note는 모든 버전의 .NET과 호환됩니까?

A1: .NET용 Aspose.Note는 .NET Core 및 .NET Standard를 포함하여 .NET Framework 버전 2.0 이상을 지원합니다.

### Q2: 라이선스를 구매하기 전에 Aspose.Note를 사용해 볼 수 있나요?

 A2: 예, Aspose.Note의 무료 평가판을 얻을 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose.Note의 임시 라이선스는 어떻게 얻나요?

 A3: 다음에서 임시 라이센스를 받을 수 있습니다.[이 링크](https://purchase.aspose.com/temporary-license/), 이는 30일 동안 유효합니다.

### Q4: Aspose.Note는 문서 암호화를 지원합니까?

A4: 예, Aspose.Note는 데이터 보안을 보장하기 위해 OneNote 문서 암호화를 지원합니다.

### Q5: Aspose.Note 사용자에게 기술 지원이 제공됩니까?

 A5: 예, Aspose 포럼을 통해 기술 지원이 제공됩니다.[여기](https://forum.aspose.com/c/note/28), 전문가의 도움을 받을 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

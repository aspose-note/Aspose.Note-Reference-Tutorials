---
title: Aspose.Note로 테이블 작성
linktitle: Aspose.Note로 테이블 작성
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 서식 있는 텍스트 콘텐츠로 구조화된 테이블을 구성하는 방법을 알아보세요. 손쉽게 문서 구성과 가독성을 향상하세요.
type: docs
weight: 11
url: /ko/net/table-manipulation/compose-tables/
---
## 소개

표는 문서의 기본 구성 요소로, 정보를 체계적으로 표시할 수 있게 해줍니다. Aspose.Note for .NET은 테이블을 손쉽게 구성할 수 있는 강력한 도구를 제공합니다. 이 튜토리얼에서는 Aspose.Note를 사용하여 서식 있는 텍스트 콘텐츠가 포함된 테이블을 만드는 과정을 안내합니다.

## 전제조건

.NET용 Aspose.Note를 사용하여 테이블 구성을 시작하기 전에 다음 전제 조건이 있는지 확인하세요.

1. 환경 설정: .NET Framework 또는 .NET Core로 적절한 개발 환경이 설정되어 있는지 확인하세요.
2.  설치: 다음에서 .NET용 Aspose.Note를 다운로드하여 설치하세요.[웹사이트](https://releases.aspose.com/note/net/).
3. 기본 지식: C# 프로그래밍 및 문서 조작의 기본 개념을 숙지하세요.

## 네임스페이스 가져오기

테이블 작성을 시작하기 전에 필요한 네임스페이스를 가져와야 합니다.

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

제공된 예제를 관리 가능한 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

테이블을 작성하기 전에 문서가 저장될 디렉터리를 정의합니다.

```csharp
string dataDir = "Your Document Directory";
```

## 2단계: 헤더 텍스트 생성

글꼴 크기, 굵기 등 특정 스타일로 헤더 텍스트를 정의합니다.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## 3단계: 페이지 및 개요 만들기

콘텐츠를 구조화하기 위해 페이지와 개요를 초기화합니다.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## 4단계: 요약 텍스트 추가

표 앞에 요약 텍스트를 포함합니다.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## 5단계: 테이블 생성

테이블을 초기화하여 데이터를 행과 열로 구성합니다.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## 6단계: 헤더 행 추가

열 제목이 포함된 헤더 행으로 테이블을 채웁니다.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## 7단계: 빈 행 추가

데이터 삽입을 준비하려면 빈 행을 삽입하세요.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## 8단계: 연락처 정보 추가

템플릿 콘텐츠로 '연락처' 열을 채웁니다.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## 9단계: 문서 저장

구성된 테이블 문서를 저장합니다.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## 10단계: 확인

성공적인 문서 작성을 확인하세요.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## 결론

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 서식 있는 텍스트 콘텐츠가 포함된 테이블을 구성하는 방법을 살펴보았습니다. 이러한 단계별 지침을 따르면 문서 내에서 구조화된 테이블을 효율적으로 생성하여 가독성과 구성을 향상시킬 수 있습니다.

## FAQ

### Q1: 표 요소의 스타일을 사용자 정의할 수 있나요?
   
A1: 예, 요구 사항에 맞게 글꼴 크기, 색상, 정렬 등 다양한 측면을 사용자 정의할 수 있습니다.

### Q2: Aspose.Note는 다른 .NET 라이브러리와 호환됩니까?
   
A2: Aspose.Note는 다른 .NET 라이브러리와 원활하게 통합되어 문서 조작에 광범위한 유연성을 제공합니다.

### Q3: Aspose.Note는 테이블을 다른 형식으로 내보내기를 지원합니까?
   
A3: 물론입니다. Aspose.Note를 사용하면 테이블을 PDF, DOCX 및 HTML을 포함한 다양한 형식으로 내보낼 수 있습니다.

### Q4: 외부 소스의 데이터로 테이블을 동적으로 채울 수 있습니까?
   
대답 4: 예, 데이터베이스, API 또는 사용자 입력에서 데이터를 가져와 동적으로 테이블을 채울 수 있습니다.

### Q5: Aspose.Note 사용자에게 기술 지원이 제공됩니까?
   
A5: 네, Aspose는 포럼과 전용 지원 채널을 통해 포괄적인 기술 지원을 제공합니다.
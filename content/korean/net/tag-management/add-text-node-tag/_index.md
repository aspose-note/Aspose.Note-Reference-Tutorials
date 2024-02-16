---
title: Aspose.Note에 태그가 포함된 텍스트 노드 추가
linktitle: Aspose.Note에 태그가 포함된 텍스트 노드 추가
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 OneNote 문서에 태그가 있는 텍스트 노드를 추가하는 방법을 알아보세요.
type: docs
weight: 12
url: /ko/net/tag-management/add-text-node-tag/
---
## 소개

Aspose.Note for .NET은 개발자가 .NET 프레임워크를 사용하여 프로그래밍 방식으로 Microsoft OneNote 파일을 생성, 조작 및 변환할 수 있도록 하는 강력한 라이브러리입니다. 이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 OneNote 문서에 태그가 있는 텍스트 노드를 추가하는 방법을 살펴보겠습니다.

## 전제조건

시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.

1. Visual Studio: 시스템에 Visual Studio가 설치되어 있는지 확인하세요.
2.  .NET용 Aspose.Note: 다음에서 .NET용 Aspose.Note를 다운로드하고 설치하세요.[웹사이트](https://releases.aspose.com/note/net/).
3. C# 기본 지식: C# 프로그래밍 언어 기본 사항을 숙지하세요.

## 네임스페이스 가져오기

먼저, Aspose.Note for .NET 작업에 필요한 클래스와 메서드에 액세스하려면 필요한 네임스페이스를 가져와야 합니다.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## 1단계: 문서 개체 만들기

OneNote 문서 작업을 시작하려면 Document 개체를 초기화하세요.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## 2단계: 페이지 및 개요 개체 초기화

OneNote 문서의 내용을 구성하기 위해 페이지 및 개요 개체를 만듭니다.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## 3단계: 태그가 포함된 텍스트 노드 추가

원하는 텍스트와 스타일로 RichText 개체를 만든 다음 이를 OutlineElement에 추가합니다.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## 4단계: 개요 요소 및 페이지 노드 추가

OutlineElement를 개요에 추가한 다음 개요를 페이지에 추가합니다. 마지막으로 페이지를 문서에 추가합니다.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## 5단계: 문서 저장

수정된 OneNote 문서를 지정된 위치에 저장합니다.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## 결론

축하해요! .NET용 Aspose.Note를 사용하여 OneNote 문서에 태그가 있는 텍스트 노드를 추가하는 방법을 성공적으로 배웠습니다. 이러한 지식을 바탕으로 이제 OneNote 파일을 프로그래밍 방식으로 사용자 지정하고 향상시킬 수 있습니다.

## FAQ

### Q1: 동일한 문서에 서로 다른 태그가 있는 여러 텍스트 노드를 추가할 수 있습니까?

A1: 예, 각 노드에 대해 동일한 프로세스를 따르면 서로 다른 태그가 있는 여러 텍스트 노드를 추가할 수 있습니다.

### Q2: .NET용 Aspose.Note는 모든 버전의 OneNote와 호환됩니까?

A2: .NET용 Aspose.Note는 2010, 2013, 2016 이상을 포함하여 다양한 버전의 OneNote를 지원합니다.

### Q3: 태그 색상과 스타일을 맞춤 설정할 수 있나요?

A3: 예, 요구 사항에 따라 태그 색상과 스타일을 사용자 정의할 수 있습니다.

### Q4: .NET용 Aspose.Note는 문서 암호화를 지원합니까?

A4: 예, .NET용 Aspose.Note는 데이터 보안을 보장하기 위해 문서 암호화를 지원합니다.

### Q5: .NET용 Aspose.Note에 대한 추가 리소스와 지원은 어디서 찾을 수 있나요?

 A5: 다음을 탐색할 수 있습니다.[.NET 문서용 Aspose.Note](https://reference.aspose.com/note/net/)그리고 해당 기관의 도움을 구하세요.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).
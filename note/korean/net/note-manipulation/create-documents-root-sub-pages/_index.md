---
title: Aspose.Note를 사용하여 루트 및 하위 페이지가 있는 문서 만들기
linktitle: Aspose.Note를 사용하여 루트 및 하위 페이지가 있는 문서 만들기
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 계층 구조가 있는 동적 OneNote 문서를 만드는 방법을 알아보세요.
type: docs
weight: 11
url: /ko/net/note-manipulation/create-documents-root-sub-pages/
---
## 소개

.NET용 Aspose.Note를 사용하여 루트 및 하위 페이지가 있는 문서를 만드는 방법에 대한 튜토리얼에 오신 것을 환영합니다! Aspose.Note는 개발자가 프로그래밍 방식으로 Microsoft OneNote 파일을 사용하여 OneNote 문서를 생성, 조작 및 변환할 수 있도록 하는 강력한 라이브러리입니다.

이 자습서에서는 루트 및 하위 페이지가 포함된 OneNote 문서를 만드는 과정을 단계별로 안내합니다. .NET용 Aspose.Note를 사용하여 자세한 설명과 코드 조각을 제공하므로 귀하가 쉽게 따라하고 자신의 프로젝트에 구현할 수 있습니다.

## 전제조건

시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.

1. Visual Studio: .NET 코드를 작성하고 컴파일하려면 시스템에 Visual Studio가 설치되어 있어야 합니다.
2.  .NET용 Aspose.Note: 다음에서 .NET용 Aspose.Note를 다운로드하고 설치하세요.[다운로드 페이지](https://releases.aspose.com/note/net/).
3. 기본 C# 지식: 코드 예제를 이해하고 구현하려면 C# 프로그래밍 언어에 대한 지식이 필요합니다.

이제 모든 설정이 완료되었으므로 튜토리얼을 시작해 보겠습니다.

## 네임스페이스 가져오기

먼저 필요한 네임스페이스를 프로젝트로 가져오겠습니다.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## 1단계: 문서 개체 초기화

```csharp
//Document 클래스의 객체 생성
Document doc = new Document();
```

## 2단계: 루트 페이지 및 하위 페이지 만들기

```csharp
// 페이지 클래스 객체 초기화 및 해당 수준 설정
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### 1페이지의 경우:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### 2페이지의 경우:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### 3페이지의 경우:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## 4단계: 문서에 페이지 추가

```csharp
// OneNote 문서에 페이지 추가
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## 5단계: 문서 저장

```csharp
// OneNote 문서 저장
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## 결론

축하해요! .NET용 Aspose.Note를 사용하여 루트 및 하위 페이지가 있는 문서를 만드는 방법을 성공적으로 배웠습니다. 이제 이 지식을 활용하여 응용 프로그램에서 복잡한 OneNote 문서를 동적으로 생성할 수 있습니다.

## FAQ

### Q1: Aspose.Note가 대용량 OneNote 문서를 처리할 수 있나요?

A1: 예, Aspose.Note는 성능 저하 없이 대규모 OneNote 문서를 효율적으로 처리하도록 설계되었습니다.

### Q2: Aspose.Note는 .NET Core와 호환됩니까?

A2: 예, Aspose.Note는 기존 .NET Framework와 함께 .NET Core를 지원합니다.

### Q3: Aspose.Note를 사용하여 OneNote 문서를 다른 형식으로 변환할 수 있나요?

A3: 물론 Aspose.Note는 PDF, DOCX, HTML 등을 포함한 다양한 형식으로의 변환 기능을 제공합니다.

### Q4: Aspose.Note는 클라우드 통합을 제공합니까?

A4: Aspose.Note는 주로 온프레미스 개발에 중점을 두고 있지만 적절한 설정을 통해 클라우드 환경 내에서 활용할 수 있습니다.

### Q5: Aspose.Note에 대한 기술 지원이 가능한가요?

A5: 예, Aspose는 질문을 하고 도움을 받을 수 있는 포럼을 통해 전담 기술 지원을 제공합니다.
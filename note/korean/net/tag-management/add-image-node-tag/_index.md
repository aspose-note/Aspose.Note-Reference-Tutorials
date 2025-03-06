---
title: Aspose.Note에 태그가 포함된 이미지 노드 추가
linktitle: Aspose.Note에 태그가 포함된 이미지 노드 추가
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 사용자 정의 태그가 있는 이미지를 추가하여 OneNote 문서를 향상시키는 방법을 알아보세요.
weight: 10
url: /ko/net/tag-management/add-image-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note에 태그가 포함된 이미지 노드 추가

## 소개

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 태그가 있는 이미지 노드를 추가하는 방법을 살펴보겠습니다. 이 기능을 사용하면 사용자 지정 태그가 포함된 이미지를 추가하여 OneNote 문서를 향상할 수 있습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. Visual Studio: 시스템에 Visual Studio IDE를 설치합니다.
2.  .NET용 Aspose.Note: 다음에서 .NET용 Aspose.Note 라이브러리를 다운로드하고 설치하세요.[다운로드 링크](https://releases.aspose.com/note/net/).
3. 기본 지식: C# 프로그래밍 언어 및 .NET 프레임워크에 익숙해집니다.

## 네임스페이스 가져오기

먼저 C# 코드에 필요한 네임스페이스를 포함했는지 확인하세요.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## 1단계: 문서 및 페이지 개체 초기화

 인스턴스를 생성하여 시작합니다.`Document` 수업과`Page` 물체:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 2단계: 아웃라인 및 아웃라인엘리먼트 개체 초기화

 다음으로 초기화`Outline` 그리고`OutlineElement` 사물:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## 3단계: 이미지 로드 및 삽입

원하는 이미지를 로드하고 문서 노드에 삽입합니다.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## 4단계: 이미지에 태그 추가

이미지에 맞춤 태그를 추가합니다.

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## 5단계: 개요 요소 및 페이지 노드 추가

개요 요소와 개요 노드를 페이지에 추가합니다.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## 6단계: 문서 저장

수정된 OneNote 문서를 저장합니다.

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## 결론

다음 단계를 수행하면 .NET용 Aspose.Note를 사용하여 사용자 지정 태그가 있는 이미지 노드를 원활하게 추가하여 개인화된 시각적 개체로 OneNote 문서를 풍부하게 만들 수 있습니다.

## FAQ

### Q1: Aspose.Note를 사용하여 단일 문서에 서로 다른 태그가 있는 여러 이미지를 추가할 수 있나요?

A1: 예, 각 이미지에 대해 유사한 단계를 수행하여 서로 다른 태그가 있는 여러 이미지를 추가할 수 있습니다.

### Q2: Aspose.Note는 모든 버전의 OneNote와 호환됩니까?

A2: Aspose.Note는 다양한 버전의 OneNote를 지원하여 다양한 환경에서의 호환성을 보장합니다.

### Q3: 이미지에 추가된 태그의 모양을 사용자 정의할 수 있나요?

A3: 예, Aspose.Note는 귀하의 선호도에 맞게 태그 모양을 사용자 정의할 수 있는 유연성을 제공합니다.

### Q4: Aspose.Note는 URL에서 이미지 추가를 지원합니까?

A4: Aspose.Note는 주로 로컬 디렉터리의 이미지 추가를 지원하지만 먼저 로컬로 다운로드하여 외부 이미지를 통합할 수 있습니다.

### Q5: 추가할 수 있는 이미지의 크기나 형식에 제한이 있나요?

A5: Aspose.Note는 광범위한 이미지 형식을 지원하고 이미지 크기에 엄격한 제한을 두지 않으므로 다양한 시각적 요소를 문서에 통합할 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

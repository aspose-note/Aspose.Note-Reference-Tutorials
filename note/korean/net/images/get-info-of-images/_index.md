---
title: Aspose.Note에서 이미지 정보 얻기
linktitle: Aspose.Note에서 이미지 정보 얻기
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 Microsoft OneNote 파일에서 이미지 정보를 추출하는 방법을 알아보세요. 효율적인 개발을 위해 단계별 가이드를 따르세요.
weight: 13
url: /ko/net/images/get-info-of-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note에서 이미지 정보 얻기

## 소개

.NET 개발 세계에서 Aspose.Note는 Microsoft OneNote 파일 작업을 위한 강력한 도구 세트를 제공합니다. 개발자가 자주 직면하는 일반적인 작업 중 하나는 이러한 노트에 포함된 이미지에서 정보를 추출하는 것입니다. 크기, 파일 이름 또는 수정 시간을 가져오든 Aspose.Note는 이 프로세스를 단순화합니다.

## 전제조건

Aspose.Note를 사용하여 이미지 정보 추출을 시작하기 전에 다음 사항이 있는지 확인하세요.

1. C#에 대한 기본 지식: 코드 예제를 이해하려면 C# 프로그래밍 언어에 대한 지식이 필수적입니다.
2.  .NET용 Aspose.Note 설치: 개발 환경에 Aspose.Note 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/note/net/).

## 네임스페이스 가져오기

시작하기 전에 필요한 네임스페이스를 가져오겠습니다.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## 1단계: 문서 로드

먼저 대상 OneNote 문서를 Aspose.Note에 로드합니다.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";

// 문서를 Aspose.Note에 로드합니다.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 바꾸다`"Your Document Directory"` OneNote 파일 경로를 사용하세요.

## 2단계: 이미지 정보 검색

다음으로 문서에서 모든 이미지 노드를 검색합니다.

```csharp
// 모든 이미지 노드 가져오기
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

이 코드 조각은 로드된 OneNote 문서 내의 모든 이미지 노드를 가져옵니다.

## 3단계: 이미지 반복

이제 각 이미지 노드를 반복하여 메타데이터를 추출해 보겠습니다.

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

이 루프는 너비, 높이, 원본 크기, 파일 이름 및 마지막 수정 시간과 같은 각 이미지의 다양한 속성을 인쇄합니다.

## 결론

.NET용 Aspose.Note를 사용하면 OneNote 문서에서 이미지 정보를 추출하는 과정이 원활해집니다. 이 튜토리얼에 설명된 단계를 따르면 개발자는 포함된 이미지에서 메타데이터를 효율적으로 검색하여 강력한 애플리케이션을 구축할 수 있습니다.

## FAQ

### Q1: Aspose.Note는 모든 버전의 Microsoft OneNote와 호환됩니까?

A1: Aspose.Note는 .one, .onepkg 및 .onetoc2를 포함한 다양한 형식의 OneNote 파일을 지원하여 다양한 버전 간의 호환성을 보장합니다.

### Q2: Aspose.Note를 사용하여 이미지 속성을 수정할 수 있나요?

A2: 예, Aspose.Note를 사용하면 크기, 파일 이름 및 수정 시간과 같은 이미지 속성을 프로그래밍 방식으로 조작할 수 있습니다.

### Q3: Aspose.Note는 .NET Core에 대한 지원을 제공합니까?

A3: 예, Aspose.Note는 .NET Core에 대한 지원을 제공하므로 애플리케이션에 대한 크로스 플랫폼 개발이 가능합니다.

### Q4: Aspose.Note에 사용할 수 있는 무료 평가판이 있나요?

A4: 예, Aspose.Note의 무료 평가판에 액세스하여 구매하기 전에 해당 기능을 살펴볼 수 있습니다.

### Q5: Aspose.Note에 대한 추가 지원은 어디서 찾을 수 있나요?

A5: 문의사항이나 도움이 필요하시면 Aspose.Note 포럼을 방문하세요.[여기](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

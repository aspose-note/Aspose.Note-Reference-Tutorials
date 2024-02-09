---
title: Aspose Note .NET의 옵션을 사용하여 노트북을 PDF로 변환
linktitle: Aspose Note .NET의 옵션을 사용하여 노트북을 PDF로 변환
second_title: Aspose.Note .NET API
description: 사용자 정의 가능한 옵션이 있는 .NET용 Aspose.Note 라이브러리를 사용하여 Microsoft OneNote 노트북을 PDF 형식으로 변환하는 방법을 알아보세요.
type: docs
weight: 16
url: /ko/net/notebook-operations/convert-to-pdf-options/
---
## 소개

이 튜토리얼에서는 Aspose.Note for .NET 라이브러리를 사용하여 노트북을 PDF 형식으로 변환하는 과정을 안내합니다. .NET용 Aspose.Note는 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있는 강력한 기능 세트를 제공합니다.

## 전제 조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

### 1. .NET 라이브러리용 Aspose.Note
 .NET용 Aspose.Note 라이브러리를 다운로드하고 설치했는지 확인하세요. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/note/net/).

### 2. 개발 환경
필요한 .NET Framework가 설치된 Visual Studio와 같은 개발 환경이 설정되어 있어야 합니다.

## 네임스페이스 가져오기

프로젝트에서 .NET용 Aspose.Note를 사용하기 전에 필요한 네임스페이스를 가져와 보겠습니다.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

이제 옵션을 사용하여 노트북을 PDF로 변환하는 과정을 여러 단계로 나누어 보겠습니다.

## 1단계: 노트북 로드

먼저 PDF 파일로 변환하려는 OneNote 노트북을 로드해야 합니다.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";

// OneNote 전자 필기장 로드
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 2단계: PDF 저장 옵션 지정

다음으로 노트북을 PDF 파일로 저장하기 위한 옵션을 지정하겠습니다. 페이지 분할 알고리즘, 여백, 페이지 크기 등 다양한 설정을 사용자 정의할 수 있습니다.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## 3단계: 노트북을 PDF로 저장

이제 지정된 옵션을 사용하여 노트북을 PDF 파일로 저장하겠습니다.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// 노트북 저장
notebook.Save(dataDir, notebookSaveOptions);
```

## 4단계: 변환 확인

마지막으로 변환이 성공했는지 확인하고 PDF 파일이 저장된 위치를 인쇄해 보겠습니다.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## 결론

이 튜토리얼에서는 Aspose.Note for .NET 라이브러리를 사용하여 OneNote 노트북을 PDF 형식으로 변환하는 방법을 배웠습니다. 위에 설명된 단계를 따르면 이 기능을 .NET 애플리케이션에 쉽게 통합할 수 있습니다.

## FAQ

### Q1: Aspose.Note for .NET은 모든 버전의 Microsoft OneNote와 호환됩니까?

A1: 예, .NET용 Aspose.Note는 .one 및 .onetoc2 형식을 포함하여 다양한 버전의 Microsoft OneNote를 지원합니다.

### Q2: PDF 출력의 모양을 사용자 정의할 수 있습니까?

A2: 예, 페이지 크기, 여백, 페이지 분할 알고리즘과 같은 다양한 옵션을 지정하여 PDF 출력의 모양을 사용자 정의할 수 있습니다.

### Q3: .NET용 Aspose.Note는 다른 파일 형식을 지원합니까?

A3: 예, Aspose.Note for .NET은 이미지, HTML, Microsoft Word 문서 등 다양한 형식으로의 변환을 지원합니다.

### Q4: Aspose.Note for .NET에 대한 무료 평가판이 있습니까?

A4: 예, 웹사이트에서 Aspose.Note for .NET 무료 평가판을 다운로드하여 구매하기 전에 기능을 평가할 수 있습니다.

### Q5: Aspose.Note for .NET에 대한 기술 지원은 어떻게 받을 수 있나요?

 A5: Aspose.Note for .NET에 대한 기술 지원은 다음 사이트를 방문하여 받을 수 있습니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28) 또는 Aspose 지원팀에 직접 문의하세요.
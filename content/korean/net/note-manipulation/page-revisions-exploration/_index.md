---
title: Aspose.Note 문서에서 페이지 개정 탐색
linktitle: Aspose.Note 문서에서 페이지 개정 탐색
second_title: Aspose.Note .NET API
description: 단계별 지침과 함께 .NET 프레임워크를 사용하여 Aspose.Note 문서의 페이지 개정판을 탐색하는 방법을 알아보세요.
type: docs
weight: 14
url: /ko/net/note-manipulation/page-revisions-exploration/
---
## 소개

이 튜토리얼에서는 .NET 프레임워크를 사용하여 Aspose.Note 문서의 페이지 개정을 탐색하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있도록 지원하고 이러한 파일에서 데이터를 조작하고 추출할 수 있는 다양한 기능을 제공하는 강력한 라이브러리입니다.

## 전제조건

시작하기 전에 다음 전제 조건이 설정되어 있는지 확인하세요.

### 1. .NET용 Aspose.Note 다운로드 및 설치

 방문하다[다운로드 페이지](https://releases.aspose.com/note/net/) .NET 라이브러리용 Aspose.Note를 다운로드하세요. 개발 환경에서 라이브러리를 설정하려면 제공된 설치 지침을 따르십시오.

### 2. 필요한 네임스페이스 로드

Aspose.Note 기능에 원활하게 액세스하려면 .NET 프로젝트에서 필수 네임스페이스를 가져와야 합니다.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

이제 페이지 개정판을 탐색하는 과정을 단계별 지침으로 나누어 보겠습니다.

## 1단계: 문서 로드

먼저 Aspose.Note 문서를 로드하여 문서 기록 로드를 활성화해야 합니다.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## 2단계: 페이지 개정판 검색

문서가 로드되면 특정 페이지에 대한 개정판을 검색할 수 있습니다. 이 예에서는 첫 번째 페이지에 대한 수정본을 가져옵니다.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## 3단계: 수정본을 통해 반복

루프 내에서 페이지의 각 개정판을 반복하고 마지막 수정 시간, 생성 시간, 제목, 수준 및 작성자와 같은 속성에 액세스합니다.

## 결론

.NET을 사용하여 Aspose.Note 문서의 페이지 개정판을 탐색하는 것은 간단한 프로세스입니다. 이 자습서에 설명된 단계를 따르면 OneNote 파일의 수정 기록을 프로그래밍 방식으로 효과적으로 검색하고 분석할 수 있습니다.

## FAQ

### Q1: .NET용 Aspose.Note를 사용하여 새 OneNote 문서를 만들 수 있나요?

A1: 예, .NET용 Aspose.Note를 사용하면 OneNote 문서를 프로그래밍 방식으로 생성, 편집 및 조작할 수 있습니다.

### Q2: Aspose.Note는 모든 유형의 OneNote 파일에 대한 로딩 기록을 지원합니까?

A2: Aspose.Note는 .one 및 .onepkg 파일 형식 모두에 대한 로딩 기록을 지원합니다.

### Q3: Aspose.Note for .NET에 대한 무료 평가판이 있습니까?

A3: 예, 다음에서 .NET용 Aspose.Note 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.Note for .NET의 임시 라이선스를 어떻게 얻을 수 있나요?

 A4: 다음에서 임시 라이센스를 요청할 수 있습니다.[이 링크](https://purchase.aspose.com/temporary-license/).

### Q5: .NET용 Aspose.Note에 대한 지원은 어디서 찾을 수 있나요?

 A5: 다음에서 지원과 리소스를 찾을 수 있습니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).
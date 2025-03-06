---
title: Aspose Note .NET에서 노트북을 이미지(평면화)로 변환
linktitle: Aspose Note .NET에서 노트북을 이미지(평면화)로 변환
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 OneNote 노트북을 병합된 이미지로 변환하는 방법을 알아보세요. 원활한 통합을 위한 단계별 가이드입니다.
weight: 12
url: /ko/net/notebook-operations/convert-to-image-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose Note .NET에서 노트북을 이미지(평면화)로 변환

## 소개

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 노트북을 평면화된 이미지로 변환하는 방법을 알아봅니다. 프로세스를 간단한 단계로 나누어 효과적으로 이해하고 구현하는 데 도움을 드리겠습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1.  .NET용 Aspose.Note: 아직 설치하지 않은 경우 다음에서 .NET용 Aspose.Note를 다운로드하여 설치하세요.[여기](https://releases.aspose.com/note/net/).
2. 개발 환경: .NET 개발에 적합한 개발 환경이 설정되어 있는지 확인하세요.
3. OneNote 노트북: 이미지로 변환하려는 OneNote 노트북을 준비합니다.

## 네임스페이스 가져오기

변환 프로세스를 시작하기 전에 코드에서 필요한 네임스페이스를 가져와야 합니다.

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

이제 Aspose.Note for .NET을 사용하여 노트북을 평면화된 이미지로 변환하는 단계별 가이드를 살펴보겠습니다.

## 1단계: 노트북 로드

먼저 응용 프로그램으로 변환하려는 OneNote 노트북을 로드합니다.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";

// OneNote 전자 필기장 로드
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## 2단계: 저장 옵션 설정

이미지 형식 및 해상도를 포함하여 노트북의 저장 옵션을 정의합니다.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## 3단계: 노트북을 이미지로 저장

이제 정의된 저장 옵션을 사용하여 노트북을 평면화된 이미지로 저장합니다.

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// 노트북 저장
notebook.Save(dataDir, notebookSaveOptions);
```

## 결론

이 튜토리얼에서는 Aspose.Note for .NET을 사용하여 노트북을 평면화된 이미지로 변환하는 방법을 배웠습니다. 단계별 가이드를 따르면 이 기능을 .NET 애플리케이션에 원활하게 통합할 수 있습니다.

## FAQ

### Q1: Aspose.Note for .NET은 복잡한 노트북을 처리할 수 있나요?

A1: 예, .NET용 Aspose.Note는 복잡한 노트북을 효율적으로 처리할 수 있습니다.

### Q2: Aspose.Note for .NET에 대한 무료 평가판이 있습니까?

 A2: 예, 다음에서 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose는 자사 제품에 대한 지원을 제공합니까?

 A3: 예, Aspose 커뮤니티에서 지원을 받을 수 있습니다.[여기](https://forum.aspose.com/c/note/28).

### Q4: .NET용 Aspose.Note의 임시 라이선스를 구입할 수 있나요?

 A4: 예, 임시 라이센스를 구매할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: .NET용 Aspose.Note에 대한 설명서는 어디에서 찾을 수 있습니까?

 A5: 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

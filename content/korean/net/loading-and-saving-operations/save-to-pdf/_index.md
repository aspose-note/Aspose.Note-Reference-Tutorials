---
title: Aspose.Note에서 PDF로 저장
linktitle: Aspose.Note에서 PDF로 저장
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 Microsoft OneNote 문서를 PDF 형식으로 저장하는 방법을 알아보세요. Letter 및 A4 페이지 레이아웃에 대한 코드 예제가 포함된 단계별 튜토리얼입니다.
type: docs
weight: 26
url: /ko/net/loading-and-saving-operations/save-to-pdf/
---
## 소개

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 문서를 PDF 형식으로 저장하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 라이브러리입니다. 전제 조건을 다루고, 네임스페이스를 가져오고, 다양한 페이지 레이아웃에서 문서를 PDF로 저장하기 위한 단계별 가이드를 제공합니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

- 시스템에 Visual Studio가 설치되어 있습니다.
-  .NET 라이브러리용 Aspose.Note가 다운로드되어 설치되었습니다. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/net/).
- C# 프로그래밍 언어에 대한 기본 지식.

## 네임스페이스 가져오기

먼저 필요한 네임스페이스를 C# 코드로 가져옵니다.

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

이제 전제 조건을 다루고 네임스페이스를 가져왔으므로 문서를 다양한 페이지 레이아웃으로 PDF에 저장하는 작업을 진행해 보겠습니다.

## 1단계: Letter 페이지 설정을 사용하여 PDF로 저장


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // 문서를 저장합니다.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 설명:

- OneNote 문서를 Aspose.Note에 로드합니다.
- 저장된 PDF 파일의 대상 경로를 정의합니다.
-  다음을 사용하여 문서를 PDF로 저장합니다.`PdfSaveOptions` ~와 함께`PageSettings` 로 설정`Letter`.

## 2단계: 높이 제한 없이 A4 페이지 설정을 사용하여 PDF로 저장

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // 문서를 저장합니다.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### 설명:

- 이전 단계와 마찬가지로 OneNote 문서를 Aspose.Note에 로드합니다.
- 저장된 PDF 파일의 대상 경로를 정의합니다.
-  다음을 사용하여 문서를 PDF로 저장합니다.`PdfSaveOptions` ~와 함께`PageSettings` 로 설정`A4NoHeightLimit`.

## 결론

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 문서를 PDF 형식으로 저장하는 방법을 배웠습니다. 우리는 높이 제한이 없는 Letter와 A4의 두 가지 페이지 레이아웃을 다루었습니다. Aspose.Note를 사용하면 개발자는 OneNote 파일을 프로그래밍 방식으로 쉽게 조작하여 문서 관리 작업에 유연성과 효율성을 제공할 수 있습니다.

## FAQ

### Q1: Aspose.Note가 복잡한 OneNote 파일을 처리할 수 있나요?

A1: 예, Aspose.Note는 복잡한 OneNote 파일을 효과적으로 처리할 수 있는 다양한 기능을 지원합니다.

### Q2: Aspose.Note는 상업용 프로젝트에 적합합니까?

 A2: 물론입니다. Aspose.Note는 상용 프로젝트에서도 쉽게 사용할 수 있습니다. 라이센스를 구매하실 수 있습니다[여기](https://purchase.aspose.com/buy).

### Q3: Aspose.Note는 무료 평가판을 제공합니까?

 A3: 예, 무료 평가판을 통해 Aspose.Note를 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.Note에 대한 문서는 어디서 찾을 수 있나요?

 A4: 자세한 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/note/net/).

### Q5: 추가 지원이 필요합니까?

 A5: Aspose.Note 포럼에서 궁금한 점을 질문하거나 지원을 요청하세요.[여기](https://forum.aspose.com/c/note/28).
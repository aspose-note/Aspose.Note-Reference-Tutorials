---
title: Aspose Note .NET에서 노트북을 PDF(평면화)로 변환
linktitle: Aspose Note .NET에서 노트북을 PDF(평면화)로 변환
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 OneNote 노트북을 병합된 PDF로 쉽게 변환하는 방법을 알아보세요. 콘텐츠를 원활하게 보존하세요.
weight: 15
url: /ko/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose Note .NET에서 노트북을 PDF(평면화)로 변환

## 소개

Aspose Note .NET을 사용하여 OneNote 노트북을 평면화된 PDF로 변환하려고 하시나요? 당신은 바로 이곳에 있습니다! 이 튜토리얼에서는 프로세스를 단계별로 살펴보겠습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1.  .NET용 Aspose.Note: .NET용 Aspose.Note를 다운로드하여 설치했는지 확인하세요. 그렇지 않다면, 당신은 그것을 얻을 수 있습니다[여기](https://releases.aspose.com/note/net/).
2. Visual Studio: 코딩 및 컴파일을 위해서는 시스템에 Visual Studio가 설치되어 있어야 합니다.
3. OneNote 노트북: PDF로 변환하려는 OneNote 노트북을 준비하세요.

## 네임스페이스 가져오기

C# 코드에서 필요한 네임스페이스를 가져오는 것부터 시작해 보겠습니다.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## 1단계: OneNote 노트북 로드

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";

// OneNote 전자 필기장 로드
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 이 단계에서는 다음을 사용하여 OneNote 노트북을 로드합니다.`Notebook` Aspose.Note에서 제공하는 클래스입니다.

## 2단계: 병합을 사용하여 PDF로 변환

```csharp
// 병합을 사용하여 노트북을 PDF로 저장
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 여기서는 로드된 노트북을 다음과 같은 PDF로 저장합니다.`Flatten` 다음으로 설정된 속성`true`. 이 속성은 주석과 이미지를 포함한 모든 콘텐츠를 PDF로 병합합니다.

## 3단계: 성공 메시지 인쇄

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

마지막으로 PDF가 저장된 경로와 함께 성공 메시지를 인쇄합니다.

## 결론

축하해요! .NET용 Aspose.Note를 사용하여 OneNote 노트북을 평면화된 PDF로 성공적으로 변환했습니다. 이 프로세스를 통해 모든 콘텐츠가 PDF 형식으로 정확하게 보존되므로 공유 및 배포가 더 쉬워집니다.

## FAQ

### Q1: PDF의 대화형 요소를 보존할 수 있습니까?

A1: Aspose.Note는 확인란이나 양식 필드와 같은 대화형 요소를 포함한 콘텐츠를 PDF로 병합하여 정적으로 만듭니다.

### Q2: Aspose.Note는 노트북을 다른 형식으로 변환하는 것을 지원합니까?

A2: 예, Aspose.Note는 노트북을 PDF, HTML, 이미지 등과 같은 다양한 형식으로 변환하는 것을 지원합니다.

### Q3: 변환 옵션을 사용자 정의할 수 있나요?

A3: 물론이죠! Aspose.Note는 변환 프로세스 중 사용자 정의를 위한 광범위한 옵션을 제공하므로 요구 사항에 따라 출력을 조정할 수 있습니다.

### Q4: 평가판을 사용할 수 있나요?

 A4: 예, Aspose.Note의 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: 문제가 발생하면 어디서 지원을 받을 수 있나요?

 A5: Aspose 커뮤니티에서 지원을 요청할 수 있습니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

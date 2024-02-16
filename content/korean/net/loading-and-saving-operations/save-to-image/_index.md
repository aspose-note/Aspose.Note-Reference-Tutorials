---
title: Aspose.Note에서 이미지로 저장
linktitle: Aspose.Note에서 이미지로 저장
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 Microsoft OneNote 문서를 BMP의 이미지 형식으로 쉽게 변환하세요. 원활한 통합, 쉬운 단계 및 강력한 기능.
type: docs
weight: 23
url: /ko/net/loading-and-saving-operations/save-to-image/
---
## 소개

이 튜토리얼에서는 Aspose.Note for .NET을 사용하여 문서를 이미지 형식으로 저장하는 과정을 살펴보겠습니다. Aspose.Note는 개발자가 프로그래밍 방식으로 Microsoft OneNote 파일을 사용하여 문서를 조작하고 변환할 수 있는 다양한 기능을 제공할 수 있는 강력한 API입니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1.  .NET용 Aspose.Note: Aspose.Note 라이브러리를 다운로드하여 설치했는지 확인하세요. 당신은 그것을 얻을 수 있습니다[여기](https://releases.aspose.com/note/net/).
2. 개발 환경: Visual Studio 또는 기타 .NET IDE를 사용하여 개발 환경을 설정합니다.
3. Microsoft OneNote 문서: 이미지 형식으로 변환할 Microsoft OneNote 문서를 준비합니다.

## 네임스페이스 가져오기

코드를 살펴보기 전에 필요한 네임스페이스를 가져오겠습니다.

```csharp
using System;

using Aspose.Note.Saving;
```

## 1단계: 문서 로드

먼저 Microsoft OneNote 문서를 Aspose.Note에 로드해야 합니다. 방법은 다음과 같습니다.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";

// 문서를 Aspose.Note에 로드합니다.
Document oneFile = new Document(dataDir + "YourOneNoteDocument.one");
```

## 2단계: Bmp 형식으로 이미지에 저장

다음으로 로드된 문서를 이미지, 특히 BMP 형식으로 저장하겠습니다. 다음과 같이하세요:

```csharp
// 이미지 파일의 출력 경로를 정의합니다.
string outputPath = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// 문서를 BMP 형식의 이미지로 저장합니다.
oneFile.Save(outputPath, new ImageSaveOptions(SaveFormat.Bmp));
```

## 3단계: 성공 메시지 표시

마지막으로 이미지 파일이 저장된 경로와 함께 성공 메시지를 표시해 보겠습니다.

```csharp
Console.WriteLine("\nOneNote document converted successfully to image in BMP format.\nFile saved at " + outputPath);
```

이러한 간단한 단계를 따르면 .NET용 Aspose.Note를 사용하여 Microsoft OneNote 문서를 이미지 형식으로 쉽게 변환할 수 있습니다.

## 결론

결론적으로 .NET용 Aspose.Note는 Microsoft OneNote 문서를 다양한 이미지 형식으로 변환하는 원활한 방법을 제공하여 문서의 유연성과 접근성을 향상시킵니다. 이 자습서에 설명된 단계를 따르면 이 기능을 .NET 애플리케이션에 효율적으로 통합할 수 있습니다.

## FAQ

### Q1: 여러 Microsoft OneNote 문서를 동시에 이미지로 변환할 수 있나요?

A1: 예, Aspose.Note를 사용하여 여러 문서를 일괄 처리하여 효율성과 생산성을 보장할 수 있습니다.

### Q2: Aspose.Note는 최신 버전의 Microsoft OneNote와 호환됩니까?

A2: Aspose.Note는 Microsoft OneNote의 다양한 버전을 지원하여 호환성과 안정성을 보장합니다.

### Q3: Aspose.Note for .NET을 사용하기 위한 라이선스 요구 사항이 있나요?

A3: 네, Aspose.Note를 상업적 목적으로 사용하려면 라이선스를 취득해야 합니다. 그러나 무료 평가판을 통해 기능을 살펴볼 수도 있습니다.

### Q4: 출력 이미지 형식과 해상도를 사용자 정의할 수 있나요?

A4: 물론입니다. Aspose.Note는 요구 사항에 따라 출력 이미지 형식, 해상도 및 기타 매개 변수를 사용자 정의할 수 있는 광범위한 옵션을 제공합니다.

### Q5: Aspose.Note는 개발자에게 기술 지원을 제공합니까?

A5: 예, Aspose.Note는 포럼과 문서를 통해 포괄적인 기술 지원을 제공하여 원활한 개발 경험을 보장합니다.
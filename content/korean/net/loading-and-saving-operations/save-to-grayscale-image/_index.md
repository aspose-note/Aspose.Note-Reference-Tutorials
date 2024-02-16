---
title: Aspose.Note에서 그레이스케일 이미지로 저장
linktitle: Aspose.Note에서 그레이스케일 이미지로 저장
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 OneNote 문서를 회색조 이미지로 저장하는 방법을 알아보세요. 효율적인 문서 처리를 위해 이 포괄적인 튜토리얼을 따르십시오.
type: docs
weight: 24
url: /ko/net/loading-and-saving-operations/save-to-grayscale-image/
---
## 소개

이 튜토리얼에서는 .NET용 Aspose.Note를 활용하여 문서를 회색조 이미지로 저장하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업하여 광범위한 기능을 제공할 수 있는 강력한 라이브러리입니다.

## 전제조건

계속하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- C# 프로그래밍 언어에 대한 기본 이해.
- 시스템에 Visual Studio가 설치되어 있습니다.
-  .NET 라이브러리용 Aspose.Note가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/note/net/).
- .NET을 사용하여 파일에 액세스하고 조작하는 데 익숙합니다.

## 네임스페이스 가져오기

필요한 네임스페이스를 가져오는 것부터 시작해 보겠습니다.

```csharp
using System;

using Aspose.Note.Saving;

```

## 1단계: 문서 로드

먼저 문서를 Aspose.Note에 불러옵니다. 

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2단계: 회색조 이미지로 저장

다음으로 회색조 이미지를 저장할 경로를 지정하고 이에 따라 문서를 저장합니다.

```csharp
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
oneFile.Save(dataDir, new ImageSaveOptions(SaveFormat.Png)
					  {
						  ColorMode = ColorMode.GrayScale
					  });
```

## 3단계: 결과 확인 및 표시

마지막으로 파일 경로와 함께 성공적인 변환 메시지를 확인하고 표시합니다.

```csharp
Console.WriteLine("\nOneNote document converted successfully to grayscale image.\nFile saved at " + dataDir);
```

## 결론

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 문서를 회색조 이미지로 변환하는 방법을 배웠습니다. 이러한 간단한 단계를 따르면 개발자는 이 기능을 애플리케이션에 효율적으로 통합하여 문서 처리 기능을 향상시킬 수 있습니다.

## FAQ

### Q1: Aspose.Note가 복잡한 OneNote 파일을 처리할 수 있나요?

A1: 예, Aspose.Note는 문서 조작을 위한 강력한 기능을 제공하여 복잡한 OneNote 파일을 효율적으로 처리할 수 있습니다.

### Q2: Aspose.Note는 다른 파일 형식과 호환됩니까?

A2: 물론 Aspose.Note는 다양한 파일 형식을 지원하여 문서 처리의 유연성을 보장합니다.

### Q3: Aspose.Note는 개발자를 지원합니까?

A3: 예, 개발자는 Aspose 포럼과 문서를 통해 포괄적인 지원에 액세스할 수 있습니다.

### Q4: 구매하기 전에 Aspose.Note를 사용해 볼 수 있나요?

A4: 예, Aspose.Note 웹사이트에서 제공되는 무료 평가판을 통해 Aspose.Note를 탐색할 수 있습니다.

### Q5: Aspose.Note의 임시 라이선스는 어떻게 얻을 수 있나요?

A5: 제공된 링크를 방문하고 지침에 따라 Aspose.Note에 대한 임시 라이선스를 얻을 수 있습니다.
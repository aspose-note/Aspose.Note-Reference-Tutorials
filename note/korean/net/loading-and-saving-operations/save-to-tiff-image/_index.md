---
title: Aspose.Note에서 TIFF 이미지로 저장
linktitle: Aspose.Note에서 TIFF 이미지로 저장
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 다양한 압축 방법을 사용하여 OneNote 문서를 TIFF 이미지로 저장하는 방법을 알아보세요.
type: docs
weight: 27
url: /ko/net/loading-and-saving-operations/save-to-tiff-image/
---
## 소개

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 문서를 TIFF 형식의 이미지로 저장하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있는 강력한 API입니다. OneNote 문서를 TIFF 이미지로 저장하면 보관, 공유, 인쇄 등 다양한 응용 프로그램에 유용할 수 있습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1.  .NET용 Aspose.Note: .NET용 Aspose.Note를 설치했는지 확인하세요. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/net/).

2. 개발 환경: Visual Studio 또는 기타 .NET IDE를 사용하여 개발 환경을 설정합니다.

3. OneNote 문서: TIFF 형식으로 변환하려는 샘플 OneNote 문서를 준비합니다.

## 네임스페이스 가져오기

먼저, 필요한 네임스페이스를 프로젝트로 가져와야 합니다.

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;

```

## 1단계: JPEG 압축을 사용하여 TIFF에 저장

JPEG 압축은 품질을 유지하면서 이미지 크기를 줄이기 위해 널리 사용되는 방법입니다. JPEG 압축을 사용하여 OneNote 문서를 TIFF 이미지로 저장하는 방법은 다음과 같습니다.

```csharp
public static void SaveToTiffUsingJpegCompression()
{
    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //TIFF 이미지의 대상 경로를 설정합니다.
    var dst = "Destination_path_for_TIFF_image";

    // 문서를 JPEG 압축을 사용하여 TIFF 이미지로 저장합니다.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.Jpeg,
        Quality = 93 // 필요에 따라 품질을 조정하세요.
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using JPEG compression.\nFile saved at " + dst);
}
```

## 2단계: PackBits 압축을 사용하여 TIFF에 저장

PackBits 압축은 TIFF 이미지에 일반적으로 사용되는 간단하고 효율적인 압축 알고리즘입니다. PackBits 압축을 사용하여 OneNote 문서를 TIFF 이미지로 저장하는 방법은 다음과 같습니다.

```csharp
public static void SaveToTiffUsingPackBitsCompression()
{
    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //TIFF 이미지의 대상 경로를 설정합니다.
    var dst = "Destination_path_for_TIFF_image";

    // PackBits 압축을 사용하여 문서를 TIFF 이미지로 저장합니다.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.PackBits
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using PackBits compression.\nFile saved at " + dst);
}
```

## 3단계: CCITT 그룹 3 압축을 사용하여 TIFF에 저장

팩스 압축이라고도 하는 CCITT 그룹 3 압축은 흑백 이미지에 적합합니다. CCITT 그룹 3 압축을 사용하여 OneNote 문서를 TIFF 이미지로 저장하는 방법은 다음과 같습니다.

```csharp
public static void SaveToTiffUsingCcitt3Compression()
{
    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //TIFF 이미지의 대상 경로를 설정합니다.
    var dst = "Destination_path_for_TIFF_image";

    // CCITT 그룹 3 압축을 사용하여 문서를 TIFF 이미지로 저장합니다.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        ColorMode = ColorMode.BlackAndWhite,
        TiffCompression = TiffCompression.Ccitt3
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using CCITT Group 3 fax compression.\nFile saved at " + dst);
}
```

다음 단계를 따르면 .NET용 Aspose.Note를 사용하여 다양한 압축 옵션을 사용하여 OneNote 문서를 TIFF 이미지로 쉽게 저장할 수 있습니다.

## 결론

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 다양한 압축 방법을 사용하여 OneNote 문서를 TIFF 이미지로 저장하는 방법을 배웠습니다. JPEG, PackBits 또는 CCITT Group 3 압축이 필요한 경우 Aspose.Note는 다양한 요구 사항을 효율적으로 처리할 수 있는 유연성을 제공합니다.

## FAQ

### Q1: JPEG 압축 품질을 조정할 수 있나요?

A1: 예, JPEG 압축으로 저장할 때 품질 매개변수를 조정하여 이미지 품질과 파일 크기 간의 균형을 맞출 수 있습니다.

### Q2: Aspose.Note는 개발을 위해 Visual Studio와 호환됩니까?

A2: 예, Aspose.Note는 .NET 개발을 위해 Visual Studio에 원활하게 통합될 수 있습니다.

### Q3: 변환할 수 있는 OneNote 문서의 크기에 제한이 있나요?

A3: Aspose.Note는 심각한 성능 문제 없이 대규모 OneNote 문서를 처리할 수 있습니다.

### Q4: 여러 문서의 변환 프로세스를 자동화할 수 있습니까?

A4: 예, Aspose.Note API를 사용한 일괄 처리를 사용하여 변환 프로세스를 자동화할 수 있습니다.

### Q5: Aspose.Note에 사용할 수 있는 평가판이 있습니까?

A5: 예, Aspose.Note의 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).
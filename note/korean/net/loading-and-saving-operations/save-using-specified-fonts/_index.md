---
title: Aspose.Note에서 지정된 글꼴을 사용하여 저장
linktitle: Aspose.Note에서 지정된 글꼴을 사용하여 저장
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note에서 지정된 글꼴로 문서를 저장하는 방법을 알아보세요. 일관된 문서 형식을 위해 글꼴 설정을 쉽게 사용자 정의하세요.
weight: 28
url: /ko/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note에서 지정된 글꼴을 사용하여 저장

## 소개

이 튜토리얼에서는 Aspose.Note for .NET에서 지정된 글꼴을 사용하여 문서를 저장하는 방법을 알아봅니다. 이를 달성하기 위한 다양한 방법을 단계별로 살펴보겠습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1.  .NET용 Aspose.Note: .NET용 Aspose.Note를 설치했는지 확인하세요. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/net/).

2. 개발 환경: .NET 개발을 위해서는 개발 환경 설정이 필요합니다.

## 네임스페이스 가져오기

먼저 필요한 네임스페이스를 가져오겠습니다.

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## 1단계: 기본 글꼴 이름으로 저장

이 단계에서는 지정된 기본 글꼴 이름을 사용하여 문서를 저장합니다.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // 지정된 기본 글꼴을 사용하여 문서를 PDF로 저장합니다.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## 2단계: 파일에서 기본 글꼴로 저장

다음으로, 파일에서 로드된 기본 글꼴을 사용하여 문서를 저장해 보겠습니다.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // 파일에서 로드된 기본 글꼴을 사용하여 문서를 PDF로 저장합니다.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## 3단계: 스트림에서 기본 글꼴로 저장

마지막으로 스트림에서 로드된 기본 글꼴을 사용하여 문서를 저장해 보겠습니다.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // 스트림에서 로드된 기본 글꼴을 사용하여 문서를 PDF로 저장합니다.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## 결론

이 튜토리얼에서는 .NET용 Aspose.Note에서 지정된 글꼴을 사용하여 문서를 저장하는 방법을 살펴보았습니다. 다음 단계를 수행하면 요구 사항에 따라 글꼴 설정을 사용자 정의하여 문서 형식을 원하는 대로 지정할 수 있습니다.

## FAQ

### Q1: Aspose.Note에서 문서를 저장하는 데 어떤 글꼴이라도 사용할 수 있나요?

A1: 예, 문서 저장에 사용할 글꼴을 지정할 수 있습니다. 글꼴 파일에 액세스할 수 있고 올바르게 로드되었는지 확인하세요.

### Q2: Aspose.Note는 다른 문서 형식과 호환됩니까?

A2: Aspose.Note는 주로 OneNote 문서와 함께 작동하지만 PDF를 포함한 다양한 형식으로 저장할 수 있는 옵션을 제공합니다.

### Q3: 문서를 저장할 때 누락된 글꼴을 처리하려면 어떻게 해야 합니까?

A3: Aspose.Note는 지정된 글꼴이 누락된 경우 기본 글꼴을 사용하는 옵션을 제공하여 일관된 문서 형식을 보장합니다.

### Q4: Aspose.Note는 출력 문서에 글꼴 포함을 지원합니까?

A4: 예, Aspose.Note에서는 문서 이식성과 다양한 플랫폼 간의 일관된 렌더링을 보장하기 위해 글꼴을 포함할 수 있습니다.

### Q5: Aspose.Note에 대한 추가 지원은 어디서 받을 수 있나요?

 A5: 추가 지원이나 기술 지원을 받으려면[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

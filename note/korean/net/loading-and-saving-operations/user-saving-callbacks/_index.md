---
title: Aspose.Note의 사용자 저장 콜백
linktitle: Aspose.Note의 사용자 저장 콜백
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note에서 사용자 저장 콜백을 구현하여 글꼴, CSS 및 이미지 저장을 사용자 지정하는 방법을 알아보세요.
weight: 31
url: /ko/net/loading-and-saving-operations/user-saving-callbacks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note의 사용자 저장 콜백

## 소개

이 튜토리얼에서는 .NET용 Aspose.Note에서 사용자 저장 콜백을 구현하는 방법을 살펴보겠습니다. 이러한 콜백을 사용하면 글꼴, CSS 스타일시트 및 이미지 저장과 같은 다양한 단계에 개입할 후크를 제공하여 저장 프로세스를 사용자 정의할 수 있습니다. 이러한 콜백을 활용하면 특정 요구 사항에 맞게 저장 동작을 맞춤화하여 출력에 대한 유연성과 제어력을 향상시킬 수 있습니다.

## 전제조건

Aspose.Note에서 사용자 저장 콜백 구현을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  .NET SDK용 Aspose.Note: 다음에서 .NET SDK용 Aspose.Note를 다운로드하고 설치하세요.[다운로드 페이지](https://releases.aspose.com/note/net/).
   
2. 개발 환경: Visual Studio 또는 기타 .NET 개발 환경과 같은 적합한 개발 환경을 설정합니다.

## 네임스페이스 가져오기

시작하려면 Aspose.Note 라이브러리에서 필요한 클래스와 메서드에 액세스하기 위해 필요한 네임스페이스를 프로젝트로 가져와야 합니다.

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

이제 사용자 저장 콜백 구현을 여러 단계로 나누어 보겠습니다.

## 1단계: 콜백 속성 정의

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

여기에서는 루트 폴더, CSS 폴더, 글꼴 폴더, 이미지 폴더 및 기타 관련 설정을 지정하기 위해 다양한 속성을 정의합니다.

## 2단계: 글꼴 저장 콜백 구현

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 이 단계에서는 다음을 구현합니다.`FontSaving` 글꼴 저장을 처리하는 콜백 메서드입니다. 지정된 글꼴 폴더에 리소스를 생성하고 이에 따라 스트림과 URI를 할당합니다.

## 3단계: CSS 저장 콜백 구현

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 여기에서 우리는`CssSaving` CSS 스타일시트 저장을 관리하는 콜백 메소드입니다. 지정된 CSS 폴더에 리소스를 생성하고 이에 따라 스트림, URI 및 기타 속성을 설정합니다.

## 4단계: 이미지 저장 콜백 구현

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 마지막으로 우리는`ImageSaving` 이미지 저장을 처리하는 콜백 메소드입니다. 이전 단계와 유사하게 지정된 이미지 폴더에 리소스를 생성하고 스트림과 URI를 할당합니다.

## 결론

이 튜토리얼에서는 .NET용 Aspose.Note에서 사용자 저장 콜백을 구현하는 방법을 배웠습니다. 제공된 단계에 따라 글꼴, CSS 스타일시트 및 이미지 저장 프로세스를 사용자 정의하여 출력에 대한 유연성과 제어력을 높일 수 있습니다.

## 자주 묻는 질문

### Q1: 이러한 콜백을 사용하여 저장 프로세스의 다른 측면을 사용자 정의할 수 있습니까?

A1: 예, 이러한 콜백을 확장하거나 추가 콜백을 구현하여 필요에 따라 저장 프로세스의 다양한 측면을 사용자 정의할 수 있습니다.

### Q2: Aspose.Note for .NET은 다른 .NET 프레임워크와 호환됩니까?

A2: 예, .NET용 Aspose.Note는 .NET Core 및 .NET Standard를 포함한 다양한 .NET 프레임워크와 호환됩니다.

### Q3: 저장 과정에서 발생하는 오류나 예외를 어떻게 처리할 수 있나요?

대답 3: 각 콜백 메서드 내에 오류 처리 메커니즘을 통합하여 발생할 수 있는 모든 오류나 예외를 원활하게 처리할 수 있습니다.

### Q4: 이러한 콜백을 사용할 때 성능 고려 사항이 있습니까?

A4: 이러한 콜백은 유연성을 제공하지만, 특히 대규모 문서나 리소스를 처리할 때 성능 오버헤드를 방지하려면 효율적으로 구현되어야 합니다.

### Q5: 사용자 입력이나 기타 조건에 따라 저장 동작을 동적으로 변경할 수 있습니까?

A5: 예, 콜백 메서드 내에 조건부 논리를 통합하여 다양한 요인에 따라 저장 동작을 동적으로 조정할 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

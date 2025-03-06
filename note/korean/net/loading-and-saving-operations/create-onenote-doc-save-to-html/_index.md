---
title: OneNote 문서를 생성하고 Aspose.Note에서 HTML로 저장
linktitle: OneNote 문서를 생성하고 Aspose.Note에서 HTML로 저장
second_title: Aspose.Note .NET API
description: Aspose.Note API를 사용하여 .NET 애플리케이션에서 Microsoft OneNote 문서를 HTML 형식으로 만들고 저장하는 방법을 알아보세요. 단계별 예제가 포함된 포괄적인 튜토리얼을 따라해보세요.
weight: 14
url: /ko/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote 문서를 생성하고 Aspose.Note에서 HTML로 저장

## 소개

Aspose.Note for .NET은 개발자가 .NET 애플리케이션에서 Microsoft OneNote 문서를 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 API입니다. Aspose.Note를 사용하면 OneNote 파일을 손쉽게 생성, 조작 및 변환할 수 있습니다. 이 튜토리얼에서는 Aspose.Note for .NET API에서 제공하는 다양한 옵션을 사용하여 OneNote 문서를 생성하고 HTML 형식으로 저장하는 방법을 살펴보겠습니다.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- C# 프로그래밍 언어에 대한 기본 지식.
- 시스템에 Visual Studio가 설치되어 있습니다.
-  프로젝트에 설치된 .NET API용 Aspose.Note. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/net/).
- Microsoft OneNote 문서의 구조에 익숙합니다.

## 네임스페이스 가져오기

코딩 부분을 살펴보기 전에 필요한 네임스페이스를 가져오겠습니다.

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

이제 각 예제를 여러 단계로 나누고 OneNote 문서를 만들고 .NET용 Aspose.Note를 사용하여 HTML 형식으로 저장하는 방법을 살펴보겠습니다.

## 1단계: 기본 옵션을 사용하여 OneNote 문서 만들기

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // OneNote 문서 초기화
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // 문서의 모든 텍스트에 대한 기본 스타일입니다.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // HTML 형식으로 저장
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

이 단계에서는 새 OneNote 문서를 초기화하고, 제목이 있는 페이지를 추가하고, 기본 옵션을 사용하여 HTML 형식으로 저장합니다.

## 2단계: 특정 페이지 범위를 생성하고 HTML에 저장

```csharp
public static void CreateAndSavePageRange()
{
    // OneNote 문서 초기화
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // 문서의 모든 텍스트에 대한 기본 스타일입니다.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // HTML 형식으로 저장
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

여기에서는 문서를 만들고 특정 페이지 범위를 HTML 형식으로 저장하는 방법을 보여줍니다.

## 3단계: 포함된 리소스를 사용하여 메모리 스트림에 HTML로 저장

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // OneNote 문서 로드
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // HTML 저장 옵션 지정
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // 문서를 메모리 스트림에 저장
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

이 단계에서는 리소스(CSS, 글꼴 및 이미지)가 포함된 HTML 형식으로 OneNote 문서를 메모리 스트림에 저장하는 방법을 보여줍니다.

## 4단계: 별도의 파일에 리소스가 포함된 파일에 HTML로 저장

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // OneNote 문서 로드
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // HTML 저장 옵션 지정
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // 별도의 파일에 리소스가 저장된 HTML 파일로 문서를 저장합니다.
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

이 단계에서는 OneNote 문서를 모든 리소스(CSS, 글꼴 및 이미지)가 별도의 파일에 저장된 HTML 형식으로 저장합니다.

## 5단계: 리소스를 저장하기 위한 콜백을 사용하여 메모리 스트림에 HTML로 저장

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // 콜백 구성 저장 지정
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // HTML 저장 옵션 지정
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // OneNote 문서 로드
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // 사용자 정의 콜백으로 관리되는 리소스를 사용하여 문서를 HTML 형식으로 저장합니다.
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // CSS 스트림에 데이터를 수동으로 추가
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

여기서는 사용자 정의 콜백으로 관리되는 리소스를 사용하여 OneNote 문서를 HTML 형식으로 저장하는 방법을 보여줍니다.

## 결론

이 기사에서는 OneNote 문서로 작업하고 .NET용 Aspose.Note를 사용하여 HTML 형식으로 저장하는 방법을 살펴보았습니다. 단계별 가이드를 따르면 쉽게 할 수 있습니다.

 이 기능을 .NET 응용 프로그램에 통합하면 OneNote 파일을 효율적으로 조작할 수 있습니다.

## FAQ

### Q1: 저장된 HTML 파일의 모양을 사용자 정의할 수 있습니까?

A1: 예, 변환 프로세스 중에 생성된 CSS 스타일시트를 수정하여 모양을 사용자 정의할 수 있습니다.

### Q2: Aspose.Note는 HTML 이외의 다른 형식으로의 변환을 지원합니까?

A2: 네, Aspose.Note는 PDF, 이미지, Microsoft Word 문서 등 다양한 형식으로의 변환을 지원합니다.

### Q3: Aspose.Note는 .NET Core 애플리케이션과 호환됩니까?

A3: 예, Aspose.Note는 .NET Framework 및 .NET Core 응용 프로그램과 모두 호환됩니다.

### Q4: Aspose.Note를 사용하여 OneNote 문서에서 텍스트와 이미지를 추출할 수 있나요?

A4: 예, Aspose.Note API를 사용하면 텍스트와 이미지를 추출할 수 있을 뿐만 아니라 다양한 기타 조작을 수행할 수 있습니다.

### Q5: Aspose.Note 기능을 테스트하는 데 사용할 수 있는 평가판이 있습니까?

 A5: 예, 다음에서 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

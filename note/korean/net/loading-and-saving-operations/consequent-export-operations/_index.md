---
title: Aspose.Note의 후속 내보내기 작업
linktitle: Aspose.Note의 후속 내보내기 작업
second_title: Aspose.Note .NET API
description: OneNote 문서를 다양한 형식으로 효율적으로 저장하기 위해 .NET용 Aspose.Note에서 후속 내보내기 작업을 수행하는 방법을 알아보세요.
type: docs
weight: 10
url: /ko/net/loading-and-saving-operations/consequent-export-operations/
---
## 소개

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 후속 내보내기 작업을 수행하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 라이브러리입니다. 문서를 다른 형식으로 내보내는 것은 일반적인 요구 사항이며 Aspose.Note는 이 작업을 효율적으로 단순화합니다. 다양한 형식으로 문서를 저장하는 방법을 단계별로 살펴보겠습니다.

## 전제조건

이 튜토리얼을 진행하기 전에 다음 사항을 확인하세요.

1. C# 프로그래밍 언어에 대한 기본 이해.
2. 시스템에 Visual Studio가 설치되어 있습니다.
3. .NET 라이브러리용 Aspose.Note가 프로젝트에 통합되었습니다.

## 네임스페이스 가져오기

우선 C# 코드에서 필요한 네임스페이스를 가져와야 합니다.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Drawing;
using System.Globalization;
```

## 1단계: 문서 초기화

 먼저, 새로운 것을 초기화하십시오.`Document` 자동 레이아웃 변경 감지가 비활성화된 객체:

```csharp
Document doc = new Document() { AutomaticLayoutChangesDetectionEnabled = false };
```

## 2단계: 새 페이지 초기화

 새로 만들기`Page`개체를 선택하고 해당 속성을 지정합니다.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 3단계: 페이지 제목 설정

날짜 및 시간 정보와 함께 페이지 제목을 정의합니다.

```csharp
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## 4단계: 페이지 노드 추가

문서에 페이지 노드를 추가합니다.

```csharp
doc.AppendChildLast(page);
```

## 5단계: 다른 형식으로 문서 저장

이제 OneNote 문서를 다양한 형식으로 저장하세요.

```csharp
string dataDir = "Your Document Directory";
doc.Save(dataDir + "ConsequentExportOperations_out.html");            
doc.Save(dataDir + "ConsequentExportOperations_out.pdf");            
doc.Save(dataDir + "ConsequentExportOperations_out.jpg");            
textStyle.FontSize = 11;           
doc.DetectLayoutChanges();            
doc.Save(dataDir + "ConsequentExportOperations_out.bmp");
```

## 결론

결론적으로 우리는 .NET용 Aspose.Note를 사용하여 결과적인 내보내기 작업을 수행하는 방법을 배웠습니다. 이 자습서에 설명된 단계를 따르면 OneNote 문서를 다양한 형식으로 원활하게 저장할 수 있으므로 응용 프로그램의 다양성이 향상됩니다.

## FAQ

### Q1: 페이지 제목을 추가로 사용자 정의할 수 있나요?

A1: 예, 문서를 저장하기 전에 요구 사항에 따라 제목 텍스트, 날짜 및 시간을 수정할 수 있습니다.

### Q2: 레이아웃 변경 감지를 어떻게 처리합니까?

 A2: 설명한 대로 다음을 사용하여 레이아웃 변경 사항을 수동으로 감지할 수 있습니다.`DetectLayoutChanges()` Aspose.Note에서 제공하는 메소드입니다.

### Q3: Aspose.Note는 언급된 형식 외에 다른 내보내기 형식을 지원합니까?

A3: 예, Aspose.Note는 DOCX, PNG, TIFF 등을 포함한 광범위한 내보내기 형식을 지원합니다.

### Q4: Aspose.Note는 .NET Core와 호환됩니까?

A4: 예, Aspose.Note는 .NET Framework 및 .NET Core 환경 모두와 호환됩니다.

### Q5: Aspose.Note에 대한 추가 리소스와 지원은 어디서 찾을 수 있나요?

A5: 포괄적인 가이드, 튜토리얼 및 커뮤니티 지원을 보려면 Aspose.Note 설명서와 포럼을 방문하세요.
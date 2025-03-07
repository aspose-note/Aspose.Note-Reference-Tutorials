---
title: Aspose.Note에서 페이지 제목이 포함된 문서 만들기
linktitle: Aspose.Note에서 페이지 제목이 포함된 문서 만들기
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 제목이 있는 페이지가 있는 문서를 만드는 방법을 알아보세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
weight: 13
url: /ko/net/loading-and-saving-operations/create-doc-with-page-title/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note에서 페이지 제목이 포함된 문서 만들기

## 소개

이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 제목이 있는 페이지가 있는 문서를 만드는 과정을 안내합니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있는 강력한 API입니다.

## 전제조건

시작하기 전에 다음 필수 구성 요소가 설치 및 설정되어 있는지 확인하세요.

### 비주얼 스튜디오 설치

1. Visual Studio 다운로드: 아직 설치하지 않은 경우 Microsoft 웹사이트에서 Visual Studio를 다운로드하여 설치하세요.

2. .NET 개발 워크로드 설치: 설치 프로세스 중에 ".NET 데스크톱 개발" 워크로드를 선택하여 .NET 개발에 필요한 모든 구성 요소가 있는지 확인하십시오.

3. 새 프로젝트 만들기: Visual Studio를 열고 새 프로젝트(콘솔 애플리케이션 또는 원하는 다른 유형)를 만듭니다.

### Aspose.Note 설치

1.  Aspose.Note 가져오기: 다음에서 .NET용 Aspose.Note 라이브러리를 다운로드하세요.[웹사이트](https://releases.aspose.com/note/net/).

2. NuGet을 통해 Aspose.Note 설치: 또는 Visual Studio의 NuGet 패키지 관리자를 통해 .NET용 Aspose.Note를 설치할 수 있습니다. 간단히 "Aspose.Note"를 검색하고 최신 버전을 설치하세요.

## 네임스페이스 가져오기

먼저 프로젝트에서 Aspose.Note를 사용하려면 필요한 네임스페이스를 가져와야 합니다.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

이제 페이지 제목이 있는 문서를 만드는 과정을 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 개체 만들기

```csharp
//Document 클래스의 객체 생성
Document doc = new Aspose.Note.Document();
```

## 2단계: 페이지 클래스 개체 초기화

```csharp
// 페이지 클래스 객체 초기화
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 3단계: 텍스트의 기본 스타일 설정

```csharp
// 문서의 모든 텍스트에 대한 기본 스타일입니다.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## 4단계: 페이지 제목 속성 설정

```csharp
// 페이지 제목 속성 설정
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## 5단계: 문서에 페이지 노드 추가

```csharp
// 문서에 페이지 노드 추가
doc.AppendChildLast(page);
```

## 6단계: OneNote 문서 저장

```csharp
// OneNote 문서 저장
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## 결론

축하해요! .NET용 Aspose.Note를 사용하여 제목이 있는 페이지가 있는 문서를 성공적으로 만들었습니다. 이 튜토리얼에서는 OneNote 파일을 프로그래밍 방식으로 관리하기 위해 Aspose.Note를 .NET 애플리케이션에 통합하는 데 도움이 되는 단계별 가이드를 제공했습니다.

## FAQ

### Q1: 제목 텍스트 스타일을 사용자 정의할 수 있나요?

A1: 예, 요구 사항에 따라 제목 텍스트의 글꼴 색상, 글꼴 이름 및 글꼴 크기를 사용자 정의할 수 있습니다.

### Q2: Aspose.Note는 .NET Core와 호환됩니까?

A2: 예, Aspose.Note는 .NET Core를 지원하므로 크로스 플랫폼 애플리케이션을 개발할 수 있습니다.

### Q3: 문서에 이미지와 첨부 파일을 추가할 수 있나요?

A3: 물론이죠! Aspose.Note는 OneNote 문서에 이미지, 첨부 파일 및 기타 요소를 원활하게 추가할 수 있는 API를 제공합니다.

### Q4: Aspose.Note는 기존 OneNote 파일 읽기를 지원합니까?

A4: 예, Aspose.Note를 사용하여 기존 OneNote 파일을 쉽게 읽고, 수정하고, 조작할 수 있습니다.

### Q5: 문제가 발생하면 어디서 지원을 받을 수 있나요?

 답변 5: 다음 웹사이트에서 지원과 도움을 받으실 수 있습니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 전문가와 커뮤니티 회원이 귀하의 질문에 도움을 줄 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
date: 2026-04-03
description: Aspose.Note for .NET을 사용하여 Aspose.Note 문서에 하이퍼링크를 추가하고, 하이퍼링크 모양을 사용자
  정의하며, 여러 하이퍼링크를 삽입해 OneNote 파일을 더욱 풍부하게 만드는 방법을 배워보세요.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Aspose.Note 문서에 하이퍼링크를 추가하는 방법
second_title: Aspose.Note .NET API
title: Aspose.Note 문서에 하이퍼링크 추가 방법
url: /ko/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note 문서에 하이퍼링크 추가하는 방법

## 소개

이 튜토리얼에서는 .NET API를 사용하여 Aspose.Note 문서의 텍스트에 **하이퍼링크를 추가하는 방법**을 알아봅니다. 하이퍼링크를 추가하면 정적인 메모가 인터랙티브하고 클릭 가능한 콘텐츠로 변환되어 웹 리소스, 내부 섹션 또는 외부 파일에 연결하기에 이상적입니다. 각 단계를 차례대로 안내하고 **하이퍼링크 외관을 사용자 정의하는 방법**을 보여주며, 풍부한 OneNote 페이지가 필요할 때 **여러 하이퍼링크를 삽입하는 방법**을 설명합니다.

## 빠른 답변
- **OneNote 파일을 생성하기 위한 주요 클래스는 무엇인가요?** Aspose.Note의 `Document`.
- **텍스트를 하이퍼링크처럼 동작하게 하는 속성은 무엇인가요?** `TextStyle`의 `IsHyperlink = true`.
- **외부 웹사이트에 연결할 수 있나요?** 예, `HyperlinkAddress`를 `https://www.google.com`와 같은 URL로 설정합니다.
- **프로덕션 사용에 라이선스가 필요합니까?** 평가판이 아닌 빌드에서는 유효한 Aspose.Note 라이선스가 필요합니다.
- **지원되는 .NET 버전은 무엇인가요?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Aspose.Note에서 “하이퍼링크 추가”란 무엇인가요?
하이퍼링크를 추가한다는 것은 텍스트 조각에 URL을 연결하여 사용자가 OneNote 내부에서 클릭하면 연결된 리소스가 브라우저나 다른 애플리케이션에서 열리도록 하는 것을 의미합니다. Aspose.Note는 프로그래밍 방식으로 이를 구현하기 위해 `TextStyle.IsHyperlink` 플래그와 `HyperlinkAddress` 속성을 제공합니다.

## OneNote 문서에 하이퍼링크를 추가하는 이유
- **Improved navigation:** 관련 웹 페이지나 섹션으로 바로 이동합니다.
- **Enhanced documentation:** 메모를 떠나지 않고도 참고 자료, 튜토리얼 또는 소스 파일을 제공합니다.
- **Professional look:** 사용자 정의 가능한 색상과 스타일을 통해 하이퍼링크가 문서 디자인에 자연스럽게 어우러집니다.

## 전제 조건

1. C# 및 Visual Studio에 대한 기본 지식.
2. Aspose.Note for .NET 라이브러리가 설치되어 있어야 합니다 – [여기](https://releases.aspose.com/note/net/)에서 다운로드하십시오.
3. Aspose.Note 문서 구조(페이지, 아웃라인, 리치 텍스트)에 대한 이해.

## 네임스페이스 가져오기

먼저, 핵심 Aspose.Note 클래스와 기본 .NET 타입에 접근할 수 있도록 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Drawing;
```

## 단계별 가이드

### 단계 1: 새 Document 객체 만들기

`Document`를 인스턴스화하여 모든 페이지와 콘텐츠를 보관합니다.

```csharp
Document doc = new Document();
```

### 단계 2: 텍스트 스타일 정의 (하이퍼링크 스타일 포함)

`TextStyle` 객체 두 개를 생성합니다 – 일반 텍스트용 하나와 하이퍼링크용 하나.  
여기서는 폰트 색상을 설정하여 **하이퍼링크 외관을 사용자 정의**합니다.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **팁:** **여러 하이퍼링크**를 삽입하려면 서로 다른 `HyperlinkAddress` 값을 가진 추가 `TextStyle` 객체를 정의하고 이후 `RichText` 세그먼트에서 재사용하십시오.

### 단계 3: RichText 객체 만들기

일반 텍스트와 하이퍼링크를 혼합한 단락을 만듭니다. `Append` 메서드를 사용하면 스타일이 적용된 조각들을 체인처럼 연결할 수 있습니다.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### 단계 4: Outline 및 Outline Element 만들기

Outline은 페이지의 시각적 요소를 담는 컨테이너 역할을 합니다. 필요에 따라 크기와 위치를 설정합니다.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### 단계 5: 페이지에 요소 추가

각 OneNote 파일은 페이지로 구성됩니다. `Title`과 `Page`를 만든 뒤, outline을 첨부합니다.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### 단계 6: 문서 저장

폴더를 선택하고 전체 파일 이름을 구성한 뒤 `Save`를 호출합니다. 출력 파일은 하이퍼링크가 포함된 유효한 OneNote `.one` 파일이 됩니다.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| 하이퍼링크가 열리지 않음 | `HyperlinkAddress`에 프로토콜(`http://` 또는 `https://`)이 포함되어 있는지 확인하십시오. |
| 텍스트 색상이 적용되지 않음 | 하이퍼링크에 사용된 `TextStyle`의 `FontColor`를 설정하십시오. |
| 한 페이지에 여러 링크가 필요함 | 각각 고유한 `HyperlinkAddress`를 가진 여러 `TextStyle` 객체를 생성하고, 이를 동일하거나 다른 `RichText` 객체에 추가하십시오. |
| 문서가 OneNote에서 로드되지 않음 | 지원되는 OneNote 버전(2010 이상)을 사용하고 있는지 확인하십시오. |

## 자주 묻는 질문

**Q: Aspose.Note를 사용하여 동일한 문서에 여러 하이퍼링크를 추가할 수 있나요?**  
A: 예, 서로 다른 `HyperlinkAddress` 값을 가진 추가 `TextStyle` 인스턴스를 생성하고 이를 `RichText` 객체에 추가하면 됩니다.

**Q: 하이퍼링크의 외관을 어떻게 사용자 정의할 수 있나요?**  
A: `IsHyperlink = true`인 `TextStyle`에서 `FontColor`, `FontName`, `FontSize`와 같은 속성을 사용하십시오. 이를 통해 문서의 브랜딩에 맞출 수 있습니다.

**Q: Aspose.Note가 외부 웹사이트에 대한 하이퍼링크를 지원하나요?**  
A: 물론입니다. `HyperlinkAddress`를 유효한 URL(`http://` 또는 `https://` 포함)로 설정하면 OneNote 파일 외부로 연결할 수 있습니다.

**Q: 많은 하이퍼링크를 포함하는 단일 OneNote 파일을 생성할 수 있나요?**  
A: 예. 서로 다른 하이퍼링크 주소를 가진 스타일링된 `RichText` 세그먼트를 반복적으로 추가하면 **하나의 파일에 하이퍼링크 컬렉션을 생성**할 수 있습니다.

**Q: Aspose.Note가 최신 OneNote 버전과 호환되나요?**  
A: 이 라이브러리는 OneNote 2010 이후 버전 및 Windows 10 UWP 버전을 포함하여 작동합니다.

**마지막 업데이트:** 2026-04-03  
**테스트 환경:** Aspose.Note for .NET 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
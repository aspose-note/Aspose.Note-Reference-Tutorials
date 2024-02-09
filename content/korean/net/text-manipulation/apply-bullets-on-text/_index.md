---
title: Aspose.Note에서 텍스트에 글머리 기호 적용
linktitle: Aspose.Note에서 텍스트에 글머리 기호 적용
second_title: Aspose.Note .NET API
description: OneNote 문서를 향상시키기 위해 .NET용 Aspose.Note에서 텍스트에 글머리 기호를 적용하는 방법을 알아보세요. 효과적인 포맷을 위해서는 이 단계별 가이드를 따르세요.
type: docs
weight: 10
url: /ko/net/text-manipulation/apply-bullets-on-text/
---
## 소개
.NET용 Aspose.Note를 사용하여 텍스트에 글머리 기호를 적용하는 방법에 대한 단계별 가이드에 오신 것을 환영합니다. Aspose.Note는 개발자가 .NET 애플리케이션에서 Microsoft OneNote 파일을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 텍스트에 글머리 기호를 적용하여 OneNote 문서의 시각적 매력을 향상시키는 과정을 안내합니다.
## 전제 조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
- C# 및 .NET 프로그래밍에 대한 기본 지식.
-  .NET 라이브러리용 Aspose.Note가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/note/net/).
## 네임스페이스 가져오기
C# 코드에 필요한 네임스페이스를 포함해야 합니다.
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1단계: 문서 설정
```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";
// Document 클래스의 객체 생성
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 2단계: 페이지 및 개요 초기화
```csharp
// 페이지 클래스 객체 초기화
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// 개요 클래스 객체 초기화
Outline outline = new Outline(doc);
```
## 3단계: 기본 텍스트 스타일 설정
```csharp
// TextStyle 클래스 객체 초기화 및 서식 속성 설정
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 4단계: 글머리 기호가 있는 개요 요소 만들기
```csharp
// 아웃라인엘리먼트 클래스 객체 초기화 및 글머리 기호 적용
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// 다른 개요 요소에 대해 반복합니다.
```
## 5단계: 개요에 개요 요소 추가
```csharp
// 개요 요소 추가
outline.AppendChildLast(outlineElem1);
// 다른 개요 요소에 대해 반복합니다.
```
## 6단계: 페이지에 개요 추가
```csharp
// 개요 노드 추가
page.AppendChildLast(outline);
```
## 7단계: 문서에 페이지 추가
```csharp
// 페이지 노드 추가
doc.AppendChildLast(page);
```
## 8단계: OneNote 문서 저장
```csharp
// OneNote 문서 저장
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## 결론
축하해요! .NET용 Aspose.Note를 사용하여 텍스트에 글머리 기호를 적용하는 방법을 성공적으로 배웠습니다. 이 기능은 OneNote 문서의 서식을 크게 향상시켜 시각적으로 더욱 매력적으로 만들 수 있습니다.
## FAQ
### 목록의 각 항목에 서로 다른 글머리 기호 스타일을 적용할 수 있나요?
 예, 글머리 기호 스타일을 수정하여 사용자 정의할 수 있습니다.`NumberList` 각각의 속성`OutlineElement`.
### Aspose.Note는 최신 버전의 Microsoft OneNote와 호환됩니까?
Aspose.Note는 다양한 버전의 Microsoft OneNote를 지원하여 이전 버전과 최신 버전 모두와의 호환성을 보장합니다.
### Aspose.Note를 상업적 목적으로 사용할 수 있나요?
 예, 상업용 프로젝트에서 .NET용 Aspose.Note를 사용할 수 있습니다. 라이센스를 얻으려면 다음을 방문하십시오.[여기](https://purchase.aspose.com/buy).
### .NET용 Aspose.Note에 사용할 수 있는 평가판이 있습니까?
 예, 무료 평가판을 다운로드할 수 있습니다[여기](https://releases.aspose.com/).
### 추가 지원과 리소스는 어디에서 찾을 수 있나요?
 Aspose.Note 커뮤니티 포럼을 방문하실 수 있습니다[여기](https://forum.aspose.com/c/note/28) 지원과 토론을 위해.
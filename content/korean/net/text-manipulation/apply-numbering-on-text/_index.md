---
title: Aspose.Note에서 텍스트에 번호 매기기 적용
linktitle: Aspose.Note에서 텍스트에 번호 매기기 적용
second_title: Aspose.Note .NET API
description: 이 포괄적인 튜토리얼을 통해 .NET용 Aspose.Note에서 텍스트 번호 매기기를 적용하는 방법을 알아보세요. 손쉽게 문서 형식을 향상하세요.
type: docs
weight: 12
url: /ko/net/text-manipulation/apply-numbering-on-text/
---
## 소개
Aspose.Note for .NET은 C# 애플리케이션의 문서 조작을 위한 강력한 도구를 제공합니다. 이 튜토리얼에서는 Aspose.Note를 사용하여 텍스트에 번호 매기기를 적용하는 과정을 살펴보겠습니다. 문서 형식을 손쉽게 향상하려면 다음 단계별 지침을 따르세요.
## 전제 조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
- C# 프로그래밍 언어에 대한 기본 이해.
-  .NET용 Aspose.Note가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/note/net/).
- Visual Studio와 같은 IDE(통합 개발 환경).
## 네임스페이스 가져오기
시작하려면 C# 프로젝트에서 필요한 네임스페이스를 가져와야 합니다.
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1단계: 문서 설정
새 문서를 만들고 필요한 개체를 초기화하는 것부터 시작하세요.
```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";
// Document 클래스의 객체 생성
Document doc = new Document();
// 페이지 클래스 객체 초기화
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// 개요 클래스 객체 초기화
Outline outline = new Outline(doc);
```
## 2단계: 기본 스타일 정의
ParagraphStyle 클래스를 사용하여 텍스트의 기본 스타일을 설정합니다.
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 3단계: 번호 매기기 적용
OutlineElement 클래스 객체를 초기화하고 각 요소에 번호 매기기를 적용합니다.
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 4단계: 개요 요소 추가
개요 요소를 개요에 추가합니다.
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## 5단계: 문서 저장
번호가 적용된 OneNote 문서를 저장합니다.
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## 결론
축하해요! .NET용 Aspose.Note에서 텍스트에 번호 매기기를 적용하는 방법을 성공적으로 배웠습니다. 다양한 서식 옵션을 시험해 보고 시각적으로 매력적인 문서를 손쉽게 만들어 보세요.
## FAQ
### 1. 번호 매기기 형식을 사용자 정의할 수 있나요?
예, NumberList 클래스를 사용하면 원하는 대로 번호 매기기 형식을 사용자 정의할 수 있습니다.
### 2. 사용 가능한 다른 서식 옵션이 있습니까?
Aspose.Note는 글꼴 스타일, 색상 등을 포함한 광범위한 서식 옵션을 제공합니다.
### 3. Aspose.Note는 Visual Studio와 호환됩니까?
전적으로! Aspose.Note는 원활한 개발 경험을 위해 Visual Studio와 완벽하게 통합됩니다.
### 4. 구매하기 전에 Aspose.Note를 사용해 볼 수 있나요?
 틀림없이! 무료 평가판을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).
### 5. Aspose.Note에 대한 지원은 어디서 받을 수 있나요?
 도움이나 문의사항이 있으면 다음을 방문하세요.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).
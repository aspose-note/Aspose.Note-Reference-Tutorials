---
title: Aspose.Note 텍스트에 중국어 숫자 목록 삽입
linktitle: Aspose.Note 텍스트에 중국어 숫자 목록 삽입
second_title: Aspose.Note .NET API
description: .NET 문서용 Aspose.Note에 중국어 숫자 목록을 쉽게 삽입하는 방법을 알아보세요. 이 단계별 가이드를 통해 문서 서식 지정 기술을 향상하세요.
type: docs
weight: 20
url: /ko/net/text-manipulation/insert-chinese-number-list/
---
## 소개
중국어 번호 목록을 문서에 통합하여 .NET용 Aspose.Note 기술을 향상시키고 싶으십니까? 그렇다면, 당신은 바로 이곳에 있습니다! 이 튜토리얼에서는 .NET용 Aspose.Note를 사용하여 중국어 숫자 목록을 삽입하는 과정을 안내합니다. 이 강력한 라이브러리를 사용하면 OneNote 문서를 원활하게 조작할 수 있습니다.
## 전제조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
- C# 프로그래밍에 대한 기본 지식.
-  .NET용 Aspose.Note가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/note/net/).
## 네임스페이스 가져오기
시작하려면 필요한 네임스페이스를 프로젝트로 가져옵니다.
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## 1단계: OneNote 문서 초기화
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## 2단계: OneNote 페이지 초기화
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## 3단계: 텍스트 스타일 설정 적용
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## 4단계: 개요 요소 생성
이제 중국어 숫자 목록을 사용하여 세 가지 개요 요소를 만들어 보겠습니다.
### 4.1단계: 첫 번째 요소
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### 4.2단계: 두 번째 요소
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### 4.3단계: 세 번째 요소
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## 5단계: 개요에 요소 추가
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## 6단계: 페이지에 개요 추가
```csharp
page.AppendChildLast(outline);
```
## 7단계: 문서에 페이지 추가
```csharp
doc.AppendChildLast(page);
```
## 8단계: OneNote 문서 저장
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
축하해요! .NET 라이브러리를 사용하여 Aspose.Note 문서에 중국어 숫자 목록을 성공적으로 삽입했습니다.
## 결론
이 튜토리얼에서는 중국어 숫자 목록을 .NET용 Aspose.Note 문서에 통합하는 단계별 프로세스를 다루었습니다. 이러한 기술을 사용하여 문서 서식 기술을 향상하고 콘텐츠를 더욱 매력적으로 만드세요.
## 자주 묻는 질문
### Q: 중국어 숫자 목록의 형식을 사용자 정의할 수 있나요?
 A: 예.`NumberList` 건설자.
### Q: Aspose.Note는 최신 버전의 .NET과 호환됩니까?
A: 예, Aspose.Note는 최신 버전의 .NET을 지원하도록 정기적으로 업데이트됩니다.
### Q: 추가 예제와 문서는 어디에서 찾을 수 있습니까?
A: 포괄적인 탐색[Aspose.Note 문서](https://reference.aspose.com/note/net/).
### Q: Aspose.Note의 임시 라이선스는 어떻게 얻을 수 있나요?
 A: 임시 면허를 취득하세요[여기](https://purchase.aspose.com/temporary-license/).
### Q: Aspose.Note 관련 질문에 대해 도움을 구하거나 논의할 수 있는 곳은 어디입니까?
 답: 다음을 방문하세요.[Aspose.Note 지원 포럼](https://forum.aspose.com/c/note/28) 지역 사회 지원을 위해.
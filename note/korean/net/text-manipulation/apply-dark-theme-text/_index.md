---
title: .NET용 Aspose.Note를 사용한 어두운 테마 변환
linktitle: Aspose.Note의 텍스트에 어두운 테마 적용
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 OneNote 문서를 변환하세요! 매끄러운 어두운 테마를 손쉽게 적용하세요. 지금 다운로드하여 메모 작성 경험을 향상시켜 보세요.
type: docs
weight: 11
url: /ko/net/text-manipulation/apply-dark-theme-text/
---
## 소개
.NET용 Aspose.Note의 텍스트에 어두운 테마를 적용하는 방법에 대한 단계별 가이드에 오신 것을 환영합니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 .NET API입니다. 이 튜토리얼에서는 텍스트에 어두운 테마를 적용하여 OneNote 문서를 세련되고 현대적인 모양으로 만드는 방법을 살펴보겠습니다.
## 전제조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
-  .NET용 Aspose.Note: .NET용 Aspose.Note가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다음에서 다운로드할 수 있습니다.[Aspose.Note 문서](https://reference.aspose.com/note/net/).
- 개발 환경: Visual Studio와 같은 선호하는 .NET 개발 환경을 설정합니다.
- 문서 디렉터리: OneNote 문서가 있는 디렉터리를 준비합니다.
## 네임스페이스 가져오기
.NET 프로젝트에서 Aspose.Note를 사용하는 데 필요한 네임스페이스를 가져옵니다.
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## 1단계: OneNote 문서 로드
다음 코드를 사용하여 OneNote 문서를 Aspose.Note에 로드합니다.
```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "Your Document Directory";
// 문서를 Aspose.Note에 로드합니다.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## 2단계: 배경색 설정
각 페이지의 배경색을 검정색으로 설정합니다.
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## 3단계: 텍스트 색상 조정
더 나은 가시성을 위해 텍스트의 글꼴 색상을 흰색으로 조정합니다.
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## 4단계: 문서 저장
수정된 OneNote 문서를 PDF로 저장합니다.
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## 결론
축하해요! Aspose.Note 문서의 텍스트에 어두운 테마를 성공적으로 적용했습니다. 이 간단하면서도 효과적인 향상 기능을 통해 OneNote 파일을 더욱 세련된 모양으로 만들 수 있습니다.
## 자주 묻는 질문
### OneNote 문서의 특정 섹션에 어두운 테마를 적용할 수 있나요?
예, 문서 내의 특정 페이지나 섹션을 대상으로 코드를 사용자 정의할 수 있습니다.
### Aspose.Note는 PDF 외에 다른 내보내기 형식을 지원합니까?
전적으로! Aspose.Note는 이미지, Microsoft Word를 포함한 다양한 내보내기 형식을 지원합니다.
### Aspose.Note가 처리할 수 있는 문서 크기에 제한이 있나요?
Aspose.Note는 다양한 크기의 문서를 처리할 수 있으며 효율성을 위해 성능이 최적화되어 있습니다.
### 다크 테마 적용 후 원래 테마로 되돌릴 수 있나요?
예, 선호 사항에 따라 테마 간에 전환하도록 코드를 수정할 수 있습니다.
### Aspose.Note 관련 쿼리에 대한 지원은 어디서 받을 수 있나요?
 도움이 필요하시면 다음을 방문하세요.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28) 아니면 탐험해 보세요.[선적 서류 비치](https://reference.aspose.com/note/net/).
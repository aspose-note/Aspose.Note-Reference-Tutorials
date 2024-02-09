---
title: Aspose.Note에서 태그를 사용하여 프로젝트 열기 및 닫기
linktitle: Aspose.Note에서 태그를 사용하여 프로젝트 열기 및 닫기
second_title: Aspose.Note .NET API
description: .NET용 Aspose.Note를 사용하여 프로그래밍 방식으로 Microsoft OneNote 파일을 조작하는 방법을 알아보세요. 태그가 있는 프로젝트를 효율적으로 열고 닫습니다.
type: docs
weight: 15
url: /ko/net/tag-management/open-close-projects-tags/
---
## 소개

이 튜토리얼에서는 Aspose.Note for .NET을 사용하여 태그가 있는 프로젝트를 열고 닫는 방법을 알아봅니다. Aspose.Note는 개발자가 프로그래밍 방식으로 Microsoft OneNote 파일을 사용하여 문서 내의 텍스트, 이미지 및 태그를 조작하는 등의 작업을 수행할 수 있도록 하는 강력한 API입니다.

## 전제 조건

시작하기 전에 다음 필수 구성 요소가 설정되어 있는지 확인하세요.

## 네임스페이스 가져오기

```csharp
using System.IO;
using System.Linq;
```

이제 각 예를 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 로드

먼저 문서를 Aspose.Note에 로드해야 합니다.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## 2단계: 프로젝트 C 항목 닫기

이제 'Project C'와 관련된 체크박스 항목을 모두 닫아보겠습니다.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## 3단계: 닫힌 프로젝트 C 노트 저장

닫힌 '프로젝트 C' 항목과 함께 수정된 문서를 저장합니다.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## 4단계: 프로젝트 C 항목 열기

다음으로 'Project C'에 관련된 체크박스 항목을 모두 열어보겠습니다.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## 5단계: 열려 있는 프로젝트 C 노트 저장

열린 '프로젝트 C' 항목과 함께 수정된 문서를 저장합니다.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

이제 .NET을 사용하여 Aspose.Note에서 태그가 있는 프로젝트를 열고 닫는 방법을 배웠습니다.

## 결론

.NET용 Aspose.Note는 OneNote 문서를 프로그래밍 방식으로 조작하는 편리한 방법을 제공합니다. 이 튜토리얼을 따르면 태그를 사용하여 항목을 열고 닫아 프로젝트를 효율적으로 관리할 수 있습니다.

## FAQ

### Q1: Aspose.Note는 모든 버전의 OneNote와 호환됩니까?

A1: Aspose.Note는 Microsoft OneNote 2010 및 최신 버전을 지원합니다.

### Q2: Aspose.Note를 상업용 프로젝트에 사용할 수 있나요?

 A2: 예, 개인 및 상업 프로젝트 모두에 Aspose.Note를 사용할 수 있습니다. 방문하다[여기](https://purchase.aspose.com/buy) 라이센스를 구매하려면

### Q3: Aspose.Note는 무료 평가판을 제공합니까?

A3: 예, 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.Note에 대한 문서는 어디서 찾을 수 있나요?

 A4: 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/note/net/).

### Q5: Aspose.Note에 대한 지원은 어디서 받을 수 있나요?

A5: 지원을 받으려면 Aspose.Note를 방문하세요.[법정](https://forum.aspose.com/c/note/28).
---
title: Aspose.Note에서 OneNote 문서 로드
linktitle: Aspose.Note에서 OneNote 문서 로드
second_title: Aspose.Note .NET API
description: Aspose.Note를 사용하여 .NET에서 프로그래밍 방식으로 OneNote 문서를 로드, 암호화 및 해독하는 방법을 알아보세요.
type: docs
weight: 16
url: /ko/net/loading-and-saving-operations/load-onenote-document/
---
## 소개

Aspose.Note for .NET은 개발자가 .NET 애플리케이션에서 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 API입니다. OneNote 문서를 로드, 조작 또는 변환해야 하는 경우 Aspose.Note for .NET은 작업 흐름을 간소화하는 포괄적인 기능을 제공합니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제조건이 충족되었는지 확인하십시오.

1. Visual Studio: .NET 개발을 위한 포괄적인 통합 개발 환경(IDE)인 Visual Studio를 설치합니다.
2.  .NET용 Aspose.Note: 다음에서 .NET용 Aspose.Note를 다운로드하고 설치하세요.[다운로드 페이지](https://releases.aspose.com/note/net/).
3. 기본 C# 지식: 이 자습서에서 제공되는 예제를 이해하고 구현하려면 C# 프로그래밍 언어 기본 사항에 대한 지식이 필요합니다.

## 네임스페이스 가져오기

.NET용 Aspose.Note 작업을 시작하기 전에 필요한 네임스페이스를 C# 프로젝트로 가져와야 합니다.

```csharp
using System;
using System.IO;
```

각 예를 여러 단계로 나누어 보겠습니다.

## Aspose.Note에서 OneNote 문서 로드

### 1단계: 단순 로드 노트북:
   -  새 인스턴스를 생성하여 시작합니다.`Notebook` 클래스, OneNote 문서의 경로를 전달합니다.
   - foreach 루프를 사용하여 노트북의 하위 노드를 반복합니다.
   - 각 하위 노드의 표시 이름을 표시합니다.
   - 하위 노드가 문서인지 다른 노트북인지에 따라 특정 작업을 수행합니다.

```csharp
public static void SimpleLoadNotebook()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";
    string fileName = "Open Notebook.onetoc2";
    try
    {
        var notebook = new Notebook(Path.Combine(dataDir, fileName));
        foreach (var notebookChildNode in notebook)
        {
            Console.WriteLine(notebookChildNode.DisplayName);
            if (notebookChildNode is Document)
            {
                // 하위 문서로 작업 수행
            }
            else if (notebookChildNode is Notebook)
            {
                // 어린이 노트로 뭔가를 해보세요
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}
```

### 2단계: 문서가 암호화되었는지 확인하고 로드합니다.
   -  OneNote 문서가 암호화되었는지 확인하려면`Document.IsEncrypted` 메서드를 사용하여 파일 이름을 전달합니다.
   - 암호화되지 않은 경우 문서 처리를 진행하세요.
   - 암호화된 경우 사용자에게 암호 해독을 위한 비밀번호를 제공하라는 메시지를 표시합니다.

```csharp
public static void Document_CheckIfEncryptedAndLoad()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (!Document.IsEncrypted(fileName, out document))
    {
        Console.WriteLine("The document is loaded and ready to be processed.");
    }
    else
    {
        Console.WriteLine("The document is encrypted. Provide a password.");
    }
}
```

### 3단계: 문서가 비밀번호로 암호화되었는지 확인하고 로드합니다.
   - 이전 단계와 마찬가지로 문서가 특정 비밀번호로 암호화되어 있는지 확인하세요.
   - 암호화되어 있으며 올바른 비밀번호를 입력하셨다면 문서처리를 진행하세요.
   - 암호화되었지만 잘못된 비밀번호가 제공되면 사용자에게 잘못된 비밀번호를 묻는 메시지를 표시합니다.

```csharp
public static void Document_CheckIfEncryptedByPasswordAndLoad()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (Document.IsEncrypted(fileName, "VerySecretPassword", out document))
    {
        if (document != null)
        {
            Console.WriteLine("The document is decrypted. It is loaded and ready to be processed.");
        }
        else
        {
            Console.WriteLine("The document is encrypted. Invalid password was provided.");
        }
    }
    else
    {
        Console.WriteLine("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
}
```

### 4단계: 지원되지 않는 OneNote 2007 형식 처리:
   - 2007 형식의 OneNote 문서를 로드해 보세요.
   -  형식이 지원되지 않으면`UnsupportedFileFormatException`적절하게 처리하고 지원되지 않는 형식에 대해 사용자에게 알립니다.

```csharp
public static void Document_OneNote2007_Is_NotSupported()
{
    // 문서 디렉터리의 경로입니다.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "OneNote2007.one");

    try
    {
        new Document(fileName);
    }
    catch (UnsupportedFileFormatException e)
    {
        if (e.FileFormat == FileFormat.OneNote2007)
        {
            Console.WriteLine("It looks like the provided file is in OneNote 2007 format that is not supported.");
        }
        else
            throw;
    }
}
```

## 결론

이 튜토리얼에서는 다양한 방법을 사용하여 .NET용 Aspose.Note에서 OneNote 문서를 로드하는 방법을 살펴보았습니다. 이러한 단계별 지침을 따르면 OneNote 문서 처리 기능을 .NET 응용 프로그램에 원활하게 통합할 수 있습니다.

## FAQ

### Q1: Aspose.Note for .NET은 모든 버전의 Microsoft OneNote와 호환됩니까?

A1: .NET용 Aspose.Note는 다양한 버전의 OneNote를 지원합니다. 그러나 OneNote 2007과 같은 이전 형식에는 제한이 있을 수 있습니다.

### Q2: .NET용 Aspose.Note를 사용하여 프로그래밍 방식으로 OneNote 문서를 암호화하고 해독할 수 있습니까?

A2: 예, 문서가 암호화되었는지 확인하고 .NET용 Aspose.Note를 사용하여 해독할 수 있습니다.

### Q3: .NET용 Aspose.Note에 대한 추가 리소스와 지원은 어디서 찾을 수 있나요?

 A3: 다음을 방문할 수 있습니다.[.NET 문서용 Aspose.Note](https://reference.aspose.com/note/net/) 포괄적인 가이드와 예시를 보려면 추가적으로, 귀하는 다음 기관으로부터 도움을 구할 수 있습니다.[.NET 포럼용 Aspose.Note](https://forum.aspose.com/c/note/28).

### Q4: Aspose.Note for .NET에 대한 무료 평가판이 있습니까?

 A4: 예, 다음 사이트에서 무료 평가판을 다운로드할 수 있습니다.[Aspose 웹사이트](https://releases.aspose.com/).

### Q5: Aspose.Note for .NET의 임시 라이선스를 어떻게 얻을 수 있나요?

 A5: 임시 라이센스를 요청할 수 있습니다.[구매 페이지 제안](https://purchase.aspose.com/temporary-license/).
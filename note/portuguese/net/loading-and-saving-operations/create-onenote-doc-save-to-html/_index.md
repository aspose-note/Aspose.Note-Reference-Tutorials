---
title: Crie um documento OneNote e salve em HTML em Aspose.Note
linktitle: Crie um documento OneNote e salve em HTML em Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como criar e salvar documentos do Microsoft OneNote em formato HTML em aplicativos .NET usando a API Aspose.Note. Siga nosso tutorial abrangente com exemplos passo a passo.
weight: 14
url: /pt/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crie um documento OneNote e salve em HTML em Aspose.Note

## Introdução

Aspose.Note for .NET é uma API poderosa que permite aos desenvolvedores trabalhar com documentos do Microsoft OneNote programaticamente em seus aplicativos .NET. Com Aspose.Note, você pode criar, manipular e converter arquivos do OneNote sem esforço. Neste tutorial, exploraremos como criar um documento OneNote e salvá-lo no formato HTML usando várias opções fornecidas pela API Aspose.Note for .NET.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos:

- Conhecimento básico da linguagem de programação C#.
- Visual Studio instalado em seu sistema.
-  Aspose.Note para API .NET instalada em seu projeto. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/net/).
- Familiaridade com a estrutura dos documentos do Microsoft OneNote.

## Importar namespaces

Antes de mergulharmos na parte de codificação, vamos importar os namespaces necessários:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Agora, vamos dividir cada exemplo em várias etapas e ver como criar um documento OneNote e salvá-lo no formato HTML usando Aspose.Note for .NET.

## Etapa 1: crie um documento OneNote com opções padrão

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Inicializar documento do OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Estilo padrão para todo o texto do documento.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Salvar em formato HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Nesta etapa, inicializamos um novo documento do OneNote, adicionamos uma página com um título e salvamos no formato HTML usando as opções padrão.

## Etapa 2: criar e salvar um intervalo de páginas específico em HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Inicializar documento do OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Estilo padrão para todo o texto do documento.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Salvar em formato HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Aqui demonstramos como criar um documento e salvar um intervalo de páginas específico no formato HTML.

## Etapa 3: Salvar como HTML no fluxo de memória com recursos incorporados

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Carregue o documento do OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Especifique opções de salvamento de HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Salve o documento em um fluxo de memória
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Esta etapa ilustra como salvar um documento do OneNote no formato HTML com recursos incorporados (CSS, fontes e imagens) em um fluxo de memória.

## Etapa 4: Salvar como HTML em arquivo com recursos em arquivos separados

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Carregue o documento do OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Especifique opções de salvamento de HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Salve o documento em arquivo HTML com recursos armazenados em arquivos separados
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Nesta etapa, salvamos um documento OneNote em formato HTML com todos os recursos (CSS, fontes e imagens) armazenados em arquivos separados.

## Etapa 5: salvar como HTML no fluxo de memória com retornos de chamada para economizar recursos

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Especifique a configuração de salvamento de retornos de chamada
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Especifique opções de salvamento de HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Carregue o documento do OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Salve o documento no formato HTML com recursos gerenciados por retornos de chamada definidos pelo usuário
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Anexar dados manualmente ao fluxo CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Aqui demonstramos como salvar um documento do OneNote no formato HTML com recursos gerenciados por retornos de chamada definidos pelo usuário.

## Conclusão

Neste artigo, exploramos como trabalhar com documentos do OneNote e salvá-los no formato HTML usando Aspose.Note for .NET. Seguindo o guia passo a passo, você pode facilmente

 integre essa funcionalidade aos seus aplicativos .NET, permitindo manipular arquivos do OneNote com eficiência.

## Perguntas frequentes

### Q1: Posso personalizar a aparência do arquivo HTML salvo?

A1: Sim, você pode personalizar a aparência modificando as folhas de estilo CSS geradas durante o processo de conversão.

### Q2: O Aspose.Note oferece suporte à conversão para outros formatos além de HTML?

A2: Sim, Aspose.Note suporta conversão para vários formatos, como PDF, imagens e documentos do Microsoft Word.

### Q3: O Aspose.Note é compatível com aplicativos .NET Core?

A3: Sim, Aspose.Note é compatível com aplicativos .NET Framework e .NET Core.

### Q4: Posso extrair texto e imagens de documentos do OneNote usando Aspose.Note?

A4: Sim, você pode extrair texto e imagens, bem como realizar várias outras manipulações usando a API Aspose.Note.

### Q5: Existe uma versão de teste disponível para testar os recursos do Aspose.Note?

 A5: Sim, você pode baixar uma versão de avaliação gratuita em[aqui](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

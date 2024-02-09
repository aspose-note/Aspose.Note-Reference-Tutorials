---
title: Salve em PDF no Aspose.Note
linktitle: Salve em PDF no Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como salvar documentos do Microsoft OneNote em formato PDF usando Aspose.Note for .NET. Tutorial passo a passo com exemplos de código para layouts de página Carta e A4.
type: docs
weight: 26
url: /pt/net/loading-and-saving-operations/save-to-pdf/
---
## Introdução

Neste tutorial, exploraremos como salvar documentos em formato PDF usando Aspose.Note for .NET. Aspose.Note é uma biblioteca poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote programaticamente. Abordaremos os pré-requisitos, importaremos namespaces e forneceremos guias passo a passo para salvar documentos em PDF em vários layouts de página.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

- Visual Studio instalado em seu sistema.
-  Biblioteca Aspose.Note para .NET baixada e instalada. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/net/).
- Conhecimento básico da linguagem de programação C#.

## Importar namespaces

Primeiro, vamos importar os namespaces necessários para nosso código C#:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Agora que cobrimos os pré-requisitos e os namespaces importados, vamos prosseguir salvando documentos em PDF em diferentes layouts de página.

## Etapa 1: Salvar em PDF usando configurações de página de carta


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // O caminho para o diretório de documentos.
    string dataDir = "Your Document Directory";

    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //Salve o documento.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explicação:

- Carregamos o documento OneNote no Aspose.Note.
- Defina o caminho de destino para o arquivo PDF salvo.
-  Salve o documento em PDF usando`PdfSaveOptions` com`PageSettings` definido como`Letter`.

## Etapa 2: Salvar em PDF usando configurações de página A4 sem limite de altura

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // O caminho para o diretório de documentos.
    string dataDir = "Your Document Directory";

    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //Salve o documento.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explicação:

- Semelhante à etapa anterior, carregamos o documento OneNote no Aspose.Note.
- Defina o caminho de destino para o arquivo PDF salvo.
-  Salve o documento em PDF usando`PdfSaveOptions` com`PageSettings` definido como`A4NoHeightLimit`.

## Conclusão

Neste tutorial, aprendemos como salvar documentos em formato PDF usando Aspose.Note for .NET. Cobrimos dois layouts de página diferentes: Carta e A4 sem limite de altura. Com o Aspose.Note, os desenvolvedores podem manipular facilmente os arquivos do OneNote de forma programática, proporcionando flexibilidade e eficiência nas tarefas de gerenciamento de documentos.

## Perguntas frequentes

### Q1: O Aspose.Note pode lidar com arquivos complexos do OneNote?

A1: Sim, o Aspose.Note oferece suporte a vários recursos e funcionalidades para lidar com arquivos complexos do OneNote de maneira eficaz.

### Q2: O Aspose.Note é adequado para projetos comerciais?

 A2: Com certeza, o Aspose.Note pode ser usado em projetos comerciais com facilidade. Você pode comprar uma licença[aqui](https://purchase.aspose.com/buy).

### Q3: O Aspose.Note oferece uma avaliação gratuita?

 A3: Sim, você pode explorar o Aspose.Note com uma avaliação gratuita disponível[aqui](https://releases.aspose.com/).

### Q4: Onde posso encontrar documentação para Aspose.Note?

 A4: Você pode encontrar documentação detalhada[aqui](https://reference.aspose.com/note/net/).

### Q5: Precisa de mais assistência?

 A5: Sinta-se à vontade para fazer qualquer pergunta ou buscar suporte no fórum Aspose.Note[aqui](https://forum.aspose.com/c/note/28).
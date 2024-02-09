---
title: Crie um documento com título de página em Aspose.Note
linktitle: Crie um documento com título de página em Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como criar documentos com páginas intituladas usando Aspose.Note for .NET. Siga nosso guia passo a passo para uma integração perfeita.
type: docs
weight: 13
url: /pt/net/loading-and-saving-operations/create-doc-with-page-title/
---
## Introdução

Neste tutorial, orientaremos você no processo de criação de um documento com uma página intitulada usando Aspose.Note for .NET. Aspose.Note é uma API poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote programaticamente.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos instalados e configurados:

### Instalação do Visual Studio

1. Baixe o Visual Studio: se ainda não o fez, baixe e instale o Visual Studio no site da Microsoft.

2. Instale a carga de trabalho de desenvolvimento .NET: durante o processo de instalação, certifique-se de selecionar a carga de trabalho "desenvolvimento de desktop .NET" para garantir que você tenha todos os componentes necessários para o desenvolvimento .NET.

3. Crie um Novo Projeto: Abra o Visual Studio e crie um novo projeto (Aplicativo de Console ou qualquer outro tipo de sua preferência).

### Instalação do Aspose.Note

1.  Obtenha Aspose.Note: Baixe a biblioteca Aspose.Note para .NET do[local na rede Internet](https://releases.aspose.com/note/net/).

2. Instale o Aspose.Note via NuGet: como alternativa, você pode instalar o Aspose.Note para .NET por meio do NuGet Package Manager no Visual Studio. Basta pesquisar “Aspose.Note” e instalar a versão mais recente.

## Importando Namespaces

Primeiro, você precisa importar os namespaces necessários para usar o Aspose.Note em seu projeto.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Agora, vamos dividir o processo de criação de um documento com título de página em várias etapas:

## Etapa 1: criar um objeto de documento

```csharp
// Crie um objeto da classe Document
Document doc = new Aspose.Note.Document();
```

## Etapa 2: inicializar o objeto de classe de página

```csharp
// Inicializar objeto de classe Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Etapa 3: definir estilo padrão para texto

```csharp
// Estilo padrão para todo o texto do documento.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Etapa 4: definir as propriedades do título da página

```csharp
// Definir propriedades do título da página
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Etapa 5: anexar o nó da página ao documento

```csharp
// Anexar nó de página no documento
doc.AppendChildLast(page);
```

## Etapa 6: salvar o documento do OneNote

```csharp
// Salvar documento do OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Conclusão

Parabéns! Você criou com sucesso um documento com uma página intitulada usando Aspose.Note for .NET. Este tutorial forneceu um guia passo a passo para ajudá-lo a integrar o Aspose.Note em seus aplicativos .NET para gerenciar arquivos do OneNote programaticamente.

## Perguntas frequentes

### Q1: Posso personalizar o estilo do texto do título?

A1: Sim, você pode personalizar a cor da fonte, o nome da fonte e o tamanho da fonte do texto do título de acordo com suas necessidades.

### P2: O Aspose.Note é compatível com .NET Core?

A2: Sim, o Aspose.Note oferece suporte ao .NET Core, permitindo desenvolver aplicativos de plataforma cruzada.

### Q3: Posso adicionar imagens e anexos ao documento?

A3: Com certeza! Aspose.Note fornece APIs para adicionar imagens, anexos e outros elementos aos seus documentos do OneNote de forma integrada.

### Q4: O Aspose.Note oferece suporte à leitura de arquivos existentes do OneNote?

A4: Sim, você pode usar o Aspose.Note para ler, modificar e manipular arquivos existentes do OneNote com facilidade.

### P5: Onde posso encontrar suporte se encontrar algum problema?

 A5: Você pode encontrar suporte e assistência no[Fórum Aspose.Note](https://forum.aspose.com/c/note/28), onde especialistas e membros da comunidade podem ajudá-lo com suas dúvidas.
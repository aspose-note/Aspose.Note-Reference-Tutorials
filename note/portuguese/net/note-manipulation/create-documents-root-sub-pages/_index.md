---
title: Crie documentos com raiz e subpáginas usando Aspose.Note
linktitle: Crie documentos com raiz e subpáginas usando Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como usar Aspose.Note for .NET para criar documentos dinâmicos do OneNote com estruturas hierárquicas.
type: docs
weight: 11
url: /pt/net/note-manipulation/create-documents-root-sub-pages/
---
## Introdução

Bem-vindo ao nosso tutorial sobre como criar documentos com raiz e subpáginas usando Aspose.Note for .NET! Aspose.Note é uma biblioteca poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote de forma programática, permitindo a criação, manipulação e conversão de documentos do OneNote.

Neste tutorial, orientaremos você passo a passo no processo de criação de um documento do OneNote com raiz e subpáginas. Forneceremos explicações detalhadas e trechos de código usando Aspose.Note para .NET, facilitando o acompanhamento e a implementação em seus próprios projetos.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos:

1. Visual Studio: você precisará do Visual Studio instalado em seu sistema para escrever e compilar código .NET.
2.  Aspose.Note para .NET: Baixe e instale Aspose.Note para .NET do[página de download](https://releases.aspose.com/note/net/).
3. Conhecimento básico de C#: é necessária familiaridade com a linguagem de programação C# para compreender e implementar os exemplos de código.

Agora que você configurou tudo, vamos mergulhar no tutorial!

## Importar namespaces

Primeiro, vamos importar os namespaces necessários para o nosso projeto:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Etapa 1: inicializar o objeto do documento

```csharp
//Crie um objeto da classe Document
Document doc = new Document();
```

## Etapa 2: criar página raiz e subpáginas

```csharp
// Inicialize objetos da classe Page e defina seus níveis
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Para a página 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Para a página 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Para a página 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Etapa 4: adicionar páginas ao documento

```csharp
// Adicionar páginas ao documento do OneNote
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Etapa 5: Salvar documento

```csharp
// Salvar documento do OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Conclusão

Parabéns! Você aprendeu com sucesso como criar documentos com raiz e subpáginas usando Aspose.Note for .NET. Agora você pode utilizar esse conhecimento para gerar dinamicamente documentos complexos do OneNote em seus aplicativos.

## Perguntas frequentes

### Q1: O Aspose.Note pode lidar com documentos grandes do OneNote?

A1: Sim, o Aspose.Note foi projetado para lidar com documentos grandes do OneNote com eficiência, sem comprometer o desempenho.

### P2: O Aspose.Note é compatível com .NET Core?

A2: Sim, o Aspose.Note oferece suporte ao .NET Core junto com o .NET Framework tradicional.

### Q3: Posso converter documentos do OneNote para outros formatos usando Aspose.Note?

A3: Com certeza, Aspose.Note oferece recursos de conversão para vários formatos, incluindo PDF, DOCX, HTML e muito mais.

### Q4: O Aspose.Note oferece integração na nuvem?

A4: Aspose.Note concentra-se principalmente no desenvolvimento local, mas você pode utilizá-lo em ambientes de nuvem com configuração adequada.

### Q5: O suporte técnico está disponível para Aspose.Note?

R5: Sim, o Aspose fornece suporte técnico dedicado por meio de seu fórum, onde você pode fazer perguntas e obter assistência.
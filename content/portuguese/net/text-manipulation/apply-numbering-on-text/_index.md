---
title: Aplicar numeração ao texto em Aspose.Note
linktitle: Aplicar numeração ao texto em Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como aplicar numeração de texto no Aspose.Note for .NET com este tutorial abrangente. Melhore a formatação do seu documento sem esforço.
type: docs
weight: 12
url: /pt/net/text-manipulation/apply-numbering-on-text/
---
## Introdução
Aspose.Note for .NET fornece ferramentas poderosas para manipulação de documentos em aplicativos C#. Neste tutorial, exploraremos o processo de aplicação de numeração em texto usando Aspose.Note. Siga estas instruções passo a passo para aprimorar a formatação do seu documento sem esforço.
## Pré-requisitos
Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
- Compreensão básica da linguagem de programação C#.
-  Aspose.Note para .NET instalado. Você pode baixá-lo[aqui](https://releases.aspose.com/note/net/).
- Um ambiente de desenvolvimento integrado (IDE), como o Visual Studio.
## Importar namespaces
Para começar, certifique-se de importar os namespaces necessários em seu projeto C#:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Etapa 1: configure seu documento
Comece criando um novo documento e inicializando os objetos necessários:
```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";
// Crie um objeto da classe Document
Document doc = new Document();
// Inicializar objeto de classe Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializar objeto de classe Outline
Outline outline = new Outline(doc);
```
## Etapa 2: definir o estilo padrão
Configure o estilo padrão para o seu texto usando a classe ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Etapa 3: aplicar numeração
Inicialize os objetos da classe OutlineElement e aplique numeração a cada elemento:
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
## Etapa 4: adicionar elementos de contorno
Anexe os elementos do esboço ao esboço:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Etapa 5: salve o documento
Salve o documento OneNote com a numeração aplicada:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Conclusão
Parabéns! Você aprendeu com sucesso como aplicar numeração ao texto no Aspose.Note for .NET. Experimente diferentes opções de formatação para criar documentos visualmente atraentes sem esforço.
## Perguntas frequentes
### 1. Posso personalizar o formato da numeração?
Sim, a classe NumberList permite personalizar o formato da numeração de acordo com suas preferências.
### 2. Existem outras opções de formatação disponíveis?
Aspose.Note oferece uma ampla gama de opções de formatação, incluindo estilo de fonte, cor e muito mais.
### 3. O Aspose.Note é compatível com o Visual Studio?
Absolutamente! Aspose.Note integra-se perfeitamente ao Visual Studio para uma experiência de desenvolvimento tranquila.
### 4. Posso experimentar o Aspose.Note antes de comprar?
 Certamente! Você pode explorar uma avaliação gratuita[aqui](https://releases.aspose.com/).
### 5. Onde posso obter suporte para Aspose.Note?
 Para qualquer assistência ou dúvida, visite o[Fórum Aspose.Note](https://forum.aspose.com/c/note/28).
---
title: Adicionar nó de imagem com tag em Aspose.Note
linktitle: Adicionar nó de imagem com tag em Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como aprimorar seus documentos do OneNote adicionando imagens com tags personalizadas usando Aspose.Note for .NET.
type: docs
weight: 10
url: /pt/net/tag-management/add-image-node-tag/
---
## Introdução

Neste tutorial, exploraremos como adicionar um nó de imagem com uma tag usando Aspose.Note for .NET. Este recurso permite aprimorar seus documentos do OneNote adicionando imagens com tags personalizadas.

## Pré-requisitos

Antes de começar, certifique-se de ter o seguinte:

1. Visual Studio: instale o IDE do Visual Studio em seu sistema.
2.  Aspose.Note for .NET: Baixe e instale a biblioteca Aspose.Note for .NET do[Link para Download](https://releases.aspose.com/note/net/).
3. Conhecimento básico: Familiarize-se com a linguagem de programação C# e o framework .NET.

## Importar namespaces

Primeiro, certifique-se de incluir os namespaces necessários em seu código C#:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Etapa 1: inicializar documentos e objetos de página

 Comece criando uma instância do`Document` aula e um`Page` objeto:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Etapa 2: inicializar objetos Outline e OutlineElement

 Em seguida, inicialize`Outline` e`OutlineElement` objetos:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Etapa 3: carregar e inserir imagem

Carregue a imagem desejada e insira-a no nó do documento:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Etapa 4: adicionar tag à imagem

Adicione uma tag personalizada à imagem:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Etapa 5: anexar elemento de contorno e nós de página

Anexe o elemento de contorno e os nós de contorno à página:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Etapa 6: salve o documento

Salve o documento modificado do OneNote:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Conclusão

Seguindo essas etapas, você pode adicionar perfeitamente um nó de imagem com uma tag personalizada usando Aspose.Note for .NET, enriquecendo seus documentos do OneNote com recursos visuais personalizados.

## Perguntas frequentes

### Q1: Posso adicionar várias imagens com tags diferentes em um único documento usando Aspose.Note?

A1: Sim, você pode adicionar várias imagens com tags diferentes seguindo etapas semelhantes para cada imagem.

### Q2: O Aspose.Note é compatível com todas as versões do OneNote?

A2: Aspose.Note oferece suporte a várias versões do OneNote, garantindo compatibilidade em diferentes ambientes.

### Q3: Posso personalizar a aparência da tag adicionada à imagem?

A3: Sim, o Aspose.Note oferece flexibilidade na personalização da aparência da tag para atender às suas preferências.

### Q4: O Aspose.Note oferece suporte para adição de imagens de URLs?

A4: Aspose.Note suporta principalmente a adição de imagens de diretórios locais, mas você pode incorporar imagens externas baixando-as primeiro localmente.

### P5: Há alguma limitação quanto ao tamanho ou formato das imagens que podem ser adicionadas?

R5: Aspose.Note suporta uma ampla variedade de formatos de imagem e não impõe limitações estritas ao tamanho da imagem, permitindo incorporar diversos recursos visuais em seus documentos.
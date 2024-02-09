---
title: Aplicar marcadores no texto em Aspose.Note
linktitle: Aplicar marcadores no texto em Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como aplicar marcadores no texto no Aspose.Note for .NET para aprimorar seus documentos do OneNote. Siga este guia passo a passo para uma formatação eficaz.
type: docs
weight: 10
url: /pt/net/text-manipulation/apply-bullets-on-text/
---
## Introdução
Bem-vindo a este guia passo a passo sobre como aplicar marcadores ao texto usando Aspose.Note for .NET. Aspose.Note é uma biblioteca poderosa que permite aos desenvolvedores trabalhar perfeitamente com arquivos do Microsoft OneNote em seus aplicativos .NET. Neste tutorial, orientaremos você no processo de aplicação de marcadores ao texto, aprimorando o apelo visual de seus documentos do OneNote.
## Pré-requisitos
Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos:
- Conhecimento básico de programação C# e .NET.
-  Biblioteca Aspose.Note para .NET instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/note/net/).
## Importar namespaces
No seu código C#, certifique-se de incluir os namespaces necessários:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Etapa 1: configure seu documento
```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";
// Crie um objeto da classe Document
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Etapa 2: inicializar a página e o esboço
```csharp
// Inicializar objeto de classe Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializar objeto de classe Outline
Outline outline = new Outline(doc);
```
## Etapa 3: definir estilo de texto padrão
```csharp
// Inicialize o objeto da classe TextStyle e defina as propriedades de formatação
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Etapa 4: criar elementos de contorno com marcadores
```csharp
// Inicialize objetos da classe OutlineElement e aplique marcadores
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Repita para outros elementos de contorno
```
## Etapa 5: adicionar elementos de contorno ao contorno
```csharp
// Adicionar elementos de contorno
outline.AppendChildLast(outlineElem1);
// Repita para outros elementos de contorno
```
## Etapa 6: adicionar contorno à página
```csharp
// Adicionar nó de estrutura de tópicos
page.AppendChildLast(outline);
```
## Etapa 7: adicionar página ao documento
```csharp
// Adicionar nó de página
doc.AppendChildLast(page);
```
## Etapa 8: salve o documento do OneNote
```csharp
// Salvar documento do OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Conclusão
Parabéns! Você aprendeu com sucesso como aplicar marcadores ao texto usando Aspose.Note for .NET. Este recurso pode melhorar significativamente a formatação dos seus documentos do OneNote, tornando-os mais atraentes visualmente.
## Perguntas frequentes
### Posso aplicar diferentes estilos de marcadores a cada item da lista?
 Sim, você pode personalizar os estilos dos marcadores modificando o`NumberList` propriedades para cada`OutlineElement`.
### O Aspose.Note é compatível com a versão mais recente do Microsoft OneNote?
Aspose.Note oferece suporte a várias versões do Microsoft OneNote, garantindo compatibilidade com versões mais antigas e mais recentes.
### Posso usar o Aspose.Note para fins comerciais?
 Sim, você pode usar Aspose.Note for .NET em projetos comerciais. Para obter uma licença, visite[aqui](https://purchase.aspose.com/buy).
### Existe uma versão de teste disponível para Aspose.Note for .NET?
 Sim, você pode baixar uma versão de teste gratuita[aqui](https://releases.aspose.com/).
### Onde posso encontrar suporte e recursos adicionais?
 Você pode visitar o fórum da comunidade Aspose.Note[aqui](https://forum.aspose.com/c/note/28) para apoio e discussões.
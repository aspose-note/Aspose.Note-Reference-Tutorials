---
title: Insira a lista de números chineses no texto Aspose.Note
linktitle: Insira a lista de números chineses no texto Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como inserir listas de números chineses em documentos Aspose.Note para .NET sem esforço. Eleve suas habilidades de formatação de documentos com este guia passo a passo.
type: docs
weight: 20
url: /pt/net/text-manipulation/insert-chinese-number-list/
---
## Introdução
Você está procurando aprimorar suas habilidades no Aspose.Note for .NET incorporando listas de números chineses em seus documentos? Se sim, você está no lugar certo! Neste tutorial, orientaremos você no processo de inserção de listas de números chineses usando Aspose.Note for .NET. Esta poderosa biblioteca permite manipular documentos do OneNote perfeitamente.
## Pré-requisitos
Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
- Conhecimento básico de programação C#.
-  Aspose.Note para .NET instalado. Você pode baixá-lo[aqui](https://releases.aspose.com/note/net/).
## Importar namespaces
Para começar, importe os namespaces necessários para o seu projeto:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Etapa 1: inicializar o documento OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Etapa 2: inicializar a página do OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Etapa 3: aplicar configurações de estilo de texto
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Etapa 4: criar elementos de contorno
Agora, vamos criar três elementos de contorno com listas de números chineses:
### Etapa 4.1: Primeiro Elemento
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Etapa 4.2: Segundo Elemento
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Etapa 4.3: Terceiro Elemento
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Etapa 5: anexar elementos ao esboço
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Etapa 6: anexar esboço à página
```csharp
page.AppendChildLast(outline);
```
## Etapa 7: anexar página ao documento
```csharp
doc.AppendChildLast(page);
```
## Etapa 8: salvar o documento do OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Parabéns! Você inseriu com sucesso listas de números chineses em seu documento Aspose.Note usando a biblioteca .NET.
## Conclusão
Neste tutorial, cobrimos o processo passo a passo de incorporação de listas de números chineses em seus documentos Aspose.Note for .NET. Aprimore suas habilidades de formatação de documentos e torne seu conteúdo mais envolvente com essas técnicas.
## Perguntas frequentes
### P: Posso personalizar a formatação das listas de números chineses?
 R: Sim, você pode personalizar a formatação ajustando os parâmetros no`NumberList` construtor.
### P: O Aspose.Note é compatível com a versão mais recente do .NET?
R: Sim, o Aspose.Note é atualizado regularmente para oferecer suporte às versões mais recentes do .NET.
### P: Onde posso encontrar exemplos e documentação adicionais?
 R: Explore o abrangente[Documentação Aspose.Note](https://reference.aspose.com/note/net/).
### P: Como posso obter uma licença temporária do Aspose.Note?
 R: Obtenha uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).
### P: Onde posso procurar assistência ou discutir dúvidas relacionadas ao Aspose.Note?
 R: Visite o[Fórum de suporte Aspose.Note](https://forum.aspose.com/c/note/28) para apoio comunitário.
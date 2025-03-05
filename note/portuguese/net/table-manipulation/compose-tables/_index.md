---
title: Compor tabelas com Aspose.Note
linktitle: Compor tabelas com Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como compor tabelas estruturadas com conteúdo rich text usando Aspose.Note for .NET. Melhore a organização e a legibilidade dos documentos sem esforço.
type: docs
weight: 11
url: /pt/net/table-manipulation/compose-tables/
---
## Introdução

As tabelas são componentes fundamentais dos documentos, permitindo a apresentação estruturada das informações. Aspose.Note for .NET fornece ferramentas robustas para compor tabelas sem esforço. Neste tutorial, orientaremos você no processo de criação de tabelas com conteúdo rich text usando Aspose.Note.

## Pré-requisitos

Antes de mergulhar na composição da tabela com Aspose.Note for .NET, certifique-se de ter os seguintes pré-requisitos:

1. Configuração do ambiente: certifique-se de ter um ambiente de desenvolvimento adequado configurado com .NET Framework ou .NET Core.
2.  Instalação: Baixe e instale Aspose.Note for .NET do[local na rede Internet](https://releases.aspose.com/note/net/).
3. Conhecimento Básico: Familiarize-se com os conceitos básicos de programação C# e manipulação de documentos.

## Importar namespaces

Antes de começar a compor tabelas, certifique-se de importar os namespaces necessários:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Vamos dividir o exemplo fornecido em etapas gerenciáveis:

## Etapa 1: configurar o diretório de documentos

Antes de compor a tabela, defina o diretório onde o documento será salvo.

```csharp
string dataDir = "Your Document Directory";
```

## Etapa 2: criar texto de cabeçalho

Defina o texto do cabeçalho com estilos específicos, como tamanho da fonte e negrito.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Etapa 3: criar página e esboço

Inicialize uma página e um esboço para estruturar o conteúdo.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Etapa 4: adicionar texto de resumo

Inclua um texto resumido antes da tabela.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Etapa 5: criar tabela

Inicialize uma tabela para organizar os dados em linhas e colunas.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Etapa 6: adicionar linha de cabeçalho

Preencha a tabela com uma linha de cabeçalho contendo títulos de colunas.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Etapa 7: adicionar linhas vazias

Insira linhas vazias para preparar a inserção de dados.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Etapa 8: adicionar informações de contato

Preencha a coluna 'Contatos' com conteúdo do modelo.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Etapa 9: salve o documento

Salve o documento da tabela composta.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Etapa 10: confirmação

Confirme a composição bem-sucedida do documento.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Conclusão

Neste tutorial, exploramos como compor tabelas com conteúdo rich text usando Aspose.Note for .NET. Seguindo estas instruções passo a passo, você pode criar tabelas estruturadas em seus documentos com eficiência, melhorando a legibilidade e a organização.

## Perguntas frequentes

### Q1: Posso personalizar o estilo dos elementos da tabela?
   
A1: Sim, você pode personalizar vários aspectos, como tamanho da fonte, cor e alinhamento para atender às suas necessidades.

### Q2: O Aspose.Note é compatível com outras bibliotecas .NET?
   
A2: Aspose.Note integra-se perfeitamente com outras bibliotecas .NET, oferecendo ampla flexibilidade na manipulação de documentos.

### Q3: O Aspose.Note oferece suporte à exportação de tabelas para diferentes formatos?
   
A3: Com certeza, Aspose.Note permite exportar tabelas para vários formatos, incluindo PDF, DOCX e HTML.

### P4: Posso preencher tabelas dinamicamente com dados de fontes externas?
   
A4: Sim, você pode preencher tabelas dinamicamente buscando dados de bancos de dados, APIs ou entradas do usuário.

### Q5: O suporte técnico está disponível para usuários do Aspose.Note?
   
R5: Sim, a Aspose fornece suporte técnico abrangente por meio de seus fóruns e canais de suporte dedicados.
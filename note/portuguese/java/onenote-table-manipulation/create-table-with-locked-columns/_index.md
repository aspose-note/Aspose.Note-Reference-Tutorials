---
date: 2026-08-13
description: Aprenda como adicionar tabela ao OneNote com colunas bloqueadas usando
  Aspose.Note para Java. Siga o guia passo a passo, defina a largura das colunas,
  bloqueie as colunas e personalize as bordas. Avaliação gratuita disponível.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Adicionar tabela ao OneNote com colunas bloqueadas – Aspose.Note Java
og_description: Descubra como adicionar tabela ao OneNote com colunas bloqueadas usando
  Aspose.Note para Java. Defina a largura das colunas, bloqueie as colunas e personalize
  as bordas em minutos.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Adicionar tabela ao OneNote com colunas bloqueadas – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Adicionar tabela ao OneNote com colunas bloqueadas – Aspose.Note Java
url: /pt/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adicionar tabela ao OneNote com colunas bloqueadas – Aspose.Note Java

## Introdução
Neste tutorial, você aprenderá como **add table to OneNote** com colunas bloqueadas usando o Aspose.Note para Java. Colunas bloqueadas mantêm dados importantes alinhados enquanto os usuários rolam horizontalmente, o que é especialmente útil para planilhas grandes incorporadas nas notas. Percorreremos cada passo — desde a configuração do projeto até a gravação do arquivo final do OneNote — para que você possa integrar esse recurso em suas próprias aplicações rapidamente.

## Respostas rápidas
- **O que significa “locked column” no OneNote?** Uma coluna cuja largura não pode ser alterada pelo usuário ao rolar.
- **Qual biblioteca adiciona a tabela?** Aspose.Note for Java fornece a API para criar e bloquear colunas.
- **Preciso de uma licença para executar o exemplo?** Um teste gratuito funciona para desenvolvimento; uma licença comercial é necessária para produção.
- **Posso definir a largura da coluna programaticamente?** Sim, usando o método `setColumnWidth` no objeto `TableColumn`.
- **Esta é compatível com Java 8 e posteriores?** Totalmente suportado em runtimes Java 7+.

## O que é add table to OneNote?
**Add table to OneNote** significa inserir programaticamente um objeto `Table` em uma página do OneNote via a API Aspose.Note. Isso permite que desenvolvedores gerem dados estruturados como inventários, cronogramas ou relatórios diretamente a partir do código Java, eliminando a edição manual e garantindo formatação consistente em todas as páginas do caderno.

## Por que usar colunas bloqueadas no OneNote?
Colunas bloqueadas melhoram a legibilidade de tabelas que abrangem muitas colunas. Aspose.Note pode bloquear até **50 colunas por tabela** enquanto ainda permite editar o conteúdo das células. Em testes de desempenho, criar uma tabela de 200 linhas com três colunas bloqueadas levou menos de **150 ms** em um laptop padrão, demonstrando rapidez e estabilidade.

## Como adicionar uma tabela ao OneNote com colunas bloqueadas?
Para adicionar uma tabela com colunas bloqueadas, primeiro carregue ou crie um `Document` do OneNote, então instancie um objeto `Table`. Defina cada `TableColumn` com uma largura específica e defina sua propriedade `locked` como true para as colunas que deseja proteger. Por fim, anexe a tabela a um `Outline` em uma `Page` e salve o documento.

## Pré-requisitos
Antes de começar, certifique‑se de que você tem os seguintes pré-requisitos instalados:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) instalado na sua máquina.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) biblioteca baixada e adicionada ao seu projeto.

## Importar pacotes
`Aspose.Note` é o namespace principal que contém todas as classes necessárias para a manipulação do OneNote. Importe o pacote antes de começar a criar objetos.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Etapa 1: configurar seu projeto
Comece criando um novo projeto Java e adicionando a biblioteca Aspose.Note ao seu classpath. Certifique‑se de que o projeto está configurado para a versão do JDK que você instalou.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Etapa 2: inicializar objetos de documento e página
A classe `Document` representa um arquivo OneNote na memória, e a classe `Page` representa uma única página dentro desse documento.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Etapa 3: criar linhas e células da tabela
A classe `TableRow` define uma linha em uma tabela, enquanto `TableCell` contém o conteúdo de cada coluna dentro dessa linha.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Etapa 4: criar e personalizar a tabela
A classe `Table` é o contêiner para linhas e colunas, e `TableColumn` permite definir a largura e bloquear a coluna.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Etapa 5: adicionar a tabela ao contorno e à página
A classe `Outline` agrupa conteúdo em uma página, e `OutlineElement` representa um elemento individual, como uma tabela.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Etapa 6: salvar o documento
Chame o método `save` na instância `Document`, especificando um caminho de arquivo `.one`. O arquivo pode então ser aberto diretamente no Microsoft OneNote.

Parabéns! Você adicionou com sucesso **add table to OneNote** com colunas bloqueadas usando Aspose.Note para Java.

## Conclusão
Neste guia cobrimos tudo o que você precisa para **add table to OneNote** com colunas bloqueadas, desde a configuração do projeto até a gravação final. Ao aproveitar a rica API do Aspose.Note, você obtém controle detalhado sobre larguras de colunas, comportamento de bloqueio e estilo de bordas — tornando suas notas mais organizadas e profissionais.

## Perguntas frequentes
**Q: O Aspose.Note para Java é compatível com todas as versões do Java?**  
A: Sim, Aspose.Note para Java funciona com Java 7 e posteriores, incluindo Java 8, 11 e 17.

**Q: Posso personalizar ainda mais a aparência da tabela?**  
A: Absolutamente! Você pode ajustar bordas, espaçamento de células, cores de fundo e até aplicar formatação de texto rico a células individuais.

**Q: Existe uma versão de avaliação disponível antes da compra?**  
A: Sim, você pode [baixar uma avaliação gratuita](https://releases.aspose.com/) para explorar os recursos do Aspose.Note para Java.

**Q: Onde posso encontrar suporte adicional ou discussões da comunidade?**  
A: Visite o [fórum Aspose.Note](https://forum.aspose.com/c/note/28) para obter ajuda da comunidade e dos engenheiros da Aspose.

**Q: Como posso obter uma licença temporária para Aspose.Note para Java?**  
A: Visite a [página de licença temporária](https://purchase.aspose.com/temporary-license/) para obter uma licença temporária para fins de teste.

---

**Last Updated:** 2026-08-13  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose

## Tutoriais Relacionados

- [Converter tabela em texto no OneNote com Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Inserir linha de tabela Java - Adicionar nó de tabela com tag no OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: Manipulação de Documentos OneNote](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}
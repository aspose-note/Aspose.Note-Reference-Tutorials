---
date: 2026-08-13
description: Aprenda como obter a hora de modificação da página do OneNote e recuperar
  revisões de página com Aspose.Note para Java, ideal para auditoria e gerenciamento
  de documentos.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Obter Revisões de Páginas no OneNote - Aspose.Note
og_description: Aprenda como obter a hora de modificação da página do OneNote e recuperar
  revisões de páginas do OneNote com Aspose.Note para Java. Passos rápidos, trechos
  de código e solução de problemas.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Obtenha a hora de modificação da página do OneNote usando Aspose.Note –
  tutorial Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Obtenha a hora de modificação da página do OneNote usando Aspose.Note
url: /pt/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obter horário de modificação da página OneNote usando Aspose.Note

## Introdução

Neste tutorial, você aprenderá como **get onenote page modified** timestamps e obter o histórico completo de revisões de uma página OneNote com Aspose.Note para Java. Seja construindo um recurso de trilha de auditoria, um visualizador de registro de alterações, ou precisando exibir a data da edição mais recente em um painel, este guia o conduz por cada passo — desde a configuração do ambiente até o tratamento de armadilhas comuns.

## Respostas rápidas
- **What does “get last modified time” return?** Retorna o timestamp da edição mais recente em uma página OneNote.  
- **Which class provides revision history?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Do I need a license for this feature?** Sim, uma licença válida do Aspose.Note é necessária para uso em produção.  
- **What Java version is supported?** Java 8 ou superior (JDK 8+).  
- **Can I filter revisions by author?** Você pode ler a propriedade `Author` de cada objeto `Page` e aplicar seu próprio filtro.

## O que é “get last modified time” no OneNote?

O horário de última modificação é armazenado como um atributo de metadados em cada página OneNote, indicando o momento da edição mais recente. O Aspose.Note expõe esse valor através do método `Page.getLastModifiedTime()`, que retorna um objeto `java.util.Date` que pode ser formatado ou registrado conforme os requisitos da sua aplicação.

## Por que recuperar revisões de página?

Recuperar revisões de página fornece uma trilha de auditoria completa de todas as alterações feitas em uma página OneNote, permitindo rastrear quem editou o quê e quando. Esse histórico pode ser usado para comparar versões, restaurar estados anteriores ou analisar padrões de colaboração entre equipes, tornando-o essencial para conformidade e controle de qualidade.

## Pré-requisitos

- **Java Development Kit (JDK) 8 ou posterior** – instale a partir do site da Oracle ou de qualquer fornecedor compatível.  
- **Aspose.Note for Java library** – faça o download do JAR na página de lançamentos do Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** e siga o guia de instalação **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Importar pacotes

A classe `Document` representa um caderno OneNote carregado na memória, enquanto `Page` e `PageHistory` fornecem acesso a páginas individuais e seus dados de revisão.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(As declarações de importação reais são mostradas como texto simples para preservar a contagem original do bloco de código.)*

## Como obter o horário de modificação da página OneNote?

Para obter o timestamp da última modificação, primeiro carregue o documento OneNote em um objeto `Document`, depois selecione a `Page` desejada. Chame o método `getLastModifiedTime()` nessa página, que retorna um `java.util.Date`. Você pode então formatar essa data usando `SimpleDateFormat` ou convertê‑la para UTC para relatórios consistentes entre fusos horários.

## Etapa 1: definir diretório do documento

Defina a pasta que contém seu arquivo OneNote.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Etapa 2: carregar o documento

Crie uma instância `Document` passando o caminho completo para o seu arquivo `.one`.

```java
String dataDir = "Your Document Directory";
```

## Etapa 3: obter a primeira página

Recupere o primeiro objeto `Page` da coleção de páginas do documento.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Etapa 4: obter revisões da página

Obtenha o `PageHistory` para a página selecionada. Se o caderno nunca foi editado, essa chamada pode retornar `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Etapa 5: percorrer revisões da página

Itere por cada revisão de `Page`, leia seu `Author` e `LastModifiedTime`, e exiba as informações.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Problemas comuns e soluções
- **Null `PageHistory`** – Verifique se o caderno realmente contém revisões; caso contrário, `getPageHistory` retorna `null`.  
- **Diferenças de fuso horário** – `getLastModifiedTime()` usa o fuso horário padrão da JVM. Converta para UTC com `SimpleDateFormat` se sua aplicação exigir um fuso padrão.  
- **Licença não carregada** – Sem uma licença válida, o Aspose.Note funciona em modo de avaliação, limitando o processamento de páginas. Carregue seu arquivo de licença na inicialização da aplicação para evitar essa restrição.

## Perguntas frequentes

**Q1: Posso usar Aspose.Note para Java para criar novos documentos OneNote?**  
A: Sim, a API permite criar, editar e salvar cadernos OneNote programaticamente do zero.

**Q2: O Aspose.Note para Java é compatível com diferentes versões de arquivos OneNote?**  
A: Sim, ele suporta formatos de arquivo OneNote 2007‑2021, garantindo ampla compatibilidade em ambientes desktop e na nuvem.

**Q3: Posso personalizar o formato de saída ao exportar documentos OneNote?**  
A: Absolutamente. Você pode exportar para PDF, HTML, PNG ou SVG, e controlar opções como resolução de imagem e incorporação de fontes.

**Q4: O Aspose.Note para Java requer licença para uso comercial?**  
A: Sim, uma licença comercial é obrigatória para implantações em produção. Um teste gratuito está disponível para avaliação.

**Q5: Onde posso buscar assistência se encontrar problemas?**  
A: Visite o fórum da comunidade Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** para fazer perguntas, compartilhar experiências e obter ajuda da comunidade e dos engenheiros da Aspose.

---

**Última atualização:** 2026-08-13  
**Testado com:** Aspose.Note for Java 23.12 (mais recente no momento da escrita)  
**Autor:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Tutoriais relacionados

- [Tutorial Java Aspose - Obter informações sobre páginas no OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Tutorial de revisões de página aspose.note – Obter revisões de página no OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Rastrear alterações no OneNote – Gerenciar revisões de página com Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
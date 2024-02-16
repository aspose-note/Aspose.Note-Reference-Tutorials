---
title: Obtenha revisões de páginas no OneNote - Aspose.Note
linktitle: Obtenha revisões de páginas no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como recuperar revisões de páginas em documentos do OneNote usando Aspose.Note Java. Integre isso aos seus aplicativos Java para um gerenciamento eficiente de documentos.
type: docs
weight: 15
url: /pt/java/onenote-page-manipulation/get-revisions-of-pages/
---
## Introdução

Neste tutorial, nos aprofundaremos nos recursos do Aspose.Note for Java, uma biblioteca poderosa que permite trabalhar perfeitamente com arquivos do Microsoft OneNote em seus aplicativos Java. Especificamente, nos concentraremos em como recuperar revisões de páginas em um documento do OneNote. Ao final deste guia, você estará equipado com o conhecimento para extrair revisões de páginas com eficiência, incluindo detalhes como hora da última modificação, hora de criação, título, nível e autor.

## Pré-requisitos

Antes de mergulhar neste tutorial, certifique-se de ter os seguintes pré-requisitos configurados:

### Kit de desenvolvimento Java (JDK) instalado

Certifique-se de ter o Java Development Kit instalado em seu sistema. Você pode baixá-lo e instalá-lo no site da Oracle ou usar um gerenciador de pacotes se estiver em um sistema baseado em Unix.

### Biblioteca Aspose.Note para Java

 Baixe e instale a biblioteca Aspose.Note para Java do site. Você pode encontrar o link para download[aqui](https://releases.aspose.com/note/java/) . Siga as instruções de instalação fornecidas na documentação[aqui](https://reference.aspose.com/note/java/).

## Importar pacotes

Para começar, importe os pacotes necessários para o seu projeto Java. Esses pacotes permitirão que você aproveite a funcionalidade fornecida pelo Aspose.Note para Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Agora, vamos dividir o código de exemplo fornecido em várias etapas para entender cada componente e sua funcionalidade.

## Etapa 1: definir diretório de documentos

Defina o diretório onde seu documento do OneNote está localizado.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: carregue o documento

Carregue o documento OneNote no Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Etapa 3: obtenha a primeira página

Recupere a primeira página do documento.

```java
Page firstPage = doc.getFirstChild();
```

## Etapa 4: obtenha revisões de página

Obtenha o histórico de revisões da página.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Etapa 5: percorrer as revisões da página

Itere pela lista de revisões de página e recupere informações relevantes.

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

## Conclusão

Neste tutorial, exploramos como recuperar revisões de páginas em um documento do OneNote usando Aspose.Note para Java. Seguindo o guia passo a passo e aproveitando o código de exemplo fornecido, você pode integrar facilmente essa funcionalidade em seus aplicativos Java, permitindo o gerenciamento eficiente de arquivos do OneNote.

## Perguntas frequentes

### Q1: Posso usar Aspose.Note for Java para criar novos documentos do OneNote?

A1: Sim, Aspose.Note for Java fornece suporte abrangente para criação, leitura e manipulação de documentos do OneNote programaticamente.

### Q2: O Aspose.Note para Java é compatível com diferentes versões de arquivos do OneNote?

A2: Sim, Aspose.Note for Java oferece suporte a várias versões de arquivos do Microsoft OneNote, garantindo compatibilidade em diferentes ambientes.

### P3: Posso personalizar o formato de saída ao exportar documentos do OneNote?

A3: Com certeza, Aspose.Note for Java oferece flexibilidade na exportação de documentos do OneNote para diferentes formatos, como PDF, HTML e imagens, com opções de personalização.

### Q4: O Aspose.Note for Java requer uma licença para uso comercial?

A4: Sim, é necessária uma licença válida para uso comercial do Aspose.Note for Java. Você pode obter uma licença no site Aspose.

### P5: Onde posso procurar assistência se encontrar problemas ou tiver dúvidas sobre o Aspose.Note for Java?

 A5: Para suporte e assistência, você pode visitar o fórum Aspose.Note[aqui](https://forum.aspose.com/c/note/28)onde você pode fazer perguntas, compartilhar experiências e interagir com outros usuários e especialistas.
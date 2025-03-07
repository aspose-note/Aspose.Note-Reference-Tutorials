---
title: Obtenha revisões de página no OneNote - Aspose.Note
linktitle: Obtenha revisões de página no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como recuperar revisões de página no OneNote usando Aspose.Note para Java. Siga nosso guia passo a passo para um rastreamento eficiente das alterações.
weight: 14
url: /pt/java/onenote-page-manipulation/get-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtenha revisões de página no OneNote - Aspose.Note

## Introdução

O OneNote é uma ferramenta poderosa para organizar e gerenciar suas anotações, mas às vezes você precisa rastrear alterações e revisões feitas em suas páginas. Com Aspose.Note for Java, você pode recuperar facilmente revisões de página programaticamente. Neste tutorial, orientaremos você no processo de obtenção de revisões de página no OneNote usando Aspose.Note para Java.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos em vigor:

### 1. Kit de Desenvolvimento Java (JDK)

Certifique-se de ter o Java Development Kit (JDK) instalado em seu sistema. Você pode baixar e instalar o JDK no site da Oracle.

### 2. Aspose.Note para Java

Baixe e instale Aspose.Note para Java em[Link para Download](https://releases.aspose.com/note/java/).

### 3. Exemplo de documento do OneNote

Prepare um documento de amostra do OneNote (`Sample1.one`) que contém as páginas das quais você deseja recuperar as revisões.

## Importar pacotes

Primeiro, você precisa importar os pacotes necessários do Aspose.Note para Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Agora, vamos dividir o exemplo fornecido em várias etapas:

## Etapa 1: configurar o diretório de documentos

Defina o caminho do diretório onde seu documento do OneNote está localizado.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: carregar o documento do OneNote

 Carregue o documento do OneNote usando`LoadOptions` para ativar o histórico de carregamento.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Etapa 3: obtenha a primeira página

Recupera a primeira página do documento carregado.

```java
Page firstPage = document.getFirstChild();
```

## Etapa 4: iterar por meio de revisões de página

Itere em cada revisão de página e recupere informações relevantes, como hora da última modificação, hora de criação, título, nível e autor.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Conclusão

Neste tutorial, aprendemos como recuperar revisões de páginas no OneNote usando Aspose.Note para Java. Seguindo essas etapas, você pode rastrear com eficiência as alterações feitas nas páginas do OneNote de maneira programática.

## Perguntas frequentes

### Q1: Posso usar Aspose.Note for Java para modificar revisões de páginas?

A1: Não, Aspose.Note for Java atualmente suporta a recuperação de revisões de páginas, mas não as modifica.

### Q2: O Aspose.Note for Java é compatível com diferentes versões de documentos do OneNote?

A2: Sim, Aspose.Note for Java oferece suporte a várias versões de documentos do OneNote, permitindo que você trabalhe perfeitamente com diferentes formatos de arquivo.

### Q3: O Aspose.Note for Java requer uma licença de uso?

A3: Sim, você precisa adquirir uma licença para usar Aspose.Note for Java em projetos comerciais. No entanto, você também pode obter uma licença temporária para fins de avaliação.

### Q4: Posso procurar suporte se encontrar algum problema ao usar o Aspose.Note for Java?

 A4: Sim, você pode buscar suporte no fórum Aspose.Note[aqui](https://forum.aspose.com/c/note/28).

### Q5: Existe uma avaliação gratuita disponível para Aspose.Note for Java?

 A5: Sim, você pode acessar uma avaliação gratuita do Aspose.Note for Java no site[local na rede Internet](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Trabalhando com revisões de página no OneNote - Aspose.Note
linktitle: Trabalhando com revisões de página no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como gerenciar revisões de páginas em documentos do OneNote usando Aspose.Note para Java. Fornece guia passo a passo para colaboração e rastreamento de revisão eficazes.
weight: 21
url: /pt/java/onenote-page-manipulation/working-with-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Trabalhando com revisões de página no OneNote - Aspose.Note

## Introdução

O OneNote é uma ferramenta poderosa para organizar e gerenciar notas, mas às vezes você precisa trabalhar com revisões para rastrear alterações e colaborar de forma eficaz. Com Aspose.Note para Java, você pode gerenciar facilmente revisões de páginas em documentos do OneNote de forma programática. Este tutorial irá guiá-lo através do processo passo a passo.

## Pré-requisitos

Antes de começar, certifique-se de ter o seguinte:

### Ambiente de Desenvolvimento Java

Certifique-se de ter o Java Development Kit (JDK) instalado em seu sistema.

### Biblioteca Aspose.Note para Java

Baixe e instale a biblioteca Aspose.Note para Java em[aqui](https://releases.aspose.com/note/java/).

### Documento OneNote

Tenha um documento de amostra do OneNote pronto para fins de teste.

## Importar pacotes

Em seu projeto Java, importe os pacotes necessários para trabalhar com Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Vamos dividir o exemplo fornecido em várias etapas para uma compreensão clara.

## Etapa 1: carregar o documento do OneNote

Primeiro, carregue o documento do OneNote e obtenha a primeira página secundária.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Etapa 2: leia o resumo da revisão da página

Leia o resumo da revisão do conteúdo da página.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Etapa 3: atualizar o resumo da revisão da página

Atualize o resumo da revisão da página com o novo autor e a data de modificação.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusão

O gerenciamento programático de revisões de páginas em documentos do OneNote pode ser simplificado com Aspose.Note para Java. Seguindo as etapas descritas neste tutorial, você pode trabalhar efetivamente com revisões de página para rastrear alterações e colaborar perfeitamente.

## Perguntas frequentes

### Q1: Posso usar Aspose.Note for Java com outras bibliotecas Java?

R: Sim, Aspose.Note for Java pode ser integrado com outras bibliotecas Java para aprimorar a funcionalidade.

### Q2: O Aspose.Note para Java oferece suporte a todas as versões de documentos do OneNote?

R: Aspose.Note for Java oferece suporte a várias versões de documentos do OneNote, incluindo versões mais antigas.

### Q3: O Aspose.Note for Java é adequado para aplicativos de nível empresarial?

R: Com certeza, o Aspose.Note for Java foi projetado para atender às necessidades de aplicativos de nível empresarial com recursos robustos e escalabilidade.

### Q4: Posso personalizar revisões de página com Aspose.Note para Java?

R: Sim, você pode personalizar as revisões de página de acordo com seus requisitos usando Aspose.Note para Java.

### Q5: Onde posso obter suporte para Aspose.Note para Java?

 R: Você pode obter suporte para Aspose.Note for Java no site[Fórum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

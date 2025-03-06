---
title: Converter bloco de notas em PDF nivelado no OneNote - Aspose.Note
linktitle: Converter bloco de notas em PDF nivelado no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Converta cadernos em PDFs achatados sem esforço com Aspose.Note para Java. Aproveite opções perfeitas de integração e personalização.
weight: 16
url: /pt/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter bloco de notas em PDF nivelado no OneNote - Aspose.Note

## Introdução

Neste tutorial, exploraremos como converter um notebook em um formato PDF nivelado usando Aspose.Note para Java. A conversão de cadernos em PDFs é um requisito comum para muitos aplicativos, e o Aspose.Note simplifica esse processo com seu conjunto abrangente de recursos e API fácil de usar.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1. Java Development Kit (JDK): Certifique-se de ter o JDK instalado em seu sistema.
2.  Biblioteca Aspose.Note para Java: Baixe e instale a biblioteca Aspose.Note para Java em[aqui](https://releases.aspose.com/note/java/).
3. Ambiente de Desenvolvimento Integrado (IDE): Escolha um IDE de sua preferência, como IntelliJ IDEA ou Eclipse.

## Importar pacotes

Primeiramente, vamos importar os pacotes necessários para o seu projeto Java:

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## Etapa 1: carregar o bloco de anotações do OneNote

Para começar, carregue o bloco de notas do OneNote que deseja converter para PDF:

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Etapa 2: definir opções de conversão

 Defina as opções de conversão do caderno para PDF. Aqui, vamos definir`flatten` para`true` para nivelar o PDF:

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## Etapa 3: salve o caderno como PDF

Especifique o diretório de saída e salve o notebook como PDF com as opções definidas:

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// Salve o caderno
notebook.save(dataDir, notebookSaveOptions);
```

## Conclusão

Neste tutorial, aprendemos como converter um notebook em um formato PDF nivelado usando Aspose.Note para Java. Esse processo é simples e pode ser perfeitamente integrado aos seus aplicativos Java.

## Perguntas frequentes

### Q1: O Aspose.Note para Java é compatível com diferentes versões do OneNote?

A1: Sim, Aspose.Note for Java oferece suporte a várias versões do OneNote, garantindo compatibilidade em diferentes ambientes.

### Q2: Posso personalizar a saída do PDF usando Aspose.Note para Java?

A2: Com certeza, você pode personalizar a saída do PDF de acordo com suas necessidades, incluindo layout de página, estilos de fonte e muito mais.

### Q3: O Aspose.Note for Java oferece suporte à conversão em lote de notebooks?

A3: Sim, você pode converter em lote vários cadernos em PDFs de forma eficiente usando Aspose.Note para Java.

### Q4: Existe uma versão de teste disponível para Aspose.Note para Java?

 A4: Sim, você pode acessar uma avaliação gratuita do Aspose.Note for Java em[aqui](https://releases.aspose.com/).

### Q5: Onde posso encontrar suporte para Aspose.Note para Java?

 A5: Você pode encontrar suporte e assistência para Aspose.Note for Java no site[Fórum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

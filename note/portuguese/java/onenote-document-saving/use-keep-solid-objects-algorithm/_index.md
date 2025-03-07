---
title: Use o algoritmo Manter objetos sólidos no OneNote - Aspose.Note
linktitle: Use o algoritmo Manter objetos sólidos no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como preservar objetos sólidos em seus documentos Aspose.Note ao converter para PDF usando o algoritmo Keep Solid Objects em Java.
weight: 25
url: /pt/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Use o algoritmo Manter objetos sólidos no OneNote - Aspose.Note

## Introdução

Neste tutorial, exploraremos como utilizar o algoritmo Keep Solid Objects em Aspose.Note para Java. Este algoritmo é inestimável para manter a integridade de objetos sólidos em seus documentos ao convertê-los para o formato PDF. Descreveremos o processo passo a passo, garantindo clareza e compreensão em cada etapa.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1. Java Development Kit (JDK) instalado em seu sistema.
2.  Aspose.Note para biblioteca Java. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/java/).

## Importar pacotes

Primeiro, vamos importar os pacotes necessários:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Etapa 1: carregue o documento

Carregue o documento no Aspose.Note usando o seguinte trecho de código:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Passo 2: Configurar opções para salvar PDF

Defina PdfSaveOptions e defina PageSplittingAlgorithm como KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Etapa 3: ajustar o limite de altura (opcional)

Você pode ajustar o limite de altura das peças clonadas, se necessário:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Etapa 4: salve o documento

Por fim, salve o documento com as opções de salvamento de PDF especificadas:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Conclusão

Neste tutorial, aprendemos como utilizar o algoritmo Keep Solid Objects em Aspose.Note para Java. Este algoritmo garante que os objetos sólidos dos seus documentos sejam preservados ao convertê-los para o formato PDF, mantendo a integridade do documento.

## Perguntas frequentes

### Q1: Posso ajustar o limite de altura para peças clonadas?

 A1: Sim, você pode ajustar o limite de altura das peças clonadas de acordo com suas necessidades usando o`heightLimitOfClonedPart` parâmetro.

### P2: Onde posso encontrar mais documentação?

 A2: Você pode encontrar documentação detalhada em Aspose.Note for Java[aqui](https://reference.aspose.com/note/java/).

### Q3: Existe um teste gratuito disponível?

 A3: Sim, você pode obter uma avaliação gratuita do Aspose.Note para Java[aqui](https://releases.aspose.com/).

### P4: Como posso obter suporte se encontrar algum problema?

 A4: Você pode obter suporte da comunidade Aspose[aqui](https://forum.aspose.com/c/note/28).

### P5: Onde posso comprar uma licença?

 A5: Você pode comprar uma licença para Aspose.Note para Java[aqui](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

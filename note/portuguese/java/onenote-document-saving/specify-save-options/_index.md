---
title: Especifique as opções de salvamento no OneNote - Aspose.Note
linktitle: Especifique as opções de salvamento no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como especificar opções de salvamento no OneNote usando Aspose.Note para Java. Personalize as configurações de índice, contagem e compactação de páginas sem esforço.
weight: 24
url: /pt/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Especifique as opções de salvamento no OneNote - Aspose.Note

## Introdução

Neste tutorial, aprenderemos como especificar opções de salvamento no OneNote usando Aspose.Note para Java. Aspose.Note é uma poderosa biblioteca Java que permite aos desenvolvedores criar, manipular e converter documentos do OneNote programaticamente. Com Aspose.Note, você pode controlar facilmente várias opções de salvamento para personalizar a saída de acordo com suas necessidades.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes pré-requisitos:

1. Conhecimento básico da linguagem de programação Java.
2. JDK (Java Development Kit) instalado em seu sistema.
3.  Biblioteca Aspose.Note para Java instalada. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/java/).

## Importar pacotes

Para começar, importe os pacotes necessários em seu código Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Vamos dividir o exemplo em várias etapas:

## Etapa 1: carregar o documento OneNote

```java
// O caminho para o diretório de documentos.
String dataDir = "Your Document Directory";

// Carregue o documento no Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

 Nesta etapa, especificamos o caminho para o documento do OneNote e o carregamos no`Document` objeto.

## Etapa 2: inicializar o objeto PdfSaveOptions

```java
// Inicializar objeto PdfSaveOptions
PdfSaveOptions opts = new PdfSaveOptions();
```

 Aqui, inicializamos um`PdfSaveOptions` objeto que será usado para especificar as opções para salvar o documento como PDF.

## Etapa 3: definir índice e contagem de páginas

```java
// Definir índice de página
opts.setPageIndex(2);

// Definir contagem de páginas
opts.setPageCount(3);
```

Estas linhas definem o índice e a contagem das páginas a serem salvas. Neste exemplo, estamos salvando páginas a partir do índice 2 e um total de 3 páginas.

## Etapa 4: especificar configurações de compactação

```java
// Especifique a compactação, se necessário
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Aqui, especificamos as configurações de compactação de imagem para o PDF. Definimos a compactação para o formato JPEG e especificamos a qualidade JPEG como 90%.

## Etapa 5: salve o documento com opções

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Finalmente, salvamos o documento com as opções especificadas. O PDF de saída será salvo no local especificado com as opções fornecidas.

## Conclusão

Neste tutorial, aprendemos como especificar opções de salvamento no OneNote usando Aspose.Note para Java. Ao personalizar as opções de salvamento, você pode controlar vários aspectos do documento de saída, como índice de página, contagem e configurações de compactação.

## Perguntas frequentes

### Q1: O Aspose.Note pode lidar com documentos grandes do OneNote?

A1: Sim, o Aspose.Note foi projetado para lidar com documentos grandes do OneNote com eficiência.

### Q2: O Aspose.Note é compatível com as versões mais recentes do Java?

A2: Sim, Aspose.Note é compatível com as versões mais recentes do Java.

### Q3: Posso converter documentos do OneNote para outros formatos usando Aspose.Note?

A3: Sim, Aspose.Note oferece suporte à conversão de documentos do OneNote para vários formatos, como PDF, DOCX e HTML.

### Q4: O Aspose.Note fornece suporte para criptografia e descriptografia de documentos do OneNote?

A4: Sim, Aspose.Note fornece APIs para criptografia e descriptografia de documentos do OneNote.

### Q5: O Aspose.Note é adequado para uso comercial?

A5: Sim, o Aspose.Note pode ser usado para fins comerciais através da compra de uma licença.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

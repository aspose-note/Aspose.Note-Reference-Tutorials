---
title: Salvar usando o subsistema de fontes especificado no OneNote
linktitle: Salvar usando o subsistema de fontes especificado no OneNote
second_title: API Java Aspose.Note
description: Aprenda como salvar documentos do OneNote usando o subsistema de fontes especificado em Java com Aspose.Note. Garanta uma representação consistente de fontes em todas as plataformas sem esforço.
weight: 22
url: /pt/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar usando o subsistema de fontes especificado no OneNote

## Introdução

Aspose.Note for Java fornece recursos robustos para trabalhar com documentos do OneNote. Um requisito comum ao trabalhar com tais documentos é garantir que as fontes sejam mantidas adequadamente, especialmente se o documento for exportado ou salvo em formatos diferentes, como PDF. Este tutorial irá guiá-lo através do processo de salvar documentos do OneNote enquanto especifica o subsistema de fontes, garantindo uma representação consistente e precisa do texto em várias plataformas.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos configurados:

### 1. Kit de Desenvolvimento Java (JDK)

 Certifique-se de ter o Java Development Kit (JDK) instalado em seu sistema. Você pode baixá-lo em[aqui](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) se você ainda não o fez.

### 2. Biblioteca Aspose.Note para Java

 Baixe e configure a biblioteca Aspose.Note para Java. Você pode baixá-lo no[local na rede Internet](https://releases.aspose.com/note/java/).

## Importar pacotes

Certifique-se de importar os pacotes necessários em seu projeto Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Agora vamos dividir cada exemplo em várias etapas para entender melhor o processo.

## Etapa 1: Salvar usando o subsistema de fontes de documentos com nome de fonte padrão

Esta etapa demonstra como salvar um documento em formato PDF usando um nome de fonte padrão especificado.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Especifique a fonte padrão.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Salve o documento como PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Nesta etapa:
- O documento OneNote é carregado usando Aspose.Note.
- A fonte padrão é especificada como "Times New Roman".
- O documento é salvo em formato PDF com a fonte especificada.

## Etapa 2: Salvar usando o subsistema de fontes de documentos com fonte padrão do arquivo

Esta etapa demonstra como salvar um documento em formato PDF usando uma fonte padrão carregada de um arquivo.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Especifique o caminho para o arquivo de fonte.
    String fontFile = "geo_1.ttf";

    // Especifique a fonte padrão do arquivo.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Salve o documento como PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Nesta etapa:
- O arquivo de fonte "geo_1.ttf" é carregado.
- A fonte padrão é especificada no arquivo de fonte carregado.
- O documento é salvo em formato PDF com a fonte especificada.

## Etapa 3: Salvar usando o subsistema de fontes de documentos com fonte padrão do Stream

Esta etapa demonstra como salvar um documento em formato PDF usando uma fonte padrão carregada de um fluxo.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Especifique o caminho para o arquivo de fonte.
    String fontFile = "geo_1.ttf";

    // Carregue o arquivo de fonte como um fluxo.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Especifique a fonte padrão do stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Salve o documento como PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Nesta etapa:
- O arquivo de fonte "geo_1.ttf" é carregado como um fluxo.
- A fonte padrão é especificada no fluxo carregado.
- O documento é salvo em formato PDF com a fonte especificada.

## Conclusão

Neste tutorial, aprendemos como salvar documentos do OneNote usando o subsistema de fontes especificado em Java usando Aspose.Note. Seguindo essas etapas, você pode garantir uma representação consistente de fontes em várias plataformas ao exportar ou salvar seus documentos.

## Perguntas frequentes

### P1: Posso especificar fontes diferentes para diferentes partes do documento?

A1: Sim, você pode especificar fontes diferentes para diferentes partes do documento usando Aspose.Note para Java.

### Q2: O Aspose.Note é compatível com todas as versões do OneNote?

A2: Aspose.Note oferece suporte a várias versões do OneNote, garantindo compatibilidade em diferentes ambientes.

### P3: Como posso lidar com fontes ausentes ao salvar documentos?

A3: Aspose.Note oferece opções para especificar fontes padrão para lidar com fontes ausentes de forma eficaz durante o salvamento do documento.

### Q4: Posso personalizar as propriedades da fonte, como tamanho e estilo?

A4: Sim, você pode personalizar as propriedades da fonte, como tamanho, estilo e cor, usando Aspose.Note para Java.

### Q5: Existe uma versão de teste disponível para Aspose.Note para Java?

A5: Sim, você pode obter uma avaliação gratuita do Aspose.Note para Java no site.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

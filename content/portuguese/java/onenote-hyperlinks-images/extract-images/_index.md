---
title: Extraia imagens do documento OneNote usando Java
linktitle: Extraia imagens do documento OneNote usando Java
second_title: API Java Aspose.Note
description: Aprenda como extrair imagens de documentos do OneNote usando Java com a biblioteca Aspose.Note. Siga nosso guia passo a passo para extração perfeita de imagens.
type: docs
weight: 14
url: /pt/java/onenote-hyperlinks-images/extract-images/
---
## Introdução

Neste tutorial, orientaremos você no processo de extração de imagens de um documento do OneNote usando Java com a ajuda da biblioteca Aspose.Note.

## Pré-requisitos

Antes de começar, certifique-se de ter o seguinte:

1.  Java Development Kit (JDK): Certifique-se de ter o Java instalado em seu sistema. Você pode baixá-lo e instalá-lo no[local na rede Internet](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Biblioteca Aspose.Note: Baixe e inclua a biblioteca Aspose.Note em seu projeto Java. Você pode obtê-lo no[Link para Download](https://releases.aspose.com/note/java/).

## Importar pacotes

Para começar, importe os pacotes necessários:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Etapa 1: carregue o documento

Primeiro, carregue o documento OneNote usando Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Etapa 2: obtenha todas as imagens

A seguir, recupere todas as imagens do documento:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Etapa 3: extrair imagens

Itere pela lista de imagens e salve cada imagem em um arquivo:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Conclusão

extração de imagens de um documento OneNote usando Java pode ser realizada perfeitamente com a biblioteca Aspose.Note. Seguindo as etapas descritas neste tutorial, você pode recuperar facilmente imagens de seus documentos para processamento ou análise posterior.

## Perguntas frequentes

### P1: Posso extrair imagens de documentos do OneNote protegidos por senha?

A1: Sim, o Aspose.Note também oferece suporte à extração de imagens de documentos protegidos por senha.

### Q2: O Aspose.Note é compatível com diferentes versões do Java?

A2: Aspose.Note é compatível com várias versões de Java, garantindo flexibilidade para desenvolvedores.

### P3: Posso extrair imagens de vários documentos do OneNote em uma única execução?

A3: Com certeza, você pode iterar vários documentos e extrair imagens de cada um deles usando Aspose.Note.

### P4: Há alguma limitação de tamanho para os documentos do OneNote?

A4: Aspose.Note lida com documentos de vários tamanhos de forma eficiente, garantindo que não haja limitações no tamanho do documento para extração de imagens.

### Q5: O Aspose.Note oferece suporte à extração de outros tipos de conteúdo além de imagens?

R5: Sim, além de imagens, Aspose.Note permite a extração de texto, anexos e outros tipos de conteúdo de documentos do OneNote.
---
title: Defina a resolução da imagem de saída no OneNote - Aspose.Note
linktitle: Defina a resolução da imagem de saída no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como ajustar a resolução da imagem em documentos do OneNote usando Aspose.Note para Java. Siga nosso guia passo a passo para fácil implementação
weight: 23
url: /pt/java/onenote-document-saving/set-output-image-resolution/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Defina a resolução da imagem de saída no OneNote - Aspose.Note

## Introdução

Você deseja manipular a resolução de imagens em seus documentos do OneNote usando Java? Aspose.Note for Java oferece uma solução robusta para tais tarefas. Neste tutorial, percorreremos as etapas para definir a resolução da imagem de saída usando Aspose.Note.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos:

1. Kit de desenvolvimento Java (JDK): Instale o JDK em seu sistema.
2. Aspose.Note para Java: Baixe e instale Aspose.Note para Java do[local na rede Internet](https://releases.aspose.com/note/java/).
3. Ambiente de Desenvolvimento Integrado (IDE): Escolha seu IDE preferido, como Eclipse ou IntelliJ IDEA.

## Importar pacotes

Em seu projeto Java, importe os pacotes Aspose.Note necessários:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Etapa 1: carregar o documento OneNote

Comece carregando o documento do OneNote em seu aplicativo Java:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Substituir`"Your Document Directory"` com o diretório real onde reside o documento do OneNote.

## Etapa 2: definir opções para salvar imagens

Defina as opções de salvamento da imagem e especifique a resolução desejada:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Aqui, estamos definindo a resolução para`120 dpi`. Você pode ajustar esse valor de acordo com suas necessidades.

## Etapa 3: salve o documento com resolução modificada

Salve o documento com a resolução de imagem atualizada:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Isso salvará o documento modificado com a resolução especificada.

## Conclusão

Neste tutorial, exploramos como definir a resolução da imagem de saída em documentos do OneNote usando Aspose.Note para Java. Seguindo essas etapas simples, você pode manipular com eficiência a resolução das imagens para atender aos requisitos do seu aplicativo.


## Perguntas frequentes

### Q1: Posso ajustar a resolução da imagem para um valor superior a 120 dpi?

A1: Sim, você pode definir a resolução para qualquer valor desejado de acordo com suas necessidades.

### Q2: O Aspose.Note oferece suporte a outros formatos de imagem além de JPEG?

A2: Sim, Aspose.Note suporta vários formatos de imagem, como PNG, BMP, GIF, etc.

### Q3: O Aspose.Note é compatível com todas as versões do Java?

A3: Aspose.Note é compatível com Java 1.6 ou versões posteriores.

### Q4: Posso manipular outros aspectos de imagens em documentos do OneNote usando Aspose.Note?

R4: Sim, o Aspose.Note oferece recursos abrangentes para manipulação de imagens, incluindo redimensionamento, corte e rotação.

### Q5: Onde posso obter suporte para consultas relacionadas ao Aspose.Note?

 A5: Você pode procurar ajuda no fórum da comunidade Aspose.Note[aqui](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

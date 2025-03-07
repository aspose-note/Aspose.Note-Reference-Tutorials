---
title: Salvar em imagem em escala de cinza no OneNote - Aspose.Note
linktitle: Salvar em imagem em escala de cinza no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como salvar um documento como uma imagem em tons de cinza no OneNote usando Aspose.Note para Java. Manipule facilmente documentos do Microsoft OneNote de forma programática.
weight: 17
url: /pt/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar em imagem em escala de cinza no OneNote - Aspose.Note

## Introdução

Neste tutorial, exploraremos como salvar um documento como uma imagem em escala de cinza no OneNote usando Aspose.Note para Java. Imagens em tons de cinza são imagens monocromáticas onde as informações de cores são representadas apenas por tons de cinza. Aspose.Note é uma API Java poderosa que permite a manipulação de documentos do Microsoft OneNote de forma programática.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1. Java Development Kit (JDK) instalado em seu sistema.
2.  Aspose.Note para biblioteca Java. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/java/).
3. Compreensão básica de programação Java.

## Importar pacotes

Para começar, importe os pacotes necessários:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Etapa 1: carregue o documento

 Primeiro, carregue o documento no Aspose.Note. Substituir`"Your Document Directory"` com o caminho para o diretório do seu documento e`"Aspose.one"` com o nome do seu documento do OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Etapa 2: definir caminho de saída e opções

Defina o caminho de saída da imagem em tons de cinza e especifique as opções de salvamento. Definiremos o modo de cor para tons de cinza.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Etapa 3: salve o documento

Finalmente, salve o documento como uma imagem em tons de cinza usando as opções especificadas.

```java
oneFile.save(dataDir, options);
```

## Conclusão

Parabéns! Você aprendeu com sucesso como salvar um documento como uma imagem em escala de cinza no OneNote usando Aspose.Note para Java. Isso pode ser extremamente útil para várias aplicações onde são necessárias imagens em tons de cinza.

## Perguntas frequentes

### Q1: Posso salvar a imagem em tons de cinza em um formato diferente?

 A1: Sim, você pode. Basta alterar o`SaveFormat` parâmetro no`ImageSaveOptions` construtor para o formato desejado.

### Q2: O Aspose.Note é compatível com todas as versões de documentos do OneNote?

A2: Aspose.Note oferece suporte ao Microsoft OneNote 2010 e superior.

### Q3: O Aspose.Note requer uma licença de uso?

A3: Sim, você precisa de uma licença válida para usar o Aspose.Note em ambientes de produção. No entanto, você pode obter uma licença temporária para fins de teste.

### P4: Posso manipular outros aspectos do documento antes de salvá-lo como imagem?

A4: Com certeza! Aspose.Note oferece uma ampla gama de recursos para edição programática de documentos do OneNote.

### P5: Onde posso encontrar suporte se encontrar problemas?

A5: Você pode encontrar suporte no fórum Aspose.Note[aqui](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

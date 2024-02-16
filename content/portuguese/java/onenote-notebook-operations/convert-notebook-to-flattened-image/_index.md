---
title: Converter bloco de notas em imagem achatada no OneNote - Aspose.Note
linktitle: Converter bloco de notas em imagem achatada no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como converter um bloco de notas em uma imagem achatada no OneNote usando Aspose.Note para Java. Preserve todos os elementos em um único arquivo de imagem sem esforço.
type: docs
weight: 13
url: /pt/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## Introdução

Neste tutorial, iremos guiá-lo através do processo de conversão de um notebook em uma imagem achatada no OneNote usando Aspose.Note para Java. Isso permite que você salve seu notebook como um arquivo de imagem, garantindo que todos os elementos sejam preservados em um único formato de imagem.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1. Java Development Kit (JDK) instalado em seu sistema.
2.  Biblioteca Aspose.Note para Java baixada e configurada em seu projeto Java. Você pode baixar a biblioteca em[aqui](https://releases.aspose.com/note/java/).
3. Conhecimento básico de programação Java.

## Importar pacotes

Para começar, você precisa importar os pacotes necessários do Aspose.Note for Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Etapa 1: configurar o diretório de documentos

Primeiramente, defina o diretório onde o arquivo do seu notebook está localizado:

```java
String dataDir = "Your Document Directory";
```

 Substituir`"Your Document Directory"` com o caminho para o arquivo do seu notebook.

## Etapa 2: carregar o notebook

 Em seguida, carregue o arquivo do notebook usando o`Notebook` aula:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Certifique-se de substituir`"test.onetoc2"` com o nome do arquivo do seu notebook.

## Etapa 3: definir opções para salvar imagens

Agora, configure as opções para salvar o notebook como imagem. Especificaremos o formato de salvamento como PNG e definiremos a resolução para 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Você pode ajustar a resolução de acordo com suas necessidades.

## Etapa 4: nivelar o caderno

Para garantir que todos os elementos sejam nivelados em uma única imagem, defina o`flatten` opção para`true`:

```java
saveOptions.setFlatten(true);
```

Isso garante que a imagem resultante mantenha o layout do seu notebook.

## Etapa 5: salvar imagem

Por fim, salve o notebook como uma imagem achatada:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Substituir`"ExportImageasFlattenedNotebook_out.png"` com o nome do arquivo de saída desejado.

## Conclusão

Concluindo, usando Aspose.Note para Java, você pode facilmente converter seu notebook em uma imagem achatada no OneNote. Este processo garante que todos os elementos sejam preservados em um único formato de imagem, facilitando o compartilhamento e a visualização.

## Perguntas frequentes

### Q1: Posso ajustar a resolução da imagem de saída?

 A1: Sim, você pode ajustar a resolução de acordo com suas necessidades, modificando o`setResolution` parâmetro do método.

### Q2: O Aspose.Note oferece suporte a outros formatos de imagem para exportação?

A2: Sim, Aspose.Note suporta vários formatos de imagem, como PNG, JPEG, BMP, etc., para exportação de notebooks.

### Q3: Posso personalizar ainda mais a imagem de saída?

A3: Sim, Aspose.Note oferece amplas opções para personalizar a imagem de saída, incluindo tamanho da página, orientação e configurações de qualidade.

### Q4: Existe uma versão de teste disponível para Aspose.Note para Java?

 A4: Sim, você pode obter uma versão de avaliação gratuita em[aqui](https://releases.aspose.com/).

### Q5: Onde posso encontrar suporte para Aspose.Note para Java?

 A5: Você pode encontrar suporte e recursos no fórum Aspose.Note[aqui](https://forum.aspose.com/c/note/28).
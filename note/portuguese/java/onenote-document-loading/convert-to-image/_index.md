---
title: Converter documento do OneNote em imagem - Java
linktitle: Converter documento do OneNote em imagem - Java
second_title: API Java Aspose.Note
description: Aprenda a converter o OneNote em imagem usando Aspose.Note para Java. Siga etapas fáceis, carregue o documento, inicialize as opções e salve como PNG.
type: docs
weight: 14
url: /pt/java/onenote-document-loading/convert-to-image/
---
## Introdução

Neste tutorial, orientaremos você no processo de uso do Aspose.Note for Java para converter um documento do OneNote em uma imagem. Dividiremos cada etapa em instruções fáceis de seguir.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1. Java Development Kit (JDK) instalado em seu sistema.
2.  Aspose.Note para biblioteca Java. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/java/).

## Importar pacotes

Primeiro, importe os pacotes necessários em seu código Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Agora vamos dividir o código de exemplo fornecido em várias etapas:

## Etapa 1: configurar o diretório de documentos

Defina o diretório onde seu documento do OneNote está localizado:

```java
String dataDir = "Your Document Directory";
```

 Substituir`"Your Document Directory"` com o caminho para o seu documento do OneNote.

## Etapa 2: carregue o documento

Carregue o documento OneNote no Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Garantir`"Sample1.one"` corresponde ao nome do seu arquivo de documento do OneNote.

## Etapa 3: inicializar ImageSaveOptions

 Inicialize o`ImageSaveOptions` objeto para especificar o formato de salvamento:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Aqui, estamos salvando o documento como uma imagem PNG. Você pode escolher outros formatos como JPEG ou BMP, se necessário.

## Etapa 4: salve o documento como imagem

Salve o documento carregado como uma imagem:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Esta linha salva o documento como uma imagem PNG com as opções especificadas.

## Etapa 5: Imprimir confirmação

Imprima uma mensagem para confirmar que o arquivo foi salvo:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Esta linha notifica você sobre a conversão bem-sucedida e a localização do arquivo de imagem salvo.

## Conclusão

Seguindo as etapas descritas acima, você pode converter facilmente um documento do OneNote em uma imagem usando Aspose.Note para Java. É uma maneira simples e eficaz de lidar com conversões de documentos em seus aplicativos Java.

## Perguntas frequentes

### P1: Posso converter vários documentos do OneNote de uma só vez?

A1: Sim, você pode percorrer uma lista de documentos e realizar a operação de conversão para cada documento.

### Q2: O Aspose.Note oferece suporte a outros formatos de saída além de imagens?

A2: Sim, Aspose.Note suporta vários formatos de saída, como PDF, HTML e formatos Microsoft Word.

### Q3: O Aspose.Note é compatível com todas as versões de arquivos do OneNote?

A3: Aspose.Note oferece compatibilidade com arquivos OneNote criados em diferentes versões do Microsoft OneNote.

### Q4: Posso personalizar a resolução das imagens de saída?

A4: Sim, você pode ajustar a resolução e outros parâmetros usando as opções disponíveis no Aspose.Note.

### Q5: O Aspose.Note requer conectividade com a Internet para conversão de documentos?

A5: Não, o Aspose.Note opera localmente sem a necessidade de conexão com a Internet.
---
title: Construir documento e inserir imagem no OneNote usando Java
linktitle: Construir documento e inserir imagem no OneNote usando Java
second_title: API Java Aspose.Note
description: Aprenda como criar documentos do OneNote e inserir imagens usando Aspose.Note para Java. Tutorial passo a passo para integração perfeita.
type: docs
weight: 12
url: /pt/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## Introdução

Neste tutorial, exploraremos como usar Aspose.Note for Java para criar documentos do OneNote e inserir imagens neles. Aspose.Note é uma API Java poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote programaticamente. Descreveremos cada etapa em detalhes para guiá-lo durante o processo.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos:

1. Java Development Kit (JDK): Certifique-se de ter o JDK instalado em seu sistema.
2.  Biblioteca Aspose.Note para Java: Baixe e instale a biblioteca Aspose.Note para Java do[local na rede Internet](https://releases.aspose.com/note/java/).
3. IDE (Ambiente de Desenvolvimento Integrado): Use qualquer IDE compatível com Java, como IntelliJ IDEA ou Eclipse para codificação.

## Importar pacotes

Comece importando os pacotes necessários em seu código Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Etapa 1: configurar o documento

Primeiro, crie um novo documento do OneNote e inicialize os objetos necessários:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Etapa 2: inicializar o esboço

Configure o contorno do documento e especifique as propriedades de deslocamento:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Etapa 3: adicionar imagem

Carregue uma imagem e especifique seu alinhamento:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Etapa 4: adicionar imagem ao elemento de contorno

Anexe a imagem a um elemento de contorno:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Etapa 5: adicionar nós de contorno e de página

Adicione o esboço e os nós de página ao documento:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Etapa 6: Salvar documento

Por fim, salve o documento do OneNote:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusão

Parabéns! Você aprendeu com sucesso como criar documentos do OneNote e inserir imagens neles usando Aspose.Note para Java. Seguindo essas etapas, você pode gerenciar e manipular com eficiência arquivos do OneNote em seus aplicativos Java.

## Perguntas frequentes

### Q1: Onde posso encontrar a documentação do Aspose.Note para Java?

 A1: Você pode acessar a documentação[aqui](https://reference.aspose.com/note/java/).

### Q2: Como faço o download do Aspose.Note para Java?

 A2: Você pode baixar Aspose.Note para Java no[página de download](https://releases.aspose.com/note/java/).

### Q3: Existe uma avaliação gratuita disponível para Aspose.Note para Java?

 A3: Sim, você pode obter uma avaliação gratuita no[local na rede Internet](https://releases.aspose.com/).

### Q4: Onde posso obter suporte para Aspose.Note para Java?

 A4: Para obter suporte, visite o[Fórum Aspose.Note](https://forum.aspose.com/c/note/28).

### Q5: Posso obter uma licença temporária para Aspose.Note for Java?

 A5: Sim, você pode solicitar uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

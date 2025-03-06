---
title: Salvar documento no OneNote usando SaveFormat - Aspose.Note
linktitle: Salvar documento no OneNote usando SaveFormat - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como salvar documentos no formato OneNote usando Aspose.Note para Java. Siga este tutorial passo a passo para integração perfeita com seus aplicativos Java.
weight: 12
url: /pt/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar documento no OneNote usando SaveFormat - Aspose.Note

## Introdução

Aspose.Note for Java é uma biblioteca poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote programaticamente. Salvar um documento no formato OneNote usando SaveFormat é um processo simples. Neste tutorial, percorreremos as etapas necessárias para realizar esta tarefa.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1. Java Development Kit (JDK) instalado em seu sistema.
2.  Biblioteca Aspose.Note para Java baixada. Você pode obtê-lo de[aqui](https://releases.aspose.com/note/java/).
3. Compreensão básica da linguagem de programação Java.

## Importar pacotes

 Primeiro, você precisa importar os pacotes necessários para o seu projeto Java. Isto inclui importar o`com.aspose.note` pacote para trabalhar com funcionalidades Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Etapa 1: configurar o diretório de documentos

Defina o diretório onde seu documento está localizado e onde deseja salvar o arquivo de saída.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: carregar o documento

 Carregue o documento em seu aplicativo Java usando o`Document` classe fornecida por Aspose.Note.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## Etapa 3: salvar o documento no formato OneNote

Salve o documento carregado no formato OneNote usando o`save` método e especificando o formato de arquivo de saída desejado como`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## Conclusão

Neste tutorial, aprendemos como salvar um documento no formato OneNote usando SaveFormat em Aspose.Note para Java. Seguindo estas etapas simples, você pode integrar perfeitamente essa funcionalidade em seus aplicativos Java.

## Perguntas frequentes

### Q1: O Aspose.Note para Java é compatível com todas as versões do Microsoft OneNote?

A1: Aspose.Note for Java oferece suporte a várias versões do Microsoft OneNote, garantindo compatibilidade em diferentes ambientes.

### Q2: Posso experimentar o Aspose.Note para Java antes de comprá-lo?

 A2: Sim, você pode baixar uma versão de avaliação gratuita do Aspose.Note para Java em[aqui](https://releases.aspose.com/).

### Q3: Onde posso encontrar documentação para Aspose.Note para Java?

 A3: Documentação detalhada para Aspose.Note para Java pode ser encontrada[aqui](https://reference.aspose.com/note/java/).

### Q4: Como posso obter suporte técnico para Aspose.Note para Java?

 A4: Para assistência técnica e suporte, você pode visitar o fórum Aspose.Note[aqui](https://forum.aspose.com/c/note/28).

### Q5: Existe uma opção de licença temporária disponível para Aspose.Note for Java?

 A5: Sim, você pode obter uma licença temporária para Aspose.Note for Java em[aqui](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

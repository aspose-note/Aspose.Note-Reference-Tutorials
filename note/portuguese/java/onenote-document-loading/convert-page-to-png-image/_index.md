---
date: 2025-11-29
description: Aprenda a exportar uma página do OneNote para PNG usando o Aspose.Note
  para Java. Siga instruções passo a passo para definir o índice da página, converter
  a página e salvar a imagem.
language: pt
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Exportar página do OneNote para imagem PNG em Java usando Aspose.Note
url: /java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar página do OneNote para imagem PNG em Java usando Aspose.Note

## Introdução

Neste tutorial você descobrirá **como exportar uma página do OneNote** para uma imagem PNG usando a biblioteca Aspose.Note para Java. Vamos percorrer tudo o que você precisa — desde preparar o ambiente até definir o índice da página e, finalmente, salvar a página como um arquivo PNG de alta qualidade. Ao final, você poderá adicionar essa funcionalidade a qualquer aplicação Java que trabalhe com documentos OneNote.

## Respostas rápidas
- **Qual biblioteca é necessária?** Aspose.Note para Java.  
- **Posso exportar uma única página?** Sim — use `setPageIndex` para direcionar a página exata.  
- **Formatos de imagem suportados?** PNG, JPEG, GIF, BMP, TIFF (PNG mostrado aqui).  
- **Preciso de licença?** Um teste gratuito está disponível; uma licença é necessária para produção.  
- **Quanto tempo leva a implementação?** Normalmente menos de 10 minutos para uma conversão básica.

## O que é “exportar página do OneNote”?
Exportar uma página do OneNote significa converter uma página específica dentro de um documento `.one` em um arquivo de imagem independente (PNG neste caso). Isso é útil quando você precisa compartilhar, incorporar ou processar o conteúdo do OneNote fora do ambiente do OneNote.

## Por que usar Aspose.Note para Java para converter OneNote em PNG?
- **Sem dependência do Microsoft Office** – funciona em qualquer plataforma que execute Java.  
- **Controle granular** – você pode escolher qualquer página via `setPageIndex`.  
- **Saída de alta qualidade** – PNG preserva gráficos vetoriais e clareza do texto.  
- **Pronto para lote** – fácil de percorrer páginas para conversão em massa.

## Pré-requisitos

Antes de começar, certifique‑se de que você tem:

1. **Java Development Kit (JDK)** – versão 8 ou superior.  
2. **Aspose.Note para Java** – baixe o JAR mais recente no [site da Aspose](https://releases.aspose.com/note/java/).  
3. **Um documento OneNote** (`.one`) que contenha a página que você deseja exportar.

## Importar Pacotes

Primeiro, importe as classes Java necessárias:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Guia passo a passo

### Etapa 1: Carregar o documento OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Usamos a classe `Document` para ler o arquivo OneNote do disco. O objeto `LoadOptions` permite personalizar o comportamento de carregamento, se necessário.

### Etapa 2: Inicializar ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` informa ao Aspose.Note que queremos a saída no formato **PNG**. Você pode mudar para JPEG, BMP etc., alterando `SaveFormat`.

### Etapa 3: Definir o índice da página (Como converter página do OneNote)

```java
// set page index
opts.setPageIndex(0);
```

O método `setPageIndex` seleciona qual página exportar. A numeração das páginas começa em **0**, portanto `0` refere‑se à primeira página. Ajuste esse valor para exportar outra página.

### Etapa 4: Salvar o documento como PNG (Salvar OneNote como PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Chamar `save` grava a página selecionada em um arquivo PNG no disco. O nome de arquivo `ConvertSpecificPageToPngImage_out.png` é apenas um exemplo — você pode nomeá‑lo como desejar.

## Problemas comuns e dicas

- **Índice de página incorreto** – Lembre‑se de que a indexação começa em 0. Se a imagem ficar em branco, verifique o valor do índice.  
- **JAR do Aspose.Note ausente** – Certifique‑se de que o JAR está no seu classpath; caso contrário, você verá `ClassNotFoundException`.  
- **Páginas muito grandes** – Para páginas muito grandes, considere aumentar o tamanho do heap da JVM (`-Xmx`) para evitar `OutOfMemoryError`.

## Perguntas frequentes

### Q1: Posso converter várias páginas em imagens PNG de uma só vez usando Aspose.Note para Java?
A1: Sim, você pode percorrer as páginas do documento, atualizar `opts.setPageIndex(i)` e chamar `save` em cada iteração.

### Q2: O Aspose.Note para Java suporta outros formatos de imagem além de PNG?
A2: Absolutamente. Você pode definir `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` ou `SaveFormat.Tiff` em `ImageSaveOptions`.

### Q3: Existe uma versão de teste gratuita do Aspose.Note para Java?
A3: Sim, você pode baixar uma versão de teste gratuita no [site](https://releases.aspose.com/).

### Q4: Posso obter assistência técnica se encontrar problemas com Aspose.Note para Java?
A4: Absolutamente, você pode buscar suporte no fórum da comunidade Aspose [aqui](https://forum.aspose.com/c/note/28).

### Q5: Onde posso comprar uma licença para Aspose.Note para Java?
A5: Você pode adquirir uma licença na [página de compra](https://purchase.aspose.com/buy).

### Q6: Como exportar uma página que contém imagens incorporadas?
A6: Imagens incorporadas são renderizadas automaticamente na saída PNG; nenhum código extra é necessário.

### Q7: Posso definir DPI ou resolução da imagem?
A7: Sim, use `opts.setResolution(int dpi)` antes de chamar `save` para controlar a qualidade da saída.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-11-29  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

---
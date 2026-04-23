---
date: 2026-02-05
description: Aprenda como exportar páginas do OneNote e salvar o OneNote como imagem.
  Este guia mostra como converter .one para png, definir o índice da página e exportar
  a imagem da página do OneNote usando Aspose.Note para Java.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Como Exportar uma Página do OneNote para Imagem PNG em Java usando Aspose.Note
url: /pt/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar página do OneNote para imagem PNG em Java usando Aspose.Note

## Introdução

Neste tutorial você descobrirá **como exportar página do OneNote** para uma imagem PNG usando a biblioteca Aspose.Note para Java. **Como exportar onenote** páginas é uma necessidade comum quando você deseja compartilhar notas fora do ecossistema do OneNote, incorporá‑las em relatórios ou processá‑las com ferramentas de processamento de imagens. Vamos percorrer tudo o que você precisa — desde preparar seu ambiente até definir o índice da página, converter a página e salvar o resultado como um arquivo PNG de alta qualidade. Ao final, você será capaz de **salvar onenote como imagem** em qualquer aplicação Java.

## Respostas Rápidas
- **Qual biblioteca é necessária?** Aspose.Note for Java.  
- **Posso exportar uma única página?** Sim — use `setPageIndex` para direcionar a página exata.  
- **Formatos de imagem suportados?** PNG, JPEG, GIF, BMP, TIFF (PNG mostrado aqui).  
- **Preciso de licença?** Um teste gratuito está disponível; uma licença é necessária para produção.  
- **Quanto tempo leva a implementação?** Normalmente menos de 10 minutos para uma conversão básica.  
- **Como converter .one para png?** Carregue o arquivo `.one` com `Document`, defina o índice da página e salve com `ImageSaveOptions`.  

## O que é “exportar página do OneNote”?
Exportar uma página do OneNote significa converter uma página específica dentro de um documento `.one` em um arquivo de imagem independente (PNG neste caso). Isso é útil quando você precisa **exportar imagem da página do onenote** para compartilhamento, incorporação ou análise adicional baseada em imagens.

## Por que usar Aspose.Note para Java para converter OneNote em PNG?
- **Sem dependência do Microsoft Office** – funciona em qualquer plataforma que execute Java.  
- **Controle granular** – você pode escolher qualquer página via `setPageIndex`.  
- **Saída de alta qualidade** – PNG mantém gráficos vetoriais e clareza de texto.  
- **Pronto para lote** – fácil de percorrer as páginas para conversão em massa, tornando simples **converter onenote para png** de várias páginas de uma vez.  

## Pré-requisitos

Antes de começar, certifique‑se de que você tem:

1. **Java Development Kit (JDK)** – versão 8 ou superior.  
2. **Aspose.Note for Java** – faça o download do JAR mais recente no [site da Aspose](https://releases.aspose.com/note/java/).  
3. **Um documento OneNote** (`.one`) que contém a página que você deseja exportar.

## Importar Pacotes

Primeiro, importe as classes Java necessárias:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Essas importações dão acesso à API principal do Aspose.Note, incluindo carregamento de documentos e configuração de opções de salvamento de imagem.

## Guia passo a passo

### Etapa 1: Carregar o documento OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Usamos a classe `Document` para ler o arquivo OneNote do disco. O objeto `LoadOptions` permite personalizar o comportamento de carregamento, se necessário. Esta etapa é a base para **converter .one para png**.

### Etapa 2: Inicializar ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` informa ao Aspose.Note que queremos a saída no formato **PNG**. Você pode mudar para JPEG, BMP, etc., alterando `SaveFormat`. Este objeto também permite controlar DPI, profundidade de cor e outras configurações específicas de imagem.

### Etapa 3: Definir o índice da página (Como converter página do OneNote)

```java
// set page index
opts.setPageIndex(0);
```

O método `setPageIndex` seleciona qual página exportar. A numeração das páginas começa em **0**, portanto `0` refere‑se à primeira página. Ajuste esse valor para **exportar uma página diferente** ou para percorrer as páginas quando precisar **salvar onenote como imagem** para cada uma.

### Etapa 4: Salvar o documento como PNG (Salvar OneNote como PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Chamar `save` grava a página selecionada em um arquivo PNG no disco. O nome do arquivo `ConvertSpecificPageToPngImage_out.png` é apenas um exemplo — você pode nomeá‑lo como quiser. Esta etapa final **exporta imagem da página do onenote** pronta para uso em relatórios, páginas web ou processamento adicional.

## Problemas comuns e dicas

- **Índice de página incorreto** – Lembre‑se de que a indexação começa em 0. Se você obtiver uma imagem em branco, verifique o valor do índice.  
- **JAR do Aspose.Note ausente** – Certifique‑se de que o JAR está no seu classpath; caso contrário, você verá `ClassNotFoundException`.  
- **Páginas grandes** – Para páginas muito grandes, considere aumentar o tamanho do heap da JVM (`-Xmx`) para evitar `OutOfMemoryError`.  
- **Controle de resolução** – Use `opts.setResolution(300)` (ou qualquer DPI que precisar) antes de chamar `save` para melhorar a clareza da imagem.  

## Perguntas Frequentes

### Q1: Posso converter várias páginas em imagens PNG de uma só vez usando Aspose.Note para Java?
A1: Sim, você pode percorrer as páginas do documento, atualizar `opts.setPageIndex(i)` e chamar `save` em cada iteração.

### Q2: O Aspose.Note para Java suporta outros formatos de imagem além de PNG?
A2: Absolutamente. Você pode definir `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` ou `SaveFormat.Tiff` em `ImageSaveOptions`.

### Q3: Existe uma versão de teste gratuita disponível para Aspose.Note para Java?
A3: Sim, você pode baixar um teste gratuito no [site](https://releases.aspose.com/).

### Q4: Posso obter assistência técnica se encontrar algum problema com Aspose.Note para Java?
A4: Absolutamente, você pode buscar suporte no fórum da comunidade Aspose [aqui](https://forum.aspose.com/c/note/28).

### Q5: Onde posso comprar uma licença para Aspose.Note para Java?
A5: Você pode comprar uma licença na [página de compra](https://purchase.aspose.com/buy).

### Q6: Como exporto uma página que contém imagens incorporadas?
A6: Imagens incorporadas são renderizadas automaticamente na saída PNG; nenhum código extra é necessário.

### Q7: Posso definir o DPI ou a resolução da imagem?
A7: Sim, use `opts.setResolution(int dpi)` antes de chamar `save` para controlar a qualidade da saída.

---

**Última atualização:** 2026-02-05  
**Testado com:** Aspose.Note for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
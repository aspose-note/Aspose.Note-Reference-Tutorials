---
date: 2026-11-05
description: Aprenda como reduzir o tamanho de arquivos TIFF ao converter cadernos
  do OneNote para TIFF em Java usando Aspose.Note. Inclui opções JPEG, PackBits e
  TIFF preto‑e‑branco.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Como reduzir o tamanho de arquivos TIFF ao converter OneNote em Java
og_description: Aprenda como reduzir o tamanho de arquivos TIFF ao converter cadernos
  do OneNote para TIFF em Java usando Aspose.Note. Inclui opções JPEG, PackBits e
  TIFF preto‑e‑branco.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Como reduzir o tamanho de arquivos TIFF ao converter OneNote em Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Como reduzir o tamanho de arquivos TIFF ao converter OneNote em Java
url: /pt/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como reduzir o tamanho de arquivos TIFF ao converter OneNote em Java

## Introdução

Neste tutorial, você descobrirá como **reduzir o tamanho de arquivos TIFF** ao converter cadernos do OneNote em imagens TIFF usando Aspose.Note para Java. Vamos percorrer três métodos de compressão — TIFF JPEG, PackBits e CCITT Group 3 (TIFF preto‑e‑branco) — e mostrar como ajustar a qualidade da imagem, controlar o modo de cor e manter os tamanhos de arquivo ideais para web, arquivamento ou cenários de fax.

## Respostas rápidas
- **O que é compressão TIFF JPEG?** Um método de compressão com perdas que reduz o tamanho de arquivos TIFF enquanto preserva a qualidade visual.  
- **Qual biblioteca realiza a conversão?** Aspose.Note para Java.  
- **Preciso de uma licença?** Uma avaliação gratuita funciona para testes; uma licença é necessária para produção.  
- **Posso alterar a qualidade da imagem?** Sim, defina a propriedade `quality` em `ImageSaveOptions`.  
- **A conversão em lote é possível?** Absolutamente – percorra os documentos e aplique as mesmas opções.

## Visão geral da compressão TIFF JPEG

A compressão TIFF JPEG armazena os dados da imagem em um contêiner TIFF, mas aplica o algoritmo com perdas do JPEG para reduzir o arquivo. É ideal quando você precisa de um equilíbrio entre **qualidade da imagem TIFF** e tamanho de arquivo menor, especialmente para cenários web ou de arquivamento.

## Por que usar diferentes tipos de compressão TIFF?

Você escolhe o tipo de compressão com base no conteúdo e nas necessidades de armazenamento: JPEG funciona melhor para fotografias, PackBits oferece compressão sem perdas para gráficos com grandes áreas uniformes, e CCITT Group 3 fornece compressão de alta taxa para documentos monocromáticos no estilo fax. Selecionar o método correto permite que você **reduza o tamanho de arquivos TIFF** sem comprometer a fidelidade visual exigida pela sua aplicação.

## Escolhendo a compressão correta

- **JPEG** – Qualidade ajustável (0‑100) permite equilibrar tamanho e detalhe, perfeito para páginas com cores ricas.  
- **PackBits** – Codificação run‑length sem perdas; ideal quando você precisa manter cada pixel exatamente.  
- **CCITT Group 3** – Apenas monocromático; maximiza a compressão para textos escaneados ou documentos de fax.  

## Converter OneNote para TIFF usando Aspose.Note

Se o seu objetivo é **converter OneNote para TIFF**, os três métodos abaixo cobrem os cenários mais comuns. Cada método carrega um arquivo `.one`, configura `ImageSaveOptions` e salva o resultado como um arquivo `.tiff`.

## Pré-requisitos

- Java Development Kit (JDK) instalado.  
- Biblioteca Aspose.Note para Java adicionada ao seu projeto (Maven/Gradle ou JAR manual).  
- Familiaridade básica com a sintaxe Java.

## Importar pacotes

As classes `ImageSaveOptions`, `TiffCompression` e `ColorMode` são o núcleo da API de conversão.  

`ImageSaveOptions` define as opções para salvar imagens, como formato e compressão.  
`TiffCompression` enumera os algoritmos de compressão TIFF suportados.  
`ColorMode` especifica a profundidade de cor, por exemplo, colorido ou preto‑e‑branco.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Etapa 1: salvar em TIFF usando compressão TIFF JPEG

### Salvando TIFF com compressão JPEG em Java

Carregue o arquivo OneNote, configure `ImageSaveOptions` com compressão JPEG, opcionalmente defina o valor `quality` e chame o método de salvamento. Esse padrão de duas etapas fornece controle total sobre o tamanho da saída e a fidelidade visual.

1. Aponte `dataDir` para a pasta que contém seu arquivo `.one`.  
2. Chame `SaveToTiffUsingJpegCompression()` a partir do seu método principal ou serviço.  
3. O arquivo `.tiff` resultante aparecerá no mesmo diretório.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Explicação**

- `ImageSaveOptions` informa ao Aspose.Note para gerar um arquivo TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` seleciona compressão JPEG.  
- `setQuality(93)` (opcional) ajusta finamente a qualidade da imagem; valores menores produzem arquivos menores.

## Visão geral da compressão TIFF PackBits

PackBits é um algoritmo de compressão sem perdas que funciona melhor para imagens com grandes áreas de cor sólida. Frequentemente é referido como **compressão tiff packbits** na documentação.

## Salvando TIFF com compressão PackBits em Java

Se você precisar de uma opção sem perdas, PackBits é um algoritmo simples de run‑length que funciona bem para gráficos com cores sólidas. Configure `ImageSaveOptions` com `TiffCompression.PackBits` e salve o documento.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Explicação**

- `setTiffCompression(TiffCompression.PackBits)` altera o método de compressão.  
- Nenhuma configuração de qualidade é necessária porque PackBits é sem perdas.

## Salvando TIFF com compressão CCITT Group 3 em Java

Para documentos no estilo fax, você geralmente deseja um **TIFF preto e branco**. CCITT Group 3 fornece alta compressão para imagens monocromáticas. Defina o modo de cor para preto‑e‑branco e escolha o enum de compressão CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Explicação**

- `setColorMode(ColorMode.BlackAndWhite)` força uma saída monocromática.  
- `setTiffCompression(TiffCompression.Ccitt3)` aplica a compressão orientada a fax.

## Problemas comuns e dicas

| Problema | Solução |
|-------|----------|
| **O arquivo de saída é maior que o esperado** | Tente reduzir o valor `quality` do JPEG ou mude para PackBits se a compressão sem perdas for aceitável. |
| **As cores parecem desbotadas** | Certifique-se de que não definiu acidentalmente `ColorMode.BlackAndWhite` quando precisar de cores completas. |
| **Erro de formato de imagem não suportado** | Verifique se está usando uma versão recente do Aspose.Note; builds mais antigos podem não ter certos enums de compressão. |
| **LicenseException em tempo de execução** | Instale uma licença válida do Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Perguntas frequentes

**Q: Posso converter outros tipos de documento (por exemplo, PDF, DOCX) para TIFF com essas opções?**  
A: Sim. Embora o Aspose.Note se concentre em arquivos OneNote, Aspose.PDF, Aspose.Words e outras bibliotecas fornecem `ImageSaveOptions` semelhantes para seus formatos.

**Q: Como a compressão TIFF JPEG difere de um arquivo JPEG padrão?**  
A: O algoritmo JPEG é o mesmo, mas os dados da imagem ficam dentro de um contêiner TIFF, que pode conter várias páginas e metadados mais ricos.

**Q: É possível processar em lote muitos arquivos `.one`?**  
A: Absolutamente. Percorra um diretório, chame qualquer um dos três métodos para cada arquivo e colete os TIFFs resultantes.

**Q: Posso controlar o DPI/resolução do TIFF de saída?**  
A: Sim. Use `options.setResolution(int dpi)` antes de salvar.

**Q: O Aspose.Note suporta processamento assíncrono?**  
A: A própria API é síncrona, mas você pode envolver as chamadas em `CompletableFuture` do Java ou em um pool de threads para execução paralela.

## Conclusão

Agora você tem um conjunto completo de ferramentas de **conversão TIFF em Java** que permite **reduzir o tamanho de arquivos TIFF** ao salvar documentos OneNote como arquivos TIFF usando compressão JPEG, PackBits ou CCITT Group 3 Fax. Ajuste a qualidade, o modo de cor e a resolução para atender aos seus requisitos específicos e integre esses métodos em fluxos de trabalho em lote para máxima produtividade.

---

**Última atualização:** 2026-11-05  
**Testado com:** Aspose.Note for Java 26.4 (latest at time of writing)  
**Autor:** Aspose

## Tutoriais relacionados

- [Como renderizar a imagem da página OneNote (JPEG) usando Save Format com Aspose.Note para Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Usar Aspose.Note para Java para salvar OneNote como PNG com opções – Converter caderno em imagem](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Como exportar OneNote como imagem em escala de cinza – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
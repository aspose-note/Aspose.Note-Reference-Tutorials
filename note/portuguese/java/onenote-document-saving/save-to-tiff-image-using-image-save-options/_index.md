---
date: 2026-03-14
description: Aprenda a salvar documentos do OneNote como arquivos TIFF usando compressão
  TIFF JPEG, compressão TIFF PackBits ou CCITT Group 3 Fax em Java. Controle a qualidade
  da imagem, o tamanho do arquivo e o modo de cor com o Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Salvar como imagem TIFF usando compressão TIFF JPEG no OneNote
url: /pt/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar imagem TIFF usando compressão TIFF JPEG no OneNote

## Introdução

Neste tutorial você descobrirá **como salvar um documento OneNote em um arquivo TIFF usando compressão TIFF JPEG** e dois outros métodos de compressão populares. Vamos percorrer a configuração necessária, importar os pacotes Java necessários e fornecer código passo a passo claro para cada opção de compressão. Ao final, você poderá controlar **a qualidade da imagem TIFF**, reduzir o tamanho do arquivo e até produzir TIFFs em preto e branco para saída no estilo fax.

## Respostas rápidas
- **O que é compressão TIFF JPEG?** Um método de compressão com perdas que reduz o tamanho do arquivo TIFF enquanto preserva a qualidade visual.  
- **Qual biblioteca realiza a conversão?** Aspose.Note for Java.  
- **Preciso de licença?** Um teste gratuito funciona para testes; uma licença é necessária para produção.  
- **Posso alterar a qualidade da imagem?** Sim, defina a propriedade `quality` em `ImageSaveOptions`.  
- **É possível conversão em lote?** Absolutamente – percorra os documentos e aplique as mesmas opções.

## O que é compressão TIFF JPEG?
A compressão TIFF JPEG armazena os dados da imagem em um contêiner TIFF, mas aplica o algoritmo com perdas do JPEG para reduzir o arquivo. É ideal quando você precisa equilibrar **a qualidade da imagem TIFF** e um tamanho de arquivo menor, especialmente para cenários web ou de arquivamento.

## Por que usar diferentes tipos de compressão TIFF?
- **JPEG** – Bom para fotografias; oferece qualidade ajustável.  
- **PackBits** – Codificação simples sem perdas de comprimento de execução; útil para gráficos com áreas uniformes grandes.  
- **CCITT Group 3 Fax** – Apenas preto e branco; perfeito para documentos escaneados e transmissão por fax.  

Escolher a compressão correta permite atender às restrições de armazenamento sem sacrificar a fidelidade visual necessária para sua aplicação.

## Converter OneNote para TIFF usando Aspose.Note
Se o seu objetivo é **converter OneNote para TIFF**, os três métodos abaixo cobrem os cenários mais comuns. Cada método carrega um arquivo `.one`, configura `ImageSaveOptions` e salva o resultado como um arquivo `.tiff`.

## Pré-requisitos

- Java Development Kit (JDK) instalado.  
- Biblioteca Aspose.Note for Java adicionada ao seu projeto (Maven/Gradle ou JAR manual).  
- Familiaridade básica com a sintaxe Java.

## Importar Pacotes

Primeiro, traga as classes necessárias do Aspose.Note para o seu arquivo Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Etapa 1: Salvar em TIFF usando compressão TIFF JPEG

A seguir está o método completo que carrega um arquivo OneNote e o salva como TIFF com compressão JPEG. Ajuste o valor `quality` (0‑100) para controlar **a qualidade da imagem TIFF**.

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

- `ImageSaveOptions` indica ao Aspose.Note que a saída será um arquivo TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` seleciona a compressão JPEG.  
- `setQuality(93)` (opcional) ajusta finamente a qualidade da imagem; valores menores produzem arquivos menores.

### Como salvar TIFF com compressão JPEG em Java
1. Aponte `dataDir` para a pasta que contém seu arquivo `.one`.  
2. Chame `SaveToTiffUsingJpegCompression()` a partir do seu método principal ou serviço.  
3. O arquivo `.tiff` resultante aparecerá no mesmo diretório.

## Visão geral da compressão TIFF PackBits

PackBits é um algoritmo de compressão sem perdas que funciona melhor para imagens com grandes áreas de cor sólida. Frequentemente é referido como **compressão tiff packbits** na documentação.

## Etapa 2: Salvar em TIFF usando compressão PackBits

Se você precisar de uma opção sem perdas, PackBits é um algoritmo simples de comprimento de execução que funciona bem para gráficos com cores sólidas.

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

- `setTiffCompression(TiffCompression.PackBits)` troca o método de compressão.  
- Nenhuma configuração de qualidade é necessária porque PackBits é sem perdas.

## Etapa 3: Salvar em TIFF usando compressão CCITT Group 3 Fax (TIFF preto e branco)

Para documentos no estilo fax, geralmente você deseja um **TIFF preto e branco**. CCITT Group 3 oferece alta compressão para imagens monocromáticas.

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

## Problemas comuns & Dicas

| Problema | Solução |
|----------|----------|
| **O arquivo de saída é maior que o esperado** | Tente reduzir o valor `quality` do JPEG ou troque para PackBits se a compressão sem perdas for aceitável. |
| **As cores parecem desbotadas** | Certifique-se de não ter definido `ColorMode.BlackAndWhite` inadvertidamente quando precisar de cores completas. |
| **Erro de formato de imagem não suportado** | Verifique se está usando uma versão recente do Aspose.Note; builds antigos podem não ter certos enums de compressão. |
| **LicenseException em tempo de execução** | Instale uma licença válida do Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Perguntas Frequentes

**P: Posso converter outros tipos de documento (ex.: PDF, DOCX) para TIFF com essas opções?**  
R: Sim. Embora o Aspose.Note foque em arquivos OneNote, Aspose.PDF, Aspose.Words e outras bibliotecas fornecem `ImageSaveOptions` semelhantes para seus formatos.

**P: Como a compressão TIFF JPEG difere de um arquivo JPEG padrão?**  
R: O algoritmo JPEG é o mesmo, mas os dados da imagem ficam dentro de um contêiner TIFF, que pode conter várias páginas e metadados mais ricos.

**P: É possível processar em lote muitos arquivos `.one`?**  
R: Absolutamente. Percorra um diretório, chame qualquer um dos três métodos para cada arquivo e colete os TIFFs resultantes.

**P: Posso controlar o DPI/resolução do TIFF de saída?**  
R: Sim. Use `options.setResolution(int dpi)` antes de salvar.

**P: O Aspose.Note suporta processamento assíncrono?**  
R: A API em si é síncrona, mas você pode envolver as chamadas em `CompletableFuture` do Java ou em um pool de threads para execução paralela.

## Conclusão

Agora você tem um conjunto completo de ferramentas **java tiff conversion** que permite salvar documentos OneNote como arquivos TIFF usando compressão JPEG, PackBits ou CCITT Group 3 Fax. Ajuste a qualidade, o modo de cor e a resolução para atender aos requisitos específicos de **qualidade da imagem TIFF**, e integre esses métodos em fluxos de trabalho em lote para máxima produtividade.

---

**Última atualização:** 2026-03-14  
**Testado com:** Aspose.Note for Java 23.12 (mais recente no momento da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
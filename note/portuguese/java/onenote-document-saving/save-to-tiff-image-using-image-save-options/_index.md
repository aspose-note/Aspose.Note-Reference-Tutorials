---
date: 2025-12-17
description: Aprenda a salvar documentos do OneNote como arquivos TIFF usando compressão
  TIFF JPEG, PackBits ou CCITT Group 3 Fax em Java. Controle a qualidade da imagem,
  o tamanho do arquivo e o modo de cor com o Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Salvar como imagem TIFF usando compressão JPEG TIFF no OneNote
url: /pt/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar Imagem TIFF Usando Compressão TIFF JPEG no OneNote

## Introdução

Neste tutorial você descobrirá **como salvar um documento OneNote em um arquivo TIFF usando compressão TIFF JPEG** e dois outros métodos de compressão populares. Vamos percorrer a configuração necessária, importar os pacotes Java necessários e fornecer código passo a passo claro para cada opção de compressão. Ao final, você poderá controlar **a qualidade da imagem TIFF**, reduzir o tamanho do arquivo e até produzir TIFFs preto‑e‑branco para saída no estilo fax.

## Respostas Rápidas
- **O que é compressão TIFF JPEG?** Um método de compressão com perdas que reduz o tamanho do arquivo TIFF enquanto preserva a qualidade visual.  
- **Qual biblioteca realiza a conversão?** Aspose.Note for Java.  
- **Preciso de licença?** Um teste gratuito funciona para testes; uma licença é necessária para produção.  
- **Posso alterar a qualidade da imagem?** Sim, defina a propriedade `quality` em `ImageSaveOptions`.  
- **A conversão em lote é possível?** Absolutamente – percorra os documentos e aplique as mesmas opções.

## O que é Compressão TIFF JPEG?
A compressão TIFF JPEG armazena os dados da imagem no contêiner TIFF, mas aplica o algoritmo JPEG com perdas para reduzir o arquivo. É ideal quando você precisa de um equilíbrio entre **qualidade da imagem TIFF** e tamanho de arquivo menor, especialmente para cenários web ou de arquivamento.

## Por que Usar Diferentes Tipos de Compressão TIFF?
- **JPEG** – Boa para fotografias; oferece qualidade ajustável.  
- **PackBits** – Codificação run‑length simples e sem perdas; útil para gráficos com áreas uniformes grandes.  
- **CCITT Group 3 Fax** – Apenas preto‑e‑branco; perfeito para documentos escaneados e transmissão por fax.  

Escolher a compressão correta permite atender às restrições de armazenamento sem sacrificar a fidelidade visual necessária para sua aplicação.

## Pré‑requisitos

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

## Etapa 1: Salvar como TIFF Usando Compressão TIFF JPEG

Abaixo está o método completo que carrega um arquivo OneNote e o salva como TIFF com compressão JPEG. Ajuste o valor `quality` (0‑100) para controlar **a qualidade da imagem TIFF**.

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
- `setQuality(93)` (opcional) ajusta a qualidade da imagem; valores menores produzem arquivos menores.

### Como Salvar TIFF com Compressão JPEG em Java
1. Aponte `dataDir` para a pasta que contém seu arquivo `.one`.  
2. Chame `SaveToTiffUsingJpegCompression()` a partir do seu método `main` ou serviço.  
3. O arquivo `.tiff` resultante aparecerá no mesmo diretório.

## Etapa 2: Salvar como TIFF Usando Compressão PackBits

Se precisar de uma opção sem perdas, PackBits é um algoritmo run‑length simples que funciona bem para gráficos com cores sólidas.

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
- Não é necessário definir qualidade porque PackBits é sem perdas.

## Etapa 3: Salvar como TIFF Usando Compressão Fax CCITT Grupo 3 (TIFF Preto‑e‑Branco)

Para documentos no estilo fax, geralmente se deseja um **TIFF preto‑e‑branco**. CCITT Group 3 oferece alta compressão para imagens monocromáticas.

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

- `setColorMode(ColorMode.BlackAndWhite)` força a saída monocromática.  
- `setTiffCompression(TiffCompression.Ccitt3)` aplica a compressão orientada a fax.

## Problemas Comuns & Dicas

| Problema | Solução |
|----------|---------|
| **O arquivo de saída é maior que o esperado** | Tente reduzir o valor `quality` do JPEG ou troque para PackBits se a perda de qualidade for aceitável. |
| **As cores parecem desbotadas** | Certifique‑se de que não está definindo `ColorMode.BlackAndWhite` quando precisar de cores completas. |
| **Erro de formato de imagem não suportado** | Verifique se está usando uma versão recente do Aspose.Note; versões antigas podem não ter alguns enums de compressão. |
| **LicenseException em tempo de execução** | Instale uma licença válida do Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Perguntas Frequentes

**P: Posso converter outros tipos de documento (por exemplo, PDF, DOCX) para TIFF com essas opções?**  
R: Sim. O Aspose.Note foca em arquivos OneNote, mas as outras bibliotecas da Aspose (PDF, Words) fornecem `ImageSaveOptions` semelhantes para seus respectivos formatos.

**P: Como a compressão TIFF JPEG difere dos arquivos JPEG padrão?**  
R: Os dados da imagem são armazenados dentro de um contêiner TIFF, preservando metadados e permitindo múltiplas páginas, enquanto o algoritmo de compressão continua sendo JPEG.

**P: É possível processar em lote muitos arquivos `.one`?**  
R: Absolutamente. Percorra uma pasta, chame qualquer um dos três métodos por arquivo e colete os TIFFs resultantes.

**P: Posso controlar o DPI/resolução do TIFF de saída?**  
R: Sim. Use `options.setResolution(int dpi)` antes de salvar.

**P: O Aspose.Note suporta processamento assíncrono?**  
R: A API em si é síncrona, mas você pode envolver as chamadas em `CompletableFuture` ou pools de threads do Java para execução paralela.

## Conclusão

Agora você possui um conjunto completo de ferramentas **java tiff conversion** que permite salvar documentos OneNote como arquivos TIFF usando compressão JPEG, PackBits ou CCITT Group 3 Fax. Ajuste qualidade, modo de cor e resolução para atender aos seus requisitos específicos de **qualidade da imagem TIFF** e integre esses métodos em fluxos de trabalho em lote para máxima produtividade.

---

**Última atualização:** 2025-12-17  
**Testado com:** Aspose.Note for Java 23.12 (mais recente no momento da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
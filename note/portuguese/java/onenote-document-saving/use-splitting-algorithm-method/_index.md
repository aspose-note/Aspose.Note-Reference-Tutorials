---
date: 2026-03-16
description: Aprenda a exportar PDF do OneNote usando Aspose.Note para Java com o
  método Algoritmo de Divisão, controlar quebras de página e comprimir imagens PDF
  de forma eficiente.
linktitle: Export OneNote PDF with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Exportar PDF do OneNote com método de algoritmo de divisão – Aspose.Note
url: /pt/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PDF do OneNote com o Método do Algoritmo de Divisão – Aspose.Note

## Introduction

Se você precisar **exportar PDF do OneNote** programaticamente, o Aspose.Note for Java torna isso simples. Neste tutorial, percorreremos o Método do Algoritmo de Divisão, que permite controlar como o conteúdo é dividido entre as páginas, garantindo uma saída PDF limpa e legível. Você verá como definir as opções de salvamento em PDF, escolher o algoritmo de divisão de página correto e, finalmente, gerar o arquivo PDF — tudo com apenas algumas linhas de código Java.

## Quick Answers
- **O que o Algoritmo de Divisão faz?** Ele determina como os objetos que atravessam limites de página são tratados ao exportar páginas do OneNote para PDF.  
- **Qual biblioteca é necessária?** Aspose.Note for Java (download do site oficial da Aspose).  
- **Preciso de uma licença?** É necessária uma licença temporária ou completa para uso em produção; uma avaliação gratuita está disponível.  
- **Posso exportar cadernos grandes do OneNote?** Sim — a biblioteca processa arquivos grandes de forma eficiente e permite definir regras de divisão de página.  
- **Quais formatos de saída são suportados?** PDF, JPEG, PNG, XPS e mais; este guia foca na exportação para PDF.  
- **Como posso compactar imagens em PDF?** Use `pdfSaveOptions.setCompressImages(true)` para reduzir o tamanho das imagens no PDF gerado.  

## How to export OneNote PDF with Splitting Algorithm
Esta seção orienta você pelos passos exatos necessários para **converter páginas do OneNote** em um PDF, tratando quebras de página de forma inteligente.

## What is export onenote pdf?
Exportar PDF do OneNote significa converter o formato nativo `.one` em um documento PDF portátil. Isso é útil para compartilhar, arquivar ou imprimir conteúdo sem precisar do aplicativo OneNote.

## Why use the Splitting Algorithm for export onenote pdf?
O algoritmo oferece controle detalhado sobre como objetos complexos (tabelas, imagens, desenhos) são tratados nas quebras de página. Ao selecionar o algoritmo apropriado, você pode:

* Preservar o layout visual de cada página.  
* Evitar conteúdo cortado que de outra forma seria truncado.  
* Reduzir o número de páginas geradas quando objetos podem ser movidos para a página seguinte de forma limpa.  

## Prerequisites

Antes de começarmos, certifique‑se de que você tem os seguintes pré‑requisitos:

1. Java Development Kit (JDK): Certifique‑se de que o JDK está instalado em seu sistema. Você pode baixá‑lo no [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Biblioteca Aspose.Note for Java: Baixe e instale a biblioteca Aspose.Note for Java a partir do [download link](https://releases.aspose.com/note/java/).

## Import Packages

No seu projeto Java, importe os pacotes necessários para utilizar as funcionalidades do Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Define Document Directory

Configure o diretório onde seu documento OneNote está localizado.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the OneNote Document

Carregue o documento OneNote usando a classe `Document` do Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Step 3: Set PDF Save Options

Crie uma instância de `PdfSaveOptions` para especificar opções ao salvar o documento como PDF. É aqui que você **define o comportamento de divisão de página** e outras configurações relacionadas ao PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Step 4: Set Page Splitting Algorithm

Escolha o algoritmo de divisão apropriado de acordo com seus requisitos. Aqui, estamos usando `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, que mantém parte de um objeto na página atual e clona o restante para a página seguinte.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Step 5: Save the Document

Salve o documento com as opções de salvamento em PDF especificadas. Esta etapa **gera a saída PDF do OneNote** que você pode abrir, compartilhar ou imprimir.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Common Issues and Solutions

| Problema | Solução |
|----------|---------|
| **Objetos são cortados nos limites da página** | Experimente um algoritmo diferente, como `AlwaysSplitObjectsAlgorithm`, ou aumente o valor de limiar em `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **PDF de saída está em branco** | Verifique se o arquivo `.one` de origem não está corrompido e se o caminho `dataDir` está correto. |
| **Desempenho lento com cadernos grandes** | Use `pdfSaveOptions.setCompressImages(true)` para reduzir o uso de memória e considere processar o caderno em seções menores. |

## Frequently Asked Questions

**Q: Posso usar Aspose.Note for Java com outras linguagens de programação?**  
A: Sim, o Aspose.Note também está disponível para .NET, C++ e Python.

**Q: O Aspose.Note é adequado para processar arquivos grandes do OneNote?**  
A: Absolutamente. A biblioteca é otimizada para lidar com cadernos grandes de forma eficiente.

**Q: Onde posso encontrar recursos adicionais e suporte para Aspose.Note?**  
A: Você pode consultar a [documentação](https://reference.aspose.com/note/java/) e o [forum](https://forum.aspose.com/c/note/28) para suporte e orientações.

**Q: Posso experimentar o Aspose.Note antes de comprar?**  
A: Sim, você pode aproveitar um [teste gratuito](https://releases.aspose.com/) para explorar os recursos antes de efetuar a compra.

**Q: Como posso obter uma licença temporária para Aspose.Note?**  
A: Você pode solicitar uma [licença temporária](https://purchase.aspose.com/temporary-license/) para avaliar o produto durante um período de teste.

**Última atualização:** 2026-03-16  
**Testado com:** Aspose.Note 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
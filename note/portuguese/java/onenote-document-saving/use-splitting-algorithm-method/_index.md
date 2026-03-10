---
date: 2025-12-18
description: Aprenda a exportar páginas do OneNote para PDF usando Aspose.Note para
  Java. Escolha algoritmos de divisão, defina a divisão de páginas e gere arquivos
  PDF facilmente.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Exportar páginas do OneNote com método de algoritmo de divisão – Aspose.Note
url: /pt/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar Páginas do OneNote com o Método de Algoritmo de Divisão – Aspose.Note

## Introdução

Se você precisa **exportar páginas do OneNote** para um documento PDF programaticamente, o Aspose.Note para Java torna isso simples. Neste tutorial vamos percorrer o Método de Algoritmo de Divisão, que permite controlar como o conteúdo é dividido entre as páginas, garantindo um PDF limpo e legível. Você verá como definir as opções de salvamento em PDF, escolher o algoritmo de divisão de página adequado e, finalmente, gerar o arquivo PDF — tudo com apenas algumas linhas de código Java.

## Respostas Rápidas
- **O que o Algoritmo de Divisão faz?** Ele determina como os objetos que atravessam os limites das páginas são tratados ao exportar páginas do OneNote para PDF.  
- **Qual biblioteca é necessária?** Aspose.Note para Java (download no site oficial da Aspose).  
- **Preciso de licença?** É necessária uma licença temporária ou completa para uso em produção; há uma versão de avaliação gratuita.  
- **Posso exportar blocos de notas grandes do OneNote?** Sim – a biblioteca processa arquivos grandes de forma eficiente e permite definir regras de divisão de página.  
- **Quais formatos de saída são suportados?** PDF, JPEG, PNG, XPS e mais; este guia foca na exportação para PDF.

## O que é **exportar páginas do onenote**?
Exportar páginas do OneNote significa converter o formato nativo `.one` para um formato mais portátil, como PDF. Isso é útil para compartilhar, arquivar ou imprimir o conteúdo sem precisar do aplicativo OneNote.

## Por que usar o Algoritmo de Divisão para **exportar páginas do onenote**?
O algoritmo oferece controle detalhado sobre como objetos complexos (tabelas, imagens, desenhos) são tratados nas quebras de página. Ao selecionar o algoritmo apropriado, você pode:

* Preservar o layout visual de cada página.  
* Evitar conteúdo cortado que, de outra forma, seria truncado.  
* Reduzir o número de páginas geradas quando os objetos podem ser movidos para a página seguinte de forma limpa.  

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem os seguintes pré‑requisitos:

1. Java Development Kit (JDK): Garanta que o JDK esteja instalado em seu sistema. Você pode baixá‑lo no [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Biblioteca Aspose.Note para Java: Baixe e instale a biblioteca Aspose.Note para Java a partir do [download link](https://releases.aspose.com/note/java/).

## Importar Pacotes

No seu projeto Java, importe os pacotes necessários para utilizar as funcionalidades do Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Etapa 1: Definir Diretório do Documento

Configure o diretório onde seu documento OneNote está localizado.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Carregar o Documento OneNote

Carregue o documento OneNote usando a classe `Document` do Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Etapa 3: Definir Opções de Salvamento em PDF

Crie uma instância de `PdfSaveOptions` para especificar as opções de salvamento do documento como PDF. É aqui que você **define o comportamento de divisão de página** e outras configurações relacionadas ao PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Etapa 4: Definir Algoritmo de Divisão de Página

Escolha o algoritmo de divisão adequado de acordo com suas necessidades. Aqui, estamos usando `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, que mantém parte de um objeto na página atual e clona o restante para a página seguinte.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Etapa 5: Salvar o Documento

Salve o documento com as opções de salvamento em PDF especificadas. Esta etapa **gera a saída PDF do onenote** que você pode abrir, compartilhar ou imprimir.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Problemas Comuns e Soluções

| Problema | Solução |
|----------|---------|
| **Objetos são cortados nos limites da página** | Experimente outro algoritmo, como `AlwaysSplitObjectsAlgorithm`, ou aumente o valor de limiar em `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **PDF de saída está em branco** | Verifique se o arquivo `.one` de origem não está corrompido e se o caminho `dataDir` está correto. |
| **Desempenho lento com blocos de notas grandes** | Use `pdfSaveOptions.setCompressImages(true)` para reduzir o uso de memória e considere processar o bloco de notas em seções menores. |

## Perguntas Frequentes

**P: Posso usar o Aspose.Note para Java com outras linguagens de programação?**  
R: Sim, o Aspose.Note está disponível também para .NET, C++ e Python.

**P: O Aspose.Note é adequado para processar arquivos grandes do OneNote?**  
R: Absolutamente. A biblioteca é otimizada para lidar com blocos de notas extensos de forma eficiente.

**P: Onde posso encontrar recursos adicionais e suporte para o Aspose.Note?**  
R: Você pode consultar a [documentação](https://reference.aspose.com/note/java/) e o [forum](https://forum.aspose.com/c/note/28) para obter suporte e orientações.

**P: Posso testar o Aspose.Note antes de comprar?**  
R: Sim, você pode aproveitar um [free trial](https://releases.aspose.com/) para explorar os recursos antes de efetuar a compra.

**P: Como obter uma licença temporária para o Aspose.Note?**  
R: Você pode solicitar uma [temporary license](https://purchase.aspose.com/temporary-license/) para avaliar o produto durante um período de teste.

---

**Última atualização:** 2025-12-18  
**Testado com:** Aspose.Note 24.12 para Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
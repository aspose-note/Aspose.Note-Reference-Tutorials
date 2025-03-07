---
title: Criar documento com raiz e subpáginas no OneNote
linktitle: Criar documento com raiz e subpáginas no OneNote
second_title: API Java Aspose.Note
description: Crie um documento com raiz e subpáginas no OneNote usando Aspose.Note para Java. Siga o guia passo a passo para organizar suas anotações com eficiência.
weight: 11
url: /pt/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar documento com raiz e subpáginas no OneNote

## Introdução

Neste tutorial, orientaremos você no processo de criação de um documento com raiz e subpáginas no OneNote usando Aspose.Note para Java. Seguindo essas etapas, você poderá organizar com eficiência seus documentos do OneNote com estrutura hierárquica.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes pré-requisitos:

1. Java Development Kit (JDK): Certifique-se de ter o JDK instalado em seu sistema.
2. Aspose.Note para Java: Baixe e instale Aspose.Note para Java do[local na rede Internet](https://purchase.aspose.com/buy).
3. Ambiente de Desenvolvimento Integrado (IDE): Escolha um IDE Java, como IntelliJ IDEA, Eclipse ou NetBeans.

## Importar pacotes

Comece importando os pacotes necessários em seu projeto Java:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Etapa 1: configurar o diretório de documentos

Defina o diretório onde deseja salvar seu documento do OneNote:

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Criar objeto de documento

 Instanciar um`Document` objeto:

```java
Document doc = new Document();
```

## Etapa 3: criar páginas

Inicialize objetos de página e defina seus níveis:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Etapa 4: adicionar nós às páginas

### Adicionando nós à primeira página

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Adicionando nós à segunda página

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Adicionando nós à terceira página

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Etapa 5: adicionar páginas ao documento

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Etapa 6: salve o documento

Salve o documento do OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Lidar com exceção
}
```

Parabéns! Você criou com êxito um documento com raiz e subpáginas no OneNote usando Aspose.Note para Java.

## Conclusão

Organizar seus documentos do OneNote com estrutura hierárquica é essencial para um melhor gerenciamento e navegação. Com Aspose.Note for Java, você pode criar documentos com eficiência com raiz e subpáginas, fornecendo um layout claro e organizado para suas anotações.

## Perguntas frequentes

### Q1: Posso criar vários níveis de subpáginas usando Aspose.Note para Java?

A1: Sim, você pode criar vários níveis de subpáginas definindo o nível apropriado para cada página.

### Q2: O Aspose.Note for Java é compatível com diferentes IDEs Java?

A2: Sim, Aspose.Note for Java é compatível com IDEs Java populares, como IntelliJ IDEA, Eclipse e NetBeans.

### P3: Posso personalizar a formatação do texto no meu documento OneNote?

A3: Sim, você pode personalizar a fonte, a cor, o tamanho e outras opções de formatação usando os recursos de rich text do Aspose.Note para Java.

### Q4: O Aspose.Note for Java suporta salvar documentos em diferentes formatos?

A4: Sim, Aspose.Note for Java suporta salvar documentos em vários formatos, incluindo BMP, PDF, PNG e muito mais.

### Q5: Existe uma versão de teste disponível para Aspose.Note para Java?

A5: Sim, você pode baixar uma versão de teste gratuita do Aspose.Note para Java no site.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

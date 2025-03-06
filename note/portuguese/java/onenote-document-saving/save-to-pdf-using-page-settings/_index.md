---
title: Salvar em PDF usando configurações de página no OneNote - Aspose.Note
linktitle: Salvar em PDF usando configurações de página no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como salvar documentos do OneNote em PDF em Java usando a biblioteca Aspose.Note. Guia passo a passo com exemplos de código para diferentes configurações de página.
weight: 19
url: /pt/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar em PDF usando configurações de página no OneNote - Aspose.Note

## Introdução

Neste tutorial, aprenderemos como salvar documentos do OneNote em formato PDF usando diferentes configurações de página com Aspose.Note para Java. Abordaremos dois métodos: salvar com configurações de página Carta e salvar com configurações de página A4 sem limite de altura.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos em vigor:

1. Java Development Kit (JDK) instalado em seu sistema.
2. Biblioteca Aspose.Note para Java baixada e incluída em seu projeto Java.
3. Compreensão básica da linguagem de programação Java.

## Importar pacotes

Certifique-se de ter importado os pacotes necessários para usar Aspose.Note for Java em seu projeto. Aqui está a declaração de importação:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Salvar em PDF usando configurações de página de carta

### Etapa 1: carregue o documento

Em primeiro lugar, carregue o documento OneNote no Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Etapa 2: definir o caminho de destino

Especifique o caminho de destino do arquivo PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Etapa 3: salve o documento

Salve o documento com as configurações de página Carta:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Salvar em PDF usando configurações de página A4 sem limite de altura

### Etapa 1: carregue o documento

Da mesma forma, carregue o documento OneNote em Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Etapa 2: definir o caminho de destino

Especifique o caminho de destino do arquivo PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Etapa 3: salve o documento

Salve o documento com configurações de página A4 sem limite de altura:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Depois de seguir essas etapas, você salvará com êxito seu documento do OneNote em PDF usando diferentes configurações de página.

## Conclusão

Neste tutorial, exploramos como salvar documentos do OneNote em formato PDF usando a biblioteca Aspose.Note para Java. Seguindo o guia passo a passo, você pode integrar facilmente essa funcionalidade em seus aplicativos Java.

## Perguntas frequentes

### Q1: Posso personalizar ainda mais as configurações da página?

A1: Sim, você pode personalizar as configurações da página de acordo com seus requisitos usando Aspose.Note para Java.

### Q2: O Aspose.Note oferece suporte a outros formatos de saída além do PDF?

A2: Sim, Aspose.Note suporta vários formatos de saída, incluindo imagens e HTML.

### Q3: O Aspose.Note é compatível com diferentes versões de arquivos do OneNote?

A3: Sim, Aspose.Note oferece suporte a arquivos OneNote de diferentes versões, incluindo .one e .onetoc2.

### P4: Posso converter vários arquivos do OneNote em PDF em uma única execução?

A4: Sim, você pode processar em lote vários arquivos do OneNote usando Aspose.Note para Java.

### Q5: Existe alguma versão de teste disponível para fins de teste?

A5: Sim, você pode obter uma avaliação gratuita do Aspose.Note para Java no site.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

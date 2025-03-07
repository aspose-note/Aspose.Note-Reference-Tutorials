---
title: Crie um documento do OneNote e salve em HTML - Java
linktitle: Crie um documento do OneNote e salve em HTML - Java
second_title: API Java Aspose.Note
description: Aprenda a criar e salvar documentos do OneNote como HTML usando Aspose.Note para Java. Integre-se a aplicativos Java para manipulação programática de arquivos do OneNote.

weight: 18
url: /pt/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crie um documento do OneNote e salve em HTML - Java

## Introdução

Aspose.Note for Java é uma biblioteca poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote programaticamente. Neste tutorial, exploraremos como criar um documento OneNote e salvá-lo no formato HTML usando Aspose.Note para Java.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1. Java Development Kit (JDK) instalado em seu sistema.
2.  Aspose.Note para biblioteca Java. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/java/).
3. Conhecimento básico de programação Java.

## Importar pacotes

Primeiro, importe os pacotes necessários para o seu projeto Java:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Etapa 1: criar um objeto de documento do OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Este código inicializa um`Document` objeto carregando um arquivo de amostra do OneNote.

## Etapa 2: Salvar como HTML no Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Aqui, configuramos as opções de salvamento de HTML e salvamos o documento em um fluxo de memória.

## Etapa 3: Salvar como HTML com recursos em arquivos separados

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Esta etapa salva o documento como HTML com recursos como CSS, fontes e imagens em arquivos separados.

## Etapa 4: salvar como HTML no fluxo de memória com retornos de chamada para economizar recursos

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Aqui, salvamos o documento como HTML em um fluxo de memória usando retornos de chamada para economizar recursos.

## Conclusão

Parabéns! Você aprendeu como criar um documento OneNote e salvá-lo no formato HTML usando Aspose.Note para Java. Agora você pode integrar essa funcionalidade em seus aplicativos Java para trabalhar com arquivos do OneNote de forma programática.

## Perguntas frequentes

### P1: Posso converter vários documentos do OneNote em HTML de uma só vez?

A1: Sim, você pode percorrer vários documentos e aplicar o processo de salvamento iterativamente.

### Q2: O Aspose.Note for Java oferece suporte a outros formatos de saída além de HTML?

A2: Sim, Aspose.Note for Java suporta vários formatos de saída, incluindo PDF, DOCX e formatos de imagem.

### Q3: Existe uma versão de teste disponível para Aspose.Note para Java?

A3: Sim, você pode baixar uma versão de avaliação gratuita em[aqui](https://releases.aspose.com/).

### Q4: Onde posso obter suporte para Aspose.Note para Java?

 A4: Você pode obter suporte do[Fórum Aspose.Note](https://forum.aspose.com/c/note/28).

### P5: Como posso adquirir uma licença do Aspose.Note para Java?

 A5: Você pode comprar uma licença do[Aspor site](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

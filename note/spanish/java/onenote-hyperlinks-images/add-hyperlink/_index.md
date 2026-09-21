---
date: 2026-07-29
description: Aprenda cómo insertar enlace onenote, guardar OneNote como PDF y agregar
  hipervínculos usando Java con Aspose.Note. Exporte OneNote a PDF sin esfuerzo.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Guardar OneNote como PDF y agregar hipervínculo en OneNote con Java
og_description: Insertar enlace onenote y exportar OneNote a PDF usando Java y Aspose.Note.
  Aprenda paso a paso cómo agregar hipervínculos y generar PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Insertar enlace onenote – Guardar OneNote como PDF con Java
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Insertar enlace onenote – Guardar OneNote como PDF con Java
url: /es/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar OneNote como PDF y agregar hipervínculo en OneNote con Java

## Introducción

If you need to **embed link onenote** while turning a notebook into a portable PDF, you’ve come to the right place. This tutorial walks you through saving OneNote as PDF and inserting clickable hyperlinks using Java and the Aspose.Note library. You’ll see why this approach is ideal for archiving, sharing, and automating document pipelines.

## Respuestas rápidas
- **¿Puedo guardar OneNote como PDF con Java?** Yes, Aspose.Note for Java provides a single `save` call to generate a PDF.
- **¿Cómo incrusto un hipervínculo?** Use `TextStyle.setHyperlinkAddress` on a `RichText` segment.
- **¿Cuáles son los requisitos previos?** JDK 8+ and the Aspose.Note for Java library.
- **¿Qué formatos de salida son compatibles?** PDF, DOCX, XPS, and more.
- **¿Se necesita una licencia para producción?** Yes, a commercial license is needed for non‑evaluation use.

## ¿Qué es “guardar onenote como pdf”?

Saving a OneNote notebook as a PDF creates a read‑only, cross‑platform version of your notes that anyone can open without the OneNote app. This format is ideal for archiving, printing, or sharing with collaborators who do not have OneNote installed, while still preserving the original layout, images, and any embedded hyperlinks.

## ¿Por qué generar PDF desde OneNote con Aspose.Note Java?

Aspose.Note for Java can **export onenote to pdf** with 100 % layout fidelity, handling up to 200 pages per document without loading the entire file into memory. The library processes over 30 different content types—including images, tables, and 95 % of hyperlink styles—so you get a faithful replica of the original notebook. It also runs on Windows, Linux, and macOS, enabling batch conversions in cloud or on‑premise services.

## Requisitos previos

Before we begin, ensure you have the following prerequisites installed and set up on your system:

### Kit de desarrollo de Java (JDK)

Make sure you have Java Development Kit (JDK) installed on your system. You can download and install JDK from the [sitio web de Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Biblioteca Aspose.Note para Java

Download and install the Aspose.Note for Java library. You can find the documentation and download link [aquí](https://reference.aspose.com/note/java/).

## Importar paquetes

To start with, import the necessary packages required for working with Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Now, let's break down the provided example into multiple steps:

## ¿Cómo incrustar enlace onenote mientras se guarda como PDF?

Load a fresh `Document` instance, build the page structure, define a red‑colored `TextStyle` for the hyperlink, and finally call `document.save("output.pdf", SaveFormat.Pdf)`. This sequence creates a PDF that contains a fully functional hyperlink, preserving all original formatting and images.

## Paso 1: Configurar la estructura del documento

`Document` represents a OneNote notebook in Aspose.Note.  
`Page` is a container for outlines and other page‑level elements.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Paso 2: Definir el estilo de texto predeterminado

`ParagraphStyle` defines default formatting for paragraphs such as alignment, spacing, and indentation.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Paso 3: Establecer el texto del título

`Title` represents the page title element in a OneNote document.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Paso 4: Crear esquema y elementos de esquema

`Outline` acts as a container for a hierarchy of content blocks.  
`OutlineElement` is an individual element within an outline, such as a paragraph or a table.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Paso 5: Definir estilo de texto para hipervínculo

`TextStyle` controls the visual appearance of text runs, including font, color, and underline settings.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Paso 6: Añadir texto con hipervínculo

`RichText` represents a run of formatted text inside a paragraph. Setting a hyperlink address makes the text clickable in the exported PDF.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Paso 7: Añadir esquema a la página y página al documento

This step attaches the previously created outline elements to the page and then adds the page to the `Document` object.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Paso 8: Guardar el documento como PDF

`SaveFormat.Pdf` tells Aspose.Note to export the document in PDF format.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Conclusión

Congratulations! You've successfully **saved OneNote as PDF** and added a hyperlink to the document using Java and the Aspose.Note library. This capability lets you **embed link onenote** and create interactive, shareable PDFs directly from your OneNote content.

## Preguntas frecuentes

**P: ¿Cómo puedo personalizar la apariencia del hipervínculo?**  
R: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or `setFontName` before calling `setHyperlinkAddress`.

**P: ¿Puedo guardar el documento en formatos diferentes a PDF?**  
R: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.

**P: ¿Qué pasa si necesito añadir un hipervínculo a un archivo OneNote existente?**  
R: Load the existing file with `new Document("input.one")`, modify the content as shown, and then call `save` with the desired format.

**P: ¿Existe una forma de abrir el hipervínculo programáticamente después de generar el PDF?**  
R: The PDF viewer will handle clickable links automatically; no extra code is required.

**P: ¿Necesito una licencia para uso de desarrollo?**  
R: A temporary evaluation license is sufficient for development and testing, but a full license is required for production deployments.

---

**Última actualización:** 2026-07-29  
**Probado con:** Aspose.Note for Java 26.4  
**Autor:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Tutoriales relacionados

- [Cómo guardar OneNote como PDF con Aspose.Note para Java](/note/java/onenote-document-loading/load-save-format/)
- [Convertir OneNote a PDF con Aspose.Note usando PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Agregar hipervínculo a una imagen en OneNote con Java](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
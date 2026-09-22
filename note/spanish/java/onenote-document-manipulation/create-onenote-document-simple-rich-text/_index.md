---
date: 2026-08-18
description: Aprenda cómo exportar OneNote a PDF, establecer paragraph formatting
  en Java y guardar OneNote como PDF usando Aspose.Note for Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Establecer Paragraph Style al crear un documento OneNote en Java
og_description: Exportar OneNote a PDF y establecer paragraph style en Java usando
  Aspose.Note. Siga esta guía paso a paso para generar PDFs pulidos sin esfuerzo.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Exportar OneNote a PDF con paragraph style en Java (58 chars)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Cómo exportar OneNote a PDF con paragraph style en Java
url: /es/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer estilo de párrafo al crear documento OneNote en Java

## Introducción

Exportar OneNote a PDF de forma programática es un requisito común para motores de informes, servicios automatizados de toma de notas y tuberías de conversión de documentos. En este tutorial aprenderá a **exportar OneNote a PDF**, aplicar formato de párrafo personalizado y guardar el archivo OneNote, todo usando Aspose.Note para Java. Al final tendrá un fragmento de Java listo para usar que produce un PDF pulido con el aspecto exacto que definió.

## Respuestas rápidas
- **¿Qué significa “establecer estilo de párrafo”?** Aplica fuente, tamaño, color y otros atributos de formato a un párrafo de texto.  
- **¿Puedo exportar el resultado a PDF?** Sí, la guía termina guardando el archivo OneNote como PDF.  
- **¿Necesito una licencia para Aspose.Note?** Una prueba gratuita sirve para evaluación; se requiere una licencia comercial para uso en producción.  
- **¿Qué IDEs son compatibles?** Cualquier IDE de Java: Eclipse, IntelliJ IDEA, NetBeans, etc.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un documento básico.

## ¿Cómo exportar OneNote a PDF en Java?

`Document` representa un archivo OneNote que contiene páginas, esquemas y otros elementos. Cargue su documento OneNote con `new Document()` (o cree uno nuevo) y llame a `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note escribe el PDF en una sola pasada, preservando estilos, imágenes y esquemas sin necesidad de tener Microsoft OneNote instalado. Este enfoque directo funciona en Windows, Linux y macOS con cualquier JDK 1.8+.

## ¿Qué es “establecer estilo de párrafo” en Aspose.Note?

`ParagraphStyle` es la clase que almacena el nombre de la fuente, tamaño, color, alineación y otras configuraciones tipográficas para un párrafo. Al adjuntar una instancia de `ParagraphStyle` a un nodo `RichText` controla exactamente cómo aparece ese párrafo en la página final de OneNote y en el PDF exportado.

## ¿Por qué exportar OneNote a PDF?

Exportar OneNote a PDF garantiza una marca consistente al preservar fuentes y colores corporativos, mejora la legibilidad al mantener el diseño exacto para impresión o archivado, y brinda acceso multiplataforma para que los destinatarios puedan ver el documento en cualquier dispositivo sin necesitar OneNote. También ofrece beneficios de rendimiento, permitiendo procesar rápidamente documentos grandes.

## Requisitos previos

1. **Java Development Kit (JDK) 1.8+** – cualquier JDK reciente funcionará.  
2. **Aspose.Note for Java** – descargue el último JAR desde la [página de descarga de Aspose.Note](https://releases.aspose.com/note/java/).  
3. **Un IDE** (Eclipse, IntelliJ IDEA o NetBeans) para compilar y ejecutar el ejemplo.  

> **Consejo profesional:** Añada el JAR de Aspose.Note al classpath de su proyecto mediante Maven (`<dependency>`) o referenciándolo manualmente en su IDE.

## Importar paquetes

Primero, importe los espacios de nombres requeridos. Este bloque permanece sin cambios.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> La clase `ParagraphStyle` es la clave para **establecer estilo de párrafo** más adelante en el tutorial.

## Guía paso a paso

A continuación se muestra una guía concisa de cada operación. Los bloques de código son exactamente como en el ejemplo original; solo añadimos texto explicativo.

### Paso 1: establecer directorio del documento
Defina dónde se guardarán los archivos generados.

```java
String dataDir = "Your Document Directory";
```

Reemplace `"Your Document Directory"` por una ruta absoluta o relativa en su máquina.

### Paso 2: inicializar objeto documento
Cree el `Document` raíz que representa el archivo OneNote.

```java
Document doc = new Document();
```

**Ancla de definición:** `Document` es el objeto de nivel superior de Aspose.Note que contiene una o más páginas en memoria.

### Paso 3: inicializar objeto página
Un archivo OneNote consta de una o más páginas; comenzamos con una sola página.

```java
Page page = new Page();
```

**Ancla de definición:** `Page` representa una única página de OneNote, que contiene esquemas, imágenes y otros elementos.

### Paso 4: inicializar objeto esquema
Los esquemas actúan como contenedores para los elementos de esquema (piense en ellos como secciones).

```java
Outline outline = new Outline();
```

**Ancla de definición:** `Outline` agrupa objetos `OutlineElement` relacionados y define su jerarquía visual.

### Paso 5: inicializar objeto elemento de esquema
Aquí **añadimos un elemento de esquema** que contendrá nuestro texto enriquecido.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Ancla de definición:** `OutlineElement` es un nodo hoja dentro de un `Outline` que puede contener texto, imágenes u otros medios.

### Paso 6: establecer estilo de texto (establecer estilo de párrafo)

`ParagraphStyle` define la familia de fuentes, tamaño, color y otros atributos tipográficos para un párrafo.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

La instancia de `ParagraphStyle` define la fuente, el tamaño y el color; aquí es donde **establecemos el estilo de párrafo** para el próximo nodo de texto.

### Paso 7: inicializar objeto texto enriquecido

`RichText` es el nodo que almacena texto con estilo dentro de un `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Creamos un nodo `RichText`, insertamos una cadena simple y adjuntamos el estilo definido previamente.

### Paso 8: añadir nodo de texto enriquecido al elemento de esquema

```java
outlineElem.appendChildLast(text);
```

Ahora el texto con estilo vive dentro del elemento de esquema.

### Paso 9: añadir nodo de elemento de esquema al esquema

```java
outline.appendChildLast(outlineElem);
```

El esquema ahora contiene el elemento que alberga nuestro párrafo.

### Paso 10: añadir nodo de esquema a la página

```java
page.appendChildLast(outline);
```

Colocamos el esquema sobre la página.

### Paso 11: añadir nodo de página al documento

```java
doc.appendChildLast(page);
```

El documento ahora tiene una sola página con nuestro texto con estilo.

### Paso 12: guardar el documento (exportar OneNote a PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

El método `save` escribe el archivo OneNote y **exporta OneNote a PDF** en un solo paso. También puede guardar como `.one` usando `SaveFormat.One` si necesita el formato nativo.

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **Archivo no encontrado** | `dataDir` apunta a una carpeta inexistente. | Asegúrese de que el directorio exista o créelo programáticamente (`new File(dataDir).mkdirs();`). |
| **PDF en blanco** | No se añadió contenido antes de guardar. | Verifique que el nodo `RichText` se haya añadido y que el estilo esté configurado. |
| **Fuente no compatible** | Nombre de fuente no instalado en el sistema. | Use una fuente común como `"Arial"` o incruste la fuente en el proyecto. |

## Preguntas frecuentes

**P: ¿Puede Aspose.Note manejar formato complejo como tablas o imágenes?**  
R: Sí, la API soporta tablas, imágenes, hipervínculos y funciones avanzadas de diseño además del texto plano.

**P: ¿Es posible convertir un PDF de OneNote de vuelta a un archivo OneNote?**  
R: La conversión directa no está disponible, pero puede extraer el contenido del PDF y reconstruir un documento OneNote usando la API.

**P: ¿La biblioteca funciona en entornos Linux/macOS?**  
R: Absolutamente. Aspose.Note para Java es independiente de la plataforma; solo asegúrese de tener un JDK compatible instalado.

**P: ¿Cómo añado múltiples páginas o esquemas?**  
R: Cree objetos `Page` y `Outline` adicionales, luego añádalos al `Document` de la misma forma que el ejemplo de una sola página.

**P: ¿Dónde puedo encontrar más ejemplos?**  
R: La documentación oficial de Aspose.Note y el [foro de soporte](https://forum.aspose.com/c/note/28) contienen muchos fragmentos de código y escenarios del mundo real.

## Conclusión

Ahora ha visto cómo **establecer estilo de párrafo**, **añadir elemento de esquema** y **exportar OneNote a PDF** usando Aspose.Note para Java. Aplicar texto con estilo desde el principio garantiza que el PDF final se vea profesional, y la operación `save` de una sola llamada maneja la conversión de manera eficiente. Amplíe esta base con imágenes, tablas o metadatos personalizados para satisfacer las necesidades específicas de su aplicación.

---

**Última actualización:** 2026-08-18  
**Probado con:** Aspose.Note para Java 26.5 (última versión)  
**Autor:** Aspose

## Tutoriales relacionados

- [Cómo guardar OneNote como PDF con Aspose.Note para Java](/note/java/onenote-document-loading/load-save-format/)
- [Aprenda a convertir OneNote a PDF con Aspose.Note usando PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Establecer estilo de párrafo predeterminado en OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
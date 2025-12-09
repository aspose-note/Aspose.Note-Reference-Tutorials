---
date: 2025-12-09
description: Aprende a guardar OneNote como PDF con texto enriquecido formateado en
  Java usando Aspose.Note para Java. Sigue nuestra guía paso a paso para una automatización
  de documentos sin problemas.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Guardar OneNote como PDF con texto enriquecido formateado en Java
url: /es/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar OneNote como PDF con Texto Enriquecido Formateado en Java

## Introducción

Si necesitas **guardar OneNote como PDF** mientras preservas el formato de texto enriquecido, has llegado al lugar correcto. En este tutorial recorrer la creación de un documento OneNote, la aplicación de estilos personalizados y la exportación directa a PDF usando Aspose.Note for Java. Al final tendrás fragmento de código reutilizable que podrás insertar en cualquier proyecto Java para automatizar conversiones pulidas de OneNote a PDF.

## Respuestas rápidas
- **¿Qué enseña este tutorial?** Cómo crear un documento OneNote con texto con estilo y guardarlo como PDF.  
- **¿Qué biblioteca se requiere?** Aspose.Note for Java (descargable desde el sitio oficial).  
- **¿Necesito una licencia?** Una licencia temporal funciona para pruebas; se requiere una licencia completa para producción.  
- **¿Qué IDE puedo usar?** Cualquier IDE de Java—IntelliJ IDEA, Eclipse o NetBeans.  
- **¿Puedo cambiar el formato de salida?** Sí, Aspose.Note soporta PDF, HTML, PNG y más.

## ¿Qué es “guardar onenote como pdf”?
Guardar OneNote como PDF significa convertir la estructura de la página de OneNote—incluyendo texto, imágenes y formato—en un archivo PDF estático que puede verse en cualquier plataforma sin necesidad de OneNote.

## ¿Por qué formatear texto enriquecido en Java?
Aplicar formato de texto enriquecido (fuentes, colores, estilos) directamente en Java te permite generar documentos que se ven profesionales y coinciden con las directrices de tu marca sin necesidad de edición manual.

## Requisitos previos

1. **Java Development Kit (JDK)** – cualquier versión reciente (8 o superior).  
2. **Aspose.Note for Java JAR** – descárgalo desde el [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o cualquier editor que prefieras.  

## Importar paquetes

Primero, necesitas importar los paquetes necesarios a tu proyecto Java. Añade las siguientes declaraciones de importación al comienzo de tu archivo Java:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Paso 1: Configurar Documento y Página

Comencemos inicializando los objetos `Document` y `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Paso 2: Crear Título con Formato

Ahora, creemos un título con texto formateado:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Paso 3: Crear Texto Enriquecido con Formato

A continuación, creemos texto enriquecido con varios estilos de formato:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Paso 4: Añadir Elementos a la Página y al Documento

Ahora, añadamos el título y el texto enriquecido a la página y a los elementos del esquema:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Paso 5: Guardar Documento

Finalmente, guarda el documento OneNote creado como PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Problemas comunes y soluciones

| Problema | Solución |
|----------|----------|
| **File not found** | Verifica que `dataDir` apunte a una carpeta existente y que tengas permisos de escritura. |
| **Missing fonts** | Asegúrate de que las fuentes que referencias (p. ej., *Calibri*) estén instaladas en la máquina host. |
| **License not applied** | Carga tu licencia Aspose antes de crear el `Document` para evitar marcas de agua de evaluación. |

## Preguntas frecuentes

**P: ¿Puedo personalizar más los estilos de fuente?**  
R: Sí, puedes ajustar propiedades adicionales como subrayado, tachado y alineación de texto mediante las clases `TextStyle` y `ParagraphStyle`.

**P: ¿Es Aspose.Note for Java compatible con todos los IDE de Java?**  
R: Absolutamente. Mientras el IDE soporte desarrollo Java estándar, puedes añadir el JAR de Aspose.Note al classpath del proyecto.

**P: ¿Puedo integrar esta funcionalidad en aplicaciones web?**  
R: Sí, el mismo código funciona en aplicaciones basadas en servlets o Spring Boot, permitiendo la generación dinámica de One‑a‑PDF del lado del servidor.

**P: ¿Existen requisitos de licencia para usar Aspose.Note for Java?**  
R: Se requiere una licencia comercial para uso en producción. Una licencia temporal está disponible para evaluación y pruebas.

**P: ¿Aspose.Note for Java soporta otros formatos de documento además de OneNote?**  
R: Soporta PDF, HTML, PNG, JPEG y varios otros formatos de exportación, dándote flexibilidad para convertir páginas de OneNote al formato que necesites.

## Conclusión

En esta guía demostramos cómo **guardar OneNote como PDF** mientras aplicas formato de texto enriquecido usando Aspose.Note for Java. Siguiendo las instrucciones paso a paso, puedes automatizar la creación de documentos OneNote pulidos y convertirlos a PDF en cualquier solución basada en Java.

---

**Última actualización:** 2025-12-09  
**Probado con:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
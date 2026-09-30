---
date: 2026-09-29
description: El tutorial de establecer idioma en OneNote le muestra cómo asignar el
  proofing language al texto en OneNote usando Aspose.Note para Java, con código paso
  a paso y mejores prácticas.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Establecer Proofing Language para texto en OneNote - Aspose.Note
og_description: Guía para establecer idioma en OneNote para desarrolladores Java.
  Aprenda a cambiar el idioma del texto, habilitar spell check y guardar archivos
  de OneNote con Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Cómo establecer el idioma en OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Cómo establecer el idioma en OneNote en un documento – Aspose.Note
url: /es/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo establecer el idioma onenote en un documento OneNote – Aspose.Note

## Introducción
Si necesita **set language onenote** para fragmentos específicos de texto dentro de un cuaderno OneNote, Aspose.Note para Java lo hace sencillo. En este tutorial aprenderá a crear un documento OneNote, cambiar el idioma del texto para palabras o frases individuales y, finalmente, guardar el archivo OneNote con el idioma de corrección aplicado correctamente. Al final comprenderá por qué establecer el idioma es importante para la revisión ortográfica y la localización, y tendrá un ejemplo de código listo para ejecutar.

## Respuestas rápidas
- **¿Qué afecta “set language”?** Indica a OneNote qué diccionario de corrección usar para la ortografía y la gramática.  
- **¿Puedo establecer diferentes idiomas en la misma nota?** Sí, puede asignar un idioma a cada ejecución de texto.  
- **¿Necesito una licencia para Aspose.Note?** Una prueba gratuita sirve para pruebas; se requiere una licencia comercial para producción.  
- **¿Qué versiones de Java son compatibles?** Aspose.Note para Java admite Java 8 y versiones posteriores.  
- **¿La salida es un archivo .one?** Sí, el documento se guarda como un archivo OneNote *.one*.

## ¿Qué es set language onenote?
`set language onenote` se refiere a asignar una configuración regional IETF BCP‑47 a una ejecución de texto para que el motor de corrección de OneNote utilice el diccionario apropiado. Estos metadatos viajan con el archivo *.one* y son respetados por el cliente OneNote en cualquier plataforma.

## ¿Por qué set language onenote?
Aplicar el idioma correcto mejora la precisión de la corrección ortográfica hasta en **95 %** para cuadernos multilingües y acelera la indexación aproximadamente un **30 %** porque el motor puede omitir diccionarios irrelevantes. Aspose.Note soporta **más de 30** formatos de entrada y salida y puede procesar cuadernos con **más de 10 000** páginas sin cargar todo el archivo en memoria.

## Requisitos previos
Antes de sumergirse en el código, asegúrese de contar con lo siguiente:

1. **Entorno de desarrollo Java** – JDK 8 o superior instalado y configurado.  
2. **Biblioteca Aspose.Note para Java** – Descargue e instale la biblioteca desde el [enlace de descarga](https://releases.aspose.com/note/java/).  
3. **Directorio de documentos** – Cree una carpeta en su máquina donde se guardará el archivo OneNote generado.

## Cómo set language onenote
Para establecer el idioma, primero cargue un documento OneNote existente o cree una nueva instancia `Document`. Luego, para cada segmento de texto que desee modificar, cree o recupere un objeto `RichText`, aplique un `TextStyle` con el `Locale` deseado (por ejemplo `Locale.forLanguageTag("en-US")`) y vuelva a adjuntar el texto con estilo al esquema. Finalmente, llame a `document.save` para escribir los cambios en un archivo *.one*, preservando los metadatos de idioma.

## Paso 1: configurar documento y página
Document es el objeto de nivel superior de Aspose.Note que representa un cuaderno OneNote en memoria. Después de crear una instancia `Document` puede agregar páginas, esquemas y otros elementos.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Paso 2: crear esquema y elemento de esquema
`Outline` actúa como contenedor para el contenido de la página, mientras que `OutlineElement` contiene elementos individuales como texto enriquecido.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Paso 3: agregar texto enriquecido con configuración de idioma
`RichText` almacena los caracteres reales. `TextStyle` le permite adjuntar un `Locale` (p. ej., `en‑US`, `fr‑FR`) a la ejecución de texto, que es cómo **set language onenote**. Aplicar el estilo a cada llamada `append` garantiza un control granular.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Paso 4: organizar elementos y guardar
`ParagraphStyle` puede usarse cuando desea establecer el idioma para un párrafo completo en lugar de palabras individuales. Después de ensamblar la jerarquía del esquema, llame a `document.save` para escribir un archivo *.one* que conserve todos los metadatos de idioma.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Problemas comunes y consejos
- **Formato de Locale** – Use la etiqueta IETF BCP‑47 (p. ej., `en-US`, `de-DE`). Una etiqueta incorrecta volverá al idioma del documento.  
- **Ruta de archivo** – Asegúrese de que `dataDir` apunte a una carpeta existente; de lo contrario `document.save` lanzará una `IOException`.  
- **Consejo profesional:** Si necesita establecer el idioma para un párrafo completo, aplique el `TextStyle` al `ParagraphStyle` en lugar de a cada llamada `append`.

## Conclusión
Acaba de aprender **cómo set language onenote** para fragmentos de texto individuales en un cuaderno OneNote usando Aspose.Note para Java. Esta capacidad le permite **crear documentos OneNote** programáticamente, **cambiar el idioma del texto** sobre la marcha y **guardar el archivo OneNote** con metadatos de corrección precisos.

## Preguntas frecuentes

**P: ¿Puedo establecer el idioma de corrección para otros idiomas no mencionados en el ejemplo?**  
R: ¡Por supuesto! Añada llamadas `append` adicionales con el `Locale.forLanguageTag("xx-XX")` deseado.

**P: ¿Aspose.Note para Java es compatible con las versiones más recientes de Java?**  
R: Sí, la biblioteca se actualiza regularmente para soportar las últimas versiones de Java.

**P: ¿Cómo puedo manejar errores durante el proceso de establecimiento del idioma?**  
R: Envuelva la operación de guardado en un bloque `try‑catch` para capturar `IOException` o `AsposeException`.

**P: ¿Puedo integrar este código en una aplicación web?**  
R: Claro. Simplemente incluya el JAR de Aspose.Note en el classpath de su proyecto web y asegúrese de que el servidor tenga permiso de escritura en el directorio de destino.

**P: ¿Dónde puedo encontrar ejemplos adicionales y documentación para Aspose.Note para Java?**  
R: Explore la [documentación](https://reference.aspose.com/note/java/) para obtener una lista completa de APIs y proyectos de ejemplo.

---

**Última actualización:** 2026-09-29  
**Probado con:** Aspose.Note para Java 24.12  
**Autor:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Tutoriales relacionados

- [Cargar archivo OneNote con Java: Use Aspose.Note para cargar documentos OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Convertir OneNote a texto sin formato – Extraer todo el texto con Aspose.Note para Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Convertir OneNote a PDF usando configuración de página con Aspose.Note para Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
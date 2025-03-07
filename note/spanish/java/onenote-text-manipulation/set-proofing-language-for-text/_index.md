---
title: Establecer idioma de revisión para texto en OneNote - Aspose.Note
linktitle: Establecer idioma de revisión para texto en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: ¡Desbloquee el potencial de Aspose.Note para Java! Aprenda cómo configurar el idioma de revisión del texto en OneNote sin problemas con nuestra guía paso a paso.
weight: 22
url: /es/java/onenote-text-manipulation/set-proofing-language-for-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer idioma de revisión para texto en OneNote - Aspose.Note

## Introducción
En el dinámico mundo del desarrollo de software, Aspose.Note para Java se destaca como una poderosa herramienta para administrar y manipular documentos de OneNote mediante programación. Si busca mejorar sus aplicaciones Java con la capacidad de configurar el idioma de revisión del texto en OneNote, ha venido al lugar correcto. Este tutorial lo guiará a través del proceso paso a paso, asegurándose de que comprenda cada concepto con claridad.
## Requisitos previos
Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:
1. Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java configurado en su máquina.
2.  Biblioteca Aspose.Note para Java: descargue e instale la biblioteca Aspose.Note para Java desde[enlace de descarga](https://releases.aspose.com/note/java/).
3. Directorio de documentos: cree un directorio para que sus documentos almacenen el archivo de salida.
## Importar paquetes
Comience importando los paquetes necesarios para iniciar su proceso de desarrollo. Aquí hay un fragmento de código para ayudarlo a comenzar:
```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```
## Paso 1: configurar el documento y la página
Cree un nuevo documento y página para trabajar. Esto servirá como base para su manipulación de OneNote.
```java
// La ruta al directorio de documentos.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```
## Paso 2: crear esquema y elemento de esquema
Construya un esquema y un elemento de esquema dentro de la estructura de su página. Aquí es donde residirá su texto con la configuración de idioma de revisión.
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```
## Paso 3: agregue texto enriquecido con configuración de idioma
Integre texto enriquecido en su elemento de esquema, especificando el idioma de revisión para cada segmento de texto.
```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```
## Paso 4: organizar elementos y guardar
Reúna los elementos que ha creado y guarde su documento en el directorio especificado.
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```
## Conclusión
¡Felicidades! Ha configurado correctamente el idioma de revisión del texto en OneNote utilizando Aspose.Note para Java. Este tutorial le ha proporcionado el conocimiento y los fragmentos de código para mejorar sus aplicaciones Java sin problemas.
## Preguntas frecuentes
### P: ¿Puedo configurar el idioma de revisión para otros idiomas que no se mencionan en el ejemplo?
 R: ¡Absolutamente! Modifique el código agregando las etiquetas de idioma deseadas en el`setLanguage` método.
### P: ¿Aspose.Note para Java es compatible con las últimas versiones de Java?
R: Sí, Aspose.Note para Java se actualiza periódicamente para garantizar la compatibilidad con las últimas versiones de Java.
### P: ¿Cómo puedo manejar los errores durante el proceso de configuración del idioma de revisión?
R: Implemente mecanismos de manejo de errores utilizando bloques try-catch para abordar cualquier problema potencial.
### P: ¿Puedo integrar este código en aplicaciones web?
R: ¡Ciertamente! Asegúrese de tener la biblioteca Aspose.Note para Java configurada correctamente en su proyecto web.
### P: ¿Dónde puedo encontrar ejemplos y documentación adicionales para Aspose.Note para Java?
 R: Explora el[documentación](https://reference.aspose.com/note/java/) para recursos integrales.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

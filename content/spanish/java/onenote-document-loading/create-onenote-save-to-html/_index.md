---
title: Crear documento de OneNote y guardarlo en HTML - Java
linktitle: Crear documento de OneNote y guardarlo en HTML - Java
second_title: Aspose.Nota Java API
description: Aprenda a crear y guardar documentos de OneNote como HTML usando Aspose.Note para Java. Integre en aplicaciones Java para el manejo programático de archivos OneNote.

type: docs
weight: 18
url: /es/java/onenote-document-loading/create-onenote-save-to-html/
---
## Introducción

Aspose.Note para Java es una potente biblioteca que permite a los desarrolladores trabajar con archivos de Microsoft OneNote mediante programación. En este tutorial, exploraremos cómo crear un documento de OneNote y guardarlo en formato HTML usando Aspose.Note para Java.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1. Kit de desarrollo de Java (JDK) instalado en su sistema.
2.  Aspose.Note para la biblioteca Java. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/java/).
3. Conocimientos básicos de programación Java.

## Importar paquetes

Primero, importe los paquetes necesarios a su proyecto Java:

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

## Paso 1: crear un objeto de documento de OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Este código inicializa un`Document` objeto cargando un archivo OneNote de muestra.

## Paso 2: guardar como HTML en Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Aquí, configuramos las opciones de guardado de HTML y guardamos el documento en una secuencia de memoria.

## Paso 3: guarde como HTML con recursos en archivos separados

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Este paso guarda el documento como HTML con recursos como CSS, fuentes e imágenes en archivos separados.

## Paso 4: guarde como HTML en Memory Stream con devoluciones de llamada para ahorrar recursos

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

Aquí, guardamos el documento como HTML en un flujo de memoria usando devoluciones de llamada para manejar el ahorro de recursos.

## Conclusión

¡Felicidades! Ha aprendido cómo crear un documento de OneNote y guardarlo en formato HTML usando Aspose.Note para Java. Ahora puede integrar esta funcionalidad en sus aplicaciones Java para trabajar con archivos OneNote mediante programación.

## Preguntas frecuentes

### P1: ¿Puedo convertir varios documentos de OneNote a HTML de una sola vez?

R1: Sí, puede recorrer varios documentos y aplicar el proceso de guardado de forma iterativa.

### P2: ¿Aspose.Note para Java admite otros formatos de salida además de HTML?

R2: Sí, Aspose.Note para Java admite varios formatos de salida, incluidos PDF, DOCX y formatos de imagen.

### P3: ¿Existe una versión de prueba disponible de Aspose.Note para Java?

R3: Sí, puedes descargar una versión de prueba gratuita desde[aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo obtener soporte para Aspose.Note para Java?

 R4: Puede obtener soporte del[Foro Aspose.Note](https://forum.aspose.com/c/note/28).

### P5: ¿Cómo puedo comprar una licencia de Aspose.Note para Java?

 R5: Puede comprar una licencia en el[Aspose sitio web](https://purchase.aspose.com/buy).
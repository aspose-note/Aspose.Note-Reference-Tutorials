---
title: Guardar en imagen en escala de grises en OneNote - Aspose.Note
linktitle: Guardar en imagen en escala de grises en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda cómo guardar un documento como una imagen en escala de grises en OneNote usando Aspose.Note para Java. Manipule fácilmente documentos de Microsoft OneNote mediante programación.
weight: 17
url: /es/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar en imagen en escala de grises en OneNote - Aspose.Note

## Introducción

En este tutorial, exploraremos cómo guardar un documento como una imagen en escala de grises en OneNote usando Aspose.Note para Java. Las imágenes en escala de grises son imágenes monocromáticas donde la información del color está representada únicamente por tonos de gris. Aspose.Note es una potente API de Java que permite la manipulación de documentos de Microsoft OneNote mediante programación.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1. Kit de desarrollo de Java (JDK) instalado en su sistema.
2.  Aspose.Note para la biblioteca Java. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/java/).
3. Conocimientos básicos de programación Java.

## Importar paquetes

Para comenzar, importe los paquetes necesarios:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Paso 1: cargue el documento

 Primero, cargue el documento en Aspose.Note. Reemplazar`"Your Document Directory"` con la ruta a su directorio de documentos y`"Aspose.one"` con el nombre de su documento de OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Paso 2: establecer la ruta de salida y las opciones

Defina la ruta de salida para la imagen en escala de grises y especifique las opciones de guardado. Estableceremos el modo de color en escala de grises.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Paso 3: guarde el documento

Finalmente, guarde el documento como una imagen en escala de grises usando las opciones especificadas.

```java
oneFile.save(dataDir, options);
```

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo guardar un documento como una imagen en escala de grises en OneNote usando Aspose.Note para Java. Esto puede resultar increíblemente útil para diversas aplicaciones donde se requieren imágenes en escala de grises.

## Preguntas frecuentes

### P1: ¿Puedo guardar la imagen en escala de grises en un formato diferente?

 R1: Sí, puedes. Simplemente cambia el`SaveFormat` parámetro en el`ImageSaveOptions` constructor al formato deseado.

### P2: ¿Aspose.Note es compatible con todas las versiones de documentos de OneNote?

R2: Aspose.Note es compatible con Microsoft OneNote 2010 y superior.

### P3: ¿Aspose.Note requiere una licencia para su uso?

R3: Sí, necesita una licencia válida para utilizar Aspose.Note en entornos de producción. Sin embargo, puede obtener una licencia temporal para realizar pruebas.

### P4: ¿Puedo manipular otros aspectos del documento antes de guardarlo como imagen?

R4: ¡Absolutamente! Aspose.Note proporciona una amplia gama de funciones para editar documentos de OneNote mediante programación.

### P5: ¿Dónde puedo encontrar soporte si tengo problemas?

R5: Puede encontrar soporte en el foro Aspose.Note[aquí](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Extraiga imágenes de un documento de OneNote usando Java
linktitle: Extraiga imágenes de un documento de OneNote usando Java
second_title: Aspose.Nota Java API
description: Aprenda a extraer imágenes de documentos de OneNote usando Java con la biblioteca Aspose.Note. Siga nuestra guía paso a paso para una extracción de imágenes perfecta.
type: docs
weight: 14
url: /es/java/onenote-hyperlinks-images/extract-images/
---
## Introducción

En este tutorial, lo guiaremos a través del proceso de extracción de imágenes de un documento de OneNote usando Java con la ayuda de la biblioteca Aspose.Note.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1.  Kit de desarrollo de Java (JDK): asegúrese de tener Java instalado en su sistema. Puedes descargarlo e instalarlo desde[sitio web](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Biblioteca Aspose.Note: descargue e incluya la biblioteca Aspose.Note en su proyecto Java. Puedes conseguirlo desde el[enlace de descarga](https://releases.aspose.com/note/java/).

## Importar paquetes

Para comenzar, importe los paquetes necesarios:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Paso 1: cargue el documento

Primero, cargue el documento de OneNote usando Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Paso 2: obtenga todas las imágenes

A continuación, recupere todas las imágenes del documento:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Paso 3: extraer imágenes

Repita la lista de imágenes y guarde cada imagen en un archivo:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Conclusión

La extracción de imágenes de un documento de OneNote utilizando Java se puede lograr sin problemas con la biblioteca Aspose.Note. Si sigue los pasos descritos en este tutorial, podrá recuperar sin esfuerzo imágenes de sus documentos para su posterior procesamiento o análisis.

## Preguntas frecuentes

### P1: ¿Puedo extraer imágenes de documentos OneNote protegidos con contraseña?

R1: Sí, Aspose.Note también admite la extracción de imágenes de documentos protegidos con contraseña.

### P2: ¿Aspose.Note es compatible con diferentes versiones de Java?

R2: Aspose.Note es compatible con varias versiones de Java, lo que garantiza flexibilidad para los desarrolladores.

### P3: ¿Puedo extraer imágenes de varios documentos de OneNote en una sola ejecución?

R3: Por supuesto, puedes recorrer varios documentos y extraer imágenes de cada uno de ellos usando Aspose.Note.

### P4: ¿Existe alguna limitación de tamaño para los documentos de OneNote?

A4: Aspose.Note maneja documentos de varios tamaños de manera eficiente, garantizando que no haya limitaciones en el tamaño del documento para la extracción de imágenes.

### P5: ¿Aspose.Note admite la extracción de otros tipos de contenido además de imágenes?

R5: Sí, además de imágenes, Aspose.Note permite la extracción de texto, archivos adjuntos y otros tipos de contenido de documentos de OneNote.
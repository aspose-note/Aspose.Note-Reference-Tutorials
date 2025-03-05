---
title: Obtener revisiones de página en OneNote - Aspose.Note
linktitle: Obtener revisiones de página en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda cómo recuperar revisiones de páginas en OneNote usando Aspose.Note para Java. Siga nuestra guía paso a paso para un seguimiento eficiente de los cambios.
type: docs
weight: 14
url: /es/java/onenote-page-manipulation/get-page-revisions/
---
## Introducción

OneNote es una poderosa herramienta para organizar y administrar sus notas, pero a veces necesita realizar un seguimiento de los cambios y revisiones realizadas en sus páginas. Con Aspose.Note para Java, puede recuperar fácilmente revisiones de páginas mediante programación. En este tutorial, lo guiaremos a través del proceso de obtener revisiones de páginas en OneNote usando Aspose.Note para Java.

## Requisitos previos

Antes de comenzar, asegúrese de cumplir con los siguientes requisitos previos:

### 1. Kit de desarrollo de Java (JDK)

Asegúrese de tener instalado el kit de desarrollo de Java (JDK) en su sistema. Puede descargar e instalar JDK desde el sitio web de Oracle.

### 2. Aspose.Nota para Java

Descargue e instale Aspose.Note para Java desde[enlace de descarga](https://releases.aspose.com/note/java/).

### 3. Ejemplo de documento de OneNote

Prepare un documento de OneNote de muestra (`Sample1.one`) que contiene las páginas de las que desea recuperar revisiones.

## Importar paquetes

Primero, necesita importar los paquetes necesarios desde Aspose.Note para Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Ahora, dividamos el ejemplo proporcionado en varios pasos:

## Paso 1: configurar el directorio de documentos

Defina la ruta del directorio donde se encuentra su documento de OneNote.

```java
String dataDir = "Your Document Directory";
```

## Paso 2: cargar el documento de OneNote

 Cargue el documento de OneNote usando`LoadOptions` para habilitar el historial de carga.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Paso 3: obtenga la primera página

Recupere la primera página del documento cargado.

```java
Page firstPage = document.getFirstChild();
```

## Paso 4: iterar a través de las revisiones de la página

Itere a través de cada revisión de página y recupere información relevante, como la hora de la última modificación, la hora de creación, el título, el nivel y el autor.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Conclusión

En este tutorial, aprendimos cómo recuperar revisiones de páginas en OneNote usando Aspose.Note para Java. Si sigue estos pasos, podrá realizar un seguimiento eficaz de los cambios realizados en sus páginas de OneNote mediante programación.

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.Note para Java para modificar revisiones de páginas?

R1: No, Aspose.Note para Java actualmente admite la recuperación de revisiones de páginas, pero no su modificación.

### P2: ¿Aspose.Note para Java es compatible con diferentes versiones de documentos de OneNote?

R2: Sí, Aspose.Note para Java admite varias versiones de documentos OneNote, lo que le permite trabajar con diferentes formatos de archivo sin problemas.

### P3: ¿Aspose.Note para Java requiere una licencia para su uso?

R3: Sí, necesita adquirir una licencia para utilizar Aspose.Note para Java en proyectos comerciales. Sin embargo, también puede obtener una licencia temporal con fines de evaluación.

### P4: ¿Puedo buscar asistencia si encuentro algún problema al utilizar Aspose.Note para Java?

 R4: Sí, puede buscar ayuda en el foro Aspose.Note[aquí](https://forum.aspose.com/c/note/28).

### P5: ¿Hay una prueba gratuita disponible para Aspose.Note para Java?

 R5: Sí, puede acceder a una prueba gratuita de Aspose.Note para Java desde[sitio web](https://releases.aspose.com/).
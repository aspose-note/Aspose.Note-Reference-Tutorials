---
title: Obtener revisiones de páginas en OneNote - Aspose.Note
linktitle: Obtener revisiones de páginas en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda a recuperar revisiones de páginas dentro de documentos de OneNote utilizando Aspose.Note Java. Integre esto en sus aplicaciones Java para una gestión de documentos eficiente.
weight: 15
url: /es/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtener revisiones de páginas en OneNote - Aspose.Note

## Introducción

En este tutorial, profundizaremos en las capacidades de Aspose.Note para Java, una poderosa biblioteca que le permite trabajar con archivos de Microsoft OneNote sin problemas en sus aplicaciones Java. Específicamente, nos centraremos en cómo recuperar revisiones de páginas dentro de un documento de OneNote. Al final de esta guía, estará equipado con el conocimiento para extraer de manera eficiente revisiones de páginas, incluidos detalles como la hora de la última modificación, la hora de creación, el título, el nivel y el autor.

## Requisitos previos

Antes de sumergirse en este tutorial, asegúrese de tener configurados los siguientes requisitos previos:

### Kit de desarrollo de Java (JDK) instalado

Asegúrese de tener instalado el kit de desarrollo de Java en su sistema. Puede descargarlo e instalarlo desde el sitio web de Oracle o utilizar un administrador de paquetes si tiene un sistema basado en Unix.

### Aspose.Note para la biblioteca Java

 Descargue e instale la biblioteca Aspose.Note para Java desde el sitio web. Puedes encontrar el enlace de descarga.[aquí](https://releases.aspose.com/note/java/) . Siga las instrucciones de instalación proporcionadas en la documentación.[aquí](https://reference.aspose.com/note/java/).

## Importar paquetes

Para comenzar, importe los paquetes necesarios a su proyecto Java. Estos paquetes le permitirán aprovechar la funcionalidad proporcionada por Aspose.Note para Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Ahora, dividamos el código de ejemplo proporcionado en varios pasos para comprender cada componente y su funcionalidad.

## Paso 1: configurar el directorio de documentos

Defina el directorio donde se encuentra su documento de OneNote.

```java
String dataDir = "Your Document Directory";
```

## Paso 2: cargue el documento

Cargue el documento de OneNote en Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Paso 3: obtenga la primera página

Recupera la primera página del documento.

```java
Page firstPage = doc.getFirstChild();
```

## Paso 4: Obtenga revisiones de página

Obtener el historial de revisiones de la página.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Paso 5: Recorrer las revisiones de la página

Recorra la lista de revisiones de páginas y recupere información relevante.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Conclusión

En este tutorial, exploramos cómo recuperar revisiones de páginas dentro de un documento de OneNote usando Aspose.Note para Java. Si sigue la guía paso a paso y aprovecha el código de ejemplo proporcionado, puede integrar fácilmente esta funcionalidad en sus aplicaciones Java, lo que permite una gestión eficiente de los archivos de OneNote.

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.Note para Java para crear nuevos documentos de OneNote?

R1: Sí, Aspose.Note para Java proporciona soporte integral para crear, leer y manipular documentos de OneNote mediante programación.

### P2: ¿Aspose.Note para Java es compatible con diferentes versiones de archivos OneNote?

R2: Sí, Aspose.Note para Java admite varias versiones de archivos de Microsoft OneNote, lo que garantiza la compatibilidad entre diferentes entornos.

### P3: ¿Puedo personalizar el formato de salida al exportar documentos de OneNote?

R3: Por supuesto, Aspose.Note para Java ofrece flexibilidad para exportar documentos de OneNote a diferentes formatos como PDF, HTML e imágenes, con opciones de personalización.

### P4: ¿Aspose.Note para Java requiere una licencia para uso comercial?

R4: Sí, se requiere una licencia válida para el uso comercial de Aspose.Note para Java. Puede obtener una licencia en el sitio web de Aspose.

### P5: ¿Dónde puedo buscar ayuda si tengo problemas o tengo preguntas sobre Aspose.Note para Java?

 R5: Para obtener soporte y asistencia, puede visitar el foro Aspose.Note[aquí](https://forum.aspose.com/c/note/28)donde podrás hacer preguntas, compartir experiencias e interactuar con otros usuarios y expertos.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

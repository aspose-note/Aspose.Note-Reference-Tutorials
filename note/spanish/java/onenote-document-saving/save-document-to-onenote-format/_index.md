---
title: Guardar documento en formato OneNote - Aspose.Note
linktitle: Guardar documento en formato OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda a guardar documentos en formato OneNote usando Aspose.Note para Java. Siga nuestra guía paso a paso para una integración perfecta.
type: docs
weight: 10
url: /es/java/onenote-document-saving/save-document-to-onenote-format/
---
## Introducción

Bienvenido al tutorial sobre cómo guardar documentos en formato OneNote usando Aspose.Note para Java. Aspose.Note es una poderosa biblioteca de Java que le permite trabajar con archivos de Microsoft OneNote mediante programación, lo que le permite crear, manipular y convertir documentos de OneNote sin esfuerzo.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

1. Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su sistema.
2.  Aspose.Note para Java JAR: descargue e incluya la biblioteca Aspose.Note para Java en su proyecto. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/java/).
3. Entorno de desarrollo integrado (IDE): elija su IDE preferido para el desarrollo de Java, como IntelliJ IDEA, Eclipse o NetBeans.

## Importar paquetes

Para comenzar, importe los paquetes necesarios en su proyecto Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.examples.Utils;
```

## Paso 1: descargue e instale Aspose.Note para Java

En primer lugar, descargue la biblioteca Aspose.Note para Java desde[enlace de descarga](https://releases.aspose.com/note/java/).

## Paso 2: configure su entorno de desarrollo

Configure su entorno de desarrollo creando un nuevo proyecto Java en su IDE elegido e incluyendo el archivo JAR Aspose.Note en la ruta de clases de su proyecto.

## Paso 3: guarde el documento en formato OneNote

Ahora, dividamos el ejemplo de código proporcionado en varios pasos:

### Paso 3.1: Definir el directorio de documentos

```java
String dataDir = "Your Document Directory";
```

 Reemplazar`"Your Document Directory"` con la ruta al directorio donde se encuentra su documento de OneNote.

### Paso 3.2: cargar el documento de OneNote

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Esta línea de código carga el documento de OneNote denominado "Sample1.one" desde el directorio especificado.

### Paso 3.3: guardar el documento en formato OneNote

```java
doc.save(dataDir + "SaveDocToOneNoteFormat_out.one");
```

Finalmente, este código guarda el documento de OneNote cargado en el archivo de salida especificado en formato OneNote.

## Conclusión

En conclusión, este tutorial le ha proporcionado una guía paso a paso sobre cómo guardar documentos en formato OneNote utilizando Aspose.Note para Java. Si sigue estas instrucciones, podrá integrar perfectamente la manipulación de documentos de OneNote en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Aspose.Note para Java puede funcionar con todas las versiones de archivos OneNote?

R1: Sí, Aspose.Note para Java admite trabajar con archivos OneNote creados en todas las versiones de Microsoft OneNote.

### P2: ¿Hay una prueba gratuita disponible para Aspose.Note para Java?

 R2: Sí, puede obtener una prueba gratuita de Aspose.Note para Java desde[aquí](https://releases.aspose.com/).

### P3: ¿Cómo puedo obtener soporte técnico para Aspose.Note para Java?

 R3: Puede obtener soporte técnico visitando el foro Aspose.Note[aquí](https://forum.aspose.com/c/note/28).

### P4: ¿Puedo comprar una licencia temporal de Aspose.Note para Java?

 R4: Sí, puede comprar una licencia temporal en[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo encontrar documentación detallada de Aspose.Note para Java?

 A5: Puedes acceder a la documentación detallada[aquí](https://reference.aspose.com/note/java/).
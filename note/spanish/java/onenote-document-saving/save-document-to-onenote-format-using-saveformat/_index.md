---
title: Guardar documento en OneNote usando SaveFormat - Aspose.Note
linktitle: Guardar documento en OneNote usando SaveFormat - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda a guardar documentos en formato OneNote usando Aspose.Note para Java. Siga este tutorial paso a paso para una integración perfecta en sus aplicaciones Java.
weight: 12
url: /es/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar documento en OneNote usando SaveFormat - Aspose.Note

## Introducción

Aspose.Note para Java es una potente biblioteca que permite a los desarrolladores trabajar con archivos de Microsoft OneNote mediante programación. Guardar un documento en formato OneNote usando SaveFormat es un proceso sencillo. En este tutorial, recorreremos los pasos necesarios para realizar esta tarea.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1. Kit de desarrollo de Java (JDK) instalado en su sistema.
2.  Descarga la biblioteca Aspose.Note para Java. Puedes obtenerlo de[aquí](https://releases.aspose.com/note/java/).
3. Conocimientos básicos del lenguaje de programación Java.

## Importar paquetes

 Primero, necesita importar los paquetes necesarios a su proyecto Java. Esto incluye importar el`com.aspose.note` paquete para trabajar con las funcionalidades de Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Paso 1: configurar el directorio de documentos

Defina el directorio donde se encuentra su documento y donde desea guardar el archivo de salida.

```java
String dataDir = "Your Document Directory";
```

## Paso 2: cargar el documento

 Cargue el documento en su aplicación Java usando el`Document` clase proporcionada por Aspose.Note.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## Paso 3: guarde el documento en formato OneNote

Guarde el documento cargado en el formato OneNote usando el`save` método y especificando el formato de archivo de salida deseado como`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## Conclusión

En este tutorial, aprendimos cómo guardar un documento en formato OneNote usando SaveFormat en Aspose.Note para Java. Si sigue estos sencillos pasos, podrá integrar perfectamente esta funcionalidad en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Aspose.Note para Java es compatible con todas las versiones de Microsoft OneNote?

R1: Aspose.Note para Java admite varias versiones de Microsoft OneNote, lo que garantiza la compatibilidad entre diferentes entornos.

### P2: ¿Puedo probar Aspose.Note para Java antes de comprarlo?

 R2: Sí, puede descargar una versión de prueba gratuita de Aspose.Note para Java desde[aquí](https://releases.aspose.com/).

### P3: ¿Dónde puedo encontrar documentación para Aspose.Note para Java?

 A3: Puede encontrar documentación detallada para Aspose.Note para Java[aquí](https://reference.aspose.com/note/java/).

### P4: ¿Cómo puedo obtener soporte técnico para Aspose.Note para Java?

 R4: Para obtener asistencia y soporte técnico, puede visitar el foro Aspose.Note[aquí](https://forum.aspose.com/c/note/28).

### P5: ¿Existe una opción de licencia temporal disponible para Aspose.Note para Java?

 R5: Sí, puede obtener una licencia temporal de Aspose.Note para Java en[aquí](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

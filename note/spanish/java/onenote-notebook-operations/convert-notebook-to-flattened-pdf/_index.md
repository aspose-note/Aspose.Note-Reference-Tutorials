---
title: Convierta Notebook a PDF aplanado en OneNote - Aspose.Note
linktitle: Convierta Notebook a PDF aplanado en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Convierta cuadernos a archivos PDF aplanados sin esfuerzo con Aspose.Note para Java. Disfrute de opciones perfectas de integración y personalización.
weight: 16
url: /es/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convierta Notebook a PDF aplanado en OneNote - Aspose.Note

## Introducción

En este tutorial, exploraremos cómo convertir un cuaderno a un formato PDF aplanado usando Aspose.Note para Java. La conversión de cuadernos a PDF es un requisito común para muchas aplicaciones y Aspose.Note simplifica este proceso con su conjunto completo de funciones y su API fácil de usar.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1. Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su sistema.
2.  Biblioteca Aspose.Note para Java: descargue e instale la biblioteca Aspose.Note para Java desde[aquí](https://releases.aspose.com/note/java/).
3. Entorno de desarrollo integrado (IDE): elija un IDE de su preferencia, como IntelliJ IDEA o Eclipse.

## Importar paquetes

En primer lugar, importemos los paquetes necesarios en su proyecto Java:

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## Paso 1: cargue el cuaderno OneNote

Para comenzar, cargue el cuaderno de OneNote que desea convertir a PDF:

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Paso 2: configurar las opciones de conversión

 Defina las opciones para convertir el cuaderno a PDF. Aquí configuraremos`flatten` a`true` para aplanar el PDF:

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## Paso 3: guarde el cuaderno como PDF

Especifique el directorio de salida y guarde el cuaderno como PDF con las opciones definidas:

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// Guarde el cuaderno
notebook.save(dataDir, notebookSaveOptions);
```

## Conclusión

En este tutorial, aprendimos cómo convertir un cuaderno a un formato PDF aplanado usando Aspose.Note para Java. Este proceso es sencillo y se puede integrar perfectamente en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Aspose.Note para Java es compatible con diferentes versiones de OneNote?

R1: Sí, Aspose.Note para Java admite varias versiones de OneNote, lo que garantiza la compatibilidad entre diferentes entornos.

### P2: ¿Puedo personalizar la salida del PDF usando Aspose.Note para Java?

R2: Por supuesto, puedes personalizar la salida del PDF según tus requisitos, incluido el diseño de la página, los estilos de fuente y más.

### P3: ¿Aspose.Note para Java admite la conversión por lotes de cuadernos?

R3: Sí, puede convertir por lotes varios cuadernos a PDF de manera eficiente utilizando Aspose.Note para Java.

### P4: ¿Existe una versión de prueba disponible de Aspose.Note para Java?

 R4: Sí, puede acceder a una prueba gratuita de Aspose.Note para Java desde[aquí](https://releases.aspose.com/).

### P5: ¿Dónde puedo encontrar soporte para Aspose.Note para Java?

 R5: Puede encontrar soporte y asistencia para Aspose.Note para Java en el[Foro Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Utilice el algoritmo Mantener objetos sólidos en OneNote - Aspose.Note
linktitle: Utilice el algoritmo Mantener objetos sólidos en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda cómo conservar objetos sólidos en sus documentos Aspose.Note al convertirlos a PDF utilizando el algoritmo Mantener objetos sólidos en Java.
type: docs
weight: 25
url: /es/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---
## Introducción

En este tutorial, exploraremos cómo utilizar el algoritmo Mantener objetos sólidos en Aspose.Note para Java. Este algoritmo es invaluable para mantener la integridad de los objetos sólidos dentro de sus documentos al convertirlos al formato PDF. Desglosaremos el proceso paso a paso, garantizando claridad y comprensión en cada etapa.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1. Kit de desarrollo de Java (JDK) instalado en su sistema.
2.  Aspose.Note para la biblioteca Java. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/java/).

## Importar paquetes

Primero, importemos los paquetes necesarios:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Paso 1: cargue el documento

Cargue el documento en Aspose.Note usando el siguiente fragmento de código:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Paso 2: configurar las opciones de guardar PDF

Defina PdfSaveOptions y establezca PageSplittingAlgorithm en KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Paso 3: ajustar el límite de altura (opcional)

Puede ajustar el límite de altura de las piezas clonadas si es necesario:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Paso 4: guarde el documento

Finalmente, guarde el documento con las opciones de guardado de PDF especificadas:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Conclusión

En este tutorial, aprendimos cómo utilizar el algoritmo Mantener objetos sólidos en Aspose.Note para Java. Este algoritmo garantiza que los objetos sólidos dentro de sus documentos se conserven al convertirlos a formato PDF, manteniendo la integridad del documento.

## Preguntas frecuentes

### P1: ¿Puedo ajustar el límite de altura para piezas clonadas?

 R1: Sí, puede ajustar el límite de altura de las piezas clonadas según sus requisitos utilizando el`heightLimitOfClonedPart` parámetro.

### P2: ¿Dónde puedo encontrar más documentación?

 R2: Puede encontrar documentación detallada en Aspose.Note para Java[aquí](https://reference.aspose.com/note/java/).

### P3: ¿Hay una prueba gratuita disponible?

 R3: Sí, puede obtener una prueba gratuita de Aspose.Note para Java[aquí](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener asistencia si tengo algún problema?

 R4: Puede obtener soporte de la comunidad Aspose[aquí](https://forum.aspose.com/c/note/28).

### P5: ¿Dónde puedo comprar una licencia?

 R5: Puede adquirir una licencia de Aspose.Note para Java[aquí](https://purchase.aspose.com/buy).

---
title: Especificar opciones de guardar en OneNote - Aspose.Note
linktitle: Especificar opciones de guardar en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda a especificar opciones de guardado en OneNote usando Aspose.Note para Java. Personalice las configuraciones de índice, recuento y compresión de páginas sin esfuerzo.
weight: 24
url: /es/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Especificar opciones de guardar en OneNote - Aspose.Note

## Introducción

En este tutorial, aprenderemos cómo especificar opciones de guardado en OneNote usando Aspose.Note para Java. Aspose.Note es una potente biblioteca Java que permite a los desarrolladores crear, manipular y convertir documentos OneNote mediante programación. Con Aspose.Note, puede controlar fácilmente varias opciones de guardado para personalizar la salida según sus requisitos.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

1. Conocimientos básicos del lenguaje de programación Java.
2. JDK (Java Development Kit) instalado en su sistema.
3.  Aspose.Note para la biblioteca Java instalada. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/java/).

## Importar paquetes

Para comenzar, importe los paquetes necesarios en su código Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Dividamos el ejemplo en varios pasos:

## Paso 1: cargue el documento de OneNote

```java
// La ruta al directorio de documentos.
String dataDir = "Your Document Directory";

// Cargue el documento en Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

 En este paso, especificamos la ruta al documento de OneNote y lo cargamos en el`Document` objeto.

## Paso 2: inicializar el objeto PdfSaveOptions

```java
// Inicializar el objeto PdfSaveOptions
PdfSaveOptions opts = new PdfSaveOptions();
```

 Aquí inicializamos un`PdfSaveOptions` objeto que se utilizará para especificar las opciones para guardar el documento como PDF.

## Paso 3: establecer el índice y el recuento de páginas

```java
// Establecer índice de página
opts.setPageIndex(2);

// Establecer recuento de páginas
opts.setPageCount(3);
```

Estas líneas establecen el índice y el recuento de las páginas que se guardarán. En este ejemplo, estamos guardando páginas a partir del índice 2 y un total de 3 páginas.

## Paso 4: especificar la configuración de compresión

```java
// Especifique la compresión si es necesario
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Aquí, especificamos la configuración de compresión de imágenes para el PDF. Configuramos la compresión en formato JPEG y especificamos la calidad JPEG al 90%.

## Paso 5: guarde el documento con opciones

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Finalmente guardamos el documento con las opciones especificadas. El PDF de salida se guardará en la ubicación especificada con las opciones dadas.

## Conclusión

En este tutorial, hemos aprendido cómo especificar opciones de guardado en OneNote usando Aspose.Note para Java. Al personalizar las opciones de guardado, puede controlar varios aspectos del documento de salida, como el índice de páginas, el recuento y la configuración de compresión.

## Preguntas frecuentes

### P1: ¿Puede Aspose.Note manejar documentos OneNote de gran tamaño?

R1: Sí, Aspose.Note está diseñado para manejar documentos grandes de OneNote de manera eficiente.

### P2: ¿Aspose.Note es compatible con las últimas versiones de Java?

R2: Sí, Aspose.Note es compatible con las últimas versiones de Java.

### P3: ¿Puedo convertir documentos de OneNote a otros formatos usando Aspose.Note?

R3: Sí, Aspose.Note admite la conversión de documentos de OneNote a varios formatos, como PDF, DOCX y HTML.

### P4: ¿Aspose.Note proporciona soporte para el cifrado y descifrado de documentos de OneNote?

R4: Sí, Aspose.Note proporciona API para cifrar y descifrar documentos de OneNote.

### P5: ¿Aspose.Note es adecuado para uso comercial?

R5: Sí, Aspose.Note se puede utilizar con fines comerciales comprando una licencia.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

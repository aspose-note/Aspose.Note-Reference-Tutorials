---
title: Guardar en PDF usando la configuración de página en OneNote - Aspose.Note
linktitle: Guardar en PDF usando la configuración de página en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda cómo guardar documentos de OneNote en PDF en Java usando la biblioteca Aspose.Note. Guía paso a paso con ejemplos de código para diferentes configuraciones de página.
weight: 19
url: /es/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar en PDF usando la configuración de página en OneNote - Aspose.Note

## Introducción

En este tutorial, aprenderemos cómo guardar documentos de OneNote en formato PDF usando diferentes configuraciones de página con Aspose.Note para Java. Cubriremos dos métodos: guardar con la configuración de página Carta y guardar con la configuración de página A4 sin límite de altura.

## Requisitos previos

Antes de comenzar, asegúrese de cumplir con los siguientes requisitos previos:

1. Kit de desarrollo de Java (JDK) instalado en su sistema.
2. Biblioteca Aspose.Note para Java descargada e incluida en su proyecto Java.
3. Conocimientos básicos del lenguaje de programación Java.

## Importar paquetes

Asegúrese de haber importado los paquetes necesarios para usar Aspose.Note para Java en su proyecto. Aquí está la declaración de importación:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Guardar en PDF usando la configuración de página Carta

### Paso 1: cargue el documento

En primer lugar, cargue el documento de OneNote en Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Paso 2: definir la ruta de destino

Especifique la ruta de destino del archivo PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Paso 3: guarde el documento

Guarde el documento con la configuración de página Carta:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Guardar en PDF usando la configuración de página A4 sin límite de altura

### Paso 1: cargue el documento

De manera similar, cargue el documento de OneNote en Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Paso 2: definir la ruta de destino

Especifique la ruta de destino del archivo PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Paso 3: guarde el documento

Guarde el documento con configuración de página A4 sin límite de altura:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Después de seguir estos pasos, habrá guardado con éxito su documento de OneNote en PDF usando diferentes configuraciones de página.

## Conclusión

En este tutorial, hemos explorado cómo guardar documentos de OneNote en formato PDF usando la biblioteca Aspose.Note para Java. Si sigue la guía paso a paso, podrá integrar fácilmente esta funcionalidad en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Puedo personalizar aún más la configuración de la página?

R1: Sí, puede personalizar la configuración de la página según sus requisitos utilizando Aspose.Note para Java.

### P2: ¿Aspose.Note admite otros formatos de salida además de PDF?

R2: Sí, Aspose.Note admite varios formatos de salida, incluidas imágenes y HTML.

### P3: ¿Aspose.Note es compatible con diferentes versiones de archivos OneNote?

R3: Sí, Aspose.Note admite archivos OneNote de diferentes versiones, incluidas .one y .onetoc2.

### P4: ¿Puedo convertir varios archivos de OneNote a PDF en una sola ejecución?

R4: Sí, puede procesar por lotes varios archivos de OneNote utilizando Aspose.Note para Java.

### P5: ¿Existe alguna versión de prueba disponible para fines de prueba?

R5: Sí, puede obtener una prueba gratuita de Aspose.Note para Java desde el sitio web.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

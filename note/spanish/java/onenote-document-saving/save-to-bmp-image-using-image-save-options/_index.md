---
date: 2025-12-16
description: Aprenda cómo guardar documentos de OneNote como imágenes BMP usando las
  opciones de guardado de imágenes de Aspose.Note para Java. También vea cómo guardar
  OneNote en PDF o PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Cómo guardar OneNote como imagen BMP usando opciones de guardado de imagen
url: /es/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# cómo guardar OneNote como imagen BMP usando opciones de guardado de imagen

## Introducción

## Respuestas rápidas
- **¿Qué hace la clase Image Save Options?** Permite especificar el formato de imagen de salida (BMP, PNG, JPEG, etc.) al convertir una página de OneNote.  
- **¿Necesito una licencia para ejecutar el ejemplo?** Una prueba gratuita sirve para evaluación, pero se requiere una licencia comercial para uso en producción.  
- **¿Puedo convertir una página de OneNote a PDF o PNG en lugar de BMP?** Sí, simplemente cambie el enum `SaveFormat` (p.ej., `SaveFormat.Pdf` o `SaveFormat.Png`).  
- **¿Qué versión de Java es compatible?** Java 8 y posteriores son totalmente compatibles.  
- **¿Hay algún manejo especial para documentos grandes?** Puede transmitir la salida para evitar un alto consumo de memoria.

## ¿Qué es “Image Save Options” en Aspose.Note?
La clase `ImageSaveOptions` proporciona un control detallado sobre cómo se renderizan las páginas de OneNote como imágenes raster. Puede establecer el formato de imagen, la resolución, la profundidad de color y más. Esta flexibilidad facilita generar archivos BMP para sistemas heredados o archivos PNG/JPEG para uso web.

## Requisitos previos

1. Conocimientos básicos del lenguaje de programación Java.  
2. JDK (Java Development Kit) instalado en su máquina.  
3. Un IDE como Eclipse o IntelliJ IDEA.  
4. Biblioteca Aspose.Note for Java – descárguela desde [aquí](https://releases.aspose.com/note/java/).

## Importar paquetes

First, import the necessary Aspose.Note classes and standard Java I/O utilities:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Paso 1: Cargar el documento OneNote

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Aquí apuntamos a la carpeta que contiene el archivo OneNote fuente (`Aspose.one`) y lo cargamos en un objeto `Document`. Este objeto le brinda acceso completo a páginas, secciones y otros elementos dentro del cuaderno.

## Paso 2: Guardar el documento como imagen BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Concatenamos el nombre del archivo de salida y luego llamamos a `save` con una instancia de `ImageSaveOptions` configurada para **BMP** (`SaveFormat.Bmp`).  
Si desea **guardar una página de OneNote** como PNG, simplemente reemplace `SaveFormat.Bmp` por `SaveFormat.Png`. De manera similar, `SaveFormat.Pdf` le permite realizar una conversión **de OneNote a PDF**.

## ¿Por qué elegir BMP?
- **Calidad sin pérdida** – BMP almacena datos de píxeles sin procesar, preservando la apariencia exacta de la página original.  
- **Compatibilidad** – Las aplicaciones antiguas de Windows a menudo requieren archivos BMP.  
- **Simplicidad** – Sin artefactos de compresión, lo que lo hace ideal para procesamiento de imágenes posterior.

## Problemas comunes y consejos

- **Errores de ruta de archivo** – Asegúrese de que `dataDir` termine con el separador de archivos apropiado (`/` o `\`).  
- **Cuadernos grandes** – Para archivos OneNote muy grandes, considere guardar cada página individualmente para mantener bajo el uso de memoria.  
- **Excepciones de licencia** – Ejecutar el código sin una licencia válida añadirá una marca de agua a la imagen generada.

## Conclusión

En esta guía demostramos **cómo guardar documentos OneNote** como imágenes BMP usando `ImageSaveOptions` de Aspose.Note for Java. Al cambiar el enum `SaveFormat` también puede generar PNG, JPEG, PDF u otros formatos compatibles, brindándole una forma flexible de exportar contenido de OneNote para cualquier escenario posterior.

## Preguntas frecuentes

**Q1: ¿Puedo guardar documentos OneNote en otros formatos de imagen además de BMP?**  
R: Sí, puede usar `ImageSaveOptions` con `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` o `SaveFormat.Tiff` para exportar a esos formatos.

**Q2: ¿Aspose.Note for Java admite la conversión entre diferentes formatos de documento?**  
R: Absolutamente. Además de los formatos de imagen, puede convertir archivos OneNote a PDF, DOCX, HTML y más usando el `SaveFormat` apropiado.

**Q3: ¿Aspose.Note for Java es compatible con las versiones más recientes de OneNote?**  
R: Sí, la biblioteca se actualiza regularmente para mantenerse sincronizada con las últimas versiones de OneNote.

**Q4: ¿Puedo manipular el contenido de los documentos OneNote programáticamente?**  
R: Sí, puede agregar, editar o eliminar páginas, secciones y contenido enriquecido (texto, imágenes, tablas) a través de la API.

**Q5: ¿Aspose.Note for Java ofrece soporte técnico?**  
R: Sí, Aspose ofrece soporte técnico y un foro dedicado. Visite el [foro de Aspose.Note](https://forum.aspose.com/c/note/28) para obtener ayuda.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose
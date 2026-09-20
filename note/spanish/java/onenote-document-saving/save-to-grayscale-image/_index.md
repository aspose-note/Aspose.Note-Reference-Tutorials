---
date: 2026-06-30
description: Aprenda cómo exportar OneNote guardando un documento como una imagen
  PNG en escala de grises usando Aspose.Note para Java. Incluye los pasos para cargar
  el documento de OneNote y crear una imagen en escala de grises.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Cómo exportar OneNote como imagen en escala de grises – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Cómo exportar OneNote como imagen en escala de grises – Aspose.Note
url: /es/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar como imagen en escala de grises en OneNote - Aspose.Note

## Introducción

En este tutorial descubrirás **cómo exportar onenote** convirtiendo un archivo OneNote `.one` en una imagen PNG en escala de grises de alta calidad usando Aspose.Note para Java. Los desarrolladores Java a menudo necesitan la conversión a escala de grises para impresión, archivado, o para **reducir el tamaño de OneNote** sin perder contenido esencial. Recorreremos la carga de un documento OneNote, la configuración de las opciones de guardado —incluyendo **ajustar la resolución de la imagen**— y finalmente guardaremos el documento como PNG.

## Respuestas rápidas
- **¿Qué significa “how to export onenote”?** Se refiere a convertir programáticamente un archivo OneNote a otro formato, como una imagen, usando código.  
- **¿Qué formato es el mejor para salida en escala de grises?** PNG funciona bien porque preserva calidad sin pérdidas y soporta un modo de color en escala de grises dedicado.  
- **¿Necesito una licencia?** Se requiere una licencia válida de Aspose.Note para uso en producción; una licencia de prueba temporal está disponible para pruebas.  
- **¿Qué versión de Java se requiere?** Se recomienda Java 8 o superior.  
- **¿Puedo cambiar el tamaño de la imagen?** Sí, puedes ajustar las propiedades de `ImageSaveOptions` como `Resolution` o `PageSize` antes de guardar.

## ¿Qué es “how to export onenote”?

Exportar OneNote significa convertir programáticamente un archivo OneNote `.one` a otra representación—como PDF, HTML o una imagen. En esta guía nos centramos en **crear imágenes PNG en escala de grises**, un requisito común para documentación o flujos de trabajo listos para imprimir. Usando Aspose.Note, la conversión ocurre completamente en memoria, por lo que nunca necesitas Microsoft OneNote instalado en el servidor.

## ¿Por qué exportar OneNote como una imagen en escala de grises?

Los PNG en escala de grises son típicamente **30‑40 % más pequeños** que sus contrapartes en color completo, lo que acelera la entrega web y reduce los costos de almacenamiento. También proporcionan **un contraste más claro** en impresoras láser, facilitando la lectura de los informes. Debido a que PNG es universalmente compatible, los archivos resultantes funcionan en navegadores, dispositivos móviles y editores de escritorio sin códecs adicionales.

## Requisitos previos

1. Java Development Kit (JDK) 8 o una versión más reciente instalado.  
2. Biblioteca Aspose.Note para Java – descarga la última versión desde [here](https://releases.aspose.com/note/java/).  
3. Un entendimiento básico de la sintaxis de Java y la configuración de proyectos Maven/Gradle.  

## Importar paquetes

La clase `ImageSaveOptions` controla cómo se renderiza el documento a una imagen.  
`ColorMode` es una enumeración que permite cambiar entre salida en color completo y escala de grises.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Paso 1: Cargar el documento OneNote

`Document` representa un cuaderno OneNote y proporciona métodos para cargar, editar y guardar su contenido. Primero, **carga el documento OneNote** en Aspose.Note. Reemplaza `"Your Document Directory"` con la ruta a tu carpeta local y `"Aspose.one"` con el nombre de tu archivo OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Paso 2: Establecer la ruta de salida y las opciones

`ImageSaveOptions` configura cómo se renderiza un documento OneNote a un archivo de imagen. La enumeración `ColorMode` selecciona el modo de renderizado de color, como escala de grises o color completo. Define la ruta de salida para la imagen en escala de grises y especifica las opciones de guardado. Configuraremos `ColorMode` a `GrayScale` y usaremos el formato **save document as PNG**. También puedes **ajustar la resolución de la imagen** a 300 DPI para impresiones de alta calidad.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Paso 3: Guardar el documento

Finalmente, guarda el documento como una imagen PNG en escala de grises usando las opciones configuradas. El método `save` escribe el archivo en disco sin requerir archivos temporales intermedios.

```java
oneFile.save(dataDir, options);
```

## Problemas comunes y soluciones
- **FileNotFoundException** – Verifica que `dataDir` apunte a la carpeta correcta y que el archivo `.one` exista.  
- **LicenseException** – Asegúrate de haber aplicado una licencia válida de Aspose.Note antes de llamar a `save`.  
- **Low‑resolution output** – Ajusta `options.setResolution(300)` para incrementar DPI; un DPI más alto produce impresiones más nítidas pero archivos de mayor tamaño.  

## Preguntas frecuentes

**Q1: ¿Puedo guardar la imagen en escala de grises en un formato diferente?**  
A1: Sí, simplemente cambia el parámetro `SaveFormat` en el constructor `ImageSaveOptions` a `Jpeg`, `Bmp`, o cualquiera de los más de 20 formatos de imagen compatibles.

**Q2: ¿Aspose.Note es compatible con todas las versiones de documentos OneNote?**  
A2: Aspose.Note es compatible con Microsoft OneNote 2010 y versiones posteriores, cubriendo más del 95 % de los cuadernos en uso activo hoy.

**Q3: ¿Aspose.Note requiere una licencia para usarlo?**  
A3: Se requiere una licencia válida para uso en producción, pero se puede obtener una licencia de prueba temporal para evaluación sin costo.

**Q4: ¿Puedo manipular otros aspectos del documento antes de guardarlo como imagen?**  
A4: ¡Absolutamente! Aspose.Note proporciona APIs para editar secciones, páginas y elementos individuales como texto, tablas e imágenes antes de la exportación.

**Q5: ¿Dónde puedo encontrar soporte si encuentro problemas?**  
A5: Puedes encontrar soporte en el foro de Aspose.Note [aquí](https://forum.aspose.com/c/note/28).

## Conclusión

Ahora has aprendido **cómo exportar onenote** cargando un archivo OneNote, configurando las opciones de guardado para **crear una imagen en escala de grises**, y **guardando el documento como PNG**. Este enfoque es ideal para generar visuales ligeros y listos para imprimir a partir de cuadernos OneNote. Siéntete libre de experimentar con otras configuraciones de `ColorMode`, valores de DPI más altos o formatos de imagen alternativos para adaptarlos a los requisitos de tu proyecto.

---

**Última actualización:** 2026-06-30  
**Probado con:** Aspose.Note 27.0 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Exportar página OneNote a imagen PNG en Java usando Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote establecer resolución jpeg – Establecer resolución de imagen de salida en OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Cómo guardar OneNote como PDF con Aspose.Note para Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
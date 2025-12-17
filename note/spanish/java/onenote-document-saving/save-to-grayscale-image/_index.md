---
date: 2025-12-17
description: Aprenda cómo exportar OneNote guardando un documento como una imagen
  PNG en escala de grises usando Aspose.Note para Java. Incluye los pasos para cargar
  el documento de OneNote y crear una imagen en escala de grises.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
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

En este tutorial, le mostraremos **cómo exportar onenote** guardando un documento como una imagen en escala de grises usando Aspose.Note para Java. Las en escala de grises son fotos monocromáticas que contienen solo tonos de gris, lo que puede ser útil para impresión, archivado o reducir el tamaño del archivo. Recorreremos la carga de un documento OneNote, la configuración de las opciones de guardado para **crear una imagen en escala de grises**, y finalmente **guardar el documento como PNG**.

## Respuestas rápidas
- **¿Qué significa “how to export onenote”?** Se refiere a convertir un archivo OneNote a otro formato, como una imagen, de forma programática.  
- **¿Qué formato es el mejor para salida en escala de grises?** PNG funciona bien porque preserva calidad sin pérdida y soporta modo de color en escala de grises.  
- **¿Necesito una licencia?** Se requiere una licencia válida de Aspose.Note para uso en producción; una licencia de prueba temporal está disponible para pruebas.  
- **¿Qué versión de Java se requiere?** Se recomienda Java 8 o superior.  
- **¿Puedo cambiar el tamaño de la imagen?** Sí, puede ajustar las propiedades de `ImageSaveOptions` como `Resolution` o `PageSize` antes de guardar.

## Qué es “how to export onenote”?
Exportar OneNote significa convertir programáticamente un archivo OneNote `.one` a otra representación—como PDF, HTML o una imagen. En esta guía nos centramos en exportar a una imagen **PNG en escala de grises**, que es un requisito común para documentación o flujos de trabajo de impresión.

## Por qué exportar OneNote como una imagen en escala de grises?
- **Tamaño de archivo reducido** – Los PNG en escala de grises suelen ser más pequeños que las imágenes a color completo.  
- **Mejor legibilidad** – Para informes impresos, la escala de grises a menudo brinda mayor contraste.  
- **Compatibilidad** – PNG es ampliamente compatible en navegadores, editores y dispositivos móviles.  

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1. Java Development Kit (JDK) instalado en su sistema.  
2. Biblioteca Aspose.Note para Java. Puede descargarla desde [aquí](https://releases.aspose.com/note/java/).  
3. Comprensión básica de la programación Java.  

## Importar paquetes

Para comenzar, importe los paquetes necesarios:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Paso 1: Cargar el documento OneNote

Primero, **cargue onenote document** en Aspose.Note. Reemplace `"Your Document Directory"` con la ruta a su carpeta local y `"Aspose.one"` con el nombre de su archivo OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Paso 2: Establecer la ruta de salida y las opciones

Defina la ruta de salida para la imagen en escala de grises y especifique las opciones de guardado. Configuraremos `ColorMode` a `GrayScale` y usaremos el formato **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Paso 3: Guardar el documento

Finalmente, guarde el documento como una imagen PNG en escala de grises usando las opciones configuradas.

```java
oneFile.save(dataDir, options);
```

## Problemas comunes y soluciones
- **FileNotFoundException** – Verifique que `dataDir` apunte a la carpeta correcta y que el archivo `.one` exista.  
- **LicenseException** – Asegúrese de haber aplicado una licencia válida de Aspose.Note antes de llamar a `save`.  
- **Salida de baja resolución** – Ajuste `options.setResolution(300)` para aumentar DPI si es necesario.

## Preguntas frecuentes

**Q1: ¿Puedo guardar la imagen en escala de grises en un formato diferente?**  
A1: Sí, simplemente cambie el parámetro `SaveFormat` en el constructor `ImageSaveOptions` a `Jpeg`, `Bmp`, etc.

**Q2: ¿Aspose.Note es compatible con todas las versiones de documentos OneNote?**  
A2: Aspose.Note soporta Microsoft OneNote 2010 y versiones posteriores.

**Q3: ¿Aspose.Note requiere una licencia para usarlo?**  
A3: Se requiere una licencia válida para uso en producción, pero se puede obtener una licencia de prueba temporal para evaluación.

**Q4: ¿Puedo manipular otros aspectos del documento antes de guardarlo como imagen?**  
A4: ¡Absolutamente! Aspose.Note ofrece una API completa para editar secciones, páginas y contenido antes de la exportación.

**Q5: ¿Dónde puedo encontrar soporte si encuentro problemas?**  
A5: Puede encontrar soporte en el foro de Aspose.Note [aquí](https://forum.aspose.com/c/note/28).

## Conclusión

Ahora ha aprendido **cómo exportar onenote** cargando un archivo OneNote, configurando las opciones de guardado para **crear una imagen en escala de grises**, y **guardando el documento como PNG**. Esta técnica es útil para generar visuales ligeros y listos para imprimir a partir de cuadernos OneNote. Siéntase libre de experimentar con otras configuraciones de `ColorMode` o formatos de imagen para adaptarse a las necesidades de su proyecto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose
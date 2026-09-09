---
date: 2026-03-05
description: Aprende cómo guardar OneNote como PDF mientras creas una lista numerada
  usando Aspose.Note para Java. Incluye pasos para establecer el estilo de texto predeterminado
  y personalizar la numeración.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Guardar OneNote como PDF – Crear lista numerada con Aspose.Note
url: /es/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar OneNote como PDF – Crear lista numerada con Aspose.Note

## Introducción
Aspose.Note for Java permite a los desarrolladores Java **save OneNote as PDF** y enriquecer el documento con formato avanzado, como listas numeradas. En este tutorial, le guiaremos a través del proceso completo—desde establecer un estilo de texto predeterminado hasta personalizar el formato de numeración—para que pueda exportar OneNote a PDF con un aspecto profesional.

## Respuestas rápidas
- **¿Qué cubre este tutorial?** Crear una lista numerada en OneNote y guardar el archivo como PDF usando Aspose.Note for Java.  
- **¿Qué palabra clave principal se dirige?** *save onenote as pdf*  
- **¿Necesito una licencia?** Hay una versión de prueba disponible; se requiere una licencia comercial para producción.  
- **¿Qué versión de Java se necesita?** JDK 8 o posterior.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10–15 minutos para una lista básica.

## ¿Qué es “save OneNote as PDF”?
Guardar OneNote como PDF convierte la página de OneNote con texto enriquecido en un documento portátil de diseño fijo que puede compartirse entre plataformas sin requerir OneNote. Esto es especialmente útil para archivado, informes o distribución de contenido a usuarios que no tienen OneNote instalado.

## ¿Por qué crear una lista numerada antes de exportar?
Una lista numerada agrega estructura y legibilidad, haciendo que el PDF exportado parezca un informe pulido. Con Aspose.Note puedes **customizar el formato de numeración**, establecer fuentes y controlar el espaciado, todo mientras preservas el diseño original de OneNote.

## Requisitos previos
Antes de comenzar, asegúrese de tener:

- Kit de desarrollo de Java (JDK) instalado en su máquina.  
- Biblioteca Aspose.Note for Java descargada desde [here](https://releases.aspose.com/note/java/).  

## Importando paquetes
Primero, importe las clases requeridas para trabajar con objetos OneNote y la conversión a PDF.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## ¿Cómo guardar OneNote como PDF con una lista numerada?
A continuación se muestra una guía paso a paso que explica **cómo crear elementos de lista**, **establecer el estilo de texto predeterminado** y, finalmente, **exportar OneNote a PDF**.

### Paso 1: Inicializar objetos Document, Page y Outline
Comenzamos creando las estructuras centrales de OneNote. Esto también demuestra el uso de **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Consejo profesional:** Mantenga la ruta `dataDir` absoluta o use `System.getProperty("user.dir")` para evitar problemas de ruta.

### Paso 2: Establecer estilo de texto predeterminado
Un estilo consistente asegura que la lista tenga un aspecto uniforme en todos los elementos.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Paso 3: Crear elementos Outline (lista numerada)
Aquí **customizamos el formato de numeración** usando `NumberList`. El patrón `"{0})"` produce “1)”, “2)”, etc.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Por qué es importante:** Al adjuntar un `NumberList` a cada `OutlineElement`, obtiene control total sobre el estilo de numeración, la fuente y el tamaño.

### Paso 4: Añadir elementos Outline al Outline
Ahora agrupamos los elementos individuales de la lista en un solo outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Paso 5: Adjuntar Outline a la página
El outline pasa a formar parte de la jerarquía de la página de OneNote.

```java
page.appendChildLast(outline);
```

### Paso 6: Guardar el documento como PDF
Finalmente, **save OneNote as PDF**. El archivo de salida contendrá la lista numerada exactamente como se definió.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Ejecutar el código anterior genera un PDF llamado `CreateNumberedList_out.pdf` en el directorio especificado, preservando el formato de la lista numerada.

## Problemas comunes y soluciones
| Problema | Solución |
|----------|----------|
| **PDF está vacío** | Asegúrese de que `doc.appendChildLast(page);` se llame antes de `doc.save()`. |
| **La numeración no se muestra** | Verifique que el patrón de `NumberList` y `NumberFormat` estén configurados correctamente. |
| **Error de archivo no encontrado** | Use una ruta absoluta para `dataDir` o cree el directorio con antelación. |
| **Desajuste de fuente** | Instale la fuente (p. ej., Arial) en la máquina donde se ejecuta el código. |

## Preguntas frecuentes
### P: ¿Puedo personalizar el formato de numeración en mi lista de OneNote?
R: ¡Absolutamente! Puede personalizar el formato de numeración usando la clase `NumberList` proporcionada por Aspose.Note for Java.

### P: ¿Hay una versión de prueba disponible para Aspose.Note for Java?
R: Sí, puede descargar una prueba gratuita [here](https://releases.aspose.com/).

### P: ¿Cómo puedo obtener soporte para Aspose.Note for Java?
R: Visite el [foro de Aspose.Note for Java](https://forum.aspose.com/c/note/28) para obtener soporte de la comunidad.

### P: ¿Dónde puedo encontrar documentación detallada para Aspose.Note for Java?
R: Consulte la [documentación](https://reference.aspose.com/note/java/) para obtener información completa.

### P: ¿Cómo compro una licencia para Aspose.Note for Java?
R: Puede adquirir una licencia [here](https://purchase.aspose.com/buy).

## Conclusión
En este tutorial demostramos cómo **save OneNote as PDF** mientras creamos una lista numerada limpia usando Aspose.Note for Java. Al establecer un estilo de texto predeterminado, personalizar el formato de numeración y seguir la guía paso a paso, puede generar PDFs profesionales a partir de páginas de OneNote de forma rápida y fiable.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2026-03-05  
**Probado con:** Aspose.Note for Java 24.11  
**Autor:** Aspose
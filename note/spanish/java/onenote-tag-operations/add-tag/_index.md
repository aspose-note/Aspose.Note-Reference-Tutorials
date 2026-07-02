---
date: 2026-01-28
description: Aprenda a crear esquemas en OneNote, añadir etiquetas a OneNote y generar
  PDF desde OneNote usando Aspose.Note para Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Crear esquema en OneNote y agregar etiqueta – Aspose.Note
url: /es/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear esquema en OneNote y agregar etiqueta – Aspose.Note

## Introducción
¿Está buscando **crear esquema en OneNote** y mejorar la colaboración con etiquetas usando Java? Aspose.Note para Java facilita agregar etiquetas, estructurar sus notas e incluso **generar PDF a partir de archivos OneNote**. En este tutorial recorreremos cada paso, explicaremos *por qué* cada elemento es importante y le mostraremos cómo producir un PDF pulido al final.

## Respuestas rápidas
- **¿Qué significa “crear esquema en OneNote”?** Construye una estructura jerárquica (esquemas) que organiza el contenido como encabezados y subsecciones.  
- **¿Qué biblioteca agrega etiquetas a OneNote?** Aspose.Note para Java proporciona la clase `NoteTag` para marcadores visuales.  
- **¿Puedo exportar el resultado a PDF?** Sí – use `SaveFormat.Pdf` para **generar PDF a partir de OneNote**.  
- **¿Necesito una licencia para producción?** Hay una licencia temporal disponible para pruebas; se requiere una licencia completa para uso comercial.  
- **¿Cuáles son los requisitos principales?** Tener instalado JDK, la biblioteca Aspose.Note para Java y conocimientos básicos de Java.

## ¿Qué es “crear esquema en OneNote”?
Crear un esquema en OneNote significa agregar objetos `Outline` y `OutlineElement` que definen una estructura tipo árbol para sus notas. Esta jerarquía le permite contraer, expandir y organizar la información al igual que los encabezados en un documento.

## ¿Por qué agregar una etiqueta a OneNote?
Las etiquetas como estrellas, marcas de verificación o íconos personalizados brindan a los lectores pistas visuales, mejoran la capacidad de búsqueda y ayudan a los equipos a priorizar elementos. Con Aspose.Note puede adjuntar programáticamente un `NoteTag` a cualquier fragmento de texto.

## Requisitos previos
Antes de comenzar, confirme que tiene:
- Java Development Kit (JDK) instalado.
- Biblioteca Aspose.Note para Java descargada. Puede obtenerla [aquí](https://releases.aspose.com/note/java/).
- Una comprensión básica de la programación en Java.

## Importar paquetes
Asegúrese de importar los paquetes necesarios para iniciar su proyecto:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Desglosemos el código anterior en una guía paso a paso.

## Paso 1: Configurar el documento y la página
Comience creando un nuevo objeto `Document` e inicializando un objeto `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Aquí, establecemos la ruta al directorio de documentos, creamos un nuevo `Document` y inicializamos una `Page`.

## Paso 2: Crear un esquema
A continuación, cree un objeto `Outline` para estructurar su contenido:
```java
Outline outline = new Outline();
```
Los esquemas proporcionan una estructura jerárquica a su documento, facilitando **crear esquema en OneNote** y mantener la información organizada.

## Paso 3: Inicializar OutlineElement y ParagraphStyle
Ahora, inicialice un `OutlineElement` y establezca `ParagraphStyle` para el formato del texto:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` representa un elemento dentro del esquema, y `ParagraphStyle` define las propiedades de formato del texto.

## Paso 4: Agregar RichText con NoteTag
Cree un objeto `RichText`, añada su texto de OneNote y agregue un `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` le permite incorporar texto con formato, y el `NoteTag` **agrega una etiqueta a OneNote** como pista visual.

## Paso 5: Construir la estructura del esquema
Agregue el nodo de texto, el nodo de elemento de esquema y el nodo de esquema para construir la estructura del documento:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Este paso asegura que su contenido esté organizado dentro del documento, completando el proceso de **crear esquema en OneNote**.

## Paso 6: Guardar el documento
Guarde el documento en formato PDF, lo que **genera PDF a partir de OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Ahora, su documento OneNote con etiquetas agregadas se guarda como PDF.

Siguiendo estos pasos, puede mejorar fácilmente sus documentos OneNote usando Aspose.Note para Java.

## Conclusión
En este tutorial exploramos cómo **crear esquema en OneNote**, agregar una etiqueta a OneNote y luego **generar PDF a partir de OneNote** usando Aspose.Note para Java. Aprovechar Java le brinda control total sobre la estructura de notas, el etiquetado visual y las opciones de exportación, haciendo sus notas más organizadas y compartibles.

## Preguntas frecuentes
### 1. ¿Puedo usar Aspose.Note para Java con otros lenguajes de programación?
Aspose.Note principalmente soporta Java, pero también hay versiones disponibles para .NET.

### 2. ¿Es Aspose.Note para Java adecuado para principiantes?
Sí, Aspose.Note para Java ofrece documentación y soporte completos, lo que lo hace accesible tanto para principiantes como para desarrolladores experimentados.

### 3. ¿Cómo puedo obtener una licencia temporal para Aspose.Note para Java?
Puede obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### 4. ¿Dónde puedo encontrar soporte adicional?
Para cualquier consulta o asistencia, visite el [foro de Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. ¿Hay una prueba gratuita disponible?
Sí, puede explorar una prueba gratuita [aquí](https://releases.aspose.com/).

**Preguntas y respuestas adicionales**

**Q: ¿Puedo personalizar el ícono de la etiqueta?**  
A: Sí – Aspose.Note proporciona muchos íconos predefinidos a través de `TagIcon` y también permite imágenes personalizadas.

**Q: ¿Cómo cambio la configuración de salida del PDF?**  
A: Use `PdfSaveOptions` para controlar la calidad de imagen, compresión y seguridad antes de llamar a `doc.save`.

**Q: ¿Es posible agregar múltiples etiquetas al mismo texto?**  
A: Absolutamente. Llame a `text.getTags().add()` varias veces con diferentes instancias de `NoteTag`.

---

**Última actualización:** 2026-01-28  
**Probado con:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
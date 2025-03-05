---
title: Agregar nuevo nodo de imagen con etiqueta en OneNote - Aspose.Note
linktitle: Agregar nuevo nodo de imagen con etiqueta en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Aprenda cómo agregar un nuevo nodo de imagen con una etiqueta en OneNote usando Aspose.Note para Java. Mejore sus habilidades de programación Java sin esfuerzo.
type: docs
weight: 10
url: /es/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## Introducción
En el ámbito de la programación Java, Aspose.Note se destaca como una poderosa herramienta para manejar documentos de OneNote con facilidad. Si busca mejorar sus habilidades y aprender cómo agregar un nuevo nodo de imagen con una etiqueta en OneNote usando Aspose.Note, ha venido al lugar correcto. Esta guía paso a paso lo guiará a través del proceso, asegurándose de que comprenda cada concepto a fondo.
## Requisitos previos
Antes de sumergirnos en el tutorial, asegurémonos de que tiene todo lo que necesita:
1.  Aspose.Note para Java: asegúrese de tener instalada la biblioteca Aspose.Note. Si no, puedes descargarlo.[aquí](https://releases.aspose.com/note/java/).
2. Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java funcional configurado en su máquina.
Ahora que tenemos los requisitos previos establecidos, pasemos a los siguientes pasos.
## Importar paquetes
En su proyecto Java, comience importando los paquetes necesarios:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Paso 1: crear un objeto de documento
```java
// La ruta al directorio de documentos.
String dataDir = "Your Document Directory";
// crear un objeto de la clase Documento
Document doc = new Document();
```
## Paso 2: inicializar el objeto de clase de página
```java
// inicializar objeto de clase de página
Page page = new Page();
```
## Paso 3: inicializar el objeto de clase de esquema
```java
// inicializar objeto de clase de esquema
Outline outline = new Outline();
```
## Paso 4: inicializar el objeto de clase OutlineElement
```java
// inicializar el objeto de clase OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Paso 5: cargar e insertar imagen
```java
// cargar una imagen
Image image = new Image(null, dataDir + "Input.jpg");
// insertar imagen en el nodo del documento
outlineElem.appendChildLast(image);
```
## Paso 6: agregar etiqueta de nota a la imagen
```java
// agregue una etiqueta de nota de estrella amarilla a la imagen
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Paso 7: Agregar nodo de elemento de esquema
```java
// agregar nodo de elemento de esquema
outline.appendChildLast(outlineElem);
```
## Paso 8: Agregar nodo de esquema
```java
// agregar nodo de esquema
page.appendChildLast(outline);
```
## Paso 9: Agregar nodo de página
```java
// agregar nodo de página
doc.appendChildLast(page);
```
## Paso 10: guarde el documento de OneNote
```java
// guardar el documento de OneNote como PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
¡Felicidades! Ha agregado con éxito un nuevo nodo de imagen con una etiqueta en OneNote usando Aspose.Note para Java.
## Conclusión
 Dominar Aspose.Note para Java abre posibilidades interesantes en la manipulación de documentos de OneNote. Al seguir este tutorial, habrá adquirido una habilidad práctica que se puede aplicar a varios proyectos. Sigue explorando la documentación de Aspose.Note[aquí](https://reference.aspose.com/note/java/)para funciones y posibilidades más avanzadas.
## Preguntas frecuentes
### ¿Dónde puedo encontrar la documentación de Aspose.Note?
 Puedes encontrar la documentación.[aquí](https://reference.aspose.com/note/java/).
### ¿Cómo descargo Aspose.Note para Java?
 Puedes descargarlo desde la página de lanzamientos.[aquí](https://releases.aspose.com/note/java/).
### ¿Hay una prueba gratuita disponible?
 Sí, puedes acceder a la prueba gratuita.[aquí](https://releases.aspose.com/).
### ¿Dónde puedo obtener soporte para Aspose.Note?
 Visita el foro de la comunidad[aquí](https://forum.aspose.com/c/note/28) para soporte.
### ¿Necesito una licencia temporal?
 Si es necesario, puede obtener una licencia temporal.[aquí](https://purchase.aspose.com/temporary-license/).
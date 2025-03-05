---
title: Crear tabla con columnas bloqueadas en OneNote - Aspose.Note
linktitle: Crear tabla con columnas bloqueadas en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Mejore su experiencia OneNote con Aspose.Note para Java. Aprenda a crear tablas con columnas bloqueadas usando una guía paso a paso. ¡Descarga tu prueba gratuita ahora!
type: docs
weight: 12
url: /es/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## Introducción
OneNote es una poderosa herramienta para organizar información y Aspose.Note para Java mejora sus capacidades al proporcionar una forma sencilla de crear tablas con columnas bloqueadas. En este tutorial, lo guiaremos a través del proceso de uso de Aspose.Note para Java para crear una tabla con columnas bloqueadas en OneNote.
## Requisitos previos
Antes de comenzar, asegúrese de cumplir con los siguientes requisitos previos:
- [Kit de desarrollo de Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)instalado en su máquina.
- [Aspose.Nota para Java](https://downloads.aspose.com/note/java) biblioteca descargada y agregada a su proyecto.
## Importar paquetes
En su proyecto Java, importe los paquetes necesarios para trabajar con Aspose. Nota:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Paso 1: configura tu proyecto
Comience creando un nuevo proyecto Java y agregando la biblioteca Aspose.Note a su classpath. Asegúrese de que su proyecto esté configurado para utilizar el JDK.
## Paso 2: inicializar documentos y objetos de página
```java
// La ruta al directorio de documentos.
String dataDir = "Your Document Directory";
//Crear un objeto de la clase Documento.
Document doc = new Document();
// Inicializar objeto de clase de página
Page page = new Page();
```
## Paso 3: crear filas y celdas de tabla
```java
// Inicializar el objeto de clase TableRow
TableRow row1 = new TableRow();
// Inicialice el objeto de clase TableCell y establezca el contenido del texto
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Inicializar el objeto de clase TableRow
TableRow row2 = new TableRow();
// Inicialice el objeto de clase TableCell y establezca el contenido del texto
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Paso 4: crea y personaliza la tabla
```java
// Inicializar objeto de clase de tabla
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Agregar filas
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Paso 5: agregar tabla al esquema y a la página
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Agregar nodo de tabla
outlineElem.appendChildLast(table);
// Agregar nodo de elemento de esquema
outline.appendChildLast(outlineElem);
// Agregar nodo de esquema
page.appendChildLast(outline);
// Agregar nodo de página
doc.appendChildLast(page);
```
## Paso 6: guarde el documento
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
¡Felicidades! Ha creado con éxito una tabla con columnas bloqueadas en OneNote usando Aspose.Note para Java.
## Conclusión
En este tutorial, exploramos el proceso de utilización de Aspose.Note para Java para mejorar su experiencia con OneNote mediante la creación de tablas con columnas bloqueadas. Esta funcionalidad agrega una nueva capa de organización y estructura a sus notas.
## Preguntas frecuentes
### ¿Aspose.Note para Java es compatible con todas las versiones de Java?
Sí, Aspose.Note para Java es compatible con Java 6 y versiones posteriores.
### ¿Puedo personalizar aún más la apariencia de la mesa?
¡Absolutamente! Aspose.Note para Java ofrece amplias opciones para personalizar tablas, como ajustar bordes, espaciado de celdas y más.
### ¿Hay una versión de prueba disponible antes de comprar?
 Sí tu puedes[descargar una prueba gratuita](https://releases.aspose.com/) para explorar las capacidades de Aspose.Note para Java.
### ¿Dónde puedo encontrar apoyo adicional o debates comunitarios?
 Visita el[Foro Aspose.Note](https://forum.aspose.com/c/note/28) para apoyo y debates comunitarios.
### ¿Cómo puedo obtener una licencia temporal de Aspose.Note para Java?
 Visita[este enlace](https://purchase.aspose.com/temporary-license/) obtener una licencia temporal para fines de prueba.
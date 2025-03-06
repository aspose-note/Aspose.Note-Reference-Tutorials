---
title: Crear lista con viñetas en OneNote - Aspose.Note
linktitle: Crear lista con viñetas en OneNote - Aspose.Note
second_title: Aspose.Nota Java API
description: Explore la guía paso a paso sobre cómo crear listas con viñetas en OneNote usando Aspose.Note para Java. Mejore la creación de sus documentos con facilidad.
weight: 12
url: /es/java/onenote-text-manipulation/create-bulleted-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear lista con viñetas en OneNote - Aspose.Note

## Introducción
En el panorama dinámico del desarrollo de Java, la creación de documentos atractivos y organizados es esencial. Aspose.Note para Java proporciona un potente conjunto de herramientas para mejorar el proceso de creación de documentos. Este tutorial lo guiará a través del proceso de creación de listas con viñetas en OneNote usando Aspose.Note para Java. Profundicemos en los detalles.
## Requisitos previos
Antes de comenzar, asegúrese de tener los siguientes requisitos previos:
- Conocimientos básicos de programación Java.
-  Aspose.Note para la biblioteca Java instalada. Puedes descargarlo desde el[Aspose.Note para la documentación de Java](https://reference.aspose.com/note/java/).
- Un entorno de desarrollo integrado (IDE) de Java configurado en su máquina.
## Importar paquetes
Comience importando los paquetes necesarios a su proyecto Java. Esto garantiza que tenga acceso a las funcionalidades de Aspose.Note para Java.
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Importar Aspose.Note para paquetes Java
```
## Paso 1: Inicializar documento y página
Cree un objeto de la clase Documento e inicialice un objeto de clase Página.
```java
String dataDir = "Your Document Directory";
// crear un objeto de la clase Documento
Document doc = new Document();
// inicializar objeto de clase de página
Page page = new Page();
```
## Paso 2: inicializar el esquema y el estilo de texto
Ahora, inicialice un objeto de clase Outline y un objeto de clase TextStyle con propiedades de formato.
```java
// inicializar objeto de clase de esquema
Outline outline = new Outline();
// inicializar el objeto de clase TextStyle y establecer propiedades de formato
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## Paso 3: crear elementos de lista con viñetas
Cree objetos de clase OutlineElement y aplique viñetas para crear una lista con viñetas.
```java
// inicializar objetos de clase OutlineElement y aplicar viñetas
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// inicializar el objeto de clase RichText y aplicar estilo de texto
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```
Repita los pasos anteriores para cada elemento de su lista con viñetas.
## Paso 4: agregar elementos de esquema al esquema
Agregue los objetos OutlineElement creados al Esquema.
```java
// agregar elementos de esquema
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Paso 5: agregue un esquema a la página y guárdelo
Agregue el nodo Esquema a la página y luego agregue el nodo Página al documento. Finalmente, guarde el documento.
```java
// agregar nodo de esquema
page.appendChildLast(outline);
// agregar nodo de página
doc.appendChildLast(page);
// guardar el documento
doc.save(dataDir + "CreateBulletedList_out.pdf");
```
¡Felicidades! Ha creado con éxito una lista con viñetas en OneNote utilizando Aspose.Note para Java.
## Conclusión
Aspose.Note para Java simplifica el proceso de creación de documentos bien formateados. Este tutorial lo guió a través de los pasos para crear una lista con viñetas en OneNote. Explore más posibilidades con Aspose.Note para mejorar su experiencia de creación de documentos.
## Preguntas frecuentes
### ¿Aspose.Note para Java es compatible con todos los IDE de Java?
Sí, Aspose.Note para Java es compatible con entornos de desarrollo integrados de Java populares como Eclipse e IntelliJ IDEA.
### ¿Puedo personalizar el formato de la lista con viñetas?
¡Absolutamente! Puede modificar la fuente, el color y el tamaño de los elementos de la lista con viñetas según sus preferencias.
### ¿Dónde puedo encontrar soporte adicional para Aspose.Note para Java?
 Visita el[Aspose.Note para el foro de soporte de Java](https://forum.aspose.com/c/note/28) para recibir ayuda de la comunidad.
### ¿Hay una prueba gratuita disponible para Aspose.Note para Java?
 Sí, puedes explorar una versión de prueba gratuita.[aquí](https://releases.aspose.com/).
### ¿Cómo puedo obtener una licencia temporal de Aspose.Note para Java?
 Obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

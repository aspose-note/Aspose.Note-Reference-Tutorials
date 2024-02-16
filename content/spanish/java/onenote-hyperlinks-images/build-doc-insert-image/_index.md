---
title: Cree un documento e inserte una imagen en OneNote usando Java
linktitle: Cree un documento e inserte una imagen en OneNote usando Java
second_title: Aspose.Nota Java API
description: Aprenda a crear documentos de OneNote e insertar imágenes usando Aspose.Note para Java. Tutorial paso a paso para una integración perfecta.
type: docs
weight: 12
url: /es/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## Introducción

En este tutorial, exploraremos cómo usar Aspose.Note para Java para crear documentos de OneNote e insertar imágenes en ellos. Aspose.Note es una potente API de Java que permite a los desarrolladores trabajar con archivos de Microsoft OneNote mediante programación. Desglosaremos cada paso en detalle para guiarlo a través del proceso.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

1. Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su sistema.
2.  Biblioteca Aspose.Note para Java: descargue e instale la biblioteca Aspose.Note para Java desde[sitio web](https://releases.aspose.com/note/java/).
3. IDE (entorno de desarrollo integrado): utilice cualquier IDE compatible con Java, como IntelliJ IDEA o Eclipse, para codificar.

## Importar paquetes

Comience importando los paquetes necesarios en su código Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Paso 1: configurar el documento

Primero, cree un nuevo documento de OneNote e inicialice los objetos necesarios:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Paso 2: inicializar el esquema

Configure el esquema del documento y especifique las propiedades de desplazamiento:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Paso 3: agregar imagen

Cargue una imagen y especifique su alineación:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Paso 4: agregar imagen al elemento de contorno

Adjunte la imagen a un elemento de contorno:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Paso 5: agregar nodos de página y esquema

Agregue los nodos de esquema y página al documento:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Paso 6: guardar el documento

Finalmente, guarde el documento de OneNote:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo crear documentos de OneNote e insertar imágenes en ellos usando Aspose.Note para Java. Si sigue estos pasos, podrá administrar y manipular de manera eficiente archivos OneNote en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.Note para Java?

 A1: Puedes acceder a la documentación[aquí](https://reference.aspose.com/note/java/).

### P2: ¿Cómo descargo Aspose.Note para Java?

 R2: Puede descargar Aspose.Note para Java desde el[pagina de descarga](https://releases.aspose.com/note/java/).

### P3: ¿Hay una prueba gratuita disponible para Aspose.Note para Java?

 R3: Sí, puede obtener una prueba gratuita del[sitio web](https://releases.aspose.com/).

### P4: ¿Dónde puedo obtener soporte para Aspose.Note para Java?

 R4: Para obtener ayuda, visite el[Foro Aspose.Note](https://forum.aspose.com/c/note/28).

### P5: ¿Puedo obtener una licencia temporal de Aspose.Note para Java?

 R5: Sí, puedes solicitar una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

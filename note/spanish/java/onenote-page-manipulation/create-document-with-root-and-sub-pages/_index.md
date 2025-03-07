---
title: Crear documento con páginas raíz y secundarias en OneNote
linktitle: Crear documento con páginas raíz y secundarias en OneNote
second_title: Aspose.Nota Java API
description: Cree un documento con páginas raíz y secundarias en OneNote usando Aspose.Note para Java. Siga la guía paso a paso para organizar sus notas de manera eficiente.
weight: 11
url: /es/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear documento con páginas raíz y secundarias en OneNote

## Introducción

En este tutorial, lo guiaremos a través del proceso de creación de un documento con páginas raíz y secundarias en OneNote usando Aspose.Note para Java. Si sigue estos pasos, podrá organizar eficientemente sus documentos de OneNote con una estructura jerárquica.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

1. Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su sistema.
2. Aspose.Note para Java: descargue e instale Aspose.Note para Java desde[sitio web](https://purchase.aspose.com/buy).
3. Entorno de desarrollo integrado (IDE): elija un IDE de Java como IntelliJ IDEA, Eclipse o NetBeans.

## Importar paquetes

Comience importando los paquetes necesarios en su proyecto Java:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Paso 1: configurar el directorio de documentos

Defina el directorio donde desea guardar su documento de OneNote:

```java
String dataDir = "Your Document Directory";
```

## Paso 2: crear un objeto de documento

 Crear una instancia de`Document` objeto:

```java
Document doc = new Document();
```

## Paso 3: crear páginas

Inicialice los objetos de la página y establezca sus niveles:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Paso 4: agregar nodos a las páginas

### Agregar nodos a la primera página

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Agregar nodos a la segunda página

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Agregar nodos a la tercera página

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Paso 5: agregar páginas al documento

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Paso 6: guarde el documento

Guarde el documento de OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Manejar excepción
}
```

¡Felicidades! Ha creado con éxito un documento con páginas raíz y secundarias en OneNote utilizando Aspose.Note para Java.

## Conclusión

Organizar sus documentos de OneNote con estructura jerárquica es esencial para una mejor gestión y navegación. Con Aspose.Note para Java, puede crear documentos de manera eficiente con páginas raíz y secundarias, proporcionando un diseño claro y organizado para sus notas.

## Preguntas frecuentes

### P1: ¿Puedo crear varios niveles de subpáginas usando Aspose.Note para Java?

R1: Sí, puede crear múltiples niveles de subpáginas configurando el nivel apropiado para cada página.

### P2: ¿Aspose.Note para Java es compatible con diferentes IDE de Java?

R2: Sí, Aspose.Note para Java es compatible con IDE de Java populares como IntelliJ IDEA, Eclipse y NetBeans.

### P3: ¿Puedo personalizar el formato del texto en mi documento de OneNote?

R3: Sí, puede personalizar la fuente, el color, el tamaño y otras opciones de formato utilizando Aspose.Note para las funciones de texto enriquecido de Java.

### P4: ¿Aspose.Note para Java admite guardar documentos en diferentes formatos?

R4: Sí, Aspose.Note para Java admite guardar documentos en varios formatos, incluidos BMP, PDF, PNG y más.

### P5: ¿Existe una versión de prueba disponible de Aspose.Note para Java?

R5: Sí, puede descargar una versión de prueba gratuita de Aspose.Note para Java desde el sitio web.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

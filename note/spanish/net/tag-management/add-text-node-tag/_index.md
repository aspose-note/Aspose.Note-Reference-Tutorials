---
title: Agregar nodo de texto con etiqueta en Aspose.Note
linktitle: Agregar nodo de texto con etiqueta en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda a agregar nodos de texto con etiquetas a documentos de OneNote usando Aspose.Note para .NET.
type: docs
weight: 12
url: /es/net/tag-management/add-text-node-tag/
---
## Introducción

Aspose.Note para .NET es una potente biblioteca que permite a los desarrolladores crear, manipular y convertir archivos de Microsoft OneNote mediante programación utilizando el marco .NET. En este tutorial, exploraremos cómo agregar un nodo de texto con una etiqueta a un documento de OneNote usando Aspose.Note para .NET.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

1. Visual Studio: asegúrese de tener Visual Studio instalado en su sistema.
2.  Aspose.Note para .NET: descargue e instale Aspose.Note para .NET desde[sitio web](https://releases.aspose.com/note/net/).
3. Conocimientos básicos de C#: familiarícese con los fundamentos del lenguaje de programación C#.

## Importar espacios de nombres

Primero, necesita importar los espacios de nombres necesarios para acceder a las clases y métodos necesarios para trabajar con Aspose.Note para .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Paso 1: crear un objeto de documento

Inicialice un objeto Documento para comenzar a trabajar con un documento de OneNote.

```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Paso 2: Inicializar objetos de página y esquema

Cree objetos Página y Esquema para estructurar el contenido del documento de OneNote.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Paso 3: agregar nodo de texto con etiqueta

Cree un objeto RichText con el texto y estilo deseados y luego agréguelo al OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Paso 4: Agregar elementos de esquema y nodos de página

Agregue OutlineElement al esquema y luego agregue el esquema a la página. Finalmente, agregue la página al documento.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Paso 5: guarde el documento

Guarde el documento de OneNote modificado en una ubicación especificada.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo agregar un nodo de texto con una etiqueta a un documento de OneNote usando Aspose.Note para .NET. Con este conocimiento, ahora puede personalizar y mejorar sus archivos de OneNote mediante programación.

## Preguntas frecuentes

### P1: ¿Puedo agregar varios nodos de texto con diferentes etiquetas en el mismo documento?

R1: Sí, puedes agregar varios nodos de texto con diferentes etiquetas siguiendo el mismo proceso para cada nodo.

### P2: ¿Aspose.Note para .NET es compatible con todas las versiones de OneNote?

R2: Aspose.Note para .NET admite varias versiones de OneNote, incluidas 2010, 2013, 2016 y superiores.

### P3: ¿Puedo personalizar los colores y estilos de las etiquetas?

R3: Sí, puede personalizar los colores y estilos de las etiquetas según sus requisitos.

### P4: ¿Aspose.Note para .NET admite el cifrado de documentos?

R4: Sí, Aspose.Note para .NET admite el cifrado de documentos para garantizar la seguridad de los datos.

### P5: ¿Dónde puedo encontrar más recursos y soporte para Aspose.Note para .NET?

 A5: Puedes explorar el[Aspose.Note para la documentación de .NET](https://reference.aspose.com/note/net/) buscar ayuda del[Foro Aspose.Note](https://forum.aspose.com/c/note/28).
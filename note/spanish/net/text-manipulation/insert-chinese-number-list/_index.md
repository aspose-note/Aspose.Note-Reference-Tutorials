---
title: Insertar lista de números chinos en el texto Aspose.Note
linktitle: Insertar lista de números chinos en el texto Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda a insertar listas de números chinos en Aspose.Note para documentos .NET sin esfuerzo. Mejore sus habilidades de formato de documentos con esta guía paso a paso.
weight: 20
url: /es/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Insertar lista de números chinos en el texto Aspose.Note

## Introducción
¿Está buscando mejorar sus habilidades en Aspose.Note para .NET incorporando listas de números chinos en sus documentos? Si es así, ¡estás en el lugar correcto! En este tutorial, lo guiaremos a través del proceso de insertar listas de números chinos usando Aspose.Note para .NET. Esta poderosa biblioteca le permite manipular documentos de OneNote sin problemas.
## Requisitos previos
Antes de sumergirnos en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:
- Conocimientos básicos de programación en C#.
-  Aspose.Note para .NET instalado. Puedes descargarlo[aquí](https://releases.aspose.com/note/net/).
## Importar espacios de nombres
Para comenzar, importe los espacios de nombres necesarios a su proyecto:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Paso 1: inicializar el documento de OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Paso 2: Inicializar la página OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Paso 3: aplicar la configuración de estilo de texto
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Paso 4: crear elementos de esquema
Ahora, creemos tres elementos de esquema con listas de números chinos:
### Paso 4.1: Primer Elemento
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Paso 4.2: Segundo Elemento
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Paso 4.3: Tercer Elemento
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Paso 5: agregar elementos al esquema
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Paso 6: agregar esquema a la página
```csharp
page.AppendChildLast(outline);
```
## Paso 7: agregar página al documento
```csharp
doc.AppendChildLast(page);
```
## Paso 8: guarde el documento de OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
¡Felicidades! Ha insertado con éxito listas de números chinos en su documento Aspose.Note utilizando la biblioteca .NET.
## Conclusión
En este tutorial, cubrimos el proceso paso a paso de incorporar listas de números chinos en sus documentos Aspose.Note para .NET. Mejore sus habilidades de formato de documentos y haga que su contenido sea más atractivo con estas técnicas.
## Preguntas frecuentes
### P: ¿Puedo personalizar el formato de las listas de números chinos?
 R: Sí, puede personalizar el formato ajustando los parámetros en el`NumberList` constructor.
### P: ¿Aspose.Note es compatible con la última versión de .NET?
R: Sí, Aspose.Note se actualiza periódicamente para admitir las últimas versiones de .NET.
### P: ¿Dónde puedo encontrar ejemplos y documentación adicionales?
R: Explore el completo[Documentación de Aspose.Note](https://reference.aspose.com/note/net/).
### P: ¿Cómo puedo obtener una licencia temporal para Aspose.Note?
 R: Obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).
### P: ¿Dónde puedo buscar ayuda o discutir consultas relacionadas con Aspose.Note?
 R: Visita el[Foro de soporte de Aspose.Note](https://forum.aspose.com/c/note/28) para el apoyo de la comunidad.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

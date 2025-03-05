---
title: Aplicar viñetas en texto en Aspose.Note
linktitle: Aplicar viñetas en texto en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda a aplicar viñetas en el texto en Aspose.Note para .NET para mejorar sus documentos de OneNote. Siga esta guía paso a paso para un formateo eficaz.
type: docs
weight: 10
url: /es/net/text-manipulation/apply-bullets-on-text/
---
## Introducción
Bienvenido a esta guía paso a paso sobre cómo aplicar viñetas a texto usando Aspose.Note para .NET. Aspose.Note es una potente biblioteca que permite a los desarrolladores trabajar sin problemas con archivos de Microsoft OneNote en sus aplicaciones .NET. En este tutorial, lo guiaremos a través del proceso de aplicar viñetas al texto, mejorando el atractivo visual de sus documentos de OneNote.
## Requisitos previos
Antes de sumergirnos en el tutorial, asegúrese de tener los siguientes requisitos previos:
- Conocimientos básicos de programación en C# y .NET.
-  Aspose.Note para la biblioteca .NET instalada. Puedes descargarlo[aquí](https://releases.aspose.com/note/net/).
## Importar espacios de nombres
En su código C#, asegúrese de incluir los espacios de nombres necesarios:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Paso 1: configure su documento
```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";
//Crear un objeto de la clase Documento.
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Paso 2: inicializar la página y el esquema
```csharp
// Inicializar objeto de clase de página
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializar objeto de clase de esquema
Outline outline = new Outline(doc);
```
## Paso 3: establecer el estilo de texto predeterminado
```csharp
// Inicialice el objeto de clase TextStyle y establezca las propiedades de formato
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Paso 4: crea elementos de esquema con viñetas
```csharp
// Inicializar objetos de clase OutlineElement y aplicar viñetas
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Repita para otros elementos del esquema.
```
## Paso 5: agregue elementos de esquema al esquema
```csharp
// Agregar elementos de esquema
outline.AppendChildLast(outlineElem1);
// Repita para otros elementos del esquema.
```
## Paso 6: agregue un esquema a la página
```csharp
// Agregar nodo de esquema
page.AppendChildLast(outline);
```
## Paso 7: agregar página al documento
```csharp
//Agregar nodo de página
doc.AppendChildLast(page);
```
## Paso 8: guarde el documento de OneNote
```csharp
// Guardar documento de OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Conclusión
¡Felicidades! Ha aprendido con éxito cómo aplicar viñetas al texto usando Aspose.Note para .NET. Esta característica puede mejorar significativamente el formato de sus documentos de OneNote, haciéndolos más atractivos visualmente.
## Preguntas frecuentes
### ¿Puedo aplicar diferentes estilos de viñetas a cada elemento de la lista?
 Sí, puede personalizar los estilos de viñeta modificando el`NumberList` propiedades para cada`OutlineElement`.
### ¿Aspose.Note es compatible con la última versión de Microsoft OneNote?
Aspose.Note admite varias versiones de Microsoft OneNote, lo que garantiza la compatibilidad con versiones anteriores y nuevas.
### ¿Puedo utilizar Aspose.Note con fines comerciales?
 Sí, puede utilizar Aspose.Note para .NET en proyectos comerciales. Para obtener una licencia, visite[aquí](https://purchase.aspose.com/buy).
### ¿Existe una versión de prueba disponible para Aspose.Note para .NET?
 Sí, puedes descargar una prueba gratuita.[aquí](https://releases.aspose.com/).
### ¿Dónde puedo encontrar apoyo y recursos adicionales?
 Puedes visitar el foro de la comunidad Aspose.Note[aquí](https://forum.aspose.com/c/note/28) para apoyo y discusiones.
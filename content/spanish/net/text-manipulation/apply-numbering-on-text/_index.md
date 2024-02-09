---
title: Aplicar numeración en texto en Aspose.Note
linktitle: Aplicar numeración en texto en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda cómo aplicar la numeración de texto en Aspose.Note para .NET con este completo tutorial. Mejore el formato de sus documentos sin esfuerzo.
type: docs
weight: 12
url: /es/net/text-manipulation/apply-numbering-on-text/
---
## Introducción
Aspose.Note para .NET proporciona potentes herramientas para la manipulación de documentos en aplicaciones C#. En este tutorial, exploraremos el proceso de aplicar numeración en texto usando Aspose.Note. Siga estas instrucciones paso a paso para mejorar el formato de su documento sin esfuerzo.
## Requisitos previos
Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:
- Conocimientos básicos del lenguaje de programación C#.
-  Aspose.Note para .NET instalado. Puedes descargarlo[aquí](https://releases.aspose.com/note/net/).
- Un entorno de desarrollo integrado (IDE) como Visual Studio.
## Importar espacios de nombres
Para comenzar, asegúrese de importar los espacios de nombres necesarios en su proyecto C#:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Paso 1: configure su documento
Comience creando un nuevo documento e inicializando los objetos requeridos:
```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";
// Crear un objeto de la clase Documento.
Document doc = new Document();
// Inicializar objeto de clase de página
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inicializar objeto de clase de esquema
Outline outline = new Outline(doc);
```
## Paso 2: definir el estilo predeterminado
Configure el estilo predeterminado para su texto usando la clase ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Paso 3: aplicar la numeración
Inicialice los objetos de la clase OutlineElement y aplique numeración a cada elemento:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Paso 4: agregar elementos de esquema
Agregue los elementos del esquema al esquema:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Paso 5: guarde el documento
Guarde el documento de OneNote con la numeración aplicada:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Conclusión
¡Felicidades! Ha aprendido con éxito cómo aplicar numeración en texto en Aspose.Note para .NET. Experimente con diferentes opciones de formato para crear documentos visualmente atractivos sin esfuerzo.
## Preguntas frecuentes
### 1. ¿Puedo personalizar el formato de numeración?
Sí, la clase NumberList te permite personalizar el formato de numeración según tus preferencias.
### 2. ¿Hay otras opciones de formato disponibles?
Aspose.Note proporciona una amplia gama de opciones de formato, incluido el estilo de fuente, el color y más.
### 3. ¿Aspose.Note es compatible con Visual Studio?
¡Absolutamente! Aspose.Note se integra perfectamente con Visual Studio para una experiencia de desarrollo fluida.
### 4. ¿Puedo probar Aspose.Note antes de comprarlo?
 ¡Ciertamente! Puedes explorar una prueba gratuita[aquí](https://releases.aspose.com/).
### 5. ¿Dónde puedo obtener soporte para Aspose.Note?
 Para cualquier ayuda o consulta, visite el[Foro Aspose.Note](https://forum.aspose.com/c/note/28).
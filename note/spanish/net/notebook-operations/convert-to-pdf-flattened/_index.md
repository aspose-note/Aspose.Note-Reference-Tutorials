---
title: Convierta cuadernos a PDF (aplanados) en Aspose Note .NET
linktitle: Convierta cuadernos a PDF (aplanados) en Aspose Note .NET
second_title: Aspose.Nota .NET API
description: Aprenda a convertir cuadernos de OneNote en archivos PDF acoplados sin esfuerzo utilizando Aspose.Note para .NET. Conserve su contenido sin problemas.
weight: 15
url: /es/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convierta cuadernos a PDF (aplanados) en Aspose Note .NET

## Introducción

¿Está buscando convertir sus cuadernos OneNote en archivos PDF acoplados usando Aspose Note .NET? ¡Estás en el lugar correcto! En este tutorial, recorreremos el proceso paso a paso.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1.  Aspose.Note para .NET: asegúrese de haber descargado e instalado Aspose.Note para .NET. Si no, puedes conseguirlo en[aquí](https://releases.aspose.com/note/net/).
2. Visual Studio: necesitará Visual Studio instalado en su sistema para codificar y compilar.
3. OneNote Notebook: tenga listo un OneNote Notebook que desee convertir a PDF.

## Importar espacios de nombres

Comencemos importando los espacios de nombres necesarios en su código C#:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Paso 1: cargue el cuaderno OneNote

```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";

// Cargar una libreta de OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 En este paso, cargamos OneNote Notebook usando el`Notebook` clase proporcionada por Aspose.Note.

## Paso 2: Convertir a PDF con Acoplamiento

```csharp
// Guarde el cuaderno como PDF con aplanamiento
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Aquí, guardamos el cuaderno cargado como PDF con el`Flatten` propiedad establecida en`true`. Esta propiedad aplana todo el contenido, incluidas las anotaciones y las imágenes, en el PDF.

## Paso 3: Imprimir mensaje de éxito

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Finalmente imprimimos un mensaje de éxito junto con la ruta donde se guarda el PDF.

## Conclusión

¡Felicidades! Ha convertido con éxito su OneNote Notebook a un PDF acoplado usando Aspose.Note para .NET. Este proceso garantiza que todo su contenido se conserve con precisión en formato PDF, lo que facilita compartirlo y distribuirlo.

## Preguntas frecuentes

### P1: ¿Puedo conservar elementos interactivos en el PDF?

R1: Aspose.Note aplana el contenido, incluidos elementos interactivos como casillas de verificación o campos de formulario, en el PDF, volviéndolos estáticos.

### P2: ¿Aspose.Note admite la conversión de cuadernos a otros formatos?

R2: Sí, Aspose.Note admite la conversión de cuadernos a varios formatos, como PDF, HTML, imágenes y más.

### P3: ¿Puedo personalizar las opciones de conversión?

R3: ¡Absolutamente! Aspose.Note ofrece amplias opciones de personalización durante el proceso de conversión, lo que le permite adaptar el resultado a sus necesidades.

### P4: ¿Hay una versión de prueba disponible?

 R4: Sí, puede obtener una prueba gratuita de Aspose.Note de[aquí](https://releases.aspose.com/).

### P5: ¿Dónde puedo obtener asistencia si tengo algún problema?

 R5: Puede buscar apoyo de la comunidad Aspose en[Foros de Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

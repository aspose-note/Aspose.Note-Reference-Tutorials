---
title: Guardar en PDF en Aspose.Note
linktitle: Guardar en PDF en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda cómo guardar documentos de Microsoft OneNote en formato PDF usando Aspose.Note para .NET. Tutorial paso a paso con ejemplos de código para diseños de página Carta y A4.
type: docs
weight: 26
url: /es/net/loading-and-saving-operations/save-to-pdf/
---
## Introducción

En este tutorial, exploraremos cómo guardar documentos en formato PDF usando Aspose.Note para .NET. Aspose.Note es una potente biblioteca que permite a los desarrolladores trabajar con archivos de Microsoft OneNote mediante programación. Cubriremos los requisitos previos, importaremos espacios de nombres y proporcionaremos guías paso a paso para guardar documentos en PDF en varios diseños de página.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

- Visual Studio instalado en su sistema.
-  Aspose.Note para la biblioteca .NET descargada e instalada. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/net/).
- Conocimientos básicos del lenguaje de programación C#.

## Importar espacios de nombres

Primero, importemos los espacios de nombres necesarios a nuestro código C#:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Ahora que hemos cubierto los requisitos previos y los espacios de nombres importados, procedamos a guardar documentos en PDF en diferentes diseños de página.

## Paso 1: guarde en PDF usando la configuración de página Carta


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // La ruta al directorio de documentos.
    string dataDir = "Your Document Directory";

    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //Guarde el documento.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explicación:

- Cargamos el documento de OneNote en Aspose.Note.
- Defina la ruta de destino para el archivo PDF guardado.
-  Guarde el documento en PDF usando`PdfSaveOptions` con`PageSettings` ajustado a`Letter`.

## Paso 2: guarde en PDF usando la configuración de página A4 sin límite de altura

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // La ruta al directorio de documentos.
    string dataDir = "Your Document Directory";

    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //Guarde el documento.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explicación:

- De manera similar al paso anterior, cargamos el documento de OneNote en Aspose.Note.
- Defina la ruta de destino para el archivo PDF guardado.
-  Guarde el documento en PDF usando`PdfSaveOptions` con`PageSettings` ajustado a`A4NoHeightLimit`.

## Conclusión

En este tutorial, aprendimos cómo guardar documentos en formato PDF usando Aspose.Note para .NET. Cubrimos dos diseños de página diferentes: Carta y A4 sin límite de altura. Con Aspose.Note, los desarrolladores pueden manipular fácilmente archivos OneNote mediante programación, proporcionando flexibilidad y eficiencia en las tareas de gestión de documentos.

## Preguntas frecuentes

### P1: ¿Puede Aspose.Note manejar archivos complejos de OneNote?

R1: Sí, Aspose.Note admite varias características y funcionalidades para manejar archivos complejos de OneNote de manera efectiva.

### P2: ¿Aspose.Note es adecuado para proyectos comerciales?

 R2: Por supuesto, Aspose.Note se puede utilizar en proyectos comerciales con facilidad. Puedes comprar una licencia[aquí](https://purchase.aspose.com/buy).

### P3: ¿Aspose.Note ofrece una prueba gratuita?

 R3: Sí, puedes explorar Aspose.Note con una prueba gratuita disponible[aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo encontrar documentación para Aspose.Note?

 A4: Puede encontrar documentación detallada[aquí](https://reference.aspose.com/note/net/).

### P5: ¿Necesita más ayuda?

 R5: No dude en hacer cualquier pregunta o buscar ayuda en el foro Aspose.Note[aquí](https://forum.aspose.com/c/note/28).
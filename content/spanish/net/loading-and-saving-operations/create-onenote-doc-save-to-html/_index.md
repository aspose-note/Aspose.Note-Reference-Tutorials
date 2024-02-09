---
title: Cree un documento de OneNote y guárdelo en HTML en Aspose.Note
linktitle: Cree un documento de OneNote y guárdelo en HTML en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda a crear y guardar documentos de Microsoft OneNote en formato HTML en aplicaciones .NET utilizando la API Aspose.Note. Siga nuestro completo tutorial con ejemplos paso a paso.
type: docs
weight: 14
url: /es/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Introducción

Aspose.Note para .NET es una potente API que permite a los desarrolladores trabajar con documentos de Microsoft OneNote mediante programación en sus aplicaciones .NET. Con Aspose.Note, puedes crear, manipular y convertir archivos de OneNote sin esfuerzo. En este tutorial, exploraremos cómo crear un documento de OneNote y guardarlo en formato HTML utilizando varias opciones proporcionadas por Aspose.Note para .NET API.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

- Conocimientos básicos del lenguaje de programación C#.
- Visual Studio instalado en su sistema.
-  Aspose.Note para la API .NET instalada en su proyecto. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/net/).
- Familiaridad con la estructura de los documentos de Microsoft OneNote.

## Importar espacios de nombres

Antes de sumergirnos en la parte de codificación, importemos los espacios de nombres necesarios:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Ahora, dividamos cada ejemplo en varios pasos y veamos cómo crear un documento de OneNote y guardarlo en formato HTML usando Aspose.Note para .NET.

## Paso 1: crear un documento de OneNote con opciones predeterminadas

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Inicializar documento de OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Estilo predeterminado para todo el texto del documento.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Guardar en formato HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

En este paso, inicializamos un nuevo documento de OneNote, agregamos una página con un título y la guardamos en formato HTML usando las opciones predeterminadas.

## Paso 2: cree y guarde un rango de páginas específico en HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Inicializar documento de OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Estilo predeterminado para todo el texto del documento.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Guardar en formato HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Aquí, demostramos cómo crear un documento y guardar un rango de páginas específico en formato HTML.

## Paso 3: guarde como HTML en Memory Stream con recursos integrados

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Cargue el documento de OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Especificar opciones de guardado de HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Guarde el documento en una secuencia de memoria
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Este paso ilustra cómo guardar un documento de OneNote en formato HTML con recursos integrados (CSS, fuentes e imágenes) en una secuencia de memoria.

## Paso 4: guardar como HTML en un archivo con recursos en archivos separados

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Cargue el documento de OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Especificar opciones de guardado de HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Guarde el documento en un archivo HTML con recursos almacenados en archivos separados
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

En este paso, guardamos un documento de OneNote en formato HTML con todos los recursos (CSS, fuentes e imágenes) almacenados en archivos separados.

## Paso 5: guarde como HTML en Memory Stream con devoluciones de llamada para ahorrar recursos

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Especificar la configuración para guardar devoluciones de llamadas
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Especificar opciones de guardado de HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Cargue el documento de OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Guarde el documento en formato HTML con recursos administrados por devoluciones de llamada definidas por el usuario.
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Agregar datos manualmente a la secuencia CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Aquí, demostramos cómo guardar un documento de OneNote en formato HTML con recursos administrados por devoluciones de llamada definidas por el usuario.

## Conclusión

En este artículo, exploramos cómo trabajar con documentos de OneNote y guardarlos en formato HTML usando Aspose.Note para .NET. Siguiendo la guía paso a paso, podrás fácilmente

 Integre esta funcionalidad en sus aplicaciones .NET, lo que le permitirá manipular archivos OneNote de manera eficiente.

## Preguntas frecuentes

### P1: ¿Puedo personalizar la apariencia del archivo HTML guardado?

R1: Sí, puedes personalizar la apariencia modificando las hojas de estilo CSS generadas durante el proceso de conversión.

### P2: ¿Aspose.Note admite la conversión a otros formatos además de HTML?

R2: Sí, Aspose.Note admite la conversión a varios formatos, como PDF, imágenes y documentos de Microsoft Word.

### P3: ¿Aspose.Note es compatible con aplicaciones .NET Core?

R3: Sí, Aspose.Note es compatible con aplicaciones .NET Framework y .NET Core.

### P4: ¿Puedo extraer texto e imágenes de documentos de OneNote usando Aspose.Note?

R4: Sí, puede extraer texto e imágenes, así como realizar otras manipulaciones utilizando la API Aspose.Note.

### P5: ¿Existe una versión de prueba disponible para probar las funciones de Aspose.Note?

 R5: Sí, puedes descargar una versión de prueba gratuita desde[aquí](https://releases.aspose.com/).
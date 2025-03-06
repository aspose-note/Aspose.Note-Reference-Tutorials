---
title: Guardar usando fuentes especificadas en Aspose.Note
linktitle: Guardar usando fuentes especificadas en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda cómo guardar documentos con fuentes específicas en Aspose.Note para .NET. Personalice la configuración de fuente fácilmente para lograr un formato de documento consistente.
weight: 28
url: /es/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar usando fuentes especificadas en Aspose.Note

## Introducción

En este tutorial, aprenderemos cómo guardar documentos usando fuentes específicas en Aspose.Note para .NET. Exploraremos diferentes métodos para lograrlo, paso a paso.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1.  Aspose.Note para .NET: asegúrese de haber instalado Aspose.Note para .NET. Puedes descargarlo desde[aquí](https://releases.aspose.com/note/net/).

2. Entorno de desarrollo: necesita un entorno de desarrollo configurado para el desarrollo .NET.

## Importar espacios de nombres

Primero, importemos los espacios de nombres necesarios:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Paso 1: guardar con el nombre de fuente predeterminado

En este paso, guardaremos un documento usando un nombre de fuente predeterminado especificado.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // La ruta al directorio de documentos.
    string dataDir = "Your Document Directory";

    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Guarde el documento como PDF con la fuente predeterminada especificada.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Paso 2: guardar con la fuente predeterminada del archivo

A continuación, guardemos un documento usando una fuente predeterminada cargada desde un archivo.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // La ruta al directorio de documentos.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Guarde el documento como PDF con la fuente predeterminada cargada desde el archivo.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Paso 3: guardar con la fuente predeterminada de Stream

Por último, guardemos un documento usando una fuente predeterminada cargada desde una secuencia.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // La ruta al directorio de documentos.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Guarde el documento como PDF con la fuente predeterminada cargada desde la secuencia.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Conclusión

En este tutorial, exploramos cómo guardar documentos usando fuentes específicas en Aspose.Note para .NET. Si sigue estos pasos, puede personalizar la configuración de fuente según sus requisitos, asegurándose de que sus documentos tengan el formato deseado.

## Preguntas frecuentes

### P1: ¿Puedo usar cualquier fuente para guardar documentos en Aspose.Note?

R1: Sí, puede especificar cualquier fuente para guardar documentos. Solo asegúrese de que el archivo de fuente sea accesible y esté cargado correctamente.

### P2: ¿Aspose.Note es compatible con diferentes formatos de documentos?

R2: Aspose.Note funciona principalmente con documentos de OneNote, pero ofrece opciones para guardar en varios formatos, incluido PDF.

### P3: ¿Cómo puedo manejar las fuentes que faltan al guardar documentos?

R3: Aspose.Note ofrece opciones para usar fuentes predeterminadas en caso de que falte la fuente especificada, lo que garantiza un formato de documento coherente.

### P4: ¿Aspose.Note admite la incrustación de fuentes en los documentos de salida?

R4: Sí, Aspose.Note permite incrustar fuentes para garantizar la portabilidad del documento y una representación consistente en diferentes plataformas.

### P5: ¿Dónde puedo obtener más ayuda con Aspose.Note?

 R5: Para obtener más ayuda o soporte técnico, puede visitar el[Foro Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

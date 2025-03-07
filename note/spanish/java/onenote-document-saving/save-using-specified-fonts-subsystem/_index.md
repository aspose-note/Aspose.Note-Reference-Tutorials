---
title: Guardar usando el subsistema de fuentes especificadas en OneNote
linktitle: Guardar usando el subsistema de fuentes especificadas en OneNote
second_title: Aspose.Nota Java API
description: Aprenda a guardar documentos de OneNote utilizando el subsistema de fuentes especificado en Java con Aspose.Note. Garantice una representación de fuentes coherente en todas las plataformas sin esfuerzo.
weight: 22
url: /es/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar usando el subsistema de fuentes especificadas en OneNote

## Introducción

Aspose.Note para Java proporciona capacidades sólidas para trabajar con documentos de OneNote. Un requisito común al trabajar con este tipo de documentos es garantizar que las fuentes se mantengan correctamente, especialmente si el documento se va a exportar o guardar en diferentes formatos como PDF. Este tutorial lo guiará a través del proceso de guardar documentos de OneNote mientras especifica el subsistema de fuentes, lo que garantiza una representación consistente y precisa del texto en varias plataformas.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de tener configurados los siguientes requisitos previos:

### 1. Kit de desarrollo de Java (JDK)

 Asegúrese de tener instalado el kit de desarrollo de Java (JDK) en su sistema. Puedes descargarlo desde[aquí](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) si aún no lo has hecho.

### 2. Aspose.Note para la biblioteca Java

 Descargue y configure la biblioteca Aspose.Note para Java. Puedes descargarlo desde el[sitio web](https://releases.aspose.com/note/java/).

## Importar paquetes

Asegúrese de importar los paquetes necesarios en su proyecto Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Ahora dividamos cada ejemplo en varios pasos para comprender mejor el proceso.

## Paso 1: Guardar usando el subsistema de fuentes de documentos con el nombre de fuente predeterminado

Este paso demuestra cómo guardar un documento en formato PDF utilizando un nombre de fuente predeterminado especificado.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Especifique la fuente predeterminada.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Guarde el documento como PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

En este paso:
- El documento de OneNote se carga usando Aspose.Note.
- La fuente predeterminada se especifica como "Times New Roman".
- El documento se guarda en formato PDF con la fuente especificada.

## Paso 2: Guardar usando el subsistema de fuentes de documentos con la fuente predeterminada del archivo

Este paso demuestra cómo guardar un documento en formato PDF usando una fuente predeterminada cargada desde un archivo.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Especifique la ruta al archivo de fuente.
    String fontFile = "geo_1.ttf";

    // Especifique la fuente predeterminada del archivo.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Guarde el documento como PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

En este paso:
- Se carga el archivo de fuente "geo_1.ttf".
- La fuente predeterminada se especifica desde el archivo de fuente cargado.
- El documento se guarda en formato PDF con la fuente especificada.

## Paso 3: Guardar usando el subsistema de fuentes de documentos con la fuente predeterminada de Stream

Este paso demuestra cómo guardar un documento en formato PDF usando una fuente predeterminada cargada desde una secuencia.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Cargue el documento en Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Especifique la ruta al archivo de fuente.
    String fontFile = "geo_1.ttf";

    // Cargue el archivo de fuente como una secuencia.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Especifique la fuente predeterminada de la secuencia.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Guarde el documento como PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

En este paso:
- El archivo de fuente "geo_1.ttf" se carga como una secuencia.
- La fuente predeterminada se especifica a partir de la secuencia cargada.
- El documento se guarda en formato PDF con la fuente especificada.

## Conclusión

En este tutorial, aprendimos cómo guardar documentos de OneNote utilizando el subsistema de fuentes especificado en Java usando Aspose.Note. Si sigue estos pasos, podrá garantizar una representación de fuentes coherente en varias plataformas al exportar o guardar sus documentos.

## Preguntas frecuentes

### P1: ¿Puedo especificar diferentes fuentes para diferentes partes del documento?

R1: Sí, puede especificar diferentes fuentes para diferentes partes del documento usando Aspose.Note para Java.

### P2: ¿Aspose.Note es compatible con todas las versiones de OneNote?

R2: Aspose.Note admite varias versiones de OneNote, lo que garantiza la compatibilidad en diferentes entornos.

### P3: ¿Cómo puedo manejar las fuentes que faltan al guardar documentos?

R3: Aspose.Note proporciona opciones para especificar fuentes predeterminadas para manejar las fuentes faltantes de manera efectiva al guardar el documento.

### P4: ¿Puedo personalizar las propiedades de la fuente, como el tamaño y el estilo?

R4: Sí, puede personalizar las propiedades de la fuente, como el tamaño, el estilo y el color, utilizando Aspose.Note para Java.

### P5: ¿Existe una versión de prueba disponible de Aspose.Note para Java?

R5: Sí, puede obtener una prueba gratuita de Aspose.Note para Java desde el sitio web.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

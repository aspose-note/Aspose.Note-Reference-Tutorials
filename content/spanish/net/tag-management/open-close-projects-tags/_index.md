---
title: Abrir y cerrar proyectos con etiquetas en Aspose.Note
linktitle: Abrir y cerrar proyectos con etiquetas en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda a manipular archivos de Microsoft OneNote mediante programación utilizando Aspose.Note para .NET. Abra y cierre proyectos con etiquetas de manera eficiente.
type: docs
weight: 15
url: /es/net/tag-management/open-close-projects-tags/
---
## Introducción

En este tutorial, aprenderemos cómo usar Aspose.Note para .NET para abrir y cerrar proyectos con etiquetas. Aspose.Note es una potente API que permite a los desarrolladores trabajar con archivos de Microsoft OneNote mediante programación, permitiendo tareas como manipular texto, imágenes y etiquetas dentro de los documentos.

## Requisitos previos

Antes de comenzar, asegúrese de tener configurados los siguientes requisitos previos:

## Importar espacios de nombres

```csharp
using System.IO;
using System.Linq;
```

Ahora dividamos cada ejemplo en varios pasos:

## Paso 1: cargue el documento

Primero, necesitamos cargar el documento en Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Paso 2: cerrar los elementos del proyecto C

Ahora, cerremos todas las casillas de verificación relacionadas con el 'Proyecto C'.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Paso 3: guarde las notas del proyecto C cerrado

Guarde el documento modificado con los elementos cerrados del 'Proyecto C'.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Paso 4: abra los elementos del proyecto C

A continuación, abramos todos los elementos de las casillas de verificación relacionados con el 'Proyecto C'.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Paso 5: guarde las notas del proyecto abierto C

Guarde el documento modificado con los elementos abiertos del 'Proyecto C'.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Ahora ha aprendido cómo abrir y cerrar proyectos con etiquetas en Aspose.Note usando .NET.

## Conclusión

Aspose.Note para .NET proporciona una manera conveniente de manipular documentos de OneNote mediante programación. Siguiendo este tutorial, podrá administrar eficientemente sus proyectos abriendo y cerrando elementos usando etiquetas.

## Preguntas frecuentes

### P1: ¿Aspose.Note es compatible con todas las versiones de OneNote?

R1: Aspose.Note es compatible con Microsoft OneNote 2010 y versiones más recientes.

### P2: ¿Puedo utilizar Aspose.Note para proyectos comerciales?

 R2: Sí, puedes utilizar Aspose.Note tanto para proyectos personales como comerciales. Visita[aquí](https://purchase.aspose.com/buy) para comprar una licencia.

### P3: ¿Aspose.Note ofrece una prueba gratuita?

R3: Sí, puedes obtener una prueba gratuita[aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo encontrar documentación para Aspose.Note?

 A4: Puedes encontrar la documentación.[aquí](https://reference.aspose.com/note/net/).

### P5: ¿Dónde puedo obtener soporte para Aspose.Note?

R5: Para obtener ayuda, puede visitar Aspose.Note[foro](https://forum.aspose.com/c/note/28).
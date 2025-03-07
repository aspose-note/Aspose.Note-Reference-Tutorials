---
title: Convierta cuadernos en imágenes (aplanadas) en Aspose Note .NET
linktitle: Convierta cuadernos en imágenes (aplanadas) en Aspose Note .NET
second_title: Aspose.Nota .NET API
description: Aprenda cómo convertir cuadernos de OneNote en imágenes aplanadas usando Aspose.Note para .NET. Guía paso a paso para una integración perfecta.
weight: 12
url: /es/net/notebook-operations/convert-to-image-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convierta cuadernos en imágenes (aplanadas) en Aspose Note .NET

## Introducción

En este tutorial, aprenderemos cómo usar Aspose.Note para .NET para convertir cuadernos en imágenes aplanadas. Dividiremos el proceso en pasos simples para ayudarlo a comprenderlo e implementarlo de manera efectiva.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

1.  Aspose.Note para .NET: si aún no lo ha hecho, descargue e instale Aspose.Note para .NET desde[aquí](https://releases.aspose.com/note/net/).
2. Entorno de desarrollo: asegúrese de tener un entorno de desarrollo adecuado configurado para el desarrollo .NET.
3. OneNote Notebook: prepare el cuaderno de OneNote que desea convertir en una imagen.

## Importar espacios de nombres

Antes de comenzar con el proceso de conversión, debes importar los espacios de nombres necesarios en tu código:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Ahora, profundicemos en la guía paso a paso para convertir cuadernos en imágenes aplanadas usando Aspose.Note para .NET.

## Paso 1: cargue la computadora portátil

Primero, cargue el cuaderno de OneNote que desea convertir en su aplicación.

```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";

// Cargar una libreta de OneNote
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Paso 2: configurar las opciones de guardar

Defina las opciones de guardado para el cuaderno, incluido el formato y la resolución de la imagen.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## Paso 3: guarde el cuaderno como imagen

Ahora, guarde el cuaderno como una imagen aplanada usando las opciones de guardado definidas.

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// Guarde el cuaderno
notebook.Save(dataDir, notebookSaveOptions);
```

## Conclusión

En este tutorial, aprendimos cómo convertir cuadernos en imágenes aplanadas usando Aspose.Note para .NET. Si sigue la guía paso a paso, podrá integrar perfectamente esta funcionalidad en sus aplicaciones .NET.

## Preguntas frecuentes

### P1: ¿Puede Aspose.Note para .NET manejar cuadernos complejos?

R1: Sí, Aspose.Note para .NET es capaz de manejar cuadernos complejos de manera eficiente.

### P2: ¿Hay una prueba gratuita disponible para Aspose.Note para .NET?

 R2: Sí, puedes descargar una prueba gratuita desde[aquí](https://releases.aspose.com/).

### P3: ¿Aspose brinda soporte para sus productos?

 R3: Sí, puedes obtener soporte de la comunidad Aspose[aquí](https://forum.aspose.com/c/note/28).

### P4: ¿Puedo comprar una licencia temporal de Aspose.Note para .NET?

 R4: Sí, puedes comprar una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo encontrar documentación para Aspose.Note para .NET?

 A5: Puedes encontrar la documentación.[aquí](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

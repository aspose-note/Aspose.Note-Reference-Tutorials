---
title: Agregar nodo de tabla con etiqueta en Aspose.Note
linktitle: Agregar nodo de tabla con etiqueta en Aspose.Note
second_title: Aspose.Nota .NET API
description: Aprenda a agregar tablas con etiquetas en Aspose.Note para .NET. Mejore sus habilidades de manipulación de documentos mediante programación.
type: docs
weight: 11
url: /es/net/tag-management/add-table-node-tag/
---
## Introducción

En este tutorial, lo guiaremos a través del proceso de agregar un nodo de tabla con una etiqueta usando Aspose.Note para .NET. Siga los pasos a continuación para lograrlo.

## Importar espacios de nombres

Antes de comenzar, asegúrese de importar los espacios de nombres necesarios para trabajar con Aspose. Nota:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Requisitos previos

Asegúrese de tener configurados los siguientes requisitos previos antes de continuar:

1.  Instalación: descargue e instale la biblioteca Aspose.Note para .NET desde[aquí](https://releases.aspose.com/note/net/).
2.  Licencia: Adquiera una licencia o utilice una[licencia temporal](https://purchase.aspose.com/temporary-license/) para utilizar la biblioteca.
3. Entorno de desarrollo: tenga configurado un entorno de desarrollo compatible, como Visual Studio.

## Paso 1: inicializar documentos y objetos de página

 Comience creando una instancia de`Document` clase e inicializando un`Page` objeto:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Paso 2: crear objetos de tabla, fila y celda

 Inicializar el`Table`, `TableRow` , y`TableCell` objetos:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Paso 3: insertar contenido en la celda

 Agregue contenido a la celda usando el`AppendChildLast` método:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Paso 4: Inicializar el nodo de la tabla

 Inicializar el`Table` objeto con propiedades especificadas:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Paso 5: agregar fila a la tabla

Agregue el nodo de fila a la tabla:

```csharp
table.AppendChildLast(row);
```

## Paso 6: agregar etiqueta al nodo de la tabla

Incluya una etiqueta para el nodo de la tabla:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Paso 7: agregar el nodo de tabla al elemento de esquema

 Crear un`Outline` y`OutlineElement` para agregar el nodo de la tabla:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Paso 8: guardar el documento

Guarde el documento de OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Después de seguir estos pasos, debería haber agregado exitosamente un nodo de tabla con una etiqueta usando Aspose.Note para .NET.

## Conclusión

En este tutorial, cubrimos el proceso de agregar un nodo de tabla con una etiqueta en Aspose.Note para .NET. Si sigue estos pasos, podrá manipular de manera eficiente los documentos de OneNote mediante programación, mejorando sus capacidades de administración de documentos.

## Preguntas frecuentes

### P1: ¿Aspose.Note es compatible con todas las versiones de .NET?

R1: Aspose.Note para .NET admite las versiones 2.0 y superiores de .NET Framework, incluidos .NET Core y .NET Standard.

### P2: ¿Puedo probar Aspose.Note antes de comprar una licencia?

 R2: Sí, puede obtener una prueba gratuita de Aspose.Note desde[aquí](https://releases.aspose.com/).

### P3: ¿Cómo adquiero una licencia temporal para Aspose.Note?

 R3: Puede obtener una licencia temporal de[este enlace](https://purchase.aspose.com/temporary-license/), que tiene una validez de 30 días.

### P4: ¿Aspose.Note admite el cifrado de documentos?

R4: Sí, Aspose.Note brinda soporte para cifrar documentos de OneNote para garantizar la seguridad de los datos.

### P5: ¿Hay soporte técnico disponible para los usuarios de Aspose.Note?

 R5: Sí, el soporte técnico se proporciona a través de los foros de Aspose[aquí](https://forum.aspose.com/c/note/28), donde podrá buscar ayuda de expertos.
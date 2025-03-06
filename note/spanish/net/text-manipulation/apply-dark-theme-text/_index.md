---
title: Transformación de tema oscuro con Aspose.Note para .NET
linktitle: Aplicar tema oscuro al texto en Aspose.Note
second_title: Aspose.Nota .NET API
description: ¡Transforme sus documentos OneNote con Aspose.Note para .NET! Aplica un elegante tema oscuro sin esfuerzo. Descárguelo ahora y mejore su experiencia para tomar notas.
weight: 11
url: /es/net/text-manipulation/apply-dark-theme-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Transformación de tema oscuro con Aspose.Note para .NET

## Introducción
Bienvenido a nuestra guía paso a paso sobre cómo aplicar un tema oscuro al texto en Aspose.Note para .NET. Aspose.Note es una potente API .NET que permite a los desarrolladores trabajar con archivos de Microsoft OneNote mediante programación. En este tutorial, exploraremos cómo darle a sus documentos de OneNote un aspecto elegante y moderno aplicando un tema oscuro al texto.
## Requisitos previos
Antes de sumergirnos en el tutorial, asegúrese de tener implementados los siguientes requisitos previos:
-  Aspose.Note para .NET: asegúrese de tener instalado Aspose.Note para .NET. Si no, puedes descargarlo desde[Documentación de Aspose.Note](https://reference.aspose.com/note/net/).
- Entorno de desarrollo: configure su entorno de desarrollo .NET preferido, como Visual Studio.
- Directorio de documentos: prepare el directorio donde se encuentra su documento de OneNote.
## Importar espacios de nombres
En su proyecto .NET, importe los espacios de nombres necesarios para trabajar con Aspose. Nota:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Paso 1: cargue el documento de OneNote
Cargue su documento de OneNote en Aspose.Note usando el siguiente código:
```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";
// Cargue el documento en Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Paso 2: establecer el color de fondo
Establezca el color de fondo de cada página en negro:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Paso 3: ajustar el color del texto
Ajuste el color de fuente del texto a blanco para una mejor visibilidad:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Paso 4: guarde el documento
Guarde el documento de OneNote modificado como PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Conclusión
¡Felicidades! Ha aplicado con éxito un tema oscuro al texto de su documento Aspose.Note. Esta mejora simple pero efectiva puede darle a sus archivos OneNote una apariencia más sofisticada.
## Preguntas frecuentes
### ¿Puedo aplicar un tema oscuro a secciones específicas de mi documento de OneNote?
Sí, puede personalizar el código para dirigirlo a páginas o secciones específicas dentro de su documento.
### ¿Aspose.Note admite otros formatos de exportación además de PDF?
¡Absolutamente! Aspose.Note admite varios formatos de exportación, incluidas imágenes y Microsoft Word.
### ¿Existe un límite para el tamaño del documento que Aspose.Note puede manejar?
Aspose.Note puede manejar documentos de diferentes tamaños y su rendimiento está optimizado para lograr eficiencia.
### ¿Puedo volver al tema original después de aplicar el tema oscuro?
Sí, puede modificar el código para cambiar entre temas según sus preferencias.
### ¿Dónde puedo obtener asistencia para consultas relacionadas con Aspose.Note?
 Para cualquier ayuda, visite el[Foro Aspose.Note](https://forum.aspose.com/c/note/28) o explorar el[documentación](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

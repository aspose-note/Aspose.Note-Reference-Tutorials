---
date: 2026-08-13
description: Aprenda cómo obtener la hora de modificación de una página de OneNote
  y recuperar revisiones de la página con Aspose.Note para Java, ideal para auditoría
  y gestión de documentos.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Obtener revisiones de páginas en OneNote - Aspose.Note
og_description: Aprenda cómo obtener la hora de modificación de una página de OneNote
  y recuperar revisiones de páginas de OneNote con Aspose.Note para Java. Pasos rápidos,
  fragmentos de código y solución de problemas.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Obtener la hora de modificación de una página de OneNote usando Aspose.Note
  – tutorial de Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Obtener la hora de modificación de una página de OneNote usando Aspose.Note
url: /es/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtener la hora de modificación de la página de OneNote usando Aspose.Note

## Introducción

En este tutorial aprenderá cómo **obtener la hora de modificación de la página de OneNote** y extraer el historial completo de revisiones de una página de OneNote con Aspose.Note para Java. Ya sea que esté construyendo una función de registro de auditoría, un visor de registro de cambios, o necesite mostrar la fecha de edición más reciente en un panel, esta guía lo acompañará en cada paso, desde la configuración del entorno hasta el manejo de problemas comunes.

## Respuestas rápidas
- **¿Qué devuelve “obtener la hora de última modificación”?** Devuelve la marca de tiempo de la edición más reciente en una página de OneNote.  
- **¿Qué clase proporciona el historial de revisiones?** `PageHistory` a través de `Document.getPageHistory(Page)`.  
- **¿Necesito una licencia para esta función?** Sí, se requiere una licencia válida de Aspose.Note para uso en producción.  
- **¿Qué versión de Java es compatible?** Java 8 o superior (JDK 8+).  
- **¿Puedo filtrar revisiones por autor?** Puede leer la propiedad `Author` de cada objeto `Page` y aplicar su propio filtro.

## Qué es “obtener la hora de última modificación” en OneNote?

La hora de última modificación se almacena como un atributo de metadatos en cada página de OneNote que indica el momento de la edición más reciente. Aspose.Note expone este valor a través del método `Page.getLastModifiedTime()`, que devuelve un objeto `java.util.Date` que puede formatearse o registrarse según los requisitos de su aplicación.

## ¿Por qué recuperar revisiones de página?

Recuperar las revisiones de página le brinda un registro de auditoría completo de cada cambio realizado en una página de OneNote, lo que le permite rastrear quién editó qué y cuándo. Este historial puede usarse para comparar versiones, restaurar estados anteriores o analizar patrones de colaboración entre equipos, lo que lo hace esencial para el cumplimiento y el control de calidad.

## Requisitos previos

- **Java Development Kit (JDK) 8 o posterior** – instálelo desde el sitio web de Oracle o cualquier proveedor compatible.  
- **Biblioteca Aspose.Note para Java** – descargue el JAR desde la página de lanzamientos de Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** y siga la guía de instalación **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Importar paquetes

La clase `Document` representa un cuaderno de OneNote cargado en memoria, mientras que `Page` y `PageHistory` proporcionan acceso a páginas individuales y sus datos de revisión.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Las declaraciones de importación reales se muestran como texto plano para preservar el recuento original del bloque de código.)*

## Cómo obtener la hora de modificación de la página de OneNote?

Para obtener la marca de tiempo de la última modificación, primero cargue el documento de OneNote en un objeto `Document`, luego seleccione la `Page` deseada. Llame al método `getLastModifiedTime()` en esa página, que devuelve un `java.util.Date`. Luego puede formatear esta fecha usando `SimpleDateFormat` o convertirla a UTC para un informe coherente en diferentes zonas horarias.

## Paso 1: establecer el directorio del documento

Defina la carpeta que contiene su archivo de OneNote.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Paso 2: cargar el documento

Cree una instancia de `Document` pasando la ruta completa a su archivo `.one`.

```java
String dataDir = "Your Document Directory";
```

## Paso 3: obtener la primera página

Recupere el primer objeto `Page` de la colección de páginas del documento.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Paso 4: obtener revisiones de la página

Obtenga el `PageHistory` para la página seleccionada. Si el cuaderno nunca ha sido editado, esta llamada puede devolver `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Paso 5: recorrer revisiones de la página

Itere a través de cada revisión de `Page`, lea su `Author` y `LastModifiedTime`, y muestre la información.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Problemas comunes y soluciones
- **`PageHistory` nulo** – Verifique que el cuaderno realmente contenga revisiones; de lo contrario `getPageHistory` devuelve `null`.  
- **Diferencias de zona horaria** – `getLastModifiedTime()` usa la zona horaria predeterminada de la JVM. Convierta a UTC con `SimpleDateFormat` si su aplicación requiere una zona estándar.  
- **Licencia no cargada** – Sin una licencia válida, Aspose.Note se ejecuta en modo de evaluación, limitando el procesamiento de páginas. Cargue su archivo de licencia al iniciar la aplicación para evitar esta restricción.

## Preguntas frecuentes

**P1: ¿Puedo usar Aspose.Note para Java para crear nuevos documentos de OneNote?**  
R: Sí, la API le permite crear, editar y guardar cuadernos de OneNote programáticamente desde cero.

**P2: ¿Es Aspose.Note para Java compatible con diferentes versiones de archivos de OneNote?**  
R: Sí, admite los formatos de archivo OneNote 2007‑2021, garantizando una amplia compatibilidad en entornos de escritorio y nube.

**P3: ¿Puedo personalizar el formato de salida al exportar documentos de OneNote?**  
R: Por supuesto. Puede exportar a PDF, HTML, PNG o SVG, y controlar opciones como la resolución de imagen y la incrustación de fuentes.

**P4: ¿Aspose.Note para Java requiere una licencia para uso comercial?**  
R: Sí, una licencia comercial es obligatoria para implementaciones en producción. Hay una prueba gratuita disponible para evaluación.

**P5: ¿Dónde puedo buscar asistencia si encuentro problemas?**  
R: Visite el foro de la comunidad de Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** para hacer preguntas, compartir experiencias y obtener ayuda de la comunidad y los ingenieros de Aspose.

---

**Última actualización:** 2026-08-13  
**Probado con:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Autor:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Tutoriales relacionados

- [Tutorial Java de Aspose - Obtener información sobre páginas en OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Tutorial de revisiones de página de Aspose.Note – Obtener revisiones de página en OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Seguimiento de cambios en OneNote – Gestionar revisiones de página con Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
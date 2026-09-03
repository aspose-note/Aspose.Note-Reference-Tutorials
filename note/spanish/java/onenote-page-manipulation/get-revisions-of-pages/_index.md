---
date: 2026-01-10
description: Aprende cómo obtener la hora de la última modificación y recuperar las
  revisiones de las páginas de OneNote usando Aspose.Note para Java. Integra esto
  en tus aplicaciones Java para una gestión de documentos eficiente.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cómo obtener la hora de última modificación de las páginas de OneNote – Aspose.Note
url: /es/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtener revisiones de páginas en OneNote - Aspose.Note

## Introducción

En este tutorial, **obtendrás la hora de la última modificación** de las páginas dentro de un documento OneNote y explorarás cómo recuperar el historial completo de revisiones usando Aspose.Note para Java. Ya sea que estés construyendo un sistema de gestión de documentos, auditando cambios, o simplemente necesites mostrar cuándo se editó por última vez una página, esta guía te muestra exactamente cómo extraer esa información programáticamente.

## Respuestas rápidas
- **¿Qué devuelve “get last modified time”?** La marca de tiempo de la edición más reciente en una página de OneNote.  
- **¿Qué clase proporciona el historial de revisiones?** `PageHistory` a través de `Document.getPageHistory(Page)`.  
- **¿Necesito una licencia para esta función?** Sí, se requiere una licencia válida de Aspose.Note para uso en producción.  
- **¿Qué versión de Java es compatible?** Java 8 o superior (JDK 8+).  
- **¿Puedo filtrar revisiones por autor?** Puedes leer la propiedad `Author` de cada objeto `Page` y aplicar tu propio filtro.

## ¿Qué es “get last modified time” en OneNote?

El **last modified time** es un campo de metadatos almacenado con cada página que registra cuándo se modificó por última vez. Aspose.Note expone este valor a través del método `Page.getLastModifiedTime()`, lo que facilita mostrar o registrar las fechas de cambio.

## ¿Por qué recuperar revisiones de páginas?

- **Rastreos de auditoría:** Mantener un registro de quién cambió qué y cuándo.  
- **Comparación de versiones:** Construir funcionalidades que comparen dos revisiones lado a lado.  
- **Información sobre la colaboración de usuarios:** Entender los patrones de edición en cuadernos compartidos.  

## Requisitos previos

Antes de comenzar, asegúrate de tener lo siguiente:

### Java Development Kit (JDK) instalado
Instala JDK 8 o posterior desde el sitio web de Oracle o tu gestor de paquetes preferido.

### Biblioteca Aspose.Note para Java
Descarga la biblioteca desde el sitio oficial. Puedes encontrar el enlace de descarga **[aquí](https://releases.aspose.com/note/java/)**. Sigue las instrucciones de instalación en la documentación **[aquí](https://reference.aspose.com/note/java/)**.

## Importar paquetes

Para comenzar, importa los paquetes necesarios en tu proyecto Java. Estos paquetes te permitirán aprovechar la funcionalidad proporcionada por Aspose.Note para Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Ahora, desglosaremos el código de ejemplo proporcionado en varios pasos para entender cada componente y su funcionalidad.

## Cómo obtener la hora de la última modificación de una página OneNote

### Paso 1: Establecer el directorio del documento
Define el directorio donde se encuentra tu documento OneNote.

```java
String dataDir = "Your Document Directory";
```

### Paso 2: Cargar el documento
Carga el documento OneNote en Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Paso 3: Obtener la primera página
Recupera la primera página del documento.

```java
Page firstPage = doc.getFirstChild();
```

### Paso 4: Obtener revisiones de la página
Obtén el historial de revisiones de la página.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Paso 5: Recorrer revisiones de la página
Itera a través de la lista de revisiones de la página y recupera la información relevante, incluido el **last modified time**.

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

## Problemas comunes y soluciones
- **`PageHistory` nulo:** Asegúrate de que el documento realmente contenga revisiones; de lo contrario `getPageHistory` puede devolver `null`.  
- **Diferencias de zona horaria:** `getLastModifiedTime()` devuelve un `java.util.Date` en la zona horaria predeterminada del sistema. Conviértelo a UTC si es necesario.  
- **Licencia no cargada:** Sin una licencia válida, Aspose.Note puede operar en modo de evaluación, limitando la cantidad de páginas procesadas.

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.Note para Java para crear nuevos documentos OneNote?
R1: Sí, Aspose.Note para Java ofrece soporte integral para crear, leer y manipular documentos OneNote programáticamente.

### P2: ¿Aspose.Note para Java es compatible con diferentes versiones de archivos OneNote?
R2: Sí, Aspose.Note para Java admite varias versiones de archivos Microsoft OneNote, garantizando compatibilidad en diferentes entornos.

### P3: ¿Puedo personalizar el formato de salida al exportar documentos OneNote?
R3: Absolutamente, Aspose.Note para Java ofrece flexibilidad al exportar documentos OneNote a diferentes formatos como PDF, HTML e imágenes, con opciones de personalización.

### P4: ¿Aspose.Note para Java requiere una licencia para uso comercial?
R4: Sí, se requiere una licencia válida para el uso comercial de Aspose.Note para Java. Puedes obtener una licencia en el sitio web de Aspose.

### P5: ¿Dónde puedo buscar ayuda si encuentro problemas o tengo preguntas sobre Aspose.Note para Java?
R5: Para soporte y asistencia, puedes visitar el foro de Aspose.Note **[aquí](https://forum.aspose.com/c/note/28)**, donde puedes hacer preguntas, compartir experiencias e interactuar con otros usuarios y expertos.

---

**Última actualización:** 2026-01-10  
**Probado con:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
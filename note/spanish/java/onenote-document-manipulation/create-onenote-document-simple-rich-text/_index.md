---
date: 2026-02-18
description: Aprenda cómo establecer el estilo de párrafo y agregar elementos de esquema
  al crear documentos de OneNote en Java usando Aspose.Note. Exporte OneNote a PDF,
  guarde OneNote como PDF y genere archivos de OneNote sin esfuerzo.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Exportar OneNote a PDF – Establecer estilo de párrafo al crear documento OneNote
  en Java
url: /es/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer estilo de párrafo al crear un documento OneNote en Java

## Introducción

En el panorama de desarrollo de hoy, que avanza rápidamente, poder **export OneNote to PDF** de forma programática es esencial para producir documentos pulidos y listos para compartir. Este tutorial le guía a través de la creación de un archivo OneNote, la aplicación de un estilo de párrafo personalizado y, finalmente, **export OneNote to PDF** usando Aspose.Note para Java. Ya sea que esté construyendo un motor de informes, una solución automatizada de toma de notas o un servicio de conversión de documentos, las técnicas cubiertas aquí le ayudarán a **save OneNote as PDF** con un control exacto del formato.

## Respuestas rápidas
- **What does “set paragraph style” mean?** Aplica fuente, tamaño, color y otros formatos a un párrafo de texto.  
- **Can I export the result to PDF?** Sí – el tutorial termina guardando el archivo OneNote como PDF.  
- **Do I need a license for Aspose.Note?** Una prueba gratuita funciona para evaluación; se requiere una licencia para producción.  
- **Which IDEs are supported?** Cualquier IDE de Java – Eclipse, IntelliJ IDEA, NetBeans, etc.  
- **How long does the implementation take?** Aproximadamente 10‑15 minutos para un documento básico.

## ¿Qué es “set paragraph style” en Aspose.Note?
Establecer estilo de párrafo se refiere a configurar un objeto `ParagraphStyle` (nombre de fuente, tamaño, color, etc.) y adjuntarlo a un nodo `RichText`. Esto le brinda control total sobre cómo aparece el texto dentro de una página OneNote.

## ¿Cómo establecer el estilo de párrafo en OneNote?
Aplicar un estilo es tan simple como crear una instancia de `ParagraphStyle`, personalizar sus propiedades y asignarla a un elemento `RichText`. La API hace que esto sea una operación de una sola línea una vez que el objeto de estilo está listo.

## ¿Por qué exportar OneNote a PDF?
- **Consistent branding:** Preservar fuentes y colores corporativos al compartir notas externamente.  
- **Readability:** PDF mantiene el diseño exacto, lo que lo hace ideal para imprimir o archivar.  
- **Cross‑platform access:** Los destinatarios pueden ver el PDF en cualquier dispositivo sin necesidad de OneNote.  

## Prerrequisitos

Antes de comenzar, asegúrese de tener:

1. **Java Development Kit (JDK) 1.8+** – cualquier JDK reciente funcionará.  
2. **Aspose.Note for Java** – descargue el JAR más reciente desde la [Aspose.Note download page](https://releases.aspose.com/note/java/).  
3. **An IDE** (Eclipse, IntelliJ IDEA o NetBeans) para compilar y ejecutar el ejemplo.  

> **Pro tip:** Añada el JAR de Aspose.Note al classpath de su proyecto mediante Maven o referenciando manualmente el JAR en su IDE.

## Import Packages

Primero, importe las clases que necesitaremos. Este bloque permanece sin cambios.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> La clase `ParagraphStyle` es la clave para **set paragraph style** más adelante en el tutorial.

## Guía paso a paso

A continuación se muestra una guía concisa de cada operación. Los bloques de código son exactamente como en el ejemplo original; solo añadimos texto explicativo.

### Paso 1: Set Document Directory
Defina dónde se guardarán los archivos generados.

```java
String dataDir = "Your Document Directory";
```

Reemplace `"Your Document Directory"` con una ruta absoluta o relativa en su máquina.

### Paso 2: Initialize Document Object
Cree el objeto raíz `Document` que representa el archivo OneNote.

```java
Document doc = new Document();
```

### Paso 3: Initialize Page Object
Un archivo OneNote consta de una o más páginas; comenzamos con una sola página.

```java
Page page = new Page();
```

### Paso 4: Initialize Outline Object
Los contornos actúan como contenedores para elementos de contorno (piense en ellos como secciones).

```java
Outline outline = new Outline();
```

### Paso 5: Initialize OutlineElement Object
Aquí **add outline element** que contendrá nuestro texto enriquecido.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Paso 6: Set Text Style (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

La instancia `ParagraphStyle` define la fuente, el tamaño y el color; aquí es donde **set paragraph style** para el próximo nodo de texto.

### Paso 7: Initialize RichText Object

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Creamos un nodo `RichText`, insertamos una cadena simple y adjuntamos el estilo definido previamente.

### Paso 8: Add RichText Node to OutlineElement

```java
outlineElem.appendChildLast(text);
```

Ahora el texto con estilo vive dentro del elemento de contorno.

### Paso 9: Add OutlineElement Node to Outline

```java
outline.appendChildLast(outlineElem);
```

El contorno ahora contiene el elemento que alberga nuestro párrafo.

### Paso 10: Add Outline Node to Page

```java
page.appendChildLast(outline);
```

Colocamos el contorno en la página.

### Paso 11: Add Page Node to Document

```java
doc.appendChildLast(page);
```

El documento ahora tiene una sola página con nuestro texto con estilo.

### Paso 12: Save the Document (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

El método `save` escribe el archivo OneNote y **exports OneNote PDF** en un solo paso. También puede guardar como `.one` usando `SaveFormat.One` si necesita el formato nativo.

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **File not found** | `dataDir` apunta a una carpeta que no existe. | Asegúrese de que el directorio exista o créelo programáticamente (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | No se añadió contenido antes de guardar. | Verifique que el nodo `RichText` se haya añadido y que el estilo esté configurado. |
| **Unsupported font** | Nombre de fuente no instalado en el sistema. | Use una fuente común como `"Arial"` o incruste la fuente en el proyecto. |

## Preguntas frecuentes

**Q: ¿Puede Aspose.Note manejar formato complejo como tablas o imágenes?**  
A: Sí, la API admite tablas, imágenes, hipervínculos y características de diseño más avanzadas.

**Q: ¿Es posible **convert OneNote PDF** de nuevo a un archivo OneNote?**  
A: No se proporciona una conversión directa, pero puede extraer el contenido del PDF y reconstruir un documento OneNote usando la API.

**Q: ¿La biblioteca funciona en entornos Linux/macOS?**  
A: Absolutamente. Aspose.Note para Java es independiente de la plataforma; solo asegúrese de que el JDK esté instalado.

**Q: ¿Cómo añado múltiples páginas o contornos?**  
A: Cree objetos `Page` y `Outline` adicionales, luego añádalos al `Document` de la misma forma que en el ejemplo de una sola página.

**Q: ¿Dónde puedo encontrar más ejemplos?**  
A: La documentación oficial de Aspose.Note y el [support forum](https://forum.aspose.com/c/note/28) contienen muchos ejemplos de código.

## Conclusión

Ahora ha visto cómo **set paragraph style**, **add outline element** y **generate a OneNote file** que puede **export to PDF** usando Aspose.Note para Java. Incorporar texto con estilo al inicio del proceso garantiza que el documento final se vea profesional y que cualquier operación posterior de **convert OneNote PDF** mantenga el formato. Siéntase libre de ampliar esta base con imágenes, tablas o metadatos personalizados para satisfacer las necesidades de su proyecto.

---

**Última actualización:** 2026-02-18  
**Probado con:** Aspose.Note for Java 24.11 (última versión)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
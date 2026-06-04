---
description: Aprende cómo guardar PDF de OneNote y agregar subpáginas en OneNote usando
  Aspose.Note para Java. Sigue esta guía paso a paso para organizar tus notas de manera
  eficiente.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Cómo guardar PDF de OneNote y agregar subpáginas
url: /es/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo guardar OneNote en PDF y agregar subpáginas

## Introducción

En este tutorial, descubrirás **cómo guardar OneNote en PDF** mientras creas un documento que contiene tanto páginas raíz como subpáginas usando Aspose.Note para Java. Organizar tus cuadernos de OneNote con una jerarquía clara facilita la navegación, y la capacidad de exportar a PDF garantiza que puedas compartir tus notas en un formato universalmente legible. También te mostraremos cómo **agregar subpáginas al estilo OneNote**, para que puedas construir estructuras multinivel con facilidad.

## Respuestas rápidas
- **¿Qué significa la palabra clave principal?** Se refiere a exportar un cuaderno de OneNote a PDF usando Aspose.Note.
- **¿Qué API se utiliza?** Aspose.Note para Java.
- **¿Puedo crear páginas jerárquicas?** Sí – establece el nivel de la página para crear páginas raíz y subpáginas.
- **¿Necesito una licencia?** Hay una prueba gratuita disponible; se requiere una licencia comercial para producción.
- **¿Qué formatos de salida son compatibles?** BMP, PDF, PNG y más.

## ¿Qué es “cómo guardar OneNote PDF”?
Guardar OneNote como PDF convierte las páginas del cuaderno en un documento de diseño fijo que conserva el formato, las imágenes y la jerarquía. Esto es ideal para compartir, archivar o imprimir notas.

## ¿Por qué agregar subpáginas al estilo OneNote?
Agregar subpáginas te permite agrupar contenido relacionado bajo una página padre, imitando una estructura tipo carpeta. Mejora la organización de notas, acelera la búsqueda y enriquece la experiencia de lectura cuando el cuaderno se exporta a PDF.

## Requisitos previos

Antes de comenzar, asegúrate de contar con los siguientes requisitos:

1. Java Development Kit (JDK): Verifica que tienes el JDK instalado en tu sistema.  
2. Aspose.Note para Java: Descarga e instala Aspose.Note para Java desde el [sitio web](https://purchase.aspose.com/buy).  
3. Entorno de desarrollo integrado (IDE): Elige un IDE de Java como IntelliJ IDEA, Eclipse o NetBeans.

## Importar paquetes

Comienza importando los paquetes necesarios en tu proyecto Java:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Paso 1: Configurar el directorio del documento

Define el directorio donde deseas guardar tu documento de OneNote:

```java
String dataDir = "Your Document Directory";
```

## Paso 2: Crear el objeto Document

Instancia un objeto `Document`:

```java
Document doc = new Document();
```

## Paso 3: Crear páginas

Inicializa los objetos de página y establece sus niveles. Configurar el nivel determina si una página es raíz o una subpágina:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Paso 4: Agregar nodos a las páginas

### Agregar nodos a la primera página

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Agregar nodos a la segunda página

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Agregar nodos a la tercera página

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Paso 5: Añadir páginas al documento

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Paso 6: Guardar el documento

Guarda el documento de OneNote como PDF (o BMP en este ejemplo). Cambiar el `SaveFormat` te permite exportar a PDF, cumpliendo con el requisito de “cómo guardar OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Consejo profesional:** Para exportar directamente a PDF, reemplaza `SaveFormat.Bmp` por `SaveFormat.Pdf`.

¡Felicidades! Has creado exitosamente un documento de OneNote con páginas raíz y subpáginas y aprendido **cómo guardar OneNote PDF** usando Aspose.Note para Java.

## Por qué es importante

- **Organización jerárquica:** Las páginas raíz y subpáginas te permiten imitar estructuras de carpetas dentro de OneNote.  
- **Exportación a PDF sin problemas:** Una vez organizadas, exportar a PDF conserva la jerarquía, haciendo que el documento final sea fácil de leer y compartir.  
- **Automatización:** El código puede integrarse en aplicaciones Java más grandes, habilitando la creación por lotes de cuadernos estructurados.

## Errores comunes y cómo evitarlos

| Problema | Causa | Solución |
|----------|-------|----------|
| Las páginas aparecen al mismo nivel | Valor incorrecto en `setLevel` | Usa `setLevel((byte) 1)` para páginas raíz y `setLevel((byte) 2)` (o superior) para subpáginas. |
| La salida PDF aparece en blanco | Falta `SaveFormat.Pdf` o ruta de archivo incorrecta | Verifica que el directorio exista y usa `SaveFormat.Pdf`. |
| La fuente no se aplica | Nombre de fuente incorrecto o fuente ausente en el sistema | Asegúrate de que la fuente (p. ej., “David Transparent”) esté instalada en la máquina que ejecuta el código. |

## Preguntas frecuentes

**P: ¿Puedo crear varios niveles de subpáginas usando Aspose.Note para Java?**  
R: Sí, puedes crear jerarquías más profundas estableciendo números de nivel mayores (p. ej., `setLevel((byte) 3)` para una subpágina de tercer nivel).

**P: ¿Aspose.Note para Java es compatible con diferentes IDE de Java?**  
R: Absolutamente. Funciona con IntelliJ IDEA, Eclipse, NetBeans y cualquier IDE que soporte desarrollo en Java.

**P: ¿Puedo personalizar el formato del texto en mi documento de OneNote?**  
R: Sí. Usa `ParagraphStyle` para establecer el nombre de la fuente, tamaño, color y otros atributos para cada elemento `RichText`.

**P: ¿Aspose.Note para Java admite guardar documentos en formatos distintos a BMP?**  
R: Sí. Los formatos compatibles incluyen PDF, PNG, JPEG, DOCX y más. Cambia el enum `SaveFormat` según corresponda.

**P: ¿Existe una versión de prueba disponible para Aspose.Note para Java?**  
R: Sí, puedes descargar una prueba gratuita desde el sitio web de Aspose.

## Conclusión

Organizar tus cuadernos de OneNote con una estructura jerárquica clara y exportarlos como PDFs hace que tus notas sean más accesibles y compartibles. Siguiendo los pasos anteriores, ahora sabes **cómo guardar OneNote PDF** y **agregar subpáginas al estilo OneNote** de forma programática con Aspose.Note para Java.

---

**Última actualización:** 2026-01-07  
**Probado con:** Aspose.Note para Java 24.11 (última)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
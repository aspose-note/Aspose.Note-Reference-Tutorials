---
date: 2025-12-20
description: Aprende cómo agregar imágenes a OneNote usando Aspose.Note para Java.
  Guía paso a paso para crear documentos de OneNote e insertar imágenes de forma programática.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Cómo agregar una imagen a OneNote usando Java – Construir documento e insertar
  imagen
url: /es/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo agregar una imagen a OneNote usando Java – Construir documento e insertar imagen

## Introducción

En este tutorial, aprenderás **cómo agregar una imagen a OneNote** usando la API Aspose.Note para Java. Recorreremos la creación de un documento OneNote desde cero, la inserción de una imagen y el guardado del resultado como PDF. Ya sea que estés construyendo una herramienta de informes, automatizando la toma de notas o simplemente necesites incrustar gráficos programáticamente, esta guía te ofrece una ruta clara y práctica.

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.Note para Java.  
- **¿Puedo insertar cualquier formato de imagen?** JPEG, PNG, BMP, GIF y más son compatibles.  
- **¿Qué formatos de salida están disponibles?** Puedes guardar como OneNote, PDF, XPS, HTML, etc.  
- **¿Necesito una licencia para producción?** Sí, se requiere una licencia comercial para uso que no sea de prueba.  
- **¿El código es multiplataforma?** Absolutamente – Java se ejecuta en Windows, Linux y macOS.

## ¿Qué es “agregar una imagen a OneNote”?
Agregar una imagen a OneNote significa incrustar programáticamente un archivo de imagen en una página de OneNote para que aparezca junto al texto, esquemas u otros elementos. La API Aspose.Note abstrae el formato de archivo de OneNote, permitiéndote centrarte en el contenido en lugar de la estructura XML subyacente.

## ¿Por qué agregar una imagen a OneNote usando Java?
- **Automatización:** Genera actas de reuniones con capturas de pantalla automáticamente.  
- **Consistencia:** Garantiza que cada página siga el mismo diseño y branding.  
- **Integración:** Combina datos de otros sistemas (p. ej., gráficos) directamente en los cuadernos de OneNote.  
- **Multiplataforma:** Java te permite ejecutar el mismo código en cualquier servidor o entorno de escritorio.

## Requisitos previos

Antes de comenzar, asegúrate de contar con lo siguiente:

1. **Java Development Kit (JDK)** – cualquier versión reciente (8 o superior).  
2. **Biblioteca Aspose.Note para Java** – descárgala desde el [sitio web](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o cualquier editor compatible con Java que prefieras.  

## Importar paquetes

Comienza importando las clases necesarias en tu archivo fuente Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Guía paso a paso

### Paso 1: Configurar el documento

Crea un nuevo documento OneNote y un contenedor de página donde vivirá el contenido.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Paso 2: Inicializar el esquema

Un *esquema* actúa como contenedor para elementos como texto e imágenes. Establecemos sus desplazamientos a cero para que el contenido comience en la esquina superior izquierda.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Paso 3: Cargar y alinear la imagen

Carga la imagen que deseas incrustar y alinéala al lado derecho de la página. Aquí es donde realmente **agregamos una imagen a OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Paso 4: Adjuntar la imagen a un elemento de esquema

Envuelve la imagen dentro de un `OutlineElement`. Este paso vincula el objeto visual a la jerarquía del esquema del documento.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Paso 5: Ensamblar la estructura del documento

Añade el elemento de esquema al esquema, luego adjunta el esquema a la página y, finalmente, agrega la página al documento.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Paso 6: Guardar el documento OneNote

Persiste el documento en disco. En este ejemplo exportamos a PDF, pero también puedes guardar como archivo nativo de OneNote (`.one`) cambiando el `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **La imagen no aparece** | Ruta de archivo incorrecta o formato no compatible. | Verifica que `dataDir` apunte a la carpeta correcta y usa un tipo de imagen soportado (JPEG, PNG, etc.). |
| **Documento guardado como PDF vacío** | Desplazamientos del esquema configurados incorrectamente. | Asegúrate de que se llamen `setVerticalOffset(0)` y `setHorizontalOffset(0)`, o ajusta los desplazamientos para colocar el contenido dentro de los límites de la página. |
| **IOException al guardar** | La carpeta de destino no existe o no tiene permiso de escritura. | Crea la carpeta previamente o ejecuta el programa con los permisos adecuados. |

## Preguntas frecuentes

**P1: ¿Dónde puedo encontrar la documentación de Aspose.Note para Java?**  
R1: Puedes acceder a la documentación [aquí](https://reference.aspose.com/note/java/).

**P2: ¿Cómo descargo Aspose.Note para Java?**  
R2: Puedes descargar Aspose.Note para Java desde la [página de descargas](https://releases.aspose.com/note/java/).

**P3: ¿Existe una versión de prueba gratuita de Aspose.Note para Java?**  
R3: Sí, puedes obtener una prueba gratuita desde el [sitio web](https://releases.aspose.com/).

**P4: ¿Dónde puedo obtener soporte para Aspose.Note para Java?**  
R4: Para soporte, visita el [foro de Aspose.Note](https://forum.aspose.com/c/note/28).

**P5: ¿Puedo obtener una licencia temporal para Aspose.Note para Java?**  
R5: Sí, puedes solicitar una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2025-12-20  
**Probado con:** Aspose.Note para Java 24.12 (última)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
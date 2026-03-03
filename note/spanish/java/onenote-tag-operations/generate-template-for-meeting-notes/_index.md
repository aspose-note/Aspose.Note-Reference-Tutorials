---
date: 2026-03-03
description: Aprende a crear esquemas en OneNote y generar una plantilla de notas
  de reunión con Aspose.Note para Java. Personaliza el estilo de fuente y agrega casillas
  de verificación fácilmente.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: Crear esquema en OneNote – Plantilla de notas de reunión
url: /es/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear esquema en OneNote – Plantilla de notas de reunión

## Introducción
En el mundo acelerado de hoy, crear **esquema en OneNote** de manera eficiente es esencial para una documentación clara de las reuniones. Aspose.Note for Java ofrece una forma potente de **generar una plantilla de notas de reunión** que puedes personalizar, agregar casillas de verificación y dar estilo a las fuentes exactamente como lo necesitas. En esta guía paso a paso recorreremos la creación de una plantilla reutilizable de agenda de reunión, explicando **cómo agregar casillas de verificación**, **agregar lista de verificación a OneNote**, y **personalizar estilo de fuente onenote** para un aspecto pulido.

## Respuestas rápidas
- **¿Qué significa “create outline in OneNote”?** Significa construir programáticamente una estructura jerárquica (títulos, secciones, viñetas) dentro de un archivo OneNote.  
- **¿Qué biblioteca ayuda con esto?** Aspose.Note for Java.  
- **¿Puedo agregar casillas de verificación al esquema?** Sí – usa `NoteCheckBox.createBlueCheckBox()`.  
- **¿Necesito una licencia?** Hay una versión de prueba gratuita disponible; se requiere una licencia comercial para producción.  
- **¿Qué versión de Java es compatible?** Java 8 y posteriores.

## Qué es “create outline in OneNote”?
Crear un esquema en OneNote significa definir una página con un título, múltiples secciones de esquema y numeración de listas u opcionalmente casillas de verificación. Esta estructura refleja la forma en que manualmente escribirías encabezados y viñetas dentro de la interfaz de OneNote, pero se genera automáticamente mediante código.

## ¿Por qué usar Aspose.Note para plantillas de agenda de reunión?
- **Consistencia:** Cada reunión comienza con el mismo diseño limpio.  
- **Automatización:** Reduce la escritura manual y asegura que todas las secciones requeridas (agenda, acciones, notas) estén presentes.  
- **Personalización:** Cambia fuentes, colores y agrega casillas de verificación interactivas para rastrear tareas.  
- **Integración:** Funciona con cualquier IDE de Java y puede combinarse con otras bibliotecas Aspose para PDFs, hojas de cálculo, etc.

## Requisitos previos
- Conocimientos básicos de programación en Java.  
- Biblioteca Aspose.Note for Java instalada. Puedes descargarla [aquí](https://releases.aspose.com/note/java/).  
- Un IDE como Eclipse o IntelliJ IDEA.  

## Importar paquetes
Primero, importa las clases que necesitaremos. Este fragmento permanece exactamente igual que en el tutorial original.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Paso 1: Crear la estructura del documento
Comenzamos construyendo el documento, configurando un título y preparando estilos de párrafo que luego nos ayudarán a **personalizar estilo de fuente onenote**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Lo que hicimos:*  
- Definimos dos objetos `ParagraphStyle` (`headerStyle` para encabezados, `bodyStyle` para texto normal).  
- Creamos un `Document` y añadimos un `Title` que incluye la fecha actual, proporcionando a la página un encabezado claro.

## Paso 2: Esquematizar puntos importantes
A continuación, **creamos esquema en OneNote** añadiendo un objeto `Outline` y poblando sus secciones como “Importante”. Aquí es donde viven los ítems de la agenda.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Por qué es importante:*  
- El objeto `Outline` representa la lista jerárquica que ves en OneNote.  
- Usando `createListNumberingStyle` generamos una lista numerada que puede reiniciarse para cada nueva sección.

## Paso 3: Resaltar elementos de acción (Cómo agregar casillas de verificación)
Los elementos de acción necesitan una señal visual. Al adjuntar una etiqueta de casilla de verificación a cada elemento `RichText`, habilitamos **cómo agregar casillas de verificación** directamente dentro del esquema.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Consejo profesional:* Usa `NoteCheckBox.createBlueCheckBox()` para una casilla azul; hay otros colores disponibles si necesitas un estilo visual diferente.

## Paso 4: Guardar el documento
Finalmente, escribe el archivo OneNote en disco. El archivo puede abrirse directamente en la aplicación de escritorio de OneNote.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Problemas comunes y soluciones
| Problema | Solución |
|----------|----------|
| **Casillas de verificación no aparecen** | Asegúrate de haber llamado `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` después de establecer el estilo del párrafo. |
| **Las fuentes se ven diferentes en OneNote** | Verifica que el nombre de la fuente (p. ej., “Calibri”) esté instalado en la máquina donde OneNote abre el archivo. |
| **El esquema no está sangrado** | Ajusta `setVerticalOffset` y `setHorizontalOffset` en el objeto `Outline`. |
| **La numeración se reinicia inesperadamente** | Usa correctamente el `restartFlag`; establécelo en `true` solo para la primera lista en una nueva sección. |

## Preguntas frecuentes
### ¿Puedo personalizar los estilos de fuente en mis notas de reunión?
Sí, Aspose.Note permite definir estilos de fuente personalizados para encabezados y texto del cuerpo.

### ¿Aspose.Note es compatible con otras bibliotecas Java?
Aspose.Note puede integrarse sin problemas con otras bibliotecas Java para ampliar la funcionalidad.

### ¿Cómo puedo agregar secciones adicionales a mis notas de reunión?
Puedes ampliar fácilmente la estructura del esquema siguiendo el mismo patrón demostrado en el tutorial.

### ¿Hay consideraciones de licencia para Aspose.Note?
Consulta la [documentación de Aspose.Note](https://reference.aspose.com/note/java/) para obtener detalles sobre licencias.

### ¿Existe una versión de prueba disponible para Aspose.Note?
Sí, puedes acceder a la [prueba gratuita aquí](https://releases.aspose.com/).

## Preguntas frecuentes
**Q:** ¿Cómo agrego una lista de verificación a OneNote sin usar casillas de verificación?  
**A:** Puedes crear una lista con viñetas y marcar los ítems manualmente, pero usar `NoteCheckBox` proporciona casillas interactivas que se sincronizan con la UI de OneNote.

**Q:** ¿Puedo usar esta plantilla para crear una agenda de reunión semanalmente?  
**A:** Absolutamente. Solo cambia el formato de la fecha o pasa una cadena de título personalizada para reutilizar la misma estructura cada semana.

**Q:** ¿Cuál es la mejor manera de **customizar font style onenote** para la marca?  
**A:** Define objetos `ParagraphStyle` con el nombre, tamaño y color de fuente corporativa, luego aplícalos a cada elemento `RichText` como se muestra en el Paso 1.

**Q:** ¿Aspose.Note admite exportar el esquema a PDF?  
**A:** Sí. Después de guardar el archivo OneNote, puedes cargarlo con Aspose.Note y exportarlo a PDF usando `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q:** ¿Hay una forma de marcar programáticamente una casilla como completada?  
**A:** Puedes establecer el estado de la casilla añadiendo una etiqueta `NoteCheckBox` con la propiedad `Checked` establecida en `true`.

---

**Última actualización:** 2026-03-03  
**Probado con:** Aspose.Note for Java 24.11 (última disponible al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
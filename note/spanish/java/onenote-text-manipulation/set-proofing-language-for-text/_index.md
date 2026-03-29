---
date: 2026-03-29
description: Aprende cómo establecer el idioma del texto en OneNote usando Aspose.Note
  para Java. Esta guía paso a paso te muestra cómo crear un documento de OneNote,
  cambiar el idioma del texto y guardar el archivo de OneNote de manera eficiente.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cómo establecer el idioma del texto en OneNote – Aspose.Note
url: /es/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo establecer el idioma del texto en OneNote – Aspose.Note

## Introducción
Si necesita **cómo establecer el idioma** para fragmentos específicos de texto dentro de un cuaderno de OneNote, Aspose.Note para Java lo hace sencillo. En este tutorial aprenderá a crear un documento OneNote, cambiar el idioma del texto para palabras o frases individuales, y finalmente guardar el archivo OneNote con el idioma de corrección aplicado. Al final comprenderá por qué establecer el idioma es importante para la revisión ortográfica y la localización, y tendrá un ejemplo de código listo para ejecutar.

## Respuestas rápidas
- **¿Qué afecta “establecer el idioma”?** Le indica a OneNote qué diccionario de corrección usar para la ortografía y gramática.  
- **¿Puedo establecer diferentes idiomas en la misma nota?** Sí, puede asignar un idioma a cada ejecución de texto.  
- **¿Necesito una licencia para Aspose.Note?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.  
- **¿Qué versiones de Java son compatibles?** Aspose.Note para Java es compatible con Java 8 y versiones posteriores.  
- **¿La salida es un archivo .one?** Sí, el documento se guarda como un archivo *.one* de OneNote.

## Requisitos previos
Antes de sumergirse en el código, asegúrese de contar con lo siguiente:

1. **Java Development Environment** – JDK 8 o superior instalado y configurado.  
2. **Aspose.Note for Java Library** – Descargue e instale la biblioteca desde el [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Cree una carpeta en su máquina donde se guardará el archivo OneNote generado.

## ¿Por qué establecer el idioma del texto en OneNote?
Establecer el idioma de corrección garantiza que la revisión ortográfica, las sugerencias gramaticales y la indexación de búsqueda funcionen correctamente para contenido multilingüe. Esto es especialmente útil para:

- **Equipos globales** colaborando en un solo cuaderno.  
- **Documentación localizada** donde cada sección puede estar en un idioma diferente.  
- **Aplicaciones basadas en datos** que generan notas programáticamente para usuarios de todo el mundo.

## Importar paquetes
Comience importando las clases necesarias de Aspose.Note y las utilidades de Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Paso 1: Configurar documento y página
Cree un nuevo documento OneNote y una página que contendrá su contenido. Este paso también muestra **crear documento OneNote**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Paso 2: Crear contorno y elemento de contorno
Un contorno es el contenedor del contenido del cuaderno. Aquí construimos la estructura que más adelante contendrá el texto específico de idioma.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Paso 3: Añadir texto enriquecido con configuraciones de idioma
Ahora **cambiamos el idioma del texto** adjuntando un `TextStyle` con un `Locale` específico a cada segmento de texto. Esto demuestra **establecer el idioma del texto**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Paso 4: Organizar elementos y guardar
Ensambla la jerarquía del contorno, adjúntala a la página y finalmente **guarda el archivo OneNote** con las configuraciones de idioma aplicadas.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Problemas comunes y consejos
- **Formato de Locale** – Use la etiqueta IETF BCP‑47 (p. ej., `en-US`, `de-DE`). Una etiqueta incorrecta hará que se use el idioma del documento por defecto.  
- **Ruta de archivo** – Asegúrese de que `dataDir` apunte a una carpeta existente; de lo contrario `document.save` lanzará una `IOException`.  
- **Consejo profesional:** Si necesita establecer el idioma para un párrafo completo, aplique el `TextStyle` al `ParagraphStyle` en lugar de a cada llamada `append`.

## Conclusión
Acaba de aprender **cómo establecer el idioma** para fragmentos de texto individuales en un cuaderno OneNote usando Aspose.Note para Java. Esta capacidad le permite **crear documento OneNote** programáticamente, **cambiar el idioma del texto** al instante, y **guardar el archivo OneNote** con metadatos de corrección precisos.

## Preguntas frecuentes

**P: ¿Puedo establecer el idioma de corrección para otros idiomas no mencionados en el ejemplo?**  
R: ¡Absolutamente! Añada llamadas `append` adicionales con el `Locale.forLanguageTag("xx-XX")` deseado.

**P: ¿Es Aspose.Note para Java compatible con las últimas versiones de Java?**  
R: Sí, la biblioteca se actualiza regularmente para soportar las versiones más recientes de Java.

**P: ¿Cómo puedo manejar errores durante el proceso de establecimiento del idioma?**  
R: Envuelva la operación de guardado en un bloque `try‑catch` para capturar `IOException` o `AsposeException`.

**P: ¿Puedo integrar este código en una aplicación web?**  
R: Por supuesto. Simplemente incluya el JAR de Aspose.Note en el classpath de su proyecto web y asegúrese de que el servidor tenga permiso de escritura en el directorio de destino.

**P: ¿Dónde puedo encontrar ejemplos adicionales y documentación para Aspose.Note para Java?**  
R: Explore la [documentación](https://reference.aspose.com/note/java/) para obtener una lista completa de APIs y proyectos de ejemplo.

---

**Última actualización:** 2026-03-29  
**Probado con:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
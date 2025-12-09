---
date: 2025-12-02
description: Aprenda cómo exportar fuentes mientras guarda OneNote como HTML usando
  Aspose.Note para Java. Esta guía le muestra cómo crear OneNote programáticamente
  e incrustar fuentes, CSS e imágenes.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Cómo exportar fuentes al guardar OneNote como HTML – Java
url: /es/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo exportar fuentes al guardar OneNote como HTML – Java

## Introducción

En este tutorial descubrirás **cómo exportar fuentes** cuando **guardes OneNote como HTML** usando Aspose.Note for Java. Te guiaremos paso a paso en la creación programática de un documento OneNote, la configuración de las opciones de guardado HTML y la incrustación de los archivos de fuentes necesarios para que el HTML resultante se vea exactamente como las páginas originales de OneNote. Este enfoque es perfecto cuando necesitas preservar la fidelidad visual del contenido de OneNote en un formato amigable para la web.

## Respuestas rápidas
- **¿Qué biblioteca maneja la exportación?** Aspose.Note for Java  
- **¿Se pueden incrustar fuentes en el HTML?** Sí – establezca `ExportFonts` a `ExportEmbedded`  
- **¿Necesito una licencia para producción?** Se requiere una licencia válida de Aspose.Note para uso comercial  
- **¿Qué versión de Java es compatible?** Java 8 o superior  
- **¿Es posible guardar recursos en archivos separados?** Absolutamente – configure `ResourceExportType` en consecuencia  

## ¿Qué significa “cómo exportar fuentes” en el contexto de la conversión a HTML de OneNote?

Al convertir un cuaderno de OneNote a HTML, la apariencia visual depende de CSS, imágenes y, especialmente, de las fuentes usadas en las páginas originales. **Exportar fuentes** significa incrustar los archivos de fuentes (p. ej., TTF) directamente en el paquete HTML para que los navegadores puedan renderizar el texto exactamente como aparece en OneNote, incluso si el usuario final no tiene esas fuentes instaladas localmente.

## ¿Por qué crear OneNote programáticamente y guardarlo como HTML?

- **Automatización:** Generar informes, documentación o artículos de base de conocimientos a partir de OneNote sin copiar y pegar manualmente.  
- **Consistencia:** Conservar el diseño, el estilo y las fuentes personalizadas en todos los dispositivos.  
- **Portabilidad:** HTML es universalmente visible—no se necesita el cliente de OneNote.  

## Requisitos previos

1. Java Development Kit (JDK) 8 o superior instalado.  
2. Biblioteca Aspose.Note for Java – descargue desde [aquí](https://releases.aspose.com/note/java/).  
3. Un archivo de muestra de OneNote (`.one`) para cargar, o puede crear uno nuevo programáticamente.  

## Importar paquetes

Primero, importe las clases requeridas en su proyecto Java:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## ¿Cómo exportar fuentes al guardar OneNote como HTML?

A continuación se muestra una guía paso a paso que le muestra **cómo exportar fuentes** y otros recursos.

### Paso 1: Crear un documento OneNote programáticamente  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Esta línea carga un archivo `.one` existente. Si necesita **crear OneNote programáticamente**, puede instanciar un nuevo objeto `Document` y agregar secciones/páginas mediante la API (no se muestra aquí para mantener el enfoque en la exportación de fuentes).

### Paso 2: Guardar en un flujo de memoria con fuentes incrustadas  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` indica a Aspose.Note que **exporte fuentes** directamente al paquete HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` asegura que se usen fuentes TrueType, que tienen amplio soporte en los navegadores.

### Paso 3: Guardar como HTML con archivos de recursos separados (manteniendo la exportación de fuentes)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Aunque CSS e imágenes están incrustados, puede cambiar `ResourceExportType` a `ExportExternal` si prefiere archivos separados para un almacenamiento en caché más sencillo. La parte clave—**exportar fuentes**—permanece sin cambios.

### Paso 4: Utilizar callbacks para controlar dónde se almacena cada recurso  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

La clase `UserSavingCallbacks` (deberá implementar `ICssSavingCallback`, `IImageSavingCallback` y `IFontSavingCallback`) le brinda control total sobre la estructura de carpetas, permitiéndole mantener las fuentes en un directorio dedicado `fonts` mientras sigue **exportando fuentes** correctamente.

## Problemas comunes y consejos

- **Fuentes faltantes en la salida:** Verifique que `setExportFonts(ResourceExportType.ExportEmbedded)` esté configurado y que el archivo OneNote de origen realmente use fuentes incrustadas.  
- **Archivos HTML grandes:** Incrustar fuentes puede aumentar el tamaño. Si el ancho de banda es una preocupación, cambie `ExportFonts` a `ExportExternal` y aloje las fuentes en un CDN.  
- **Errores en la implementación de callbacks:** Asegúrese de que sus clases de callback escriban correctamente el flujo y cierren los recursos para evitar corrupción de archivos.  

## Preguntas frecuentes

**P: ¿Puedo convertir varios documentos OneNote a HTML de una sola vez?**  
R: Sí, recorra cada instancia de `Document` y aplique las mismas `HtmlSaveOptions`.  

**P: ¿Aspose.Note for Java admite otros formatos de salida además de HTML?**  
R: Absolutamente. Puede exportar a PDF, DOCX, PNG, JPEG y más usando las opciones de guardado correspondientes.  

**P: ¿Existe una versión de prueba disponible para Aspose.Note for Java?**  
R: Sí, descargue una prueba gratuita desde [aquí](https://releases.aspose.com/).  

**P: ¿Dónde puedo obtener soporte para Aspose.Note for Java?**  
R: Visite el [foro de Aspose.Note](https://forum.aspose.com/c/note/28) para asistencia comunitaria y oficial.  

**P: ¿Cómo puedo comprar una licencia para Aspose.Note for Java?**  
R: Las licencias están disponibles en el [sitio web de Aspose](https://purchase.aspose.com/buy).  

## Conclusión

Ahora sabe **cómo exportar fuentes** mientras **guarda OneNote como HTML** usando Aspose.Note for Java. Configurando `HtmlSaveOptions` y, opcionalmente, usando callbacks, puede preservar el aspecto exacto de sus páginas de OneNote—incluidas las fuentes personalizadas—al entregarlas en la web. Siéntase libre de experimentar con diferentes configuraciones de `ResourceExportType` para adaptarse a los requisitos de rendimiento y almacenamiento de su proyecto.

---

**Última actualización:** 2025-12-02  
**Probado con:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
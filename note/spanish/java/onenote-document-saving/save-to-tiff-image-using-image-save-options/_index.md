---
date: 2025-12-17
description: Aprenda a guardar documentos de OneNote como archivos TIFF usando compresión
  TIFF JPEG, PackBits o CCITT Group 3 Fax en Java. Controle la calidad de la imagen,
  el tamaño del archivo y el modo de color con Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Guardar en imagen TIFF usando compresión JPEG TIFF en OneNote
url: /es/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar imagen TIFF usando compresión TIFF JPEG en OneNote

## Introducción

En este tutorial descubrirás **cómo guardar un documento de OneNote en un archivo TIFF usando compresión TIFF JPEG** y dos métodos de compresión populares adicionales. Revisaremos la configuración requerida, importaremos los paquetes Java necesarios y proporcionaremos código paso a paso claro para cada opción de compresión. Al final podrás controlar **la calidad de la imagen TIFF**, reducir el tamaño del archivo e incluso producir TIFF en blanco y negro para salida tipo fax.

## Respuestas rápidas
- **¿Qué es la compresión TIFF JPEG?** Un método de compresión con pérdida que reduce el tamaño del archivo TIFF mientras preserva la calidad visual.  
- **¿Qué biblioteca maneja la conversión?** Aspose.Note for Java.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para pruebas; se requiere una licencia para producción.  
- **¿Puedo cambiar la calidad de la imagen?** Sí, establece la propiedad `quality` en `ImageSaveOptions`.  
- **¿Es posible la conversión por lotes?** Absolutamente – recorre los documentos y aplica las mismas opciones.

## ¿Qué es la compresión TIFF JPEG?
La compresión TIFF JPEG almacena los datos de la imagen en el contenedor TIFF pero aplica el algoritmo con pérdida de JPEG para reducir el archivo. Es ideal cuando necesitas un equilibrio entre **la calidad de la imagen TIFF** y un tamaño de archivo más pequeño, especialmente para escenarios web o de archivo.

## ¿Por qué usar diferentes tipos de compresión TIFF?
- **JPEG** – Bueno para fotografías; ofrece calidad ajustable.  
- **PackBits** – Codificación simple sin pérdida de longitud de ejecución; útil para gráficos con áreas uniformes grandes.  
- **CCITT Group 3 Fax** – Solo y negro; perfecto para documentos escaneados y transmisión por fax.  

Elegir la compresión adecuada te permite cumplir con las limitaciones de almacenamiento sin sacrificar la fidelidad visual requerida para tu aplicación.

## Requisitos previos

- Java Development Kit (JDK) instalado.  
- Biblioteca Aspose.Note for Java añadida a tu proyecto (Maven/Gradle o JAR manual).  
- Familiaridad básica con la sintaxis de Java.

## Importar paquetes

Primero, trae las clases necesarias de Aspose.Note a tu archivo Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Paso 1: Guardar en TIFF usando compresión TIFF JPEG

A continuación se muestra el método completo que carga un archivo OneNote y lo guarda como TIFF con compresión JPEG. Ajusta el valor `quality` (0‑100) para controlar **la calidad de la imagen TIFF**.

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Explicación**

- `ImageSaveOptions` indica a Aspose.Note que genere un archivo TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` selecciona la compresión JPEG.  
- `setQuality(93)` (opcional) ajusta finamente la calidad de la imagen; valores más bajos producen archivos más pequeños.

### Cómo guardar TIFF con compresión JPEG en Java
1. Apunta `dataDir` a la carpeta que contiene tu archivo `.one`.  
2. Llama a `SaveToTiffUsingJpegCompression()` desde tu método principal o servicio.  
3. El archivo `.tiff` resultante aparecerá en el mismo directorio.

## Paso 2: Guardar en TIFF usando compresión PackBits

Si necesitas una opción sin pérdida, PackBits es un algoritmo simple de longitud de ejecución que funciona bien para gráficos con colores sólidos.

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Explicación**

- `setTiffCompression(TiffCompression.PackBits)` cambia el método de compresión.  
- No se necesita configurar la calidad porque PackBits es sin pérdida.

## Paso 3: Guardar en TIFF usando compresión CCITT Group 3 Fax (TIFF en blanco y negro)

Para documentos estilo fax a menudo deseas un **TIFF en blanco y negro**. CCITT Group 3 ofrece alta compresión para imágenes monocromáticas.

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Explicación**

- `setColorMode(ColorMode.BlackAndWhite)` fuerza una salida monocromática.  
- `setTiffCompression(TiffCompression.Ccitt3)` aplica la compresión orientada a fax.

## Problemas comunes y consejos

| Problema | Solución |
|----------|----------|
| **El archivo de salida es más grande de lo esperado** | Intenta reducir el valor `quality` de JPEG o cambia a PackBits si la compresión sin pérdida es aceptable. |
| **Los colores aparecen deslavados** | Asegúrate de no estar estableciendo inadvertidamente `ColorMode.BlackAndWhite` cuando necesitas color completo. |
| **Error de formato de imagen no compatible** | Verifica que estés usando una versión reciente de Aspose.Note; compilaciones antiguas pueden carecer de ciertos enums de compresión. |
| **LicenseException en tiempo de ejecución** | Instala una licencia válida de Aspose.Note (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Preguntas frecuentes

**P: ¿Puedo convertir otros tipos de documentos (p. ej., PDF, DOCX) a TIFF con estas opciones?**  
R: Sí. Aspose.Note se centra en archivos OneNote, pero las otras bibliotecas de Aspose (PDF, Words) proporcionan `ImageSaveOptions` similares para sus respectivos formatos.

**P: ¿En qué se diferencia la compresión TIFF JPEG de los archivos JPEG estándar?**  
R: Los datos de la imagen se almacenan dentro de un contenedor TIFF, preservando metadatos y permitiendo múltiples páginas, mientras que el algoritmo de compresión sigue siendo JPEG.

**P: ¿Es posible procesar por lotes muchos archivos `.one`?**  
R: Absolutamente. Recorre una carpeta, llama a cualquiera de los tres métodos por archivo y recopila los TIFF resultantes.

**P: ¿Puedo controlar el DPI/resolución del TIFF de salida?**  
R: Sí. Usa `options.setResolution(int dpi)` antes de guardar.

**P: ¿Aspose.Note admite procesamiento asíncrono?**  
R: La API en sí es síncrona, pero puedes envolver las llamadas en `CompletableFuture` de Java o en pools de hilos para ejecución paralela.

## Conclusión

Ahora tienes un conjunto completo de herramientas de **conversión tiff en java** que te permite guardar documentos OneNote como archivos TIFF usando compresión JPEG, PackBits o CCITT Group 3 Fax. Ajusta la calidad, el modo de color y la resolución para cumplir con tus requisitos específicos de **calidad de imagen TIFF**, e integra estos métodos en flujos de trabajo por lotes para máxima productividad.

---

**Última actualización:** 2025-12-17  
**Probado con:** Aspose.Note for Java 23.12 (última versión al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
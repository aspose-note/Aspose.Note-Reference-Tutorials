---
date: 2025-12-04
description: Aprenda a extraer imágenes de archivos OneNote y a convertir OneNote
  a texto en Java usando Aspose.Note. Guía paso a paso con ejemplos de código.
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Extraer imágenes de OneNote usando Document Visitor - Java
url: /es/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extraer imágenes de OneNote con Document Visitor - Java

## Introducción

Aspose.Note for Java facilita **extraer imágenes de cuadernos OneNote** así como leer el archivo subyacente `.one` en Java. En este tutorial le guiaremos paso a paso con un ejemplo completo y práctico que muestra cómo cargar un archivo OneNote, recorrer su estructura con un `DocumentVisitor` personalizado y obtener tanto imágenes como texto plano. Al final también sabrá cómo **convertir OneNote a texto** si solo necesita el contenido textual.

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.Note for Java (enlace de descarga a continuación).  
- **¿Puedo extraer solo imágenes?** Sí – implemente el método `VisitImageStart` en un `DocumentVisitor`.  
- **¿Cómo leo un archivo .one en Java?** Use `new Document(path, new LoadOptions())`.  
- **¿Necesito una licencia para producción?** Se requiere una licencia comercial para uso que no sea de prueba.  
- **¿Qué versión de Java es compatible?** JDK 8 o superior.

## Requisitos previos

Antes de comenzar, asegúrese de tener:

1. Java Development Kit (JDK) 8 o una versión más reciente instalada.  
2. Biblioteca Aspose.Note for Java descargada. Puede descargarla **[aquí](https://releases.aspose.com/note/java/)**.  
3. Un documento OneNote (archivo `.one`) del que desee extraer imágenes o convertir a texto.

## Importar paquetes

Primero, importe las clases necesarias de la API Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Paso 1: Configurar un Document Visitor personalizado

Cree una clase que extienda `DocumentVisitor`. Esta clase será invocada para cada nodo del documento OneNote, permitiéndole **extraer imágenes de OneNote** y, opcionalmente, recopilar texto.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Paso 2: Implementar los métodos del visitante

Agregue sobrescrituras para los tipos de nodo que le interesen. A continuación manejamos texto enriquecido, imágenes, títulos, páginas, esquemas y elementos de esquema. El método `VisitImageStart` es donde ocurre la extracción de la imagen.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### ¿Por qué implementar estos métodos?

- **Extraer imágenes de OneNote:** `VisitImageStart` le brinda acceso directo a los bytes crudos de la imagen.  
- **Convertir OneNote a texto:** `VisitRichTextStart` recopila el contenido textual, habilitando una operación simple de **convertir OneNote a texto**.  
- **Leer archivo .one en Java:** El patrón visitante abstrae la estructura subyacente del archivo `.one`, por lo que no necesita analizar el formato binario usted mismo.

## Paso 3: Ejecutar el visitante desde su método Main

Cargue el archivo `.one`, instancie su visitante y comience el recorrido.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Casos de uso comunes

- **Informes automatizados:** Extraiga imágenes y texto de un cuaderno OneNote de reuniones para generar un resumen en PDF o HTML.  
- **Migración de contenido:** Convierta archivos de OneNote heredados a archivos de texto plano para indexación o ingestión en motores de búsqueda.  
- **Extracción de activos digitales:** Recoja capturas de pantalla, diagramas o fotos incrustadas para reutilizarlas en otras aplicaciones.

## Solución de problemas y consejos

- **Cuadernos grandes:** Si encuentra problemas de memoria, procese las páginas individualmente verificando `VisitPageStart` y cargando recursos a nivel de página solo cuando sea necesario.  
- **Formatos de imagen:** El objeto `Image` devuelve bytes crudos; puede que necesite detectar el formato (PNG, JPEG) antes de guardarlo.  
- **Errores de licencia:** Asegúrese de haber establecido la licencia de Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) antes de cargar el documento en producción.

## Preguntas frecuentes

**P: ¿Puedo extraer tipos específicos de contenido del documento OneNote?**  
R: Sí – sobrescribiendo solo los métodos del visitante que necesite (por ejemplo, `VisitImageStart` para imágenes, `VisitRichTextStart` para texto).

**P: ¿Aspose.Note for Java es compatible con diferentes versiones de documentos OneNote?**  
R: Absolutamente. La biblioteca soporta todas las versiones principales de archivos OneNote, por lo que puede **leer archivo .one en Java** sin importar la versión original de OneNote.

**P: ¿Puedo integrar este proceso de extracción en mi aplicación Java?**  
R: Sí. El patrón visitante funciona sin problemas dentro de cualquier base de código Java; solo agregue el JAR de la biblioteca y llame al ejemplo mostrado arriba.

**P: ¿Aspose.Note for Java ofrece soporte para manejar documentos OneNote complejos?**  
R: Lo hace. Esquemas anidados, medios incrustados y datos personalizados están todos expuestos a través de la API del visitante.

**P: ¿Existe algún límite al tamaño del documento OneNote que se pueda procesar?**  
R: No hay un límite estricto, pero los cuadernos extremadamente grandes pueden requerir más memoria heap; considere procesarlos página por página.

**P: ¿Cómo convierto el texto extraído en un archivo de texto plano?**  
R: Después de que `myConverter.GetText()` devuelva un `String`, escríbalo a un archivo usando I/O estándar de Java (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Última actualización:** 2025-12-04  
**Probado con:** Aspose.Note for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
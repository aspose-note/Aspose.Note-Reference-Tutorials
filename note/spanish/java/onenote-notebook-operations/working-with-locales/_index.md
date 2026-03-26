---
date: 2026-01-05
description: Aprenda a establecer la configuración regional predeterminada, cargar
  un documento de OneNote, establecer la licencia de Aspose, convertir OneNote a PNG
  y guardar OneNote como imagen usando Aspose.Note para Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Establecer la configuración regional predeterminada en OneNote – Aspose.Note
  Java
url: /es/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer la configuración regional predeterminada en OneNote – Aspose.Note Java

## Introducción

Si necesitas **set default locale** mientras procesas archivos OneNote, Aspose.Note para Java lo hace muy fácil. En este tutorial recorreremos todo lo que necesitas—desde licenciar el producto hasta cargar un documento OneNote, cambiar la configuración regional y, finalmente, convertir el archivo a una imagen PNG. Al final, podrás personalizar la configuración de idioma y generar resultados específicos de la configuración regional con solo unas pocas líneas de código.

## Respuestas rápidas
- **¿Qué hace “set default locale”?** Define el idioma y el formato regional que Aspose.Note utiliza al leer o escribir archivos OneNote.  
- **¿Necesito una licencia?** Sí—establece la licencia de Aspose para desbloquear la funcionalidad completa.  
- **¿Qué versión de Java se requiere?** Cualquier JDK 8+ es compatible.  
- **¿Puedo convertir OneNote a PNG?** Absolutamente; la API permite guardar páginas como imágenes.  
- **¿El proceso es thread‑safe?** Establecer la configuración regional predeterminada es global, por lo que se configura una sola vez al iniciar la aplicación.

## ¿Qué es “set default locale” en Aspose.Note?
Establecer la configuración regional predeterminada le indica a Aspose.Note qué idioma y convenciones culturales aplicar al analizar fechas, números y texto. Esto es esencial para aplicaciones multirregionales que necesitan un formato consistente en diferentes configuraciones de usuario.

## ¿Por qué establecer la configuración regional predeterminada al trabajar con OneNote?
- **Representación de datos precisa:** Las fechas y los números aparecen correctamente para la audiencia objetivo.  
- **Cadenas de UI consistentes:** El texto extraído de OneNote respeta la configuración de idioma.  
- **Conversión simplificada:** Cuando conviertes posteriormente un archivo OneNote a PNG u otros formatos, el diseño visual coincide con la configuración regional esperada.

## Requisitos previos

- **Entorno de desarrollo Java:** JDK instalado y `JAVA_HOME` configurado.  
- **Biblioteca Aspose.Note:** Descarga el JAR más reciente desde el [download link](https://releases.aspose.com/note/java/).  
- **Un archivo de licencia válido de Aspose** (la prueba gratuita funciona para pruebas).

## Importar paquetes

Antes de escribir cualquier código, importa las clases que proporcionan la funcionalidad requerida.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Paso 1: Establecer la licencia de Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

Establecer la licencia de Aspose desbloquea todas las funciones, incluida la gestión de la configuración regional y la conversión de imágenes.

## Paso 2: Establecer la configuración regional predeterminada

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Aquí **set default locale** a inglés (`en`) con el código de país `rs`. Ajusta los códigos de idioma y país para que coincidan con tu región objetivo.

## Paso 3: Cargar documento OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Este paso **load(s) OneNote document** en el objeto `Document` para que puedas trabajar con su contenido.

## Paso 4: Convertir OneNote a PNG (conversión de archivo OneNote)

```java
oneFile.save("sample.png");
```

El método `save` realiza una **onenote file conversion**, exportando el cuaderno (o una página específica) como una imagen PNG—efectivamente **convert onenote to png** y **save onenote as image**.

## Problemas comunes y consejos

- **Licencia no encontrada:** Asegúrate de que la ruta a `licenseFile` sea correcta y que el archivo tenga permisos de lectura.  
- **Configuración regional no aplicada:** Llama a `Locale.setDefault` **antes** de cargar el documento.  
- **Salida de imagen faltante:** Verifica que el archivo OneNote contenga realmente páginas renderizables; los cuadernos vacíos producirán un PNG en blanco.

## Preguntas frecuentes

**P: ¿Aspose.Note es compatible con diferentes versiones de Java?**  
R: Sí, Aspose.Note soporta Java 8 y posteriores, garantizando una amplia compatibilidad en entornos de desarrollo.

**P: ¿Puedo integrar Aspose.Note con otras bibliotecas Java?**  
R: Absolutamente. La API funciona sin problemas con bibliotecas populares como Apache POI, Jackson y Spring.

**P: ¿Aspose.Note ofrece soporte para diferentes formatos de archivo?**  
R: Aunque su enfoque principal son los archivos OneNote, la biblioteca puede exportar a PNG, JPEG, PDF y otros formatos de imagen.

**P: ¿Existe un foro comunitario para usuarios de Aspose.Note donde buscar ayuda y compartir conocimientos?**  
R: Sí, el foro de la comunidad Aspose brinda una plataforma para que los usuarios interactúen con expertos, hagan preguntas y colaboren en soluciones. Visita el [support forum](https://forum.aspose.com/c/note/28) para obtener asistencia.

**P: ¿Puedo probar Aspose.Note antes de comprar?**  
R: Por supuesto, puedes explorar las capacidades de Aspose.Note aprovechando la prueba gratuita ofrecida en el sitio web.

## Conclusión

Al seguir estos pasos has aprendido cómo **set default locale**, **load OneNote document**, **set Aspose license** y **convert OneNote to PNG** usando Aspose.Note para Java. Este flujo de trabajo te permite generar informes y imágenes conscientes de la configuración regional que se adaptan a audiencias globales.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2026-01-05  
**Probado con:** Aspose.Note 24.11 for Java  
**Autor:** Aspose
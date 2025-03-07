---
title: Administrar licencia medida para OneNote en Java
linktitle: Administrar licencia medida para OneNote en Java
second_title: Aspose.Nota Java API
description: Aprenda a administrar licencias medidas para OneNote en Java usando la biblioteca Aspose.Note. Controle el uso, supervise los créditos y optimice los costos de manera eficiente.
weight: 10
url: /es/java/licensing-java/manage-metered-license/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Administrar licencia medida para OneNote en Java

## Introducción

En este tutorial, aprenderemos cómo administrar una licencia medida para OneNote usando Aspose.Note para Java. Las licencias medidas le permiten monitorear y controlar su uso en función de los créditos, lo que brinda una solución flexible y rentable.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

1.  Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su sistema. Puedes descargarlo desde[aquí](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
   
2. Biblioteca Aspose.Note para Java: debe tener la biblioteca Aspose.Note para Java. Puedes descargarlo desde el[sitio web](https://releases.aspose.com/note/java/).

## Importar paquetes

Primero, importe los paquetes necesarios a su proyecto Java:

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Paso 1: configurar la licencia medida

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

 En este paso, inicializamos el`Metered` class y configure la clave medida con sus claves públicas y privadas proporcionadas por Aspose.

## Paso 2: cargar el documento y realizar operaciones

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

 Aquí, cargamos el documento de OneNote desde el directorio especificado y lo guardamos como un archivo PDF. Asegúrese de reemplazar`"Your Document Directory"` con la ruta de su directorio real.

## Paso 3: Verificar el consumo

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Este paso recupera e imprime la cantidad de crédito y consumo antes y después de la operación.

## Conclusión

En este tutorial, aprendimos cómo administrar una licencia medida para OneNote en Java usando la biblioteca Aspose.Note. Las licencias medidas brindan flexibilidad y control sobre su uso, lo que garantiza rentabilidad y una gestión eficiente de los recursos.

## Preguntas frecuentes

### P1: ¿Qué es una licencia medida?

R1: Una licencia medida le permite monitorear y controlar su uso de una API o servicio en función de los créditos.
   
### P2: ¿Cómo obtengo una clave medida para los productos Aspose?

R2: Puede obtener una clave medida comprando una licencia en el sitio web de Aspose o solicitando una licencia temporal para fines de evaluación.
   
### P3: ¿Puedo utilizar una licencia medida para múltiples aplicaciones?

R3: Sí, una licencia medida se puede utilizar en múltiples aplicaciones, pero el consumo se agregará.
   
### P4: ¿Hay una prueba gratuita disponible para Aspose.Note para Java?

 R4: Sí, puedes descargar una prueba gratuita desde[aquí](https://releases.aspose.com/).
   
### P5: ¿Dónde puedo obtener soporte para Aspose.Note para Java?

 R5: Puede obtener soporte en los foros de la comunidad Aspose[aquí](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
title: Estrai immagini da un documento OneNote utilizzando Java
linktitle: Estrai immagini da un documento OneNote utilizzando Java
second_title: Aspose.Note API Java
description: Scopri come estrarre immagini da documenti OneNote utilizzando Java con la libreria Aspose.Note. Segui la nostra guida passo passo per un'estrazione delle immagini senza interruzioni.
weight: 14
url: /it/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Estrai immagini da un documento OneNote utilizzando Java

## introduzione

In questo tutorial ti guideremo attraverso il processo di estrazione delle immagini da un documento OneNote utilizzando Java con l'aiuto della libreria Aspose.Note.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1.  Java Development Kit (JDK): assicurati di avere Java installato sul tuo sistema. È possibile scaricarlo e installarlo da[sito web](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Libreria Aspose.Note: scarica e includi la libreria Aspose.Note nel tuo progetto Java. Puoi ottenerlo da[Link per scaricare](https://releases.aspose.com/note/java/).

## Importa pacchetti

Per iniziare, importa i pacchetti necessari:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Passaggio 1: caricare il documento

Innanzitutto, carica il documento OneNote utilizzando Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Passaggio 2: ottieni tutte le immagini

Successivamente, recupera tutte le immagini dal documento:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Passaggio 3: estrai le immagini

Scorri l'elenco delle immagini e salva ciascuna immagine in un file:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Conclusione

L'estrazione di immagini da un documento OneNote utilizzando Java può essere ottenuta senza problemi con la libreria Aspose.Note. Seguendo i passaggi descritti in questo tutorial, puoi recuperare facilmente immagini dai tuoi documenti per ulteriori elaborazioni o analisi.

## Domande frequenti

### Q1: posso estrarre immagini da documenti OneNote protetti da password?

A1: Sì, Aspose.Note supporta anche l'estrazione di immagini da documenti protetti da password.

### Q2: Aspose.Note è compatibile con diverse versioni di Java?

A2: Aspose.Note è compatibile con varie versioni di Java, garantendo flessibilità agli sviluppatori.

### Q3: posso estrarre immagini da più documenti OneNote in un'unica esecuzione?

A3: Assolutamente, puoi scorrere più documenti ed estrarre immagini da ciascuno di essi utilizzando Aspose.Note.

### Q4: Esistono limiti di dimensione per i documenti OneNote?

A4: Aspose.Note gestisce documenti di varie dimensioni in modo efficiente, garantendo l'assenza di limitazioni sulla dimensione del documento per l'estrazione delle immagini.

### Q5: Aspose.Note supporta l'estrazione di altri tipi di contenuto oltre alle immagini?

A5: Sì, oltre alle immagini, Aspose.Note consente l'estrazione di testo, allegati e altri tipi di contenuto dai documenti OneNote.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

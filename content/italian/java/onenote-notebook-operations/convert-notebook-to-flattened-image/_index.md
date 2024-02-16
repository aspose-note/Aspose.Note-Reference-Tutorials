---
title: Converti notebook in immagine appiattita in OneNote - Aspose.Note
linktitle: Converti notebook in immagine appiattita in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come convertire un taccuino in un'immagine appiattita in OneNote utilizzando Aspose.Note per Java. Conserva tutti gli elementi in un singolo file immagine senza sforzo.
type: docs
weight: 13
url: /it/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## introduzione

In questo tutorial ti guideremo attraverso il processo di conversione di un notebook in un'immagine appiattita in OneNote utilizzando Aspose.Note per Java. Ciò ti consente di salvare il tuo taccuino come file immagine, assicurando che tutti gli elementi siano conservati in un unico formato immagine.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.
2.  Aspose.Note per la libreria Java scaricata e configurata nel tuo progetto Java. È possibile scaricare la libreria da[Qui](https://releases.aspose.com/note/java/).
3. Conoscenza base della programmazione Java.

## Importa pacchetti

Per iniziare, è necessario importare i pacchetti necessari da Aspose.Note per Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Passaggio 1: impostare la directory dei documenti

Innanzitutto, definisci la directory in cui si trova il file del tuo notebook:

```java
String dataDir = "Your Document Directory";
```

 Sostituire`"Your Document Directory"` con il percorso del file del tuo notebook.

## Passaggio 2: caricare il taccuino

 Successivamente, carica il file del notebook utilizzando il file`Notebook` classe:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Assicurarsi di sostituire`"test.onetoc2"` con il nome del file del tuo notebook.

## Passaggio 3: imposta le opzioni di salvataggio dell'immagine

Ora imposta le opzioni per salvare il taccuino come immagine. Specificheremo il formato di salvataggio come PNG e imposteremo la risoluzione su 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

È possibile regolare la risoluzione in base alle proprie esigenze.

## Passaggio 4: appiattire il taccuino

Per garantire che tutti gli elementi siano unificati in un'unica immagine, impostare il file`flatten` opzione a`true`:

```java
saveOptions.setFlatten(true);
```

Ciò garantisce che l'immagine risultante mantenga il layout del tuo taccuino.

## Passaggio 5: salva l'immagine

Infine, salva il taccuino come immagine appiattita:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Sostituire`"ExportImageasFlattenedNotebook_out.png"` con il nome del file di output desiderato.

## Conclusione

In conclusione, utilizzando Aspose.Note per Java, puoi facilmente convertire il tuo notebook in un'immagine appiattita in OneNote. Questo processo garantisce che tutti gli elementi siano conservati in un unico formato immagine, facilitando la condivisione e la visualizzazione.

## Domande frequenti

### Q1: Posso regolare la risoluzione dell'immagine in uscita?

 R1: Sì, puoi regolare la risoluzione in base alle tue esigenze modificando il file`setResolution` parametro del metodo.

### Q2: Aspose.Note supporta altri formati di immagine per l'esportazione?

A2: Sì, Aspose.Note supporta vari formati di immagine come PNG, JPEG, BMP, ecc., per l'esportazione di notebook.

### Q3: Posso personalizzare ulteriormente l'immagine di output?

A3: Sì, Aspose.Note fornisce ampie opzioni per personalizzare l'immagine di output, incluse le dimensioni della pagina, l'orientamento e le impostazioni di qualità.

### Q4: È disponibile una versione di prova per Aspose.Note per Java?

 R4: Sì, puoi ottenere una versione di prova gratuita da[Qui](https://releases.aspose.com/).

### Q5: Dove posso trovare supporto per Aspose.Note per Java?

 A5: È possibile trovare supporto e risorse sul forum Aspose.Note[Qui](https://forum.aspose.com/c/note/28).
---
title: Converti un intervallo di pagine specifico in PDF in OneNote con Java
linktitle: Converti un intervallo di pagine specifico in PDF in OneNote con Java
second_title: Aspose.Note API Java
description: Scopri come convertire intervalli di pagine specifici da OneNote a PDF senza problemi con Aspose.Note per Java. Conserva la formattazione e il layout senza sforzo.
type: docs
weight: 11
url: /it/java/onenote-document-loading/convert-page-range-to-pdf/
---
## introduzione

OneNote è un potente strumento per organizzare le note, ma a volte potrebbe essere necessario esportare intervalli di pagine specifici in PDF per scopi di condivisione o archiviazione. In questo tutorial, ti guideremo attraverso il processo di conversione di un intervallo di pagine specifico in PDF utilizzando Aspose.Note per Java.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti:

1. Java Development Kit (JDK): assicurati di avere Java installato sul tuo sistema.
2.  Aspose.Note per Java: Scarica e installa Aspose.Note per Java da[Qui](https://releases.aspose.com/note/java/).
3. Documento OneNote di esempio: preparare un documento OneNote di esempio da cui si desidera estrarre l'intervallo di pagine specifico.

## Importa pacchetti

Nel tuo progetto Java, importa i pacchetti necessari per utilizzare Aspose.Note:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## Passaggio 1: caricare il documento OneNote

Carica il documento OneNote utilizzando Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

## Passaggio 2: inizializza le opzioni di salvataggio del PDF

Inizializza l'oggetto PdfSaveOptions e specifica l'indice e il conteggio della pagina:

```java
PdfSaveOptions opts = new PdfSaveOptions();
opts.setPageIndex(2);  // Indice della pagina iniziale
opts.setPageCount(3);  // Numero di pagine da includere
```

## Passaggio 3: salva come PDF

Salva l'intervallo di pagine specificato come file PDF:

```java
oneFile.save(dataDir + "ConvertSpecificPageRangeToPdf_out.pdf", opts);
System.out.println("File saved: " + dataDir + "ConvertSpecificPageRangeToPdf_out.pdf");
```

Congratulazioni! Hai convertito con successo un intervallo di pagine specifico da un documento OneNote a un PDF utilizzando Aspose.Note per Java.

## Conclusione

In questo tutorial, abbiamo imparato come convertire un intervallo di pagine specifico da un documento OneNote in PDF utilizzando Aspose.Note per Java. Questa funzionalità può essere utile per vari scopi come la condivisione di informazioni selettive o la creazione di copie di archivio.

## Domande frequenti

### Q1: Posso specificare più intervalli di pagine non contigue per la conversione?

A1: Sfortunatamente, Aspose.Note per Java attualmente supporta la conversione in PDF solo di intervalli di pagine contigue.

### Q2: Aspose.Note per Java conserva la formattazione del documento OneNote originale?

A2: Sì, Aspose.Note garantisce che la formattazione e il layout del documento OneNote originale siano preservati nel PDF generato.

### Q3: È possibile convertire documenti OneNote protetti da password in PDF?

A3: Aspose.Note per Java non supporta la conversione diretta di documenti OneNote protetti da password. È necessario rimuovere la protezione tramite password prima della conversione.

### Q4: Posso personalizzare l'aspetto del file PDF generato?

A4: Sì, puoi personalizzare vari aspetti come le dimensioni della pagina, l'orientamento e le impostazioni di intestazione/piè di pagina utilizzando le opzioni di salvataggio PDF di Aspose.Note.

### Q5: Aspose.Note per Java supporta la conversione batch di più documenti OneNote?

R5: Sì, puoi convertire in batch più documenti OneNote in PDF scorrendo ciascun documento e applicando il processo di conversione.
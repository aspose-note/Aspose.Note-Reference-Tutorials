---
title: Converti documento OneNote in immagine - Java
linktitle: Converti documento OneNote in immagine - Java
second_title: Aspose.Note API Java
description: Impara a convertire OneNote in immagine utilizzando Aspose.Note per Java. Segui semplici passaggi, carica il documento, inizializza le opzioni e salva come PNG.
type: docs
weight: 14
url: /it/java/onenote-document-loading/convert-to-image/
---
## introduzione

In questo tutorial, ti guideremo attraverso il processo di utilizzo di Aspose.Note per Java per convertire un documento OneNote in un'immagine. Suddivideremo ogni passaggio in istruzioni facili da seguire.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.
2.  Aspose.Note per la libreria Java. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/java/).

## Importa pacchetti

Innanzitutto, importa i pacchetti necessari nel tuo codice Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Ora suddividiamo il codice di esempio fornito in più passaggi:

## Passaggio 1: configura la directory dei documenti

Definisci la directory in cui si trova il tuo documento OneNote:

```java
String dataDir = "Your Document Directory";
```

 Sostituire`"Your Document Directory"` con il percorso del documento OneNote.

## Passaggio 2: caricare il documento

Carica il documento OneNote in Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Garantire`"Sample1.one"` corrisponde al nome del file di documento OneNote.

## Passaggio 3: inizializzare ImageSaveOptions

 Inizializza il`ImageSaveOptions` oggetto per specificare il formato di salvataggio:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Qui, stiamo salvando il documento come immagine PNG. Puoi scegliere altri formati come JPEG o BMP, se necessario.

## Passaggio 4: salva il documento come immagine

Salvare il documento caricato come immagine:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Questa riga salva il documento come immagine PNG con le opzioni specificate.

## Passaggio 5: stampa di conferma

Stampa un messaggio per confermare che il file è stato salvato:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Questa riga ti avvisa della conversione riuscita e della posizione del file immagine salvato.

## Conclusione

Seguendo i passaggi sopra descritti, puoi convertire facilmente un documento OneNote in un'immagine utilizzando Aspose.Note per Java. È un modo semplice ed efficace per gestire le conversioni di documenti nelle tue applicazioni Java.

## Domande frequenti

### Q1: posso convertire più documenti OneNote in una volta sola?

R1: Sì, puoi scorrere un elenco di documenti ed eseguire l'operazione di conversione per ciascun documento.

### Q2: Aspose.Note supporta altri formati di output oltre alle immagini?

A2: Sì, Aspose.Note supporta vari formati di output come PDF, HTML e Microsoft Word.

### Q3: Aspose.Note è compatibile con tutte le versioni dei file OneNote?

A3: Aspose.Note offre compatibilità con i file OneNote creati in diverse versioni di Microsoft OneNote.

### Q4: Posso personalizzare la risoluzione delle immagini di output?

A4: Sì, puoi regolare la risoluzione e altri parametri utilizzando le opzioni disponibili in Aspose.Note.

### Q5: Aspose.Note richiede la connettività Internet per la conversione dei documenti?

A5: No, Aspose.Note funziona localmente senza la necessità di una connessione Internet.
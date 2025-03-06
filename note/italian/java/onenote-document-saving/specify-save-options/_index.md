---
title: Specificare le opzioni di salvataggio in OneNote - Aspose.Note
linktitle: Specificare le opzioni di salvataggio in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come specificare le opzioni di salvataggio in OneNote utilizzando Aspose.Note per Java. Personalizza facilmente l'indice, il conteggio e le impostazioni di compressione delle pagine.
weight: 24
url: /it/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Specificare le opzioni di salvataggio in OneNote - Aspose.Note

## introduzione

In questo tutorial impareremo come specificare le opzioni di salvataggio in OneNote utilizzando Aspose.Note per Java. Aspose.Note è una potente libreria Java che consente agli sviluppatori di creare, manipolare e convertire documenti OneNote a livello di codice. Con Aspose.Note, puoi facilmente controllare varie opzioni di salvataggio per personalizzare l'output in base alle tue esigenze.

## Prerequisiti

Prima di iniziare, assicurati di possedere i seguenti prerequisiti:

1. Conoscenza base del linguaggio di programmazione Java.
2. JDK (Java Development Kit) installato sul tuo sistema.
3.  Aspose.Note per la libreria Java installata. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/java/).

## Importa pacchetti

Per iniziare, importa i pacchetti necessari nel tuo codice Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Suddividiamo l'esempio in più passaggi:

## Passaggio 1: caricare il documento OneNote

```java
// Il percorso della directory dei documenti.
String dataDir = "Your Document Directory";

// Caricare il documento in Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

 In questo passaggio specifichiamo il percorso del documento OneNote e lo carichiamo nel file`Document` oggetto.

## Passaggio 2: inizializza l'oggetto PdfSaveOptions

```java
// Inizializza l'oggetto PdfSaveOptions
PdfSaveOptions opts = new PdfSaveOptions();
```

 Qui inizializziamo a`PdfSaveOptions` oggetto che verrà utilizzato per specificare le opzioni per salvare il documento come PDF.

## Passaggio 3: imposta l'indice e il conteggio delle pagine

```java
// Imposta l'indice della pagina
opts.setPageIndex(2);

// Imposta il conteggio delle pagine
opts.setPageCount(3);
```

Queste righe impostano l'indice e il conteggio delle pagine da salvare. In questo esempio, stiamo salvando le pagine a partire dall'indice 2 e un totale di 3 pagine.

## Passaggio 4: specificare le impostazioni di compressione

```java
// Specificare la compressione, se richiesta
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Qui specifichiamo le impostazioni di compressione dell'immagine per il PDF. Impostiamo la compressione sul formato JPEG e specifichiamo la qualità JPEG al 90%.

## Passaggio 5: salva il documento con le opzioni

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Infine, salviamo il documento con le opzioni specificate. Il PDF di output verrà salvato nella posizione specificata con le opzioni specificate.

## Conclusione

In questo tutorial, abbiamo imparato come specificare le opzioni di salvataggio in OneNote utilizzando Aspose.Note per Java. Personalizzando le opzioni di salvataggio, puoi controllare vari aspetti del documento di output, come l'indice delle pagine, il conteggio e le impostazioni di compressione.

## Domande frequenti

### Q1: Aspose.Note può gestire documenti OneNote di grandi dimensioni?

A1: Sì, Aspose.Note è progettato per gestire in modo efficiente documenti OneNote di grandi dimensioni.

### Q2: Aspose.Note è compatibile con le ultime versioni Java?

A2: Sì, Aspose.Note è compatibile con le ultime versioni Java.

### Q3: posso convertire documenti OneNote in altri formati utilizzando Aspose.Note?

A3: Sì, Aspose.Note supporta la conversione di documenti OneNote in vari formati come PDF, DOCX e HTML.

### Q4: Aspose.Note fornisce supporto per la crittografia e la decrittografia dei documenti OneNote?

A4: Sì, Aspose.Note fornisce API per la crittografia e la decrittografia dei documenti OneNote.

### Q5: Aspose.Note è adatto per l'uso commerciale?

R5: Sì, Aspose.Note può essere utilizzato per scopi commerciali acquistando una licenza.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

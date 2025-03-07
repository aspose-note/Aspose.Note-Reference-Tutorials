---
title: Salva su immagine BMP utilizzando le opzioni di salvataggio immagine in OneNote
linktitle: Salva su immagine BMP utilizzando le opzioni di salvataggio immagine in OneNote
second_title: Aspose.Note API Java
description: Scopri come salvare documenti OneNote in immagini BMP a livello di codice utilizzando Aspose.Note per Java. Guida passo passo con esempi di codice.
weight: 16
url: /it/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva su immagine BMP utilizzando le opzioni di salvataggio immagine in OneNote

## introduzione

Aspose.Note per Java è una potente libreria che consente agli sviluppatori Java di lavorare con i file Microsoft OneNote a livello di codice. Con Aspose.Note per Java, puoi creare, manipolare e convertire documenti OneNote senza problemi. In questo tutorial, approfondiremo come salvare un documento OneNote in un'immagine BMP utilizzando le opzioni di salvataggio immagine fornite da Aspose.Note per Java.

## Prerequisiti

Prima di procedere con questo tutorial, assicurati di avere quanto segue:

1. Conoscenza base del linguaggio di programmazione Java.
2. JDK (Java Development Kit) installato sul tuo sistema.
3. Ambiente di sviluppo integrato (IDE) come Eclipse o IntelliJ IDEA.
4.  Aspose.Note per la libreria Java. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/java/).

## Importa pacchetti

Innanzitutto, devi importare i pacchetti necessari da Aspose.Note per Java per utilizzare le sue funzionalità. Aggiungi la seguente istruzione di importazione al tuo file Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

Ora suddividiamo l'esempio fornito in più passaggi:

## Passaggio 1: caricare il documento

```java
// Il percorso della directory dei documenti.
String dataDir = "Your Document Directory";

// Caricare il documento in Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

In questo passaggio specifichiamo il percorso della directory in cui si trova il nostro documento OneNote. Quindi, carichiamo il documento utilizzando il file`Document` classe fornita da Aspose.Note per Java.

## Passaggio 2: salva nell'immagine BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Salva il documento.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

 In questo passaggio specifichiamo il percorso di output per l'immagine BMP che verrà generata dal documento OneNote. Noi usiamo il`save` metodo del`Document` classe per salvare il documento come immagine BMP, fornendo il percorso di output e un'istanza di`ImageSaveOptions` con il desiderato`SaveFormat` (in questo caso,`SaveFormat.Bmp`).

## Conclusione

In questo tutorial, abbiamo imparato come salvare un documento OneNote in un'immagine BMP utilizzando Aspose.Note per Java. Seguendo la guida passo passo, puoi integrare perfettamente questa funzionalità nelle tue applicazioni Java, consentendoti di manipolare facilmente i documenti OneNote.

## Domande frequenti

### Q1: posso salvare documenti OneNote in altri formati di immagine oltre a BMP?

A1: Sì, puoi salvare documenti OneNote in vari formati di immagine come JPEG, PNG, GIF e TIFF utilizzando Aspose.Note per Java.

### Q2: Aspose.Note per Java supporta la conversione tra diversi formati di documenti?

A2: Sì, Aspose.Note per Java supporta la conversione tra documenti OneNote e altri formati come PDF, DOCX, HTML e altri.

### Q3: Aspose.Note per Java è compatibile con le ultime versioni di OneNote?

A3: Sì, Aspose.Note per Java viene regolarmente aggiornato per garantire la compatibilità con le ultime versioni di OneNote.

### Q4: posso manipolare il contenuto dei documenti OneNote a livello di codice utilizzando Aspose.Note per Java?

A4: Sì, è possibile manipolare il contenuto, la struttura e la formattazione dei documenti OneNote a livello di codice utilizzando Aspose.Note per Java.

### Q5: Aspose.Note per Java fornisce supporto tecnico?

 A5: Sì, Aspose fornisce supporto tecnico per i suoi prodotti. Puoi visitare il[Forum Aspose.Note](https://forum.aspose.com/c/note/28) per assistenza.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

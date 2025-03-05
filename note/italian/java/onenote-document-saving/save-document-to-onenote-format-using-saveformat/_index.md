---
title: Salva il documento su OneNote utilizzando SaveFormat - Aspose.Note
linktitle: Salva il documento su OneNote utilizzando SaveFormat - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come salvare i documenti nel formato OneNote utilizzando Aspose.Note per Java. Segui questo tutorial passo passo per una perfetta integrazione nelle tue applicazioni Java.
type: docs
weight: 12
url: /it/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---
## introduzione

Aspose.Note per Java è una potente libreria che consente agli sviluppatori di lavorare con i file Microsoft OneNote a livello di codice. Salvare un documento in formato OneNote utilizzando SaveFormat è un processo semplice. In questo tutorial, esamineremo i passaggi necessari per eseguire questa attività.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.
2.  Aspose.Note per la libreria Java scaricata. Puoi ottenerlo da[Qui](https://releases.aspose.com/note/java/).
3. Conoscenza di base del linguaggio di programmazione Java.

## Importa pacchetti

 Innanzitutto, devi importare i pacchetti necessari nel tuo progetto Java. Ciò include l'importazione di file`com.aspose.note` pacchetto per lavorare con le funzionalità Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Passaggio 1: impostare la directory dei documenti

Definisci la directory in cui si trova il tuo documento e dove desideri salvare il file di output.

```java
String dataDir = "Your Document Directory";
```

## Passaggio 2: caricare il documento

 Carica il documento nell'applicazione Java utilizzando il file`Document` classe fornita da Aspose.Note.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## Passaggio 3: salva il documento nel formato OneNote

Salvare il documento caricato nel formato OneNote utilizzando il file`save` metodo e specificando il formato del file di output desiderato come`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## Conclusione

In questo tutorial, abbiamo imparato come salvare un documento in formato OneNote utilizzando SaveFormat in Aspose.Note per Java. Seguendo questi semplici passaggi, puoi integrare perfettamente questa funzionalità nelle tue applicazioni Java.

## Domande frequenti

### Q1: Aspose.Note per Java è compatibile con tutte le versioni di Microsoft OneNote?

A1: Aspose.Note per Java supporta varie versioni di Microsoft OneNote, garantendo la compatibilità tra diversi ambienti.

### Q2: Posso provare Aspose.Note per Java prima di acquistarlo?

 A2: Sì, puoi scaricare una versione di prova gratuita di Aspose.Note per Java da[Qui](https://releases.aspose.com/).

### Q3: Dove posso trovare la documentazione per Aspose.Note per Java?

 A3: È possibile trovare la documentazione dettagliata per Aspose.Note per Java[Qui](https://reference.aspose.com/note/java/).

### Q4: Come posso ottenere supporto tecnico per Aspose.Note per Java?

 R4: Per assistenza tecnica e supporto, è possibile visitare il forum Aspose.Note[Qui](https://forum.aspose.com/c/note/28).

### Q5: È disponibile un'opzione di licenza temporanea per Aspose.Note per Java?

 A5: Sì, puoi ottenere una licenza temporanea per Aspose.Note per Java da[Qui](https://purchase.aspose.com/temporary-license/).
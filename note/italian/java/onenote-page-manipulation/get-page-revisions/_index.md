---
title: Ottieni revisioni di pagina in OneNote - Aspose.Note
linktitle: Ottieni revisioni di pagina in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come recuperare le revisioni delle pagine in OneNote utilizzando Aspose.Note per Java. Segui la nostra guida passo passo per monitorare in modo efficiente le modifiche.
type: docs
weight: 14
url: /it/java/onenote-page-manipulation/get-page-revisions/
---
## introduzione

OneNote è un potente strumento per organizzare e gestire le tue note, ma a volte è necessario tenere traccia delle modifiche e delle revisioni apportate alle tue pagine. Con Aspose.Note per Java, puoi facilmente recuperare le revisioni delle pagine a livello di codice. In questo tutorial ti guideremo attraverso il processo per ottenere revisioni di pagina in OneNote utilizzando Aspose.Note per Java.

## Prerequisiti

Prima di iniziare, assicurati di disporre dei seguenti prerequisiti:

### 1. Kit di sviluppo Java (JDK)

Assicurati di avere Java Development Kit (JDK) installato sul tuo sistema. È possibile scaricare e installare JDK dal sito Web Oracle.

### 2. Aspose.Note per Java

Scarica e installa Aspose.Note per Java dal file[Link per scaricare](https://releases.aspose.com/note/java/).

### 3. Esempio di documento OneNote

Preparare un documento OneNote di esempio (`Sample1.one`) che contiene le pagine da cui desideri recuperare le revisioni.

## Importa pacchetti

Innanzitutto, devi importare i pacchetti necessari da Aspose.Note per Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Ora suddividiamo l'esempio fornito in più passaggi:

## Passaggio 1: impostare la directory dei documenti

Definisci il percorso della directory in cui si trova il tuo documento OneNote.

```java
String dataDir = "Your Document Directory";
```

## Passaggio 2: carica il documento OneNote

 Caricare il documento OneNote utilizzando`LoadOptions` per abilitare la cronologia di caricamento.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Passaggio 3: ottieni la prima pagina

Recuperare la prima pagina dal documento caricato.

```java
Page firstPage = document.getFirstChild();
```

## Passaggio 4: scorrere le revisioni della pagina

Scorri ogni revisione della pagina e recupera informazioni rilevanti come l'ora dell'ultima modifica, l'ora di creazione, il titolo, il livello e l'autore.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Conclusione

In questo tutorial, abbiamo imparato come recuperare le revisioni delle pagine in OneNote utilizzando Aspose.Note per Java. Seguendo questi passaggi è possibile tenere traccia in modo efficiente delle modifiche apportate alle pagine OneNote a livello di codice.

## Domande frequenti

### Q1: posso utilizzare Aspose.Note per Java per modificare le revisioni delle pagine?

A1: No, Aspose.Note per Java attualmente supporta il recupero delle revisioni delle pagine ma non la loro modifica.

### Q2: Aspose.Note per Java è compatibile con diverse versioni di documenti OneNote?

A2: Sì, Aspose.Note per Java supporta varie versioni di documenti OneNote, consentendoti di lavorare senza problemi con diversi formati di file.

### Q3: Aspose.Note per Java richiede una licenza per l'utilizzo?

A3: Sì, è necessario acquistare una licenza per utilizzare Aspose.Note per Java in progetti commerciali. Tuttavia è anche possibile ottenere una licenza temporanea a scopo di valutazione.

### Q4: Posso chiedere supporto se riscontro problemi durante l'utilizzo di Aspose.Note per Java?

 A4: Sì, puoi chiedere supporto al forum Aspose.Note[Qui](https://forum.aspose.com/c/note/28).

### Q5: È disponibile una prova gratuita per Aspose.Note per Java?

 A5: Sì, puoi accedere a una prova gratuita di Aspose.Note per Java da[sito web](https://releases.aspose.com/).
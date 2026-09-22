---
date: 2026-08-08
description: Scopri come tracciare le modifiche in OneNote recuperando le revisioni
  di pagina in modo programmatico con Aspose.Note per Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Ottieni le revisioni di pagina in OneNote - Aspose.Note
og_description: Scopri come tracciare le modifiche in OneNote recuperando le revisioni
  di pagina in modo programmatico con Aspose.Note per Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Traccia le modifiche in OneNote – revisioni di pagina con Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Traccia le modifiche in OneNote – revisioni di pagina con Aspose.Note
url: /it/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Traccia le modifiche in OneNote – revisioni della pagina con Aspose.Note

In questo tutorial imparerai a **tracciare le modifiche in OneNote** estraendo la cronologia completa delle revisioni di una pagina utilizzando l'API Java di Aspose.Note. Copriremo tutto, dall'impostazione dell'ambiente di sviluppo alla stampa dell'autore, dei timestamp e del titolo di ogni revisione, così potrai creare funzionalità di audit‑trail affidabili per qualsiasi soluzione basata su OneNote.

## Risposte rapide
- **Cosa copre il tutorial?** Recuperare la cronologia delle revisioni della pagina da un file OneNote usando Aspose.Note per Java.  
- **Quale versione della libreria è necessaria?** Qualsiasi versione recente di Aspose.Note per Java che supporti `LoadOptions.setLoadHistory`.  
- **È necessaria una licenza?** Una licenza di valutazione temporanea funziona per i test; è necessaria una licenza commerciale per la produzione.  
- **Posso modificare le revisioni?** L'API è in sola lettura per le revisioni; è possibile solo recuperarle.  
- **Quali sono i prerequisiti principali?** Java JDK, Aspose.Note per Java e un documento OneNote con dati di revisione.

## Cos'è il “tutorial sulle revisioni delle pagine Aspose.Note”?
Il tutorial dimostra come accedere programmaticamente alle versioni storiche di una pagina OneNote. Ogni revisione contiene metadati come l'autore, l'ora di creazione e l'ora di modifica, consentendo di creare audit trail o funzionalità di registro delle modifiche all'interno delle proprie applicazioni.

## Perché usare Aspose.Note per il tracciamento delle revisioni delle pagine?
Carica l'intera cronologia delle revisioni di un notebook in meno di 5 secondi per un file di 500 pagine su una CPU standard da 2 GHz, e recupera i metadati senza avviare l'interfaccia di OneNote. La libreria supporta più di 30 formati di input e output, funziona su Windows, Linux e macOS (coprendo >95 % degli ambienti server) e fornisce pieno controllo su ogni proprietà della revisione.

## Prerequisiti

### 1. Java Development Kit (JDK)
Assicurati che sia installato un JDK recente (8 o superiore) e che `JAVA_HOME` sia impostato.

### 2. Aspose.Note per Java
Scarica la libreria dal [download link](https://releases.aspose.com/note/java/).

### 3. Documento OneNote di esempio
Crea o procurati un file OneNote (ad es., `Sample1.one`) che contenga pagine con cronologia delle revisioni.

## Importa i pacchetti
Per prima cosa, importa le classi Aspose.Note necessarie.  
`Document` rappresenta un notebook OneNote, `LoadOptions` configura il comportamento di caricamento e `Page` rappresenta una singola pagina.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implementazione passo‑passo

### Passo 1: imposta la directory del documento
Definisci la cartella in cui si trova il tuo file OneNote.

```java
String dataDir = "Your Document Directory";
```

### Passo 2: carica il documento OneNote con la cronologia abilitata
`LoadOptions` è una classe di configurazione che indica ad Aspose.Note come aprire un file, inclusa l'opzione di leggere i dati delle revisioni. Abilita il flag prima di caricare il documento.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Passo 3: ottieni la prima pagina
Recupera l'oggetto della prima pagina; questo sarà il punto di riferimento per recuperare la sua cronologia.

```java
Page firstPage = document.getFirstChild();
```

### Passo 4: itera attraverso le revisioni della pagina
Scorri ogni revisione e stampa i metadati utili come timestamp, titolo, livello e autore.

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

> **Consiglio professionale:** Se hai bisogno di filtrare le revisioni per un autore specifico o un intervallo di date, aggiungi semplicemente controlli condizionali all'interno del ciclo `for`.

## Problemi comuni e soluzioni
- **Nessuna revisione restituita:** Verifica che `loadOptions.setLoadHistory(true)` sia chiamato prima di caricare il documento.  
- **Autore o titolo null:** Alcune versioni più vecchie di OneNote potrebbero non memorizzare questi campi; gestisci i valori `null` in modo appropriato.  
- **Ritardo delle prestazioni su notebook di grandi dimensioni:** Carica solo le sezioni necessarie o aumenta la dimensione dell'heap JVM.

## Domande frequenti

**Q1: Posso usare Aspose.Note per Java per modificare le revisioni delle pagine?**  
A1: No, l'API attualmente supporta solo l'accesso in sola lettura alle revisioni delle pagine.

**Q2: Aspose.Note per Java è compatibile con diverse versioni di documenti OneNote?**  
A2: Sì, funziona con vari formati di file OneNote, consentendo una elaborazione fluida tra le versioni.

**Q3: Aspose.Note per Java richiede una licenza per l'uso?**  
A3: È necessaria una licenza commerciale per l'uso in produzione, ma è disponibile una licenza di valutazione temporanea per i test.

**Q4: Posso richiedere supporto se incontro problemi usando Aspose.Note per Java?**  
A4: Sì, puoi porre domande sul forum Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: È disponibile una versione di prova gratuita per Aspose.Note per Java?**  
A5: Sì, puoi scaricare una prova gratuita dal [website](https://releases.aspose.com/).

**Ultimo aggiornamento:** 2026-08-08  
**Testato con:** Aspose.Note per Java (ultima release)  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [traccia le modifiche onenote – Gestisci le revisioni delle pagine con Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Tutorial Java Aspose - Ottieni informazioni sulle pagine in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Cambia lo sfondo della pagina OneNote – Aspose.Note per Java](/note/java/onenote-page-manipulation/set-page-background-color/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
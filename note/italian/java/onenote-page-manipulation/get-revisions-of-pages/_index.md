---
date: 2026-01-10
description: Scopri come ottenere l'ora dell'ultima modifica e recuperare le revisioni
  delle pagine OneNote usando Aspose.Note per Java. Integra questo nelle tue applicazioni
  Java per una gestione efficiente dei documenti.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Come ottenere l'ora dell'ultima modifica delle pagine OneNote – Aspose.Note
url: /it/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ottieni revisioni delle pagine in OneNote - Aspose.Note

## Introduzione

In questo tutorial, otterrai **l'ora dell'ultima modifica** per le pagine all'interno di un documento OneNote ed esplorerai come recuperare l'intera cronologia delle revisioni utilizzando Aspose.Note per Java. Che tu stia costruendo un sistema di gestione dei documenti, auditando le modifiche, o semplicemente abbia bisogno di visualizzare quando una pagina è stata modificata l'ultima volta, questa guida ti mostra esattamente come estrarre queste informazioni programmaticamente.

## Risposte rapide
- **Cosa restituisce “get last modified time”?** Il timestamp dell'ultima modifica su una pagina OneNote.  
- **Quale classe fornisce la cronologia delle revisioni?** `PageHistory` tramite `Document.getPageHistory(Page)`.  
- **È necessaria una licenza per questa funzionalità?** Sì, è necessaria una licenza valida di Aspose.Note per l'uso in produzione.  
- **Quale versione di Java è supportata?** Java 8 o superiore (JDK 8+).  
- **Posso filtrare le revisioni per autore?** Puoi leggere la proprietà `Author` di ogni oggetto `Page` e applicare il tuo filtro.

## Cos'è “get last modified time” in OneNote?

Il **tempo dell'ultima modifica** è un campo di metadati memorizzato con ogni pagina che registra quando la pagina è stata modificata più recentemente. Aspose.Note espone questo valore tramite il metodo `Page.getLastModifiedTime()`, rendendo semplice visualizzare o registrare le date di modifica.

## Perché recuperare le revisioni delle pagine?

- **Tracce di audit:** Mantieni un registro di chi ha cambiato cosa e quando.  
- **Confronto versioni:** Crea funzionalità che confrontano due revisioni fianco a fianco.  
- **Approfondimenti sulla collaborazione degli utenti:** Comprendi i pattern di modifica nei taccuini condivisi.  

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

### Java Development Kit (JDK) installato
Installa JDK 8 o successivo dal sito Oracle o dal tuo gestore di pacchetti preferito.

### Libreria Aspose.Note per Java
Scarica la libreria dal sito ufficiale. Puoi trovare il link per il download **[qui](https://releases.aspose.com/note/java/)**. Segui le istruzioni di installazione nella documentazione **[qui](https://reference.aspose.com/note/java/)**.

## Importa pacchetti

Per iniziare, importa i pacchetti necessari nel tuo progetto Java. Questi pacchetti ti permetteranno di sfruttare le funzionalità offerte da Aspose.Note per Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Ora, analizziamo il codice di esempio fornito in più passaggi per comprendere ogni componente e la sua funzionalità.

## Come ottenere l'ora dell'ultima modifica di una pagina OneNote

### Passo 1: Imposta la directory del documento
Definisci la directory in cui si trova il tuo documento OneNote.

```java
String dataDir = "Your Document Directory";
```

### Passo 2: Carica il documento
Carica il documento OneNote in Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Passo 3: Ottieni la prima pagina
Recupera la prima pagina dal documento.

```java
Page firstPage = doc.getFirstChild();
```

### Passo 4: Ottieni le revisioni della pagina
Ottieni la cronologia delle revisioni della pagina.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Passo 5: Scorri le revisioni della pagina
Itera attraverso l'elenco delle revisioni della pagina e recupera le informazioni rilevanti, inclusa la **data dell'ultima modifica**.

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

## Problemi comuni e soluzioni
- **`PageHistory` nullo:** Assicurati che il documento contenga effettivamente revisioni; altrimenti `getPageHistory` potrebbe restituire `null`.  
- **Differenze di fuso orario:** `getLastModifiedTime()` restituisce un `java.util.Date` nel fuso orario predefinito del sistema. Converti a UTC se necessario.  
- **Licenza non caricata:** Senza una licenza valida, Aspose.Note può operare in modalità di valutazione, limitando il numero di pagine elaborate.

## Domande frequenti

### Q1: Posso usare Aspose.Note per Java per creare nuovi documenti OneNote?
R1: Sì, Aspose.Note per Java offre un supporto completo per creare, leggere e manipolare documenti OneNote in modo programmatico.

### Q2: Aspose.Note per Java è compatibile con diverse versioni dei file OneNote?
R2: Sì, Aspose.Note per Java supporta varie versioni dei file Microsoft OneNote, garantendo compatibilità su diversi ambienti.

### Q3: Posso personalizzare il formato di output quando esporti documenti OneNote?
R3: Assolutamente, Aspose.Note per Java offre flessibilità nell'esportare documenti OneNote in diversi formati come PDF, HTML e immagini, con opzioni di personalizzazione.

### Q4: Aspose.Note per Java richiede una licenza per uso commerciale?
R4: Sì, è necessaria una licenza valida per l'uso commerciale di Aspose.Note per Java. Puoi ottenere una licenza dal sito web di Aspose.

### Q5: Dove posso cercare assistenza se incontro problemi o ho domande su Aspose.Note per Java?
R5: Per supporto e assistenza, puoi visitare il forum Aspose.Note **[qui](https://forum.aspose.com/c/note/28)**, dove puoi fare domande, condividere esperienze e interagire con altri utenti ed esperti.

---

**Ultimo aggiornamento:** 2026-01-10  
**Testato con:** Aspose.Note for Java 23.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
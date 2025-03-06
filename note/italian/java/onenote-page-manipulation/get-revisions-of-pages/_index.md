---
title: Ottieni revisioni di pagine in OneNote - Aspose.Note
linktitle: Ottieni revisioni di pagine in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come recuperare le revisioni delle pagine all'interno dei documenti OneNote utilizzando Aspose.Note Java. Integralo nelle tue app Java per una gestione efficiente dei documenti.
weight: 15
url: /it/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ottieni revisioni di pagine in OneNote - Aspose.Note

## introduzione

In questo tutorial, approfondiremo le funzionalità di Aspose.Note per Java, una potente libreria che ti consente di lavorare senza problemi con i file Microsoft OneNote nelle tue applicazioni Java. Nello specifico, ci concentreremo su come recuperare le revisioni delle pagine all'interno di un documento OneNote. Al termine di questa guida avrai acquisito le conoscenze necessarie per estrarre in modo efficiente le revisioni delle pagine, inclusi dettagli come l'ora dell'ultima modifica, l'ora di creazione, il titolo, il livello e l'autore.

## Prerequisiti

Prima di immergerti in questo tutorial, assicurati di aver impostato i seguenti prerequisiti:

### Kit di sviluppo Java (JDK) installato

Assicurati di avere il Java Development Kit installato sul tuo sistema. Puoi scaricarlo e installarlo dal sito Web Oracle o utilizzare un gestore pacchetti se utilizzi un sistema basato su Unix.

### Aspose.Note per la libreria Java

 Scaricare e installare Aspose.Note per la libreria Java dal sito Web. È possibile trovare il collegamento per il download[Qui](https://releases.aspose.com/note/java/) . Seguire le istruzioni di installazione fornite nella documentazione[Qui](https://reference.aspose.com/note/java/).

## Importa pacchetti

Per iniziare, importa i pacchetti necessari nel tuo progetto Java. Questi pacchetti ti permetteranno di sfruttare le funzionalità fornite da Aspose.Note per Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Ora suddividiamo il codice di esempio fornito in più passaggi per comprendere ciascun componente e la sua funzionalità.

## Passaggio 1: imposta la directory dei documenti

Definisci la directory in cui si trova il tuo documento OneNote.

```java
String dataDir = "Your Document Directory";
```

## Passaggio 2: caricare il documento

Caricare il documento OneNote in Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Passaggio 3: ottieni la prima pagina

Recuperare la prima pagina dal documento.

```java
Page firstPage = doc.getFirstChild();
```

## Passaggio 4: ottieni le revisioni della pagina

Ottieni la cronologia delle revisioni della pagina.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Passaggio 5: attraversa le revisioni delle pagine

Scorri l'elenco delle revisioni della pagina e recupera le informazioni pertinenti.

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

## Conclusione

In questo tutorial, abbiamo esplorato come recuperare le revisioni delle pagine all'interno di un documento OneNote utilizzando Aspose.Note per Java. Seguendo la guida passo passo e sfruttando il codice di esempio fornito, puoi facilmente integrare questa funzionalità nelle tue applicazioni Java, consentendo una gestione efficiente dei file OneNote.

## Domande frequenti

### Q1: posso utilizzare Aspose.Note per Java per creare nuovi documenti OneNote?

A1: Sì, Aspose.Note per Java fornisce supporto completo per la creazione, la lettura e la manipolazione dei documenti OneNote a livello di codice.

### Q2: Aspose.Note per Java è compatibile con diverse versioni di file OneNote?

A2: Sì, Aspose.Note per Java supporta varie versioni di file Microsoft OneNote, garantendo la compatibilità tra diversi ambienti.

### Q3: posso personalizzare il formato di output durante l'esportazione di documenti OneNote?

A3: Assolutamente, Aspose.Note per Java offre flessibilità nell'esportazione di documenti OneNote in diversi formati come PDF, HTML e immagini, con opzioni di personalizzazione.

### Q4: Aspose.Note per Java richiede una licenza per uso commerciale?

A4: Sì, è necessaria una licenza valida per l'uso commerciale di Aspose.Note per Java. È possibile ottenere una licenza dal sito Web Aspose.

### Q5: Dove posso chiedere assistenza se riscontro problemi o ho domande su Aspose.Note per Java?

 R5: Per supporto e assistenza, è possibile visitare il forum Aspose.Note[Qui](https://forum.aspose.com/c/note/28)dove puoi porre domande, condividere esperienze e interagire con altri utenti ed esperti.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

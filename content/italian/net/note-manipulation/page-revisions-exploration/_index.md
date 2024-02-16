---
title: Esplora le revisioni delle pagine nei documenti Aspose.Note
linktitle: Esplora le revisioni delle pagine nei documenti Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come esplorare le revisioni delle pagine nei documenti Aspose.Note utilizzando .NET Framework con una guida passo passo.
type: docs
weight: 14
url: /it/net/note-manipulation/page-revisions-exploration/
---
## introduzione

In questo tutorial, approfondiremo l'esplorazione delle revisioni delle pagine nei documenti Aspose.Note utilizzando il framework .NET. Aspose.Note è una potente libreria che consente agli sviluppatori di lavorare con i file Microsoft OneNote a livello di codice, offrendo varie funzionalità per manipolare ed estrarre dati da questi file.

## Prerequisiti

Prima di iniziare, assicurati di aver configurato i seguenti prerequisiti:

### 1. Scarica e installa Aspose.Note per .NET

 Visitare il[pagina di download](https://releases.aspose.com/note/net/) e scarica la libreria Aspose.Note per .NET. Seguire le istruzioni di installazione fornite per configurare la libreria nel proprio ambiente di sviluppo.

### 2. Caricare gli spazi dei nomi necessari

Assicurati di importare gli spazi dei nomi richiesti nel tuo progetto .NET per accedere alle funzionalità Aspose.Note senza problemi.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Ora suddividiamo il processo di esplorazione delle revisioni delle pagine in istruzioni dettagliate:

## Passaggio 1: caricare il documento

Innanzitutto, dobbiamo caricare il documento Aspose.Note, assicurandoci di abilitare il caricamento della cronologia del documento.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## Passaggio 2: recuperare le revisioni della pagina

Una volta caricato il documento, possiamo recuperare le revisioni per una pagina specifica. In questo esempio, otterremo le revisioni per la prima pagina.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Passaggio 3: ripetere le revisioni

All'interno del ciclo, esegui l'iterazione di ogni revisione della pagina e accedi alle sue proprietà come l'ora dell'ultima modifica, l'ora di creazione, il titolo, il livello e l'autore.

## Conclusione

Esplorare le revisioni delle pagine nei documenti Aspose.Note utilizzando .NET è un processo semplice. Seguendo i passaggi descritti in questo tutorial, puoi recuperare e analizzare in modo efficace la cronologia delle revisioni dei tuoi file OneNote a livello di codice.

## Domande frequenti

### Q1: posso utilizzare Aspose.Note per .NET per creare nuovi documenti OneNote?

A1: Sì, Aspose.Note per .NET consente di creare, modificare e manipolare documenti OneNote a livello di codice.

### Q2: Aspose.Note supporta la cronologia di caricamento per tutti i tipi di file OneNote?

A2: Aspose.Note supporta il caricamento della cronologia per entrambi i formati di file .one e .onepkg.

### Q3: È disponibile una prova gratuita per Aspose.Note per .NET?

A3: Sì, puoi scaricare una versione di prova gratuita di Aspose.Note per .NET da[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere una licenza temporanea per Aspose.Note per .NET?

 R4: Puoi richiedere una licenza temporanea da[questo link](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare supporto per Aspose.Note per .NET?

 R5: Puoi trovare supporto e risorse su[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
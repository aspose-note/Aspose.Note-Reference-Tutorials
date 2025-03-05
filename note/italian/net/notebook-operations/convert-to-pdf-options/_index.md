---
title: Converti taccuini in PDF con le opzioni in Aspose Note .NET
linktitle: Converti taccuini in PDF con le opzioni in Aspose Note .NET
second_title: Aspose.Note API .NET
description: Scopri come convertire i taccuini Microsoft OneNote in formato PDF utilizzando la libreria Aspose.Note per .NET con opzioni personalizzabili.
type: docs
weight: 16
url: /it/net/notebook-operations/convert-to-pdf-options/
---
## introduzione

In questo tutorial, esamineremo il processo di conversione dei notebook in formato PDF utilizzando la libreria Aspose.Note per .NET. Aspose.Note per .NET fornisce un potente set di funzionalità per lavorare con i file Microsoft OneNote a livello di codice.

## Prerequisiti

Prima di iniziare, assicurati di possedere i seguenti prerequisiti:

### 1. Aspose.Note per la libreria .NET
 Assicurati di aver scaricato e installato la libreria Aspose.Note per .NET. Puoi scaricarlo da[sito web](https://releases.aspose.com/note/net/).

### 2. Ambiente di sviluppo
Dovresti avere un ambiente di sviluppo configurato, come Visual Studio, con installato il framework .NET necessario.

## Importa spazi dei nomi

Prima di iniziare a utilizzare Aspose.Note per .NET nel nostro progetto, importiamo gli spazi dei nomi richiesti:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Ora suddividiamo il processo di conversione dei taccuini in PDF con opzioni in più passaggi:

## Passaggio 1: caricare il notebook

Per prima cosa dobbiamo caricare il taccuino OneNote che vogliamo convertire in un file PDF.

```csharp
// Il percorso della directory dei documenti.
string dataDir = "Your Document Directory";

// Carica un blocco appunti di OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Passaggio 2: specificare le opzioni di salvataggio del PDF

Successivamente, specificheremo le opzioni per salvare il notebook come file PDF. Possiamo personalizzare varie impostazioni come l'algoritmo di suddivisione della pagina, i margini e le dimensioni della pagina.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## Passaggio 3: salva il taccuino come PDF

Ora salveremo il taccuino come file PDF utilizzando le opzioni specificate.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Salva il taccuino
notebook.Save(dataDir, notebookSaveOptions);
```

## Passaggio 4: verifica la conversione

Infine, verifichiamo che la conversione sia andata a buon fine e stampiamo il percorso in cui è salvato il file PDF.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Conclusione

In questo tutorial, abbiamo imparato come convertire i taccuini OneNote in formato PDF utilizzando la libreria Aspose.Note per .NET. Seguendo i passaggi sopra descritti, puoi facilmente integrare questa funzionalità nelle tue applicazioni .NET.

## Domande frequenti

### Q1: Aspose.Note per .NET è compatibile con tutte le versioni di Microsoft OneNote?

A1: Sì, Aspose.Note per .NET supporta varie versioni di Microsoft OneNote, inclusi i formati .one e .onetoc2.

### Q2: Posso personalizzare l'aspetto dell'output PDF?

R2: Sì, puoi specificare varie opzioni come dimensioni della pagina, margini e algoritmo di divisione della pagina per personalizzare l'aspetto dell'output PDF.

### Q3: Aspose.Note per .NET fornisce supporto per altri formati di file?

A3: Sì, Aspose.Note per .NET supporta la conversione in vari altri formati come immagini, HTML e documenti Microsoft Word.

### Q4: È disponibile una prova gratuita per Aspose.Note per .NET?

R4: Sì, è possibile scaricare una prova gratuita di Aspose.Note per .NET dal sito Web per valutarne le funzionalità prima di effettuare un acquisto.

### Q5: Come posso ottenere supporto tecnico per Aspose.Note per .NET?

 A5: È possibile ottenere supporto tecnico per Aspose.Note per .NET visitando il sito[Forum Aspose.Note](https://forum.aspose.com/c/note/28) o contattando direttamente il team di supporto Aspose.
---
title: Converti taccuini in PDF (appiattito) in Aspose Note .NET
linktitle: Converti taccuini in PDF (appiattito) in Aspose Note .NET
second_title: Aspose.Note API .NET
description: Scopri come convertire i taccuini OneNote in PDF appiattiti senza sforzo utilizzando Aspose.Note per .NET. Conserva i tuoi contenuti senza problemi.
weight: 15
url: /it/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti taccuini in PDF (appiattito) in Aspose Note .NET

## introduzione

Stai cercando di convertire i tuoi taccuini OneNote in PDF appiattiti utilizzando Aspose Note .NET? Sei nel posto giusto! In questo tutorial, seguiremo il processo passo dopo passo.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1.  Aspose.Note per .NET: assicurati di aver scaricato e installato Aspose.Note per .NET. In caso contrario, puoi ottenerlo da[Qui](https://releases.aspose.com/note/net/).
2. Visual Studio: avrai bisogno di Visual Studio installato sul tuo sistema per la codifica e la compilazione.
3. Blocco appunti di OneNote: tenere pronto un blocco appunti di OneNote che si desidera convertire in PDF.

## Importa spazi dei nomi

Iniziamo importando gli spazi dei nomi necessari nel codice C#:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Passaggio 1: caricare il blocco appunti di OneNote

```csharp
// Il percorso della directory dei documenti.
string dataDir = "Your Document Directory";

// Carica un blocco appunti di OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 In questo passaggio, carichiamo il blocco appunti di OneNote utilizzando il file`Notebook` classe fornita da Aspose.Note.

## Passaggio 2: converti in PDF con appiattimento

```csharp
// Salva il taccuino come PDF con appiattimento
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Qui salviamo il taccuino caricato come PDF con il file`Flatten` proprietà impostata su`true`. Questa proprietà appiattisce tutto il contenuto, comprese annotazioni e immagini, nel PDF.

## Passaggio 3: stampare il messaggio di successo

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Infine, stampiamo un messaggio di successo insieme al percorso in cui viene salvato il PDF.

## Conclusione

Congratulazioni! Hai convertito con successo il tuo blocco note OneNote in un PDF appiattito utilizzando Aspose.Note per .NET. Questo processo garantisce che tutti i tuoi contenuti siano conservati accuratamente nel formato PDF, facilitandone la condivisione e la distribuzione.

## Domande frequenti

### Q1: Posso conservare gli elementi interattivi nel PDF?

A1: Aspose.Note appiattisce il contenuto, inclusi elementi interattivi come caselle di controllo o campi modulo, nel PDF, rendendoli statici.

### Q2: Aspose.Note supporta la conversione di notebook in altri formati?

A2: Sì, Aspose.Note supporta la conversione di notebook in vari formati come PDF, HTML, Immagine e altro.

### Q3: Posso personalizzare le opzioni di conversione?

A3: Assolutamente! Aspose.Note fornisce ampie opzioni per la personalizzazione durante il processo di conversione, consentendoti di personalizzare l'output in base alle tue esigenze.

### Q4: È disponibile una versione di prova?

 A4: Sì, puoi ottenere una prova gratuita di Aspose.Note da[Qui](https://releases.aspose.com/).

### Q5: Dove posso ottenere supporto se riscontro problemi?

 R5: Puoi chiedere supporto alla comunità Aspose all'indirizzo[Aspose.Note forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

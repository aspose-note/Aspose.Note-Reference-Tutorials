---
title: Applica punti elenco sul testo in Aspose.Note
linktitle: Applica punti elenco sul testo in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come applicare punti elenco sul testo in Aspose.Note per .NET per migliorare i tuoi documenti OneNote. Segui questa guida passo passo per una formattazione efficace.
type: docs
weight: 10
url: /it/net/text-manipulation/apply-bullets-on-text/
---
## introduzione
Benvenuti in questa guida passo passo sull'applicazione di punti elenco al testo utilizzando Aspose.Note per .NET. Aspose.Note è una potente libreria che consente agli sviluppatori di lavorare senza problemi con i file Microsoft OneNote nelle loro applicazioni .NET. In questo tutorial ti guideremo attraverso il processo di applicazione dei punti elenco al testo, migliorando l'impatto visivo dei tuoi documenti OneNote.
## Prerequisiti
Prima di immergerci nel tutorial, assicurati di possedere i seguenti prerequisiti:
- Conoscenza base di programmazione C# e .NET.
-  Aspose.Note per la libreria .NET installata. Puoi scaricarlo[Qui](https://releases.aspose.com/note/net/).
## Importa spazi dei nomi
Nel codice C# assicurati di includere gli spazi dei nomi necessari:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Passaggio 1: imposta il documento
```csharp
// Il percorso della directory dei documenti.
string dataDir = "Your Document Directory";
//Crea un oggetto della classe Document
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Passaggio 2: inizializza pagina e struttura
```csharp
// Inizializza l'oggetto classe Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inizializza l'oggetto della classe Outline
Outline outline = new Outline(doc);
```
## Passaggio 3: imposta lo stile di testo predefinito
```csharp
// Inizializza l'oggetto della classe TextStyle e imposta le proprietà di formattazione
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Passaggio 4: crea elementi di contorno con punti elenco
```csharp
// Inizializza gli oggetti della classe OutlineElement e applica i punti elenco
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Ripeti per gli altri elementi del contorno
```
## Passaggio 5: aggiungi elementi di contorno alla struttura
```csharp
// Aggiungi elementi di contorno
outline.AppendChildLast(outlineElem1);
// Ripeti per gli altri elementi del contorno
```
## Passaggio 6: aggiungi la struttura alla pagina
```csharp
// Aggiungi nodo Contorno
page.AppendChildLast(outline);
```
## Passaggio 7: aggiungi la pagina al documento
```csharp
//Aggiungi nodo Pagina
doc.AppendChildLast(page);
```
## Passaggio 8: salva il documento OneNote
```csharp
// Salva il documento OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Conclusione
Congratulazioni! Hai imparato con successo come applicare i punti elenco al testo utilizzando Aspose.Note per .NET. Questa funzionalità può migliorare in modo significativo la formattazione dei tuoi documenti OneNote, rendendoli visivamente più accattivanti.
## Domande frequenti
### Posso applicare stili di punti elenco diversi a ciascun elemento dell'elenco?
 Sì, puoi personalizzare gli stili dei punti elenco modificando il file`NumberList` proprietà per ciascuno`OutlineElement`.
### Aspose.Note è compatibile con l'ultima versione di Microsoft OneNote?
Aspose.Note supporta varie versioni di Microsoft OneNote, garantendo la compatibilità sia con le versioni precedenti che con quelle più recenti.
### Posso utilizzare Aspose.Note per scopi commerciali?
 Sì, puoi utilizzare Aspose.Note per .NET in progetti commerciali. Per ottenere una licenza, visitare[Qui](https://purchase.aspose.com/buy).
### È disponibile una versione di prova per Aspose.Note per .NET?
 Sì, puoi scaricare una versione di prova gratuita[Qui](https://releases.aspose.com/).
### Dove posso trovare ulteriore supporto e risorse?
 È possibile visitare il forum della comunità Aspose.Note[Qui](https://forum.aspose.com/c/note/28) per supporto e discussioni.
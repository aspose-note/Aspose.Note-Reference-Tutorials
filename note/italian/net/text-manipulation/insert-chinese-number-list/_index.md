---
title: Inserisci l'elenco dei numeri cinesi nel testo Aspose.Note
linktitle: Inserisci l'elenco dei numeri cinesi nel testo Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come inserire elenchi di numeri cinesi in Aspose.Note per documenti .NET senza sforzo. Migliora le tue capacità di formattazione dei documenti con questa guida passo passo.
type: docs
weight: 20
url: /it/net/text-manipulation/insert-chinese-number-list/
---
## introduzione
Stai cercando di migliorare le tue competenze in Aspose.Note per .NET incorporando elenchi di numeri cinesi nei tuoi documenti? Se è così, sei nel posto giusto! In questo tutorial ti guideremo attraverso il processo di inserimento degli elenchi di numeri cinesi utilizzando Aspose.Note per .NET. Questa potente libreria ti consente di manipolare i documenti OneNote senza problemi.
## Prerequisiti
Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:
- Conoscenza base della programmazione C#.
-  Aspose.Note per .NET installato. Puoi scaricarlo[Qui](https://releases.aspose.com/note/net/).
## Importa spazi dei nomi
Per iniziare, importa gli spazi dei nomi necessari nel tuo progetto:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Passaggio 1: inizializza il documento OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Passaggio 2: inizializza la pagina OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Passaggio 3: applica le impostazioni dello stile del testo
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Passaggio 4: crea elementi di contorno
Ora creiamo tre elementi di contorno con elenchi di numeri cinesi:
### Passaggio 4.1: Primo Elemento
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Passaggio 4.2: Secondo elemento
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Passaggio 4.3: Terzo Elemento
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Passaggio 5: aggiungi elementi alla struttura
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Passaggio 6: aggiungi la struttura alla pagina
```csharp
page.AppendChildLast(outline);
```
## Passaggio 7: aggiungi la pagina al documento
```csharp
doc.AppendChildLast(page);
```
## Passaggio 8: salva il documento OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Congratulazioni! Hai inserito con successo gli elenchi di numeri cinesi nel tuo documento Aspose.Note utilizzando la libreria .NET.
## Conclusione
In questo tutorial, abbiamo trattato il processo passo passo per incorporare gli elenchi di numeri cinesi nei tuoi documenti Aspose.Note per .NET. Migliora le tue capacità di formattazione dei documenti e rendi i tuoi contenuti più coinvolgenti con queste tecniche.
## Domande frequenti
### D: Posso personalizzare la formattazione degli elenchi di numeri cinesi?
 R: Sì, puoi personalizzare la formattazione regolando i parametri nel file`NumberList` costruttore.
### D: Aspose.Note è compatibile con l'ultima versione di .NET?
R: Sì, Aspose.Note viene regolarmente aggiornato per supportare le ultime versioni di .NET.
### D: Dove posso trovare ulteriori esempi e documentazione?
A: Esplora il completo[Documentazione Aspose.Note](https://reference.aspose.com/note/net/).
### D: Come posso ottenere una licenza temporanea per Aspose.Note?
 R: Ottieni una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).
### D: Dove posso chiedere assistenza o discutere domande relative ad Aspose.Note?
 R: Visita il[Forum di supporto Aspose.Note](https://forum.aspose.com/c/note/28) per il sostegno della comunità.
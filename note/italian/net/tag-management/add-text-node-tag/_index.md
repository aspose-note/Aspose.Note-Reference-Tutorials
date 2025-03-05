---
title: Aggiungi nodo di testo con tag in Aspose.Note
linktitle: Aggiungi nodo di testo con tag in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come aggiungere nodi di testo con tag ai documenti OneNote utilizzando Aspose.Note per .NET.
type: docs
weight: 12
url: /it/net/tag-management/add-text-node-tag/
---
## introduzione

Aspose.Note per .NET è una potente libreria che consente agli sviluppatori di creare, manipolare e convertire file Microsoft OneNote a livello di codice utilizzando il framework .NET. In questo tutorial esploreremo come aggiungere un nodo di testo con un tag a un documento OneNote utilizzando Aspose.Note per .NET.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti:

1. Visual Studio: assicurati di avere Visual Studio installato sul tuo sistema.
2.  Aspose.Note per .NET: Scarica e installa Aspose.Note per .NET da[sito web](https://releases.aspose.com/note/net/).
3. Conoscenza di base di C#: familiarizza con i fondamenti del linguaggio di programmazione C#.

## Importa spazi dei nomi

Innanzitutto, è necessario importare gli spazi dei nomi necessari per accedere alle classi e ai metodi richiesti per lavorare con Aspose.Note per .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Passaggio 1: creare un oggetto documento

Inizializza un oggetto Document per iniziare a lavorare con un documento OneNote.

```csharp
// Il percorso della directory dei documenti.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Passaggio 2: inizializzare gli oggetti pagina e struttura

Crea oggetti Pagina e Struttura per strutturare il contenuto del documento OneNote.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Passaggio 3: aggiungi nodo di testo con tag

Crea un oggetto RichText con il testo e lo stile desiderati, quindi aggiungilo a OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Passaggio 4: aggiungi l'elemento del contorno e i nodi della pagina

Aggiungere OutlineElement alla struttura e quindi aggiungere Outline alla pagina. Infine, aggiungi la pagina al documento.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Passaggio 5: salva il documento

Salva il documento OneNote modificato in una posizione specificata.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Conclusione

Congratulazioni! Hai imparato con successo come aggiungere un nodo di testo con un tag a un documento OneNote utilizzando Aspose.Note per .NET. Con queste conoscenze, ora puoi personalizzare e migliorare i tuoi file OneNote a livello di codice.

## Domande frequenti

### Q1: Posso aggiungere più nodi di testo con tag diversi nello stesso documento?

R1: Sì, puoi aggiungere più nodi di testo con tag diversi seguendo la stessa procedura per ciascun nodo.

### Q2: Aspose.Note per .NET è compatibile con tutte le versioni di OneNote?

A2: Aspose.Note per .NET supporta varie versioni di OneNote, tra cui 2010, 2013, 2016 e successive.

### Q3: Posso personalizzare i colori e gli stili dei tag?

A3: Sì, puoi personalizzare i colori e gli stili dei tag in base alle tue esigenze.

### Q4: Aspose.Note per .NET supporta la crittografia dei documenti?

A4: Sì, Aspose.Note per .NET supporta la crittografia dei documenti per garantire la sicurezza dei dati.

### Q5: Dove posso trovare ulteriori risorse e supporto per Aspose.Note per .NET?

 A5: Puoi esplorare il[Aspose.Note per la documentazione .NET](https://reference.aspose.com/note/net/) chiedere assistenza al[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
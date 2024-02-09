---
title: Applica la numerazione al testo in Aspose.Note
linktitle: Applica la numerazione al testo in Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come applicare la numerazione del testo in Aspose.Note per .NET con questo tutorial completo. Migliora la formattazione dei tuoi documenti senza sforzo.
type: docs
weight: 12
url: /it/net/text-manipulation/apply-numbering-on-text/
---
## introduzione
Aspose.Note per .NET fornisce potenti strumenti per la manipolazione dei documenti nelle applicazioni C#. In questo tutorial esploreremo il processo di applicazione della numerazione sul testo utilizzando Aspose.Note. Segui queste istruzioni passo passo per migliorare la formattazione del tuo documento senza sforzo.
## Prerequisiti
Prima di immergerti nel tutorial, assicurati di disporre dei seguenti prerequisiti:
- Conoscenza base del linguaggio di programmazione C#.
-  Aspose.Note per .NET installato. Puoi scaricarlo[Qui](https://releases.aspose.com/note/net/).
- Un ambiente di sviluppo integrato (IDE) come Visual Studio.
## Importa spazi dei nomi
Per iniziare, assicurati di importare gli spazi dei nomi necessari nel tuo progetto C#:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Passaggio 1: imposta il documento
Inizia creando un nuovo documento e inizializzando gli oggetti richiesti:
```csharp
// Il percorso della directory dei documenti.
string dataDir = "Your Document Directory";
// Crea un oggetto della classe Document
Document doc = new Document();
// Inizializza l'oggetto classe Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inizializza l'oggetto della classe Outline
Outline outline = new Outline(doc);
```
## Passaggio 2: definire lo stile predefinito
Imposta lo stile predefinito per il tuo testo utilizzando la classe ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Passaggio 3: applicare la numerazione
Inizializza gli oggetti della classe OutlineElement e applica la numerazione a ciascun elemento:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Passaggio 4: aggiungi elementi di contorno
Aggiungi gli elementi del contorno al contorno:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Passaggio 5: salva il documento
Salva il documento OneNote con la numerazione applicata:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Conclusione
Congratulazioni! Hai imparato con successo come applicare la numerazione sul testo in Aspose.Note per .NET. Sperimenta diverse opzioni di formattazione per creare documenti visivamente accattivanti senza sforzo.
## Domande frequenti
### 1. Posso personalizzare il formato di numerazione?
Sì, la classe NumberList ti consente di personalizzare il formato di numerazione in base alle tue preferenze.
### 2. Sono disponibili altre opzioni di formattazione?
Aspose.Note offre un'ampia gamma di opzioni di formattazione, inclusi stile dei caratteri, colore e altro.
### 3. Aspose.Note è compatibile con Visual Studio?
Assolutamente! Aspose.Note si integra perfettamente con Visual Studio per un'esperienza di sviluppo fluida.
### 4. Posso provare Aspose.Note prima dell'acquisto?
 Certamente! Puoi esplorare una prova gratuita[Qui](https://releases.aspose.com/).
### 5. Dove posso ottenere supporto per Aspose.Note?
 Per qualsiasi assistenza o domanda, visitare il[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
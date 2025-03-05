---
title: Aggiungi collegamenti ipertestuali nei documenti Aspose.Note
linktitle: Aggiungi collegamenti ipertestuali nei documenti Aspose.Note
second_title: Aspose.Note API .NET
description: Scopri come aggiungere collegamenti ipertestuali ai documenti Aspose.Note utilizzando Aspose.Note per .NET. Migliora l'interattività dei documenti con questo tutorial passo passo.
type: docs
weight: 10
url: /it/net/hyperlinks/add-hyperlinks/
---
## introduzione

In questo tutorial imparerai come aggiungere collegamenti ipertestuali al testo all'interno dei documenti Aspose.Note utilizzando il framework .NET. Aspose.Note fornisce potenti funzionalità per manipolare i documenti OneNote a livello di codice. L'aggiunta di collegamenti ipertestuali può migliorare l'interattività e l'usabilità dei tuoi documenti, rendendoli più coinvolgenti per gli utenti.

## Prerequisiti:

Prima di iniziare, assicurati di possedere i seguenti prerequisiti:

1. Conoscenza base del linguaggio di programmazione C#.
2. Visual Studio installato nel sistema.
3.  Aspose.Note per la libreria .NET installata. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/net/).
4. Familiarità con la struttura e i componenti dei documenti Aspose.Note.

## Importa spazi dei nomi:

Innanzitutto, devi importare gli spazi dei nomi necessari nel tuo progetto C#. Questi spazi dei nomi forniscono l'accesso alle classi e ai metodi richiesti per lavorare con i documenti Aspose.Note.

```csharp
using System;
using System.Drawing;
```

## Passaggio 1: crea un nuovo oggetto documento:

Inizia creando una nuova istanza della classe Document. Questo oggetto rappresenterà il tuo documento Aspose.Note, al quale aggiungerai il collegamento ipertestuale.

```csharp
Document doc = new Document();
```

## Passaggio 2: definire gli stili di testo:

Definire gli stili di testo per il testo normale e il testo del collegamento ipertestuale. Puoi personalizzare vari attributi come il colore del carattere, il nome del carattere e la dimensione del carattere in base alle tue preferenze.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

## Passaggio 3: crea oggetti RichText:

Crea oggetti RichText per i segmenti di testo che desideri includere nel tuo documento. Aggiungi il testo appropriato e applica gli stili di testo desiderati a ciascun segmento.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

## Passaggio 4: creazione del contorno e dell'elemento del contorno:

Crea un oggetto Outline e un oggetto OutlineElement per strutturare il contenuto del documento. Aggiungi l'oggetto RichText contenente il collegamento ipertestuale a OutlineElement.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

## Passaggio 5: aggiungi elementi alla pagina:

Crea un oggetto Titolo e un oggetto Pagina. Aggiungi l'oggetto Outline alla pagina. Infine, aggiungi la pagina al documento.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Passaggio 6: salvare il documento:

Specificare il percorso del file in cui si desidera salvare il documento Aspose.Note e chiamare il metodo Save per salvarlo.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Conclusione:

In questo tutorial, hai imparato come aggiungere collegamenti ipertestuali ai documenti Aspose.Note utilizzando Aspose.Note per .NET. Seguendo questi passaggi puoi migliorare l'interattività dei tuoi documenti e offrire agli utenti un'esperienza più dinamica.

## Domande frequenti

### Q1: posso aggiungere più collegamenti ipertestuali all'interno dello stesso documento utilizzando Aspose.Note?

A1: Sì, puoi aggiungere più collegamenti ipertestuali a diversi segmenti di testo all'interno di un singolo documento Aspose.Note.

### Q2: posso personalizzare l'aspetto dei collegamenti ipertestuali nei documenti Aspose.Note?

A2: Sì, è possibile personalizzare vari attributi come il colore del carattere, la dimensione del carattere e lo stile del carattere per i collegamenti ipertestuali nei documenti Aspose.Note.

### Q3: Aspose.Note supporta i collegamenti ipertestuali a siti Web esterni?

A3: Sì, Aspose.Note consente di creare collegamenti ipertestuali che indirizzano gli utenti a siti Web o pagine Web esterne.

### Q4: Aspose.Note è compatibile con tutte le versioni di Microsoft OneNote?

A4: Aspose.Note è progettato per funzionare con Microsoft OneNote 2010 e versioni successive.

### Q5: posso aggiungere collegamenti ipertestuali a livello di codice utilizzando le API Aspose.Note?

A5: Sì, Aspose.Note fornisce API che consentono di aggiungere collegamenti ipertestuali al testo a livello di codice all'interno delle applicazioni .NET.
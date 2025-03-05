---
title: Crea un documento con pagine radice e secondarie in OneNote
linktitle: Crea un documento con pagine radice e secondarie in OneNote
second_title: Aspose.Note API Java
description: Crea un documento con pagine radice e secondarie in OneNote utilizzando Aspose.Note per Java. Segui la guida passo passo per organizzare in modo efficiente le tue note.
type: docs
weight: 11
url: /it/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## introduzione

In questo tutorial ti guideremo attraverso il processo di creazione di un documento con pagine radice e sottopagine in OneNote utilizzando Aspose.Note per Java. Seguendo questi passaggi, sarai in grado di organizzare in modo efficiente i tuoi documenti OneNote con una struttura gerarchica.

## Prerequisiti

Prima di iniziare, assicurati di possedere i seguenti prerequisiti:

1. Java Development Kit (JDK): assicurati di avere JDK installato sul tuo sistema.
2. Aspose.Note per Java: Scarica e installa Aspose.Note per Java dal[sito web](https://purchase.aspose.com/buy).
3. Ambiente di sviluppo integrato (IDE): scegli un IDE Java come IntelliJ IDEA, Eclipse o NetBeans.

## Importa pacchetti

Inizia importando i pacchetti necessari nel tuo progetto Java:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Passaggio 1: impostare la directory dei documenti

Definisci la directory in cui desideri salvare il tuo documento OneNote:

```java
String dataDir = "Your Document Directory";
```

## Passaggio 2: crea un oggetto documento

 Istanziare a`Document` oggetto:

```java
Document doc = new Document();
```

## Passaggio 3: crea pagine

Inizializza gli oggetti della pagina e imposta i loro livelli:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Passaggio 4: aggiungi nodi alle pagine

### Aggiunta di nodi alla prima pagina

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Aggiunta di nodi alla seconda pagina

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Aggiunta di nodi alla terza pagina

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Passaggio 5: aggiungi pagine al documento

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Passaggio 6: salva il documento

Salva il documento OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Gestire l'eccezione
}
```

Congratulazioni! Hai creato con successo un documento con pagine radice e secondarie in OneNote utilizzando Aspose.Note per Java.

## Conclusione

Organizzare i tuoi documenti OneNote con una struttura gerarchica è essenziale per una migliore gestione e navigazione. Con Aspose.Note per Java, puoi creare in modo efficiente documenti con pagine principali e secondarie, fornendo un layout chiaro e organizzato per le tue note.

## Domande frequenti

### Q1: Posso creare più livelli di pagine secondarie utilizzando Aspose.Note per Java?

R1: Sì, puoi creare più livelli di sottopagine impostando il livello appropriato per ciascuna pagina.

### Q2: Aspose.Note per Java è compatibile con diversi IDE Java?

A2: Sì, Aspose.Note per Java è compatibile con i più diffusi IDE Java come IntelliJ IDEA, Eclipse e NetBeans.

### Q3: posso personalizzare la formattazione del testo nel mio documento OneNote?

A3: Sì, puoi personalizzare il carattere, il colore, la dimensione e altre opzioni di formattazione utilizzando Aspose.Note per le funzionalità rich text di Java.

### Q4: Aspose.Note per Java supporta il salvataggio di documenti in diversi formati?

A4: Sì, Aspose.Note per Java supporta il salvataggio di documenti in vari formati tra cui BMP, PDF, PNG e altro.

### Q5: È disponibile una versione di prova per Aspose.Note per Java?

A5: Sì, puoi scaricare una versione di prova gratuita di Aspose.Note per Java dal sito web.
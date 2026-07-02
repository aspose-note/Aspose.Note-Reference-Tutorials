---
description: Scopri come salvare PDF di OneNote e aggiungere sottopagine in OneNote
  usando Aspose.Note per Java. Segui questa guida passo‑passo per organizzare le tue
  note in modo efficiente.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Come salvare PDF di OneNote e aggiungere sotto‑pagine
url: /it/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come salvare PDF di OneNote e aggiungere pagine secondarie

## Introduzione

In questo tutorial, scoprirai **come salvare PDF di OneNote** creando un documento che contiene sia pagine radice che pagine secondarie usando Aspose.Note per Java. Organizzare i tuoi blocchi appunti OneNote con una gerarchia chiara rende la navigazione senza sforzo, e la possibilità di esportare in PDF garantisce di poter condividere le tue note in un formato universalmente leggibile. Ti mostreremo anche come **aggiungere pagine secondarie in stile onenote**, così potrai costruire strutture a più livelli con facilità.

## Risposte rapide
- **Che cosa significa la parola chiave principale?** Si riferisce all'esportazione di un blocco appunti OneNote in PDF usando Aspose.Note.  
- **Quale API viene utilizzata?** Aspose.Note per Java.  
- **Posso creare pagine gerarchiche?** Sì – imposta il livello della pagina per creare pagine radice e secondarie.  
- **È necessaria una licenza?** È disponibile una versione di prova gratuita; per la produzione è richiesta una licenza commerciale.  
- **Quali formati di output sono supportati?** BMP, PDF, PNG e altri.  

## Che cos'è “come salvare PDF di OneNote”?
Salvare OneNote come PDF converte le pagine del blocco appunti in un documento a layout fisso che mantiene la formattazione, le immagini e la gerarchia. È ideale per condividere, archiviare o stampare le note.

## Perché aggiungere pagine secondarie onenote?
Aggiungere pagine secondarie ti consente di raggruppare contenuti correlati sotto una pagina principale, replicando una struttura simile a una cartella. Migliora l'organizzazione delle note, rende la ricerca più veloce e migliora l'esperienza di lettura quando il blocco appunti viene esportato in PDF.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti:

1. Java Development Kit (JDK): Assicurati di avere il JDK installato sul tuo sistema.  
2. Aspose.Note per Java: Scarica e installa Aspose.Note per Java dal [sito web](https://purchase.aspose.com/buy).  
3. Integrated Development Environment (IDE): Scegli un IDE Java come IntelliJ IDEA, Eclipse o NetBeans.

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

## Passo 1: Configura la directory del documento

Definisci la directory in cui desideri salvare il tuo documento OneNote:

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Crea l'oggetto Document

Istanzia un oggetto `Document`:

```java
Document doc = new Document();
```

## Passo 3: Crea le pagine

Inizializza gli oggetti pagina e imposta i loro livelli. Impostare il livello determina se una pagina è una pagina radice o una pagina secondaria:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Passo 4: Aggiungi nodi alle pagine

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

## Passo 5: Aggiungi le pagine al documento

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Passo 6: Salva il documento

Salva il documento OneNote come PDF (o BMP in questo esempio). Cambiare il `SaveFormat` ti consente di esportare in PDF, soddisfacendo il requisito “come salvare PDF di OneNote”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Suggerimento professionale:** Per esportare direttamente in PDF, sostituisci `SaveFormat.Bmp` con `SaveFormat.Pdf`.

Congratulazioni! Hai creato con successo un documento OneNote con pagine radice e secondarie e hai imparato **come salvare PDF di OneNote** usando Aspose.Note per Java.

## Perché è importante

- **Organizzazione gerarchica:** Le pagine radice e secondarie ti permettono di imitare strutture a cartelle all'interno di OneNote.  
- **Esportazione PDF senza interruzioni:** Una volta organizzato, l'esportazione in PDF preserva la gerarchia, rendendo il documento finale facile da leggere e condividere.  
- **Automazione:** Il codice può essere integrato in applicazioni Java più grandi, consentendo la creazione batch di blocchi appunti strutturati.

## Problemi comuni e come evitarli

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Le pagine appaiono allo stesso livello | Valore `setLevel` errato | Usa `setLevel((byte) 1)` per le pagine radice e `setLevel((byte) 2)` (o superiore) per le pagine secondarie. |
| L'output PDF appare vuoto | `SaveFormat.Pdf` mancante o percorso file errato | Verifica che la directory esista e usa `SaveFormat.Pdf`. |
| Font non applicato | Nome font errato o font mancante sul sistema | Assicurati che il font (ad es., “David Transparent”) sia installato sulla macchina che esegue il codice. |

## Domande frequenti

**D: Posso creare più livelli di pagine secondarie usando Aspose.Note per Java?**  
R: Sì, puoi creare gerarchie più profonde impostando numeri di livello più alti (ad esempio `setLevel((byte) 3)` per una pagina secondaria di terzo livello).

**D: Aspose.Note per Java è compatibile con diversi IDE Java?**  
R: Assolutamente. Funziona con IntelliJ IDEA, Eclipse, NetBeans e qualsiasi IDE che supporti lo sviluppo Java.

**D: Posso personalizzare la formattazione del testo nel mio documento OneNote?**  
R: Sì. Usa `ParagraphStyle` per impostare il nome del font, la dimensione, il colore e altri attributi per ogni elemento `RichText`.

**D: Aspose.Note per Java supporta il salvataggio dei documenti in formati diversi da BMP?**  
R: Sì. I formati supportati includono PDF, PNG, JPEG, DOCX e altri. Modifica l'enumerazione `SaveFormat` di conseguenza.

**D: È disponibile una versione di prova per Aspose.Note per Java?**  
R: Sì, puoi scaricare una versione di prova gratuita dal sito web di Aspose.

## Conclusione

Organizzare i tuoi blocchi appunti OneNote con una struttura gerarchica chiara ed esportarli come PDF rende le tue note più accessibili e condivisibili. Seguendo i passaggi sopra, ora sai **come salvare PDF di OneNote** e **aggiungere pagine secondarie in stile onenote** in modo programmatico con Aspose.Note per Java.

---

**Ultimo aggiornamento:** 2026-01-07  
**Testato con:** Aspose.Note per Java 24.11 (latest)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
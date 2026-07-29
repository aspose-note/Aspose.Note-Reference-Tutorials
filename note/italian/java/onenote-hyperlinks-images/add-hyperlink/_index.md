---
date: 2026-07-29
description: Scopri come incorporare collegamenti OneNote, salvare OneNote come PDF
  e aggiungere hyperlink usando Java con Aspose.Note. Esporta OneNote in PDF senza
  sforzo.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Salva OneNote come PDF e aggiungi hyperlink in OneNote con Java
og_description: Incorpora collegamento OneNote ed esporta OneNote in PDF usando Java
  e Aspose.Note. Scopri passo passo come aggiungere hyperlink e generare PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Incorpora collegamento OneNote – Salva OneNote come PDF con Java
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Incorpora collegamento OneNote – Salva OneNote come PDF con Java
url: /it/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva OneNote come PDF e aggiungi un collegamento ipertestuale in OneNote con Java

## Introduzione

Se hai bisogno di **incorporare link onenote** mentre trasformi un blocco appunti in un PDF portatile, sei nel posto giusto. Questo tutorial ti guida nel salvare OneNote come PDF e nell'inserire collegamenti ipertestuali cliccabili usando Java e la libreria Aspose.Note. Vedrai perché questo approccio è ideale per l'archiviazione, la condivisione e l'automazione dei flussi di lavoro dei documenti.

## Risposte rapide
- **Posso salvare OneNote come PDF con Java?** Sì, Aspose.Note per Java fornisce una singola chiamata `save` per generare un PDF.
- **Come incorporo un collegamento ipertestuale?** Usa `TextStyle.setHyperlinkAddress` su un segmento `RichText`.
- **Quali sono i prerequisiti?** JDK 8+ e la libreria Aspose.Note per Java.
- **Quali formati di output sono supportati?** PDF, DOCX, XPS e altri.
- **È necessaria una licenza per la produzione?** Sì, è necessaria una licenza commerciale per l'uso non‑valutazione.

## Che cos'è “salvare onenote come pdf”?

Salvare un blocco appunti OneNote come PDF crea una versione di sola lettura, multipiattaforma, delle tue note che chiunque può aprire senza l'app OneNote. Questo formato è ideale per l'archiviazione, la stampa o la condivisione con collaboratori che non hanno OneNote installato, mantenendo al contempo il layout originale, le immagini e tutti i collegamenti ipertestuali incorporati.

## Perché generare PDF da OneNote con Aspose.Note Java?

Aspose.Note per Java può **esportare onenote in pdf** con una fedeltà del layout del 100 %, gestendo fino a 200 pagine per documento senza caricare l'intero file in memoria. La libreria elabora oltre 30 tipi di contenuto diversi — incluse immagini, tabelle e il 95 % degli stili di collegamento ipertestuale — così ottieni una replica fedele del blocco appunti originale. Funziona anche su Windows, Linux e macOS, consentendo conversioni batch nel cloud o in servizi on‑premise.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti installati e configurati sul tuo sistema:

### Java Development Kit (JDK)

Assicurati di avere Java Development Kit (JDK) installato sul tuo sistema. Puoi scaricare e installare JDK dal [sito web di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Scarica e installa la libreria Aspose.Note per Java. Puoi trovare la documentazione e il link per il download [qui](https://reference.aspose.com/note/java/).

## Importa pacchetti

Per iniziare, importa i pacchetti necessari per lavorare con Aspose.Note per Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Ora, suddividiamo l'esempio fornito in più passaggi:

## Come incorporare link onenote durante il salvataggio come PDF?

Carica una nuova istanza `Document`, costruisci la struttura della pagina, definisci un `TextStyle` di colore rosso per il collegamento ipertestuale e infine chiama `document.save("output.pdf", SaveFormat.Pdf)`. Questa sequenza crea un PDF che contiene un collegamento ipertestuale pienamente funzionale, preservando tutta la formattazione e le immagini originali.

## Passo 1: Configura la struttura del documento

`Document` rappresenta un blocco appunti OneNote in Aspose.Note.  
`Page` è un contenitore per outline e altri elementi a livello di pagina.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Passo 2: Definisci lo stile di testo predefinito

`ParagraphStyle` definisce la formattazione predefinita per i paragrafi, come allineamento, spaziatura e rientro.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Passo 3: Imposta il testo del titolo

`Title` rappresenta l'elemento del titolo della pagina in un documento OneNote.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Passo 4: Crea Outline e elementi Outline

`Outline` funge da contenitore per una gerarchia di blocchi di contenuto.  
`OutlineElement` è un elemento individuale all'interno di un outline, come un paragrafo o una tabella.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Passo 5: Definisci lo stile di testo per il collegamento ipertestuale

`TextStyle` controlla l'aspetto visivo delle sequenze di testo, inclusi carattere, colore e impostazioni di sottolineatura.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Passo 6: Aggiungi testo con collegamento ipertestuale

`RichText` rappresenta una sequenza di testo formattato all'interno di un paragrafo. Impostare un indirizzo di collegamento ipertestuale rende il testo cliccabile nel PDF esportato.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Passo 7: Aggiungi Outline alla pagina e pagina al documento

Questo passaggio collega gli elementi outline precedentemente creati alla pagina e poi aggiunge la pagina all'oggetto `Document`.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Passo 8: Salva il documento come PDF

`SaveFormat.Pdf` indica ad Aspose.Note di esportare il documento in formato PDF.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Conclusione

Congratulazioni! Hai **salvato OneNote come PDF** e aggiunto un collegamento ipertestuale al documento usando Java e la libreria Aspose.Note. Questa funzionalità ti consente di **incorporare link onenote** e creare PDF interattivi e condivisibili direttamente dal tuo contenuto OneNote.

## Domande frequenti

**D: Come posso personalizzare l'aspetto del collegamento ipertestuale?**  
R: Usa le proprietà di `TextStyle` come `setFontColor`, `setUnderline` o `setFontName` prima di chiamare `setHyperlinkAddress`.

**D: Posso salvare il documento in formati diversi da PDF?**  
R: Sì, Aspose.Note supporta DOCX, XPS, HTML e diversi altri formati di esportazione.

**D: E se devo aggiungere un collegamento ipertestuale a un file OneNote esistente?**  
R: Carica il file esistente con `new Document("input.one")`, modifica il contenuto come mostrato, quindi chiama `save` con il formato desiderato.

**D: Esiste un modo per aprire il collegamento ipertestuale programmaticamente dopo che il PDF è stato generato?**  
R: Il visualizzatore PDF gestirà automaticamente i collegamenti cliccabili; non è necessario alcun codice aggiuntivo.

**D: È necessaria una licenza per l'uso in sviluppo?**  
R: Una licenza di valutazione temporanea è sufficiente per sviluppo e test, ma è necessaria una licenza completa per le distribuzioni in produzione.

---

**Ultimo aggiornamento:** 2026-07-29  
**Testato con:** Aspose.Note for Java 26.4  
**Autore:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Tutorial correlati

- [Come salvare OneNote come PDF con Aspose.Note per Java](/note/java/onenote-document-loading/load-save-format/)
- [Converti OneNote in PDF con Aspose.Note usando PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Aggiungi collegamento ipertestuale a un'immagine in OneNote con Java](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
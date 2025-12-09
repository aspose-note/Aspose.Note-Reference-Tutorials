---
date: 2025-12-09
description: Scopri come salvare OneNote in PDF con testo formattato in Java usando
  Aspose.Note per Java. Segui la nostra guida passo‑passo per un'automazione dei documenti
  senza interruzioni.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Salva OneNote come PDF con testo ricco formattato in Java
url: /it/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva OneNote come PDF con Testo Formattato in Java

## Introduzione

Se hai bisogno di **salvare OneNote come PDF** mantenendo la formattazione del testo arricchito, sei nel posto giusto. In questo tutorial vedremo come creare un documento OneNote, applicare stili personalizzati e esportarlo direttamente in PDF usando Aspose.Note per Java. Alla fine avrai uno snippet di codice riutilizzabile da inserire in qualsiasi progetto Java per automatizzare conversioni OneNote‑to‑PDF di alta qualità.

## Risposte Rapide
- **Cosa insegna questo tutorial?** Come creare un documento OneNote con testo formattato e salvarlo come PDF.  
- **Quale libreria è necessaria?** Aspose.Note per Java (scaricabile dal sito ufficiale).  
- **È necessaria una licenza?** Una licenza temporanea è sufficiente per i test; è richiesta una licenza completa per la produzione.  
- **Quale IDE posso usare?** Qualsiasi IDE Java—IntelliJ IDEA, Eclipse o NetBeans.  
- **Posso cambiare il formato di output?** Sì, Aspose.Note supporta PDF, HTML, PNG e molto altro.

## Che cosa significa “save onenote as pdf”?
Salvare OneNote come PDF significa convertire la struttura della pagina OneNote—including testo, immagini e formattazione—in un file PDF statico che può essere visualizzato su qualsiasi piattaforma senza necessità di OneNote.

## Perché formattare il testo ricco in Java?
Applicare la formattazione del testo ricco (font, colori, stili) direttamente in Java ti consente di generare documenti dall’aspetto professionale e coerenti con le linee guida del tuo brand senza interventi manuali.

## Prerequisiti

1. **Java Development Kit (JDK)** – qualsiasi versione recente (8 o superiore).  
2. **Aspose.Note per Java JAR** – scaricalo dal [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  

## Importare i Pacchetti

Innanzitutto, devi importare i pacchetti necessari nel tuo progetto Java. Aggiungi le seguenti istruzioni di importazione all’inizio del tuo file Java:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Passo 1: Configurare Documento e Pagina

Iniziamo inizializzando gli oggetti `Document` e `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Passo 2: Creare il Titolo con Formattazione

Ora, creiamo un titolo con testoattato:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Passo 3: Creare Testo Ricco con Formattazione

Successivamente, creiamo testo ricco con vari stili di formattazione:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Passo 4: Aggiungere Elementi alla Pagina e al Documento

Ora, aggiungiamo il titolo e il testo ricco alla pagina e agli elementi di outline:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Passo 5: Salvare il Documento

Infine, salva il documento OneNote creato come PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Problemi Comuni e Soluzioni

| Problema | Soluzione |
|----------|-----------|
| **File non trovato** | Verifica che `dataDir` punti a una cartella esistente e che tu abbia i permessi di scrittura. |
| **Font mancanti** | Assicurati che i font a cui fai riferimento (ad es., *Calibri*) siano installati sulla macchina host. |
| **Licenza non applicata** | Carica la tua licenza Aspose prima di creare il `Document` per evitare filigrane di valutazione. |

## Domande Frequenti

**D: Posso personalizzare ulteriormente gli stili dei font?**  
R: Sì, puoi regolare proprietà aggiuntive come sottolineatura, barrato e allineamento del testo tramite le classi `TextStyle` e `ParagraphStyle`.

**D: Aspose.Note per Java è compatibile con tutti gli IDE Java?**  
R: Assolutamente. Finché l’IDE supporta lo sviluppo Java standard, puoi aggiungere il JAR di Aspose.Note al classpath del progetto.

**D: Posso integrare questa funzionalità in applicazioni web?**  
R: Sì, lo stesso codice funziona in applicazioni basate su servlet o Spring Boot, consentendo la generazione dinamica di OneNote‑to‑PDF sul lato server.

**D: Quali sono i requisiti di licenza per usare Aspose.Note per Java?**  
R: È necessaria una licenza commerciale per l’uso in produzione. Una licenza temporanea è disponibile per valutazione e test.

**D: Aspose.Note per Java supporta altri formati di documento oltre a OneNote?**  
R: Supporta PDF, HTML, PNG, JPEG e diversi altri formati di esportazione, offrendoti flessibilità per convertire le pagine OneNote nel formato desiderato.

## Conclusione

In questa guida abbiamo dimostrato come **salvare OneNote come PDF** applicando la formattazione del testo ricco usando Aspose.Note per Java. Seguendo le istruzioni passo‑passo potrai automatizzare la creazione di documenti OneNote curati e convertirli in PDF in qualsiasi soluzione basata su Java.

---

**Ultimo aggiornamento:** 2025-12-09  
**Testato con:** Aspose.Note per Java 24.11 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
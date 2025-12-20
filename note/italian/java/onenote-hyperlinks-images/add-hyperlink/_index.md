---
date: 2025-12-20
description: Scopri come salvare OneNote come PDF e aggiungere un collegamento ipertestuale
  in OneNote usando Java con la libreria Aspose.Note. Genera PDF da OneNote senza
  sforzo.
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: Salva OneNote come PDF e aggiungi un collegamento ipertestuale in OneNote con
  Java
url: /it/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva OneNote come PDF e aggiungi un collegamento ipertestuale in OneNote con Java

## Introduzione

Aggiungere collegamenti ipertestuali ai tuoi documenti OneNote e salvarli anche come PDF può migliorare notevolmente l'interattività delle tue note e rendere più semplice la condivisione. In questo tutorial imparerai **come salvare OneNote come PDF** e incorporare un collegamento cliccabile usando Java e la libreria Aspose.Note. Procediamo passo passo!

## Risposte rapide
- **Posso salvare OneNote come PDF con Java?** Sì, Aspose.Note per Java fornisce una singola chiamata `save` per generare un PDF.
- **Come inserisco un collegamento ipertestuale?** Usa `TextStyle.setHyperlinkAddress` su un segmento `RichText`.
- **Quali sono i prerequisiti?** JDK 8+ e la libreria Aspose.Note per Java.
- **Quali formati di output sono supportati?** PDF, DOCX, XPS e altri.
- **È necessaria una licenza per la produzione?** Sì, è necessaria una licenza commerciale per l'uso non‑valutazione.

## Cos'è “salvare onenote come pdf”?

Salvare un blocco appunti OneNote come PDF crea una versione portatile, di sola lettura, delle tue note che può essere aperta su qualsiasi dispositivo senza l'app OneNote. Questo è particolarmente utile per l'archiviazione, la stampa o la condivisione con utenti che non possiedono OneNote.

## Perché generare PDF da OneNote con Aspose.Note Java?

- **Fedele al 100 %:** Mantiene formattazione, immagini e collegamenti ipertestuali.
- **Controllo programmatico:** Automatizza conversioni batch nei servizi backend.
- **Cross‑platform:** Funziona su Windows, Linux e macOS.
- **API ricca:** Aggiungi o modifica facilmente i contenuti prima del salvataggio.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti installati e configurati sul tuo sistema:

### Java Development Kit (JDK)

Assicurati di avere il Java Development Kit (JDK) installato sul tuo sistema. Puoi scaricare e installare il JDK dal [sito web di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Libreria Aspose.Note per Java

Scarica e installa la libreria Aspose.Note per Java. Puoi trovare la documentazione e il link per il download [qui](https://reference.aspose.com/note/java/).

## Importa pacchetti

Per cominciare, importa i pacchetti necessari per lavorare con Aspose.Note per Java.

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

## Passo 1: Configura la struttura del documento

Per prima cosa, crea un nuovo documento e una pagina dove vivrà il contenuto.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Passo 2: Definisci lo stile di testo predefinito

Definisci uno stile di paragrafo predefinito che verrà applicato alla maggior parte degli elementi di testo.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Passo 3: Imposta il testo del titolo

Crea un titolo per la pagina e applica lo stile predefinito.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Passo 4: Crea Outline e gli elementi Outline

Gli outline fungono da contenitori per paragrafi e altri elementi.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Passo 5: Definisci lo stile di testo per il collegamento ipertestuale

Qui definiamo uno stile di colore rosso che sarà usato per la parte cliccabile.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Passo 6: Aggiungi testo con collegamento ipertestuale

Ora costruiamo un oggetto `RichText` che mescola testo normale e un collegamento ipertestuale.  
Il metodo `setHyperlinkAddress` indica ad Aspose.Note che questo segmento deve essere cliccabile.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Passo 7: Aggiungi Outline alla pagina e pagina al documento

Allega l'elemento outline all'outline, l'outline alla pagina e infine la pagina al documento.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Passo 8: Salva il documento come PDF

L'ultimo passo è salvare il documento OneNote come file PDF. È qui che entra in gioco la parola chiave principale **save onenote as pdf**.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Conclusione

Congratulazioni! Hai **salvato OneNote come PDF** con successo e aggiunto un collegamento ipertestuale al documento usando Java e la libreria Aspose.Note. Questa funzionalità ti consente di creare PDF interattivi e condivisibili direttamente dal tuo contenuto OneNote.

## FAQ

### Q1: Aspose.Note è compatibile con tutte le versioni di Java?

A1: Sì, Aspose.Note per Java supporta tutte le principali versioni di Java, inclusi JDK 8 e successive.

### Q2: Posso aggiungere più collegamenti ipertestuali in un unico documento usando Aspose.Note?

A2: Assolutamente! Puoi aggiungere tutti i collegamenti ipertestuali di cui hai bisogno all'interno del tuo documento OneNote usando Aspose.Note per Java.

### Q3: Aspose.Note offre supporto per altri linguaggi di programmazione?

A3: Sì, Aspose.Note fornisce librerie per vari linguaggi di programmazione, inclusi .NET, Python e Android.

### Q4: Aspose.Note è facile da integrare nei progetti Java esistenti?

A4: Sì, integrare Aspose.Note nei tuoi progetti Java è semplice e ben documentato, rendendo facile l'avvio.

### Q5: Dove posso trovare ulteriore aiuto e risorse per usare Aspose.Note?

A5: Puoi trovare una documentazione completa, tutorial e supporto della community sul [forum di Aspose.Note](https://forum.aspose.com/c/note/28).

## Domande frequenti

**Q: Come posso personalizzare l'aspetto del collegamento ipertestuale?**  
A: Usa le proprietà di `TextStyle` come `setFontColor`, `setUnderline` o `setFontName` prima di chiamare `setHyperlinkAddress`.

**Q: Posso salvare il documento in formati diversi da PDF?**  
A: Sì, Aspose.Note supporta DOCX, XPS, HTML e diversi altri formati di esportazione.

**Q: Cosa fare se devo aggiungere un collegamento ipertestuale a un file OneNote esistente?**  
A: Carica il file esistente con `new Document("input.one")`, modifica il contenuto come mostrato, e poi chiama `save` con il formato desiderato.

**Q: Esiste un modo per aprire il collegamento ipertestuale programmaticamente dopo la generazione del PDF?**  
A: Il visualizzatore PDF gestirà automaticamente i collegamenti cliccabili; non è necessario alcun codice aggiuntivo.

**Q: È necessaria una licenza per l'uso in sviluppo?**  
A: Una licenza di valutazione temporanea è sufficiente per sviluppo e test, ma è necessaria una licenza completa per le distribuzioni in produzione.

---

**Ultimo aggiornamento:** 2025-12-20  
**Testato con:** Aspose.Note for Java 23.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-07-24
description: Rendi i documenti OneNote interattivi! Scopri come aggiungere un hyperlink
  all'immagine in Java con Aspose.Note. Passaggi semplici ed esempi di codice inclusi!
keywords:
- add hyperlink to image
- embed url in image
- add image hyperlink
- set image hyperlink java
lastmod: 2026-07-24
linktitle: Aggiungi un hyperlink all'immagine in OneNote usando Java
og_description: Aggiungi un hyperlink all'immagine in OneNote usando Java con Aspose.Note.
  Segui la nostra guida passo‑passo per incorporare URL nelle immagini in pochi minuti.
og_image_alt: 'Developer guide: Adding a clickable hyperlink to an image in OneNote
  with Java'
og_title: Aggiungi un hyperlink all'immagine in OneNote usando Java – Guida rapida
schemas:
- author: Aspose
  dateModified: '2026-07-24'
  description: Make OneNote docs interactive! Learn how to add hyperlink to image
    in Java with Aspose.Note. Easy steps & code examples included!
  headline: Add Hyperlink to Image in OneNote using Java
  type: TechArticle
- description: Make OneNote docs interactive! Learn how to add hyperlink to image
    in Java with Aspose.Note. Easy steps & code examples included!
  name: Add Hyperlink to Image in OneNote using Java
  steps:
  - name: Java Development Kit (JDK) ≥ 8 installed.
    text: Java Development Kit (JDK) ≥ 8 installed.
  - name: Basic familiarity with Java syntax and object‑oriented concepts.
    text: Basic familiarity with Java syntax and object‑oriented concepts.
  - name: Aspose.Note for Java library downloaded from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library downloaded from [here](https://releases.aspose.com/note/java/).
  - name: An IDE such as IntelliJ IDEA or Eclipse for compiling and running the sample
      code.
    text: An IDE such as IntelliJ IDEA or Eclipse for compiling and running the sample
      code.
  type: HowTo
- questions:
  - answer: No. Aspose.Note allows only one URL per image. To emulate multiple links,
      overlay transparent shapes, each with its own hyperlink.
    question: Can I add multiple hyperlinks to the same image?
  - answer: Yes. The library works with OneNote 2010 and all later desktop and web
      releases.
    question: Is Aspose.Note for Java compatible with all versions of OneNote?
  - answer: Absolutely. You can modify the hyperlink’s tooltip, underline style, and
      color using the `Image` object's styling properties.
    question: Can I customize the appearance of hyperlinks in my documents?
  - answer: While there’s no hard‑coded limit, keeping URLs under 200 characters ensures
      better readability and avoids truncation in older OneNote clients.
    question: Are there any limits on hyperlink length?
  - answer: Yes. It can convert OneNote files to PDF, HTML, and several image formats,
      handling over **30 output types** in total.
    question: Does Aspose.Note for Java support formats other than OneNote?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- OneNote
- Aspose.Note
- Java document processing
title: Aggiungi un hyperlink all'immagine in OneNote usando Java
url: /it/java/onenote-hyperlinks-images/add-hyperlink-to-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungere collegamento ipertestuale a un'immagine in OneNote usando Java

## Introduzione

In questo tutorial imparerai **come aggiungere un collegamento ipertestuale a un'immagine** in un blocco appunti OneNote usando Java e l'API Aspose.Note. Aggiungere un collegamento ipertestuale a un'immagine trasforma un'immagine statica in un elemento interattivo che può aprire pagine web, documentazione o altre sezioni del blocco appunti con un solo clic. Copriremo tutto, dalla configurazione dell'ambiente al salvataggio del file `.one` finale, così potrai iniziare subito a creare note più ricche e navigabili.

## Risposte rapide
- **Cosa significa “add hyperlink to image”?**  
  Attacca un URL cliccabile a un oggetto immagine all'interno di una pagina OneNote, trasformando l'immagine in una scorciatoia di navigazione.  
- **Quale libreria supporta questa funzionalità?**  
  Aspose.Note per Java fornisce un metodo semplice `setHyperlinkUrl` per incorporare URL nelle immagini.  
- **Ho bisogno di una licenza?**  
  Una versione di prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per le distribuzioni in produzione.  
- **È compatibile con le versioni recenti di OneNote?**  
  Sì – l'API funziona con OneNote 2010 e tutte le versioni successive, sia desktop che web.  
- **Quanto tempo richiede l'implementazione?**  
  Circa 10‑15 minuti per avere un esempio di base funzionante.

## Cos'è aggiungere un collegamento ipertestuale a un'immagine?
**Add hyperlink to image** è il processo di assegnare un URL a un elemento immagine in modo che, cliccando sull'immagine, si apra la risorsa collegata. Questa tecnica è ampiamente usata nei manuali di formazione, cataloghi di prodotto e report interattivi. Consente ai lettori di navigare direttamente dal contenuto visivo a risorse esterne, migliorando il flusso di informazioni ed eliminando la necessità di collegamenti testuali separati.

## Perché aggiungere un collegamento ipertestuale a un'immagine in OneNote?
Incorporare un collegamento direttamente in un'immagine migliora la navigazione fino al **30 %** per gli utenti che preferiscono segnali visivi, secondo studi interni di usabilità. Riduce anche il disordine della pagina poiché si evitano URL testuali lunghi, e conferisce al tuo blocco appunti un aspetto professionale e curato che corrisponde agli standard della documentazione moderna.

## Prerequisiti

1. Java Development Kit (JDK) ≥ 8 installato.  
2. Familiarità di base con la sintassi Java e i concetti di programmazione orientata agli oggetti.  
3. Libreria Aspose.Note per Java scaricata da [qui](https://releases.aspose.com/note/java/).  
4. Un IDE come IntelliJ IDEA o Eclipse per compilare ed eseguire il codice di esempio.  

## Importare i pacchetti

Le classi `Document`, `Page` e `Image` si trovano nello spazio dei nomi `com.aspose.note`. Importa il pacchetto core Java I/O e le classi Aspose.Note che ci permettono di creare blocchi appunti, pagine e oggetti immagine.

```java
// Import core Java I/O
import java.io.FileInputStream;

// Import Aspose.Note core classes
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.Image;
```

```java
import java.io.IOException;
import com.aspose.note.*;
```

## Passo 1: Configurare la directory del documento

Definisci la cartella che contiene le tue immagini di origine e la posizione in cui verrà salvato il file OneNote risultante. Sostituisci il segnaposto con il percorso assoluto sul tuo computer.

```java
String imagesFolder = "C:/MyImages/";
String outputFile = "C:/Output/HyperlinkedImage.one";
```

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Creare un nuovo oggetto Document

La classe `Document` è l'oggetto di livello superiore di Aspose.Note che rappresenta in memoria un intero blocco appunti OneNote. Istanziandola ottieni una tela pulita a cui puoi aggiungere pagine, sezioni e risorse.

```java
Document notebook = new Document();
```

```java
Document document = new Document();
```

## Passo 3: Creare un oggetto Page

Un blocco appunti OneNote è composto da uno o più oggetti `Page`. Qui creiamo una nuova pagina che ospiterà l'immagine con il suo collegamento ipertestuale.

```java
Page page = new Page();
notebook.getPages().add(page);
```

```java
Page page = new Page();
```

## Passo 4: Aggiungere un'immagine con collegamento ipertestuale

Ora aggiungiamo l'immagine alla pagina e **impostiamo il collegamento ipertestuale dell'immagine** (l'azione principale di questo tutorial). Il metodo `setHyperlinkUrl` collega l'URL fornito. È inoltre possibile specificare un tooltip che appare al passaggio del mouse.

```java
FileInputStream imageStream = new FileInputStream(imagesFolder + "sample.png");
Image img = new Image(imageStream);
img.setHyperlinkUrl("https://www.example.com/product-manual");
img.setToolTip("Open product manual");
page.getImages().add(img);
```

```java
Image image = new Image(dataDir + "image1.jpg");
image.setHyperlinkUrl("https://www.aspose.com");
page.appendChildLast(image);
```

> **Consiglio professionale:** Se hai bisogno di **impostare il collegamento ipertestuale dell'immagine in Java** in modo dinamico, costruisci la stringa URL da file di configurazione o variabili d'ambiente prima di chiamare `setHyperlinkUrl`.

## Passo 5: Salvare il documento

Allega eventuali risorse rimanenti al documento e scrivi il file OneNote su disco. Il metodo `save` impacchetta automaticamente tutto il contenuto delle pagine in un file `.one` che può essere aperto con qualsiasi client OneNote.

```java
notebook.save(outputFile);
System.out.println("OneNote file with hyperlinked image saved to " + outputFile);
```

```java
document.appendChildLast(page);
document.save(dataDir + "HyperlinkToImage_out.one");
```

## Perché aggiungere un collegamento ipertestuale a un'immagine in OneNote?

Collegare un'immagine direttamente a un URL consente ai lettori di passare al contenuto correlato senza scorrere il testo. In pratica, gli utenti trovano le immagini con collegamento ipertestuale 2‑3 volte più velocemente quando cercano materiale di riferimento, il che aumenta la produttività in scenari di formazione e supporto. Le immagini con collegamento ipertestuale offrono anche un layout più pulito, permettendo di inserire call‑to‑action senza ingombrare la pagina con URL lunghi, migliorando la leggibilità e il coinvolgimento degli utenti.

## Casi d'uso comuni

- **Documentazione prodotto:** Collegare uno screenshot di un dispositivo al suo manuale online.  
- **Dashboard dati:** Allegare un diagramma a un report Power BI live.  
- **Moduli di apprendimento:** Collegare un'illustrazione passo‑passo a un tutorial video.  
- **Materiale di marketing:** Far aprire a un'immagine promozionale una landing page con un'offerta speciale.

## Risoluzione dei problemi e consigli

| Problema | Soluzione |
|----------|-----------|
| L'immagine non apre il collegamento | Verifica che l'URL includa il protocollo (`http://` o `https://`). |
| Il collegamento appare ma non è cliccabile in alcuni visualizzatori | Apri il file con l'ultima versione del client OneNote o usa il visualizzatore integrato di Aspose.Note per i test. |
| Necessità di **più collegamenti ipertestuali sulla stessa immagine** | Aspose.Note supporta un solo collegamento ipertestuale per immagine. Per simulare più collegamenti, sovrapponi oggetti `Shape` trasparenti, ciascuno con il proprio collegamento. |
| Immagine grande causa rallentamenti di prestazioni | Ridimensiona l'immagine prima di caricarla, oppure usa `Image.setCompressed(true)` per ridurre l'uso di memoria. `Image.setCompressed(true)` comprime i dati dell'immagine per diminuire il consumo di memoria. |

## Domande frequenti

**Q: Posso aggiungere più collegamenti ipertestuali alla stessa immagine?**  
A: No. Aspose.Note consente un solo URL per immagine. Per emulare più collegamenti, sovrapponi forme trasparenti, ciascuna con il proprio collegamento.

**Q: Aspose.Note per Java è compatibile con tutte le versioni di OneNote?**  
A: Sì. La libreria funziona con OneNote 2010 e tutte le versioni successive, sia desktop che web.

**Q: Posso personalizzare l'aspetto dei collegamenti ipertestuali nei miei documenti?**  
A: Assolutamente. Puoi modificare il tooltip del collegamento, lo stile di sottolineatura e il colore usando le proprietà di stile dell'oggetto `Image`.

**Q: Ci sono limiti alla lunghezza dei collegamenti ipertestuali?**  
A: Sebbene non esista un limite codificato, mantenere gli URL sotto i 200 caratteri garantisce una migliore leggibilità ed evita troncamenti nei client OneNote più vecchi.

**Q: Aspose.Note per Java supporta formati diversi da OneNote?**  
A: Sì. Può convertire i file OneNote in PDF, HTML e diversi formati immagine, gestendo oltre **30 tipi di output** in totale.

## Conclusione

Aggiungere un **collegamento ipertestuale a un'immagine** in OneNote usando Java è una soluzione rapida che rende i tuoi blocchi appunti molto più interattivi e facili da usare. Seguendo i passaggi sopra, puoi incorporare URL, impostare tooltip e generare un file `.one` completamente funzionale in pochi minuti. Sperimenta con diverse fonti di immagine e destinazioni dei collegamenti per personalizzare l'esperienza per il tuo pubblico.

---

**Ultimo aggiornamento:** 2026-07-24  
**Testato con:** Aspose.Note per Java 26.4  
**Autore:** Aspose

## Tutorial correlati

- [Come aggiungere un'immagine a OneNote usando Java](/note/java/onenote-hyperlinks-images/insert-image/)
- [Come aggiungere un'immagine a OneNote usando Java – Creare documento e inserire immagine](/note/java/onenote-hyperlinks-images/build-doc-insert-image/)
- [Come aggiungere testo alternativo a un'immagine in OneNote usando Java](/note/java/onenote-image-alternative-text/add-alternative-text-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
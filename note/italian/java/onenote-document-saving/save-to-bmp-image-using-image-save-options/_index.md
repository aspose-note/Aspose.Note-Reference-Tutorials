---
date: 2025-12-16
description: Scopri come salvare i documenti OneNote in immagini BMP utilizzando le
  opzioni di salvataggio immagine di Aspose.Note per Java. Vedi anche come salvare
  OneNote in PDF o PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: come salvare OneNote in immagine BMP usando le opzioni di salvataggio immagine
url: /it/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# come salvare OneNote in immagine BMP usando Image Save Options

## Introduzione

Aspose.Note for Java è una libreria potente che consente agli sviluppatori Java di lavorare con i file Microsoft OneNote in modo programmatico. **In questo tutorial imparerai come salvare i documenti OneNote in immagini BMP** usando la funzionalità Image Save Options di Aspose.Note for Java. Cammineremo passo passo, spiegheremo perché potresti scegliere BMP rispetto ad altri formati e ti mostreremo come integrare questa capacità nelle tue applicazioni.

## Risposte rapide
- **Che cosa fa la classe Image Save Options?** Consente di specificare il formato dell'immagine di output (BMP, PNG, JPEG, ecc.) durante la conversione di una pagina OneNote.  
- **È necessaria una licenza per eseguire il campione?** Una versione di prova gratuita è sufficiente per la valutazione, ma è necessaria una licenza commerciale per l'uso in produzione.  
- **Posso convertire una pagina OneNote in PDF o PNG invece di BMP?** Sì – basta cambiare l'enumerazione `SaveFormat` (ad es., `SaveFormat.Pdf` o `SaveFormat.Png`).  
- **Quale versione di Java è supportata?** Java 8 e successive sono pienamente supportate.  
- **È necessario un trattamento speciale per documenti di grandi dimensioni?** È possibile trasmettere lo stream di output per evitare un elevato consumo di memoria.

## Cos'è “Image Save Options” in Aspose.Note?
La classe `ImageSaveOptions` fornisce un controllo fine su come le pagine OneNote vengono renderizzate come immagini raster. È possibile impostare il formato dell'immagine, la risoluzione, la profondità di colore e altro. Questa flessibilità rende facile generare file BMP per sistemi legacy o file PNG/JPEG per l'uso web.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. Conoscenza di base del linguaggio di programmazione Java.  
2. JDK (Java Development Kit) installato sulla tua macchina.  
3. Un IDE come Eclipse o IntelliJ IDEA.  
4. Libreria Aspose.Note for Java – scaricala da [here](https://releases.aspose.com/note/java/).

## Importa pacchetti

Per prima cosa, importa le classi Aspose.Note necessarie e le utility standard di I/O di Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Passo 1: Carica il documento OneNote

Qui indichiamo la cartella che contiene il file OneNote di origine (`Aspose.one`) e lo carichiamo in un oggetto `Document`. Questo oggetto ti dà pieno accesso a pagine, sezioni e altri elementi all'interno del blocco appunti.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Passo 2: Salva il documento come immagine BMP

Concateniamo il nome del file di output, quindi chiamiamo `save` con un'istanza di `ImageSaveOptions` configurata per **BMP** (`SaveFormat.Bmp`).  
Se desideri **salvare la pagina OneNote** come PNG, basta sostituire `SaveFormat.Bmp` con `SaveFormat.Png`. Allo stesso modo, `SaveFormat.Pdf` consente di eseguire una conversione **OneNote a PDF**.

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## Perché scegliere BMP?
- **Qualità lossless** – BMP memorizza i dati pixel grezzi, preservando l'aspetto esatto della pagina originale.  
- **Compatibilità** – Le vecchie applicazioni Windows spesso richiedono file BMP.  
- **Semplicità** – Nessun artefatto di compressione, rendendolo ideale per ulteriori elaborazioni di immagini.

## Problemi comuni e suggerimenti

- **Errori di percorso file** – Assicurati che `dataDir` termini con il separatore di file appropriato (`/` o `\`).  
- **Blocchi appunti grandi** – Per file OneNote molto grandi, considera di salvare ogni pagina singolarmente per mantenere basso l'uso di memoria.  
- **Eccezioni di licenza** – Eseguire il codice senza una licenza valida aggiungerà una filigrana all'immagine generata.

## Conclusione

In questa guida abbiamo dimostrato **come salvare i documenti OneNote** in immagini BMP usando `ImageSaveOptions` di Aspose.Note for Java. Cambiando l'enumerazione `SaveFormat` è possibile generare anche PNG, JPEG, PDF o altri formati supportati, offrendo un modo flessibile per esportare il contenuto OneNote per qualsiasi scenario successivo.

## Domande frequenti

**Q1: Posso salvare i documenti OneNote in altri formati immagine oltre a BMP?**  
A: Sì, è possibile utilizzare `ImageSaveOptions` con `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` o `SaveFormat.Tiff` per esportare in tali formati.

**Q2: Aspose.Note for Java supporta la conversione tra diversi formati di documento?**  
A: Assolutamente. Oltre ai formati immagine, è possibile convertire i file OneNote in PDF, DOCX, HTML e altro usando il `SaveFormat` appropriato.

**Q3: Aspose.Note for Java è compatibile con le versioni più recenti di OneNote?**  
A: Sì, la libreria viene aggiornata regolarmente per rimanere allineata alle ultime versioni di OneNote.

**Q4: Posso manipolare il contenuto dei documenti OneNote programmaticamente?**  
A: Sì, è possibile aggiungere, modificare o eliminare pagine, sezioni e contenuti ricchi (testo, immagini, tabelle) tramite l'API.

**Q5: Aspose.Note for Java fornisce supporto tecnico?**  
A: Sì, Aspose offre supporto tecnico e un forum dedicato. Visita il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per assistenza.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose
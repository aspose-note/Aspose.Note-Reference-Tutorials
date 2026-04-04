---
date: 2026-03-05
description: Scopri come esportare i documenti OneNote in immagini BMP utilizzando
  le Opzioni di Salvataggio Immagine di Aspose.Note per Java. Vedi anche come convertire
  OneNote in PDF o salvare OneNote come PNG.
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: come esportare OneNote in immagine BMP usando le opzioni di salvataggio immagine
url: /it/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# come esportare onenote in immagine BMP usando le opzioni di salvataggio immagine

## Come esportare onenote in immagine BMP

Aspose.Note for Java è una libreria potente che consente agli sviluppatori Java di lavorare con i file Microsoft OneNote in modo programmatico. **In questo tutorial imparerai a esportare documenti onenote in immagini BMP** utilizzando la funzionalità Image Save Options di Aspose.Note for Java. Ti guideremo passo passo, spiegheremo perché potresti scegliere BMP rispetto ad altri formati e ti mostreremo come integrare questa capacità nelle tue applicazioni.

## Risposte rapide
- **Cosa fa la classe Image Save Options?** Consente di specificare il formato immagine di output (BMP, PNG, JPEG, ecc.) durante la conversione di una pagina OneNote.  
- **È necessaria una licenza per eseguire il campione?** Una versione di prova gratuita è sufficiente per la valutazione, ma è richiesta una licenza commerciale per l'uso in produzione.  
- **Posso convertire una pagina OneNote in PDF o PNG invece di BMP?** Sì – basta modificare l'enumerazione `SaveFormat` (ad es., `SaveFormat.Pdf` o `SaveFormat.Png`).  
- **Quale versione di Java è supportata?** Java 8 e successive sono pienamente supportate.  
- **Esiste una gestione speciale per documenti di grandi dimensioni?** È possibile eseguire lo streaming dell'output per evitare un elevato consumo di memoria.

## Cos’è “Image Save Options” in Aspose.Note?
La classe `ImageSaveOptions` offre un controllo dettagliato su come le pagine OneNote vengono renderizzate come immagini raster. È possibile impostare il formato immagine, la risoluzione, la profondità di colore e altro. Questa flessibilità rende semplice **esportare l’immagine della pagina onenote** per sistemi legacy (BMP) o scenari web moderni (PNG/JPEG).  

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. Conoscenze di base del linguaggio di programmazione Java.  
2. JDK (Java Development Kit) installato sulla tua macchina.  
3. Un IDE come Eclipse o IntelliJ IDEA.  
4. La libreria Aspose.Note for Java – scaricala da [qui](https://releases.aspose.com/note/java/).

## Importare i pacchetti

Per prima cosa, importa le classi necessarie di Aspose.Note e le utility standard di I/O di Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Passo 1: Caricare il documento OneNote

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Qui puntiamo alla cartella che contiene il file OneNote sorgente (`Aspose.one`) e lo carichiamo in un oggetto `Document`. Questo oggetto ti dà pieno accesso a pagine, sezioni e altri elementi del notebook.

## Passo 2: Salvare il documento come immagine BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Concatenamo il nome del file di output, quindi chiamiamo `save` con un'istanza di `ImageSaveOptions` configurata per **BMP** (`SaveFormat.Bmp`).  
Se desideri **salvare la pagina onenote** come PNG, sostituisci semplicemente `SaveFormat.Bmp` con `SaveFormat.Png`. Allo stesso modo, `SaveFormat.Pdf` ti permette di eseguire una conversione **onenote to pdf**.

## Perché scegliere BMP?
- **Qualità senza perdita** – BMP memorizza i dati pixel grezzi, preservando l’aspetto esatto della pagina originale.  
- **Compatibilità** – Le vecchie applicazioni Windows spesso richiedono file BMP.  
- **Semplicità** – Nessun artefatto di compressione, ideale per ulteriori elaborazioni di immagine.

## Problemi comuni e suggerimenti

- **Errori di percorso file** – Assicurati che `dataDir` termini con il separatore di file appropriato (`/` o `\`).  
- **Notebook di grandi dimensioni** – Per file OneNote molto grandi, considera di salvare ogni pagina singolarmente per mantenere basso l’utilizzo di memoria.  
- **Eccezioni di licenza** – Eseguire il codice senza una licenza valida aggiungerà una filigrana all’immagine generata.

## Conclusione

In questa guida abbiamo dimostrato **come esportare onenote** in immagini BMP usando `ImageSaveOptions` di Aspose.Note for Java. Cambiando l’enumerazione `SaveFormat` è possibile generare anche PNG, JPEG, PDF o altri formati supportati, offrendo un modo flessibile per esportare i contenuti di OneNote per qualsiasi scenario successivo.

## Domande frequenti

**Q1: Posso salvare i documenti OneNote in altri formati immagine oltre al BMP?**  
A: Sì, puoi usare `ImageSaveOptions` con `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` o `SaveFormat.Tiff` per esportare in quei formati.

**Q2: Aspose.Note for Java supporta la conversione tra diversi formati di documento?**  
A: Assolutamente. Oltre ai formati immagine, puoi convertire i file OneNote in PDF, DOCX, HTML e altro usando il `SaveFormat` appropriato.

**Q3: Aspose.Note for Java è compatibile con le versioni più recenti di OneNote?**  
A: Sì, la libreria viene aggiornata regolarmente per rimanere in linea con le ultime versioni di OneNote.

**Q4: Posso manipolare programmaticamente il contenuto dei documenti OneNote?**  
A: Sì, è possibile aggiungere, modificare o eliminare pagine, sezioni e contenuti ricchi (testo, immagini, tabelle) tramite l’API.

**Q5: Aspose.Note for Java offre supporto tecnico?**  
A: Sì, Aspose fornisce supporto tecnico e un forum dedicato. Visita il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per assistenza.

---

**Ultimo aggiornamento:** 2026-03-05  
**Testato con:** Aspose.Note for Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
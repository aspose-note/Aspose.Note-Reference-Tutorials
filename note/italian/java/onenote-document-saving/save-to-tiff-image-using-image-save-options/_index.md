---
date: 2026-11-05
description: Scopri come ridurre le dimensioni dei file TIFF durante la conversione
  di notebook OneNote in TIFF in Java usando Aspose.Note. Include opzioni JPEG, PackBits
  e TIFF in bianco e nero.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Come ridurre le dimensioni dei file TIFF durante la conversione di OneNote
  in Java
og_description: Scopri come ridurre le dimensioni dei file TIFF durante la conversione
  di notebook OneNote in TIFF in Java usando Aspose.Note. Include opzioni JPEG, PackBits
  e TIFF in bianco e nero.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Come ridurre le dimensioni dei file TIFF durante la conversione di OneNote
  in Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Come ridurre le dimensioni dei file TIFF durante la conversione di OneNote
  in Java
url: /it/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come ridurre le dimensioni del file TIFF durante la conversione di OneNote in Java

## Introduzione

In questo tutorial scoprirai come **ridurre le dimensioni del file TIFF** durante la conversione dei taccuini OneNote in immagini TIFF usando Aspose.Note per Java. Esamineremo tre metodi di compressione—TIFF JPEG, PackBits e CCITT Group 3 (TIFF in bianco e nero)—mostrandoti come regolare la qualità dell'immagine, controllare la modalità colore e mantenere le dimensioni dei file ottimali per scenari web, di archiviazione o fax.

## Risposte rapide
- **Che cos'è la compressione TIFF JPEG?** Un metodo di compressione con perdita che riduce le dimensioni del file TIFF mantenendo la qualità visiva.  
- **Quale libreria gestisce la conversione?** Aspose.Note per Java.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita funziona per i test; è necessaria una licenza per la produzione.  
- **Posso modificare la qualità dell'immagine?** Sì, imposta la proprietà `quality` su `ImageSaveOptions`.  
- **È possibile la conversione batch?** Assolutamente – itera sui documenti e applica le stesse opzioni.

## Panoramica della compressione TIFF JPEG

La compressione TIFF JPEG memorizza i dati dell'immagine in un contenitore TIFF ma applica l'algoritmo JPEG con perdita per ridurre il file. È ideale quando è necessario un equilibrio tra **qualità dell'immagine TIFF** e dimensioni più piccole, soprattutto per scenari web o di archiviazione.

## Perché utilizzare diversi tipi di compressione TIFF?

Scegli il tipo di compressione in base al contenuto e alle esigenze di archiviazione: JPEG è il più adatto per le fotografie, PackBits offre compressione loss‑less per grafiche con ampie aree uniformi, e CCITT Group 3 fornisce compressione ad alto rapporto per documenti fax in bianco e nero. Selezionare il metodo corretto ti permette di **ridurre le dimensioni del file TIFF** senza compromettere la fedeltà visiva richiesta dalla tua applicazione.

## Scegliere la compressione giusta

- **JPEG** – Qualità regolabile (0‑100) che consente di bilanciare dimensione e dettaglio, perfetta per pagine ricche di colore.  
- **PackBits** – Codifica run‑length loss‑less; ideale quando è necessario mantenere ogni pixel esatto.  
- **CCITT Group 3** – Solo monocromatico; massimizza la compressione per testi scansionati o documenti fax.  

## Convertire OneNote in TIFF usando Aspose.Note

Se il tuo obiettivo è **convertire OneNote in TIFF**, i tre metodi seguenti coprono gli scenari più comuni. Ogni metodo carica un file `.one`, configura `ImageSaveOptions` e salva il risultato come file `.tiff`.

## Prerequisiti

- Java Development Kit (JDK) installato.  
- Libreria Aspose.Note per Java aggiunta al tuo progetto (Maven/Gradle o JAR manuale).  
- Familiarità di base con la sintassi Java.

## Importare i pacchetti

Le classi `ImageSaveOptions`, `TiffCompression` e `ColorMode` sono il nucleo dell'API di conversione.  

`ImageSaveOptions` definisce le opzioni per il salvataggio delle immagini, come formato e compressione.  
`TiffCompression` elenca gli algoritmi di compressione TIFF supportati.  
`ColorMode` specifica la profondità di colore, ad esempio a colori o in bianco e nero.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Passo 1: salvare in TIFF usando la compressione TIFF JPEG

### Salvataggio di TIFF con compressione JPEG in Java

Carica il file OneNote, configura `ImageSaveOptions` con compressione JPEG, opzionalmente imposta il valore `quality` e chiama il metodo di salvataggio. Questo schema a due passaggi ti offre il pieno controllo su dimensione dell'output e fedeltà visiva.

1. Imposta `dataDir` sulla cartella contenente il tuo file `.one`.  
2. Chiama `SaveToTiffUsingJpegCompression()` dal tuo metodo principale o servizio.  
3. Il file `.tiff` risultante apparirà nella stessa directory.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Explanation**

- `ImageSaveOptions` indica ad Aspose.Note di generare un file TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` seleziona la compressione JPEG.  
- `setQuality(93)` (opzionale) regola finemente la qualità dell'immagine; valori più bassi producono file più piccoli.

## Panoramica della compressione TIFF PackBits

PackBits è un algoritmo di compressione lossless che funziona al meglio per immagini con ampie aree di colore uniforme. È spesso indicato come **compressione tiff packbits** nella documentazione.

## Salvataggio di TIFF con compressione PackBits in Java

Se ti serve un'opzione loss‑less, PackBits è un semplice algoritmo run‑length che funziona bene per grafiche con colori solidi. Configura `ImageSaveOptions` con `TiffCompression.PackBits` e salva il documento.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Explanation**

- `setTiffCompression(TiffCompression.PackBits)` cambia il metodo di compressione.  
- Non è necessario impostare la qualità perché PackBits è loss‑less.

## Salvataggio di TIFF con compressione CCITT Group 3 in Java

Per documenti in stile fax spesso si desidera un **TIFF in bianco e nero**. CCITT Group 3 offre alta compressione per immagini monocromatiche. Imposta la modalità colore su bianco e nero e scegli l'enumerazione di compressione CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Explanation**

- `setColorMode(ColorMode.BlackAndWhite)` forza un output monocromatico.  
- `setTiffCompression(TiffCompression.Ccitt3)` applica la compressione orientata al fax.

## Problemi comuni e consigli

| Problema | Soluzione |
|----------|-----------|
| **Il file di output è più grande del previsto** | Prova a ridurre il valore `quality` JPEG o passa a PackBits se la compressione lossless è accettabile. |
| **I colori appaiono sbiaditi** | Assicurati di non aver impostato involontariamente `ColorMode.BlackAndWhite` quando è necessario il colore completo. |
| **Errore di formato immagine non supportato** | Verifica di utilizzare una versione recente di Aspose.Note; le versioni più vecchie potrebbero non includere alcune enumerazioni di compressione. |
| **LicenseException a runtime** | Installa una licenza Aspose.Note valida (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Domande frequenti

**Q: Posso convertire altri tipi di documento (ad esempio PDF, DOCX) in TIFF con queste opzioni?**  
A: Sì. Sebbene Aspose.Note si concentri sui file OneNote, Aspose.PDF, Aspose.Words e altre librerie offrono `ImageSaveOptions` simili per i loro formati.

**Q: In che modo la compressione TIFF JPEG differisce da un file JPEG standard?**  
A: L'algoritmo JPEG è lo stesso, ma i dati dell'immagine sono contenuti in un contenitore TIFF, che può contenere più pagine e metadati più ricchi.

**Q: È possibile elaborare in batch molti file `.one`?**  
A: Assolutamente. Itera su una directory, chiama uno dei tre metodi per ogni file e raccogli i TIFF risultanti.

**Q: Posso controllare DPI/risoluzione del TIFF di output?**  
A: Sì. Usa `options.setResolution(int dpi)` prima di salvare.

**Q: Aspose.Note supporta l'elaborazione asincrona?**  
A: L'API è sincrona, ma è possibile avvolgere le chiamate in `CompletableFuture` di Java o in un pool di thread per esecuzione parallela.

## Conclusione

Ora disponi di un toolkit completo per la **conversione TIFF in Java** che ti consente di **ridurre le dimensioni del file TIFF** quando salvi i documenti OneNote come file TIFF usando la compressione JPEG, PackBits o CCITT Group 3 Fax. Regola qualità, modalità colore e risoluzione per soddisfare i requisiti specifici e integra questi metodi nei flussi di lavoro batch per la massima produttività.

---

**Ultimo aggiornamento:** 2026-11-05  
**Testato con:** Aspose.Note for Java 26.4 (latest at time of writing)  
**Autore:** Aspose

## Tutorial correlati

- [Come rendere l'immagine della pagina OneNote (JPEG) usando il formato di salvataggio con Aspose.Note per Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Usa Aspose.Note per Java per salvare OneNote come PNG con opzioni – Converti il taccuino in immagine](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Come esportare OneNote come immagine in scala di grigi – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
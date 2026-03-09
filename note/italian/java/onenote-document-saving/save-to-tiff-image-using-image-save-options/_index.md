---
date: 2025-12-17
description: Scopri come salvare i documenti OneNote come file TIFF utilizzando la
  compressione TIFF JPEG, PackBits o CCITT Group 3 Fax in Java. Controlla la qualità
  dell'immagine, la dimensione del file e la modalità colore con Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Salva immagine TIFF usando la compressione JPEG TIFF in OneNote
url: /it/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva immagine TIFF usando compressione TIFF JPEG in OneNote

## Introduzione

In questo tutorial scoprirai **come salvare un documento OneNote in un file TIFF usando la compressione TIFF JPEG** e altri due metodi di compressione popolari. Ti guideremo attraverso la configurazione necessaria, importeremo i pacchetti Java richiesti e forniremo codice chiaro passo‑passo per ogni opzione di compressione. Alla fine potrai controllare **la qualità dell'immagine TIFF**, ridurre le dimensioni del file e persino produrre TIFF in bianco‑nero per output in stile fax.

## Risposte rapide
- **Cos'è la compressione TIFF JPEG?** Un metodo di compressione con perdita che riduce le dimensioni del file TIFF mantenendo la qualità visiva.  
- **Quale libreria gestisce la conversione?** Aspose.Note per Java.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza per la produzione.  
- **Posso modificare la qualità dell'immagine?** Sì, imposta la proprietà `quality` su `ImageSaveOptions`.  
- **È possibile la conversione batch?** Assolutamente – itera sui documenti e applica le stesse opzioni.

## Cos'è la compressione TIFF JPEG?
La compressione TIFF JPEG memorizza i dati dell'immagine nel contenitore TIFF ma applica l'algoritmo lossy di JPEG per ridurre il file. È ideale quando è necessario un equilibrio tra **qualità dell'immagine TIFF** e dimensioni più ridotte, specialmente per scenari web o di archiviazione.

## Perché usare diversi tipi di compressione TIFF?
- **JPEG** – Buono per le fotografie; offre qualità regolabile.  
- **PackBits** – Codifica run‑length semplice e senza perdita; utile per grafiche con ampie aree uniformi.  
- **CCITT Group 3 Fax** – Solo bianco‑nero; perfetto per documenti scansionati e trasmissione fax.  

Scegliere la compressione giusta ti consente di rispettare i vincoli di archiviazione senza sacrificare la fedeltà visiva richiesta dalla tua applicazione.

## Prerequisiti

- Java Development Kit (JDK) installato.  
- Libreria Aspose.Note per Java aggiunta al tuo progetto (Maven/Gradle o JAR manuale).  
- Familiarità di base con la sintassi Java.

## Importa pacchetti

Per prima cosa, porta le classi necessarie di Aspose.Note nel tuo file Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Passo 1: Salva in TIFF usando compressione TIFF JPEG

Di seguito trovi il metodo completo che carica un file OneNote e lo salva come TIFF con compressione JPEG. Regola il valore `quality` (0‑100) per controllare **qualità dell'immagine TIFF**.

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

**Spiegazione**

- `ImageSaveOptions` indica ad Aspose.Note di generare un file TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` seleziona la compressione JPEG.  
- `setQuality(93)` (opzionale) regola finemente la qualità dell'immagine; valori più bassi producono file più piccoli.

### Come salvare TIFF con compressione JPEG in Java
1. Imposta `dataDir` sulla cartella contenente il tuo file `.one`.  
2. Chiama `SaveToTiffUsingJpegCompression()` dal tuo metodo `main` o dal servizio.  
3. Il file `.tiff` risultante apparirà nella stessa directory.

## Passo 2: Salva in TIFF usando compressione PackBits

Se ti serve un'opzione senza perdita, PackBits è un semplice algoritmo run‑length che funziona bene per grafiche con colori solidi.

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

**Spiegazione**

- `setTiffCompression(TiffCompression.PackBits)` cambia il metodo di compressione.  
- Non è necessario impostare la qualità perché PackBits è senza perdita.

## Passo 3: Salva in TIFF usando compressione CCITT Group 3 Fax (TIFF bianco‑nero)

Per documenti in stile fax spesso si desidera un **TIFF bianco‑nero**. CCITT Group 3 fornisce alta compressione per immagini monocromatiche.

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

**Spiegazione**

- `setColorMode(ColorMode.BlackAndWhite)` forza un output monocromatico.  
- `setTiffCompression(TiffCompression.Ccitt3)` applica la compressione orientata al fax.

## Problemi comuni e consigli

| Problema | Soluzione |
|----------|-----------|
| **Il file di output è più grande del previsto** | Prova a ridurre il valore `quality` JPEG o passa a PackBits se la compressione senza perdita è accettabile. |
| **I colori appaiono sbiaditi** | Assicurati di non impostare involontariamente `ColorMode.BlackAndWhite` quando ti serve il colore completo. |
| **Errore di formato immagine non supportato** | Verifica di utilizzare una versione recente di Aspose.Note; le versioni più vecchie potrebbero non includere alcune enumerazioni di compressione. |
| **LicenseException a runtime** | Installa una licenza Aspose.Note valida (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Domande frequenti

**D: Posso convertire altri tipi di documento (ad es., PDF, DOCX) in TIFF con queste opzioni?**  
R: Sì. Aspose.Note si concentra sui file OneNote, ma le altre librerie di Aspose (PDF, Words) offrono `ImageSaveOptions` simili per i rispettivi formati.

**D: In che modo la compressione TIFF JPEG differisce dai file JPEG standard?**  
R: I dati dell'immagine sono memorizzati all'interno di un contenitore TIFF, preservando i metadati e consentendo più pagine, mentre l'algoritmo di compressione rimane JPEG.

**D: È possibile elaborare in batch molti file `.one`?**  
R: Assolutamente. Scorri una cartella, chiama uno dei tre metodi per ogni file e raccogli i TIFF risultanti.

**D: Posso controllare DPI/risoluzione del TIFF di output?**  
R: Sì. Usa `options.setResolution(int dpi)` prima di salvare.

**D: Aspose.Note supporta l'elaborazione asincrona?**  
R: L'API è sincrona, ma è possibile avvolgere le chiamate in `CompletableFuture` di Java o in pool di thread per esecuzione parallela.

## Conclusione

Ora disponi di un toolkit completo per la **conversione TIFF in Java** che ti consente di salvare documenti OneNote come file TIFF usando compressione JPEG, PackBits o CCITT Group 3 Fax. Regola qualità, modalità colore e risoluzione per soddisfare requisiti specifici di **qualità dell'immagine TIFF**, e integra questi metodi nei flussi di lavoro batch per la massima produttività.

---

**Ultimo aggiornamento:** 2025-12-17  
**Testato con:** Aspose.Note per Java 23.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
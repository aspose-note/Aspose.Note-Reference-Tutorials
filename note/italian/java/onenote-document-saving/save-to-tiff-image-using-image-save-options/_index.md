---
title: Salva in immagine TIFF utilizzando le opzioni di salvataggio immagine in OneNote
linktitle: Salva in immagine TIFF utilizzando le opzioni di salvataggio immagine in OneNote
second_title: Aspose.Note API Java
description: Converti documenti OneNote in TIFF e controlla le dimensioni e la qualità dei file! Scegli la compressione Jpeg, PackBits o Fax in Java. Ottieni esempi di codice e scopri come! #OneNote #Java #Aspose
weight: 21
url: /it/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva in immagine TIFF utilizzando le opzioni di salvataggio immagine in OneNote

## introduzione

In questo tutorial imparerai come salvare un documento in un formato immagine TIFF utilizzando diversi metodi di compressione in Aspose.Note per Java. Tratteremo i prerequisiti, l'importazione dei pacchetti e forniremo una guida passo passo per ciascun metodo di compressione.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

- Java Development Kit (JDK) installato sul tuo sistema.
- Aspose.Note per la libreria Java scaricata e configurata.
- Conoscenza di base del linguaggio di programmazione Java.

## Importa pacchetti

Innanzitutto, devi importare i pacchetti necessari nel tuo file Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Passaggio 1: salva in TIFF utilizzando la compressione JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Il percorso della directory dei documenti.
    String dataDir = "Your Document Directory";

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Caricare il documento utilizzando`Document` classe.
-  Crea un'istanza di`ImageSaveOptions` e specificare il tipo di compressione TIFF come JPEG.
- Imposta la qualità desiderata (opzionale).
- Salvare il documento in formato TIFF utilizzando le opzioni specificate.

## Passaggio 2: salva in TIFF utilizzando la compressione PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Il percorso della directory dei documenti.
    String dataDir = "Your Document Directory";

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Caricare il documento utilizzando`Document` classe.
-  Crea un'istanza di`ImageSaveOptions` e specificare il tipo di compressione TIFF come PackBits.
- Salvare il documento in formato TIFF utilizzando le opzioni specificate.

## Passaggio 3: salvare in TIFF utilizzando la compressione fax CCITT gruppo 3

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Il percorso della directory dei documenti.
    String dataDir = "Your Document Directory";

    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Caricare il documento utilizzando`Document` classe.
-  Crea un'istanza di`ImageSaveOptions` e specificare il tipo di compressione TIFF come CCITT Gruppo 3 Fax.
- Imposta la modalità colore su bianco e nero.
- Salvare il documento in formato TIFF utilizzando le opzioni specificate.

## Conclusione

In questo tutorial, hai imparato come salvare un documento nel formato immagine TIFF utilizzando diversi metodi di compressione in Aspose.Note per Java. Seguendo la guida passo passo, puoi utilizzare in modo efficiente le funzionalità di Aspose.Note per soddisfare le tue esigenze.

## Domande frequenti

### Q1: Posso utilizzare Aspose.Note per Java per convertire altri formati di documenti in TIFF?

A1: Sì, Aspose.Note per Java supporta la conversione da vari formati di documenti in TIFF, inclusi i documenti OneNote.

### Q2: Qual è il significato di specificare il tipo di compressione durante il salvataggio in TIFF?

R2: Specificando il tipo di compressione è possibile controllare la qualità dell'immagine e la dimensione del file. Diversi metodi di compressione offrono compromessi tra qualità e rapporto di compressione.

### Q3: Aspose.Note per Java è adatto per l'elaborazione batch di documenti?

A3: Sì, Aspose.Note per Java fornisce API per l'elaborazione batch, consentendo di automatizzare le attività di conversione dei documenti in modo efficiente.

### Q4: Posso personalizzare ulteriormente le impostazioni di compressione?

R4: Sì, puoi regolare parametri quali qualità, risoluzione e metodo di compressione per personalizzare l'output in base alle tue esigenze.

### Q5: Aspose.Note per Java offre supporto tecnico?

A5: Sì, Aspose fornisce supporto tecnico completo tramite forum e sistemi basati su ticket.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

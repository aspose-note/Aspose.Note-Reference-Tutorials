---
title: Salva su immagine in scala di grigi in OneNote - Aspose.Note
linktitle: Salva su immagine in scala di grigi in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come salvare un documento come immagine in scala di grigi in OneNote utilizzando Aspose.Note per Java. Manipola facilmente i documenti Microsoft OneNote a livello di codice.
type: docs
weight: 17
url: /it/java/onenote-document-saving/save-to-grayscale-image/
---
## introduzione

In questo tutorial esploreremo come salvare un documento come immagine in scala di grigi in OneNote utilizzando Aspose.Note per Java. Le immagini in scala di grigio sono immagini monocromatiche in cui le informazioni sul colore sono rappresentate solo da sfumature di grigio. Aspose.Note è una potente API Java che consente la manipolazione dei documenti Microsoft OneNote a livello di codice.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.
2.  Aspose.Note per la libreria Java. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/java/).
3. Conoscenza di base della programmazione Java.

## Importa pacchetti

Per iniziare, importa i pacchetti necessari:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Passaggio 1: caricare il documento

 Innanzitutto, carica il documento in Aspose.Note. Sostituire`"Your Document Directory"` con il percorso della directory dei documenti e`"Aspose.one"` con il nome del tuo documento OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Passaggio 2: imposta il percorso e le opzioni di output

Definire il percorso di output per l'immagine in scala di grigi e specificare le opzioni di salvataggio. Imposteremo la modalità colore su scala di grigi.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Passaggio 3: salva il documento

Infine, salva il documento come immagine in scala di grigi utilizzando le opzioni specificate.

```java
oneFile.save(dataDir, options);
```

## Conclusione

Congratulazioni! Hai imparato con successo come salvare un documento come immagine in scala di grigi in OneNote utilizzando Aspose.Note per Java. Ciò può essere incredibilmente utile per varie applicazioni in cui sono richieste immagini in scala di grigi.

## Domande frequenti

### Q1: Posso salvare l'immagine in scala di grigi in un formato diverso?

 A1: Sì, puoi. Cambia semplicemente il`SaveFormat` parametro nel`ImageSaveOptions` costruttore nel formato desiderato.

### Q2: Aspose.Note è compatibile con tutte le versioni dei documenti OneNote?

A2: Aspose.Note supporta Microsoft OneNote 2010 e versioni successive.

### Q3: Aspose.Note richiede una licenza per l'utilizzo?

A3: Sì, è necessaria una licenza valida per utilizzare Aspose.Note in ambienti di produzione. Tuttavia, è possibile ottenere una licenza temporanea a scopo di test.

### Q4: Posso manipolare altri aspetti del documento prima di salvarlo come immagine?

A4: Assolutamente! Aspose.Note offre un'ampia gamma di funzionalità per la modifica dei documenti OneNote a livello di codice.

### Q5: Dove posso trovare supporto se riscontro problemi?

A5: È possibile trovare supporto sul forum Aspose.Note[Qui](https://forum.aspose.com/c/note/28).
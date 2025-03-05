---
title: Salva in PDF utilizzando le impostazioni della pagina in OneNote - Aspose.Note
linktitle: Salva in PDF utilizzando le impostazioni della pagina in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come salvare documenti OneNote in PDF in Java utilizzando la libreria Aspose.Note. Guida passo passo con esempi di codice per diverse impostazioni di pagina.
type: docs
weight: 19
url: /it/java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## introduzione

In questo tutorial impareremo come salvare i documenti OneNote in formato PDF utilizzando diverse impostazioni di pagina con Aspose.Note per Java. Tratteremo due metodi: salvare con le impostazioni della pagina Letter e salvare con le impostazioni della pagina A4 senza limiti di altezza.

## Prerequisiti

Prima di iniziare, assicurati di disporre dei seguenti prerequisiti:

1. Java Development Kit (JDK) installato sul tuo sistema.
2. Aspose.Note per la libreria Java scaricata e inclusa nel tuo progetto Java.
3. Conoscenza di base del linguaggio di programmazione Java.

## Importa pacchetti

Assicurati di aver importato i pacchetti necessari per utilizzare Aspose.Note per Java nel tuo progetto. Ecco la dichiarazione di importazione:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Salva in PDF utilizzando le impostazioni della pagina Letter

### Passaggio 1: caricare il documento

Innanzitutto, carica il documento OneNote in Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Passaggio 2: definire il percorso di destinazione

Specificare il percorso di destinazione del file PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Passaggio 3: salva il documento

Salvare il documento con le impostazioni della pagina Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Salva in PDF utilizzando le impostazioni della pagina A4 senza limite di altezza

### Passaggio 1: caricare il documento

Allo stesso modo, carica il documento OneNote in Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Passaggio 2: definire il percorso di destinazione

Specificare il percorso di destinazione del file PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Passaggio 3: salva il documento

Salva il documento con le impostazioni della pagina A4 senza limite di altezza:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Dopo aver seguito questi passaggi, avrai salvato con successo il tuo documento OneNote in PDF utilizzando diverse impostazioni di pagina.

## Conclusione

In questo tutorial, abbiamo esplorato come salvare i documenti OneNote in formato PDF utilizzando la libreria Aspose.Note per Java. Seguendo la guida passo passo, puoi facilmente integrare questa funzionalità nelle tue applicazioni Java.

## Domande frequenti

### Q1: Posso personalizzare ulteriormente le impostazioni della pagina?

A1: Sì, puoi personalizzare le impostazioni della pagina in base alle tue esigenze utilizzando Aspose.Note per Java.

### Q2: Aspose.Note supporta altri formati di output oltre al PDF?

A2: Sì, Aspose.Note supporta vari formati di output tra cui immagini e HTML.

### Q3: Aspose.Note è compatibile con diverse versioni di file OneNote?

A3: Sì, Aspose.Note supporta file OneNote di diverse versioni tra cui .one e .onetoc2.

### Q4: Posso convertire più file OneNote in PDF in un'unica esecuzione?

A4: Sì, è possibile elaborare in batch più file OneNote utilizzando Aspose.Note per Java.

### Q5: È disponibile una versione di prova a scopo di test?

A5: Sì, puoi ottenere una prova gratuita di Aspose.Note per Java dal sito web.
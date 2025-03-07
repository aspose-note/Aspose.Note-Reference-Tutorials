---
title: Salva utilizzando il sottosistema di caratteri specificato in OneNote
linktitle: Salva utilizzando il sottosistema di caratteri specificato in OneNote
second_title: Aspose.Note API Java
description: Scopri come salvare i documenti OneNote utilizzando il sottosistema di caratteri specificato in Java con Aspose.Note. Garantisci una rappresentazione coerente dei caratteri su tutte le piattaforme senza sforzo.
weight: 22
url: /it/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva utilizzando il sottosistema di caratteri specificato in OneNote

## introduzione

Aspose.Note per Java fornisce solide funzionalità per lavorare con documenti OneNote. Un requisito comune quando si lavora con tali documenti è garantire che i caratteri siano mantenuti correttamente, soprattutto se il documento deve essere esportato o salvato in formati diversi come PDF. Questo tutorial ti guiderà attraverso il processo di salvataggio dei documenti OneNote specificando il sottosistema dei caratteri, garantendo una rappresentazione coerente e accurata del testo su varie piattaforme.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di aver impostato i seguenti prerequisiti:

### 1. Kit di sviluppo Java (JDK)

 Assicurati di avere Java Development Kit (JDK) installato sul tuo sistema. Puoi scaricarlo da[Qui](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) se non l'hai già fatto.

### 2. Aspose.Note per la libreria Java

 Scarica e configura la libreria Aspose.Note per Java. Puoi scaricarlo da[sito web](https://releases.aspose.com/note/java/).

## Importa pacchetti

Assicurati di importare i pacchetti necessari nel tuo progetto Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Ora suddividiamo ogni esempio in più passaggi per comprendere meglio il processo.

## Passaggio 1: salvare utilizzando il sottosistema dei caratteri del documento con il nome del carattere predefinito

Questo passaggio dimostra come salvare un documento in formato PDF utilizzando un nome di carattere predefinito specificato.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specificare il carattere predefinito.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Salva il documento come PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

In questo passaggio:
- Il documento OneNote viene caricato utilizzando Aspose.Note.
- Il carattere predefinito è specificato come "Times New Roman".
- Il documento viene salvato in formato PDF con il carattere specificato.

## Passaggio 2: salvare utilizzando il sottosistema dei caratteri del documento con il carattere predefinito dal file

Questo passaggio dimostra come salvare un documento in formato PDF utilizzando un carattere predefinito caricato da un file.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specificare il percorso del file del carattere.
    String fontFile = "geo_1.ttf";

    // Specificare il carattere predefinito dal file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Salva il documento come PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

In questo passaggio:
- Viene caricato il file del carattere "geo_1.ttf".
- Il carattere predefinito viene specificato dal file dei caratteri caricato.
- Il documento viene salvato in formato PDF con il carattere specificato.

## Passaggio 3: salvare utilizzando il sottosistema dei caratteri del documento con il carattere predefinito dallo stream

Questo passaggio dimostra come salvare un documento in formato PDF utilizzando un carattere predefinito caricato da un flusso.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Caricare il documento in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specificare il percorso del file del carattere.
    String fontFile = "geo_1.ttf";

    // Carica il file del carattere come flusso.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specificare il carattere predefinito dal flusso.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Salva il documento come PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

In questo passaggio:
- Il file del carattere "geo_1.ttf" viene caricato come flusso.
- Il carattere predefinito è specificato dal flusso caricato.
- Il documento viene salvato in formato PDF con il carattere specificato.

## Conclusione

In questo tutorial, abbiamo imparato come salvare i documenti OneNote utilizzando il sottosistema di caratteri specificato in Java utilizzando Aspose.Note. Seguendo questi passaggi, puoi garantire una rappresentazione coerente dei caratteri su varie piattaforme durante l'esportazione o il salvataggio dei documenti.

## Domande frequenti

### Q1: Posso specificare caratteri diversi per parti diverse del documento?

A1: Sì, puoi specificare caratteri diversi per diverse parti del documento utilizzando Aspose.Note per Java.

### Q2: Aspose.Note è compatibile con tutte le versioni di OneNote?

A2: Aspose.Note supporta varie versioni di OneNote, garantendo la compatibilità tra diversi ambienti.

### Q3: Come posso gestire i caratteri mancanti durante il salvataggio dei documenti?

A3: Aspose.Note fornisce opzioni per specificare i caratteri predefiniti per gestire in modo efficace i caratteri mancanti durante il salvataggio del documento.

### Q4: Posso personalizzare le proprietà del carattere come dimensione e stile?

A4: Sì, puoi personalizzare le proprietà del carattere come dimensione, stile e colore utilizzando Aspose.Note per Java.

### Q5: È disponibile una versione di prova per Aspose.Note per Java?

A5: Sì, puoi ottenere una prova gratuita di Aspose.Note per Java dal sito web.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

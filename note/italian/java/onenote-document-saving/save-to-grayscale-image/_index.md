---
date: 2026-06-30
description: Scopri come esportare OneNote salvando un documento come immagine PNG
  in scala di grigi utilizzando Aspose.Note per Java. Include i passaggi per caricare
  il documento OneNote e creare un'immagine in scala di grigi.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Come esportare OneNote come immagine in scala di grigi – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Come esportare OneNote come immagine in scala di grigi – Aspose.Note
url: /it/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva come immagine in scala di grigi in OneNote - Aspose.Note

## Introduzione

In questo tutorial scoprirai **come esportare onenote** convertendo un file OneNote `.one` in un'immagine PNG in scala di grigi ad alta qualità usando Aspose.Note per Java. La conversione in scala di grigi è spesso necessaria agli sviluppatori Java per la stampa, l'archiviazione o per **ridurre le dimensioni di OneNote** senza perdere contenuti essenziali. Ti guideremo attraverso il caricamento di un documento OneNote, la configurazione delle opzioni di salvataggio—including **regolare la risoluzione dell'immagine**—e infine il salvataggio del documento come PNG.

## Risposte rapide
- **Cosa significa “come esportare onenote”?** Si riferisce alla conversione programmatica di un file OneNote in un altro formato, ad esempio un'immagine, tramite codice.  
- **Quale formato è migliore per l'output in scala di grigi?** PNG funziona bene perché preserva la qualità loss‑less e supporta una modalità colore dedicata in scala di grigi.  
- **È necessaria una licenza?** È richiesta una licenza valida di Aspose.Note per l'uso in produzione; è disponibile una licenza di prova temporanea per i test.  
- **Quale versione di Java è richiesta?** Si consiglia Java 8 o superiore.  
- **Posso modificare le dimensioni dell'immagine?** Sì, è possibile regolare le proprietà di `ImageSaveOptions` come `Resolution` o `PageSize` prima del salvataggio.

## Cos'è “come esportare onenote”?

Esportare OneNote significa convertire programmaticamente un file OneNote `.one` in un'altra rappresentazione—come PDF, HTML o un'immagine. In questa guida ci concentriamo sulla **creazione di PNG in scala di grigi**, una esigenza comune per la documentazione o i flussi di lavoro pronti per la stampa. Con Aspose.Note, la conversione avviene interamente in memoria, quindi non è mai necessario avere Microsoft OneNote installato sul server.

## Perché esportare OneNote come immagine in scala di grigi?

I PNG in scala di grigi sono tipicamente **30‑40 % più piccoli** rispetto alle loro controparti a colori, il che velocizza la consegna sul web e riduce i costi di archiviazione. Offrono anche **un contrasto più netto** sulle stampanti laser, rendendo i report più leggibili. Poiché PNG è supportato universalmente, i file risultanti funzionano su browser, dispositivi mobili e editor desktop senza codec aggiuntivi.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. Java Development Kit (JDK) 8 o versioni successive installate.  
2. Libreria Aspose.Note per Java – scarica l'ultima versione da [qui](https://releases.aspose.com/note/java/).  
3. Una conoscenza di base della sintassi Java e della configurazione di progetti Maven/Gradle.  

## Importare i pacchetti

La classe `ImageSaveOptions` controlla come il documento viene renderizzato in un'immagine.  
`ColorMode` è un'enumerazione che consente di passare da output a colori completi a scala di grigi.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Passo 1: Caricare il documento OneNote

`Document` rappresenta un notebook OneNote e fornisce metodi per caricare, modificare e salvare i suoi contenuti. Prima, **carica il documento OneNote** in Aspose.Note. Sostituisci `"Your Document Directory"` con il percorso della tua cartella locale e `"Aspose.one"` con il nome del tuo file OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Passo 2: Impostare percorso di output e opzioni

`ImageSaveOptions` configura come un documento OneNote viene renderizzato in un file immagine. L'enumerazione `ColorMode` seleziona la modalità di rendering colore, come scala di grigi o a colori completi. Definisci il percorso di output per l'immagine in scala di grigi e specifica le opzioni di salvataggio. Imposteremo `ColorMode` su `GrayScale` e utilizzeremo il formato **salva documento come PNG**. Puoi anche **regolare la risoluzione dell'immagine** a 300 DPI per stampe di alta qualità.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Passo 3: Salvare il documento

Infine, salva il documento come immagine PNG in scala di grigi usando le opzioni configurate. Il metodo `save` scrive il file su disco senza richiedere file temporanei intermedi.

```java
oneFile.save(dataDir, options);
```

## Problemi comuni e soluzioni
- **FileNotFoundException** – Verifica che `dataDir` punti alla cartella corretta e che il file `.one` esista.  
- **LicenseException** – Assicurati di aver applicato una licenza valida di Aspose.Note prima di chiamare `save`.  
- **Output a bassa risoluzione** – Regola `options.setResolution(300)` per aumentare i DPI; DPI più alti producono stampe più nitide ma file di dimensioni maggiori.  

## Domande frequenti

**D1: Posso salvare l'immagine in scala di grigi in un formato diverso?**  
R1: Sì, basta cambiare il parametro `SaveFormat` nel costruttore `ImageSaveOptions` in `Jpeg`, `Bmp` o in uno dei oltre 20 formati immagine supportati.

**D2: Aspose.Note è compatibile con tutte le versioni dei documenti OneNote?**  
R2: Aspose.Note supporta Microsoft OneNote 2010 e versioni successive, coprendo oltre il 95 % dei notebook attivi oggi.

**D3: Aspose.Note richiede una licenza per l'uso?**  
R3: È necessaria una licenza valida per l'uso in produzione, ma è possibile ottenere una licenza di prova temporanea per la valutazione senza costi.

**D4: Posso manipolare altri aspetti del documento prima di salvarlo come immagine?**  
R4: Assolutamente! Aspose.Note fornisce API per modificare sezioni, pagine e singoli elementi come testo, tabelle e immagini prima dell'esportazione.

**D5: Dove posso trovare supporto se incontro problemi?**  
R5: Puoi trovare supporto sul forum Aspose.Note [qui](https://forum.aspose.com/c/note/28).

## Conclusione

Ora hai appreso **come esportare onenote** caricando un file OneNote, configurando le opzioni di salvataggio per **creare un'immagine in scala di grigi**, e **salvando il documento come PNG**. Questo approccio è ideale per generare visuali leggere e pronte per la stampa da notebook OneNote. Sentiti libero di sperimentare con altre impostazioni `ColorMode`, valori DPI più alti o formati immagine alternativi per soddisfare i requisiti del tuo progetto.

---

**Ultimo aggiornamento:** 2026-06-30  
**Testato con:** Aspose.Note 27.0 per Java  
**Autore:** Aspose  

---

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Export OneNote Page to PNG Image in Java using Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – Set Output Image Resolution in OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [How to Save OneNote as PDF with Aspose.Note for Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
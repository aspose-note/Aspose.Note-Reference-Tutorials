---
date: 2025-12-17
description: Scopri come esportare OneNote salvando un documento come immagine PNG
  in scala di grigi usando Aspose.Note per Java. Include i passaggi per caricare il
  documento OneNote e creare un'immagine in scala di grigi.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Come esportare OneNote in immagine in scala di grigi – Aspose.Note
url: /it/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva come immagine in scala di grigi in OneNote - Aspose.Note

## Introduzione

In questo tutorial, mostreremo **come esportare onenote** salvando un documento come immagine in scala di grigi usando Aspose.Note per Java. Le immagini in scala di grigi sono foto monocromatiche che contengono solo sfature di grigio, utili per la stampa, l'archiviazione o la riduzione delle dimensioni del file. Vi guideremo attraverso il caricamento di un documento OneNote, la configurazione delle opzioni di salvataggio per **creare un'immagine in scala di grigi**, e infine **salvare il documento come PNG**.

## Risposte rapide
- **Cosa significa “how to export onenote”?** Si riferisce alla conversione di un file OneNote in un altro formato, ad esempio un'immagine, in modo programmatico.  
- **Quale formato è migliore per l'output in scala di grigi?** PNG funziona bene perché preserva la qualità loss‑less e supporta la modalità colore in scala di grigi.  
- **È necessaria una licenza?** È richiesta una licenza valida di Aspose.Note per l'uso in produzione; è disponibile una licenza di prova temporanea per i test.  
- **Quale versione di Java è richiesta?** Si consiglia Java 8 o superiore.  
- **Posso modificare le dimensioni dell'immagine?** Sì, è possibile regolare le proprietà di `ImageSaveOptions` come `Resolution` o `PageSize` prima del salvataggio.

## Cos'è “how to export onenote”?
Esportare OneNote significa convertire programmaticamente un file OneNote `.one` in un'altra rappresentazione—come PDF, HTML o un'immagine. In questa guida ci concentriamo sull'esportazione in un'immagine **PNG in scala di grigi**, una esigenza comune per la documentazione o i flussi di lavoro di stampa.

## Perché esportare OneNote come immagine in scala di grigi?
- **Dimensione del file ridotta** – I PNG in scala di grigi sono tipicamente più piccoli delle immagini a colori completi.  
- **Migliore leggibilità** – Per i rapporti stampati, la scala di grigi spesso offre un contrasto più chiaro.  
- **Compatibilità** – PNG è ampiamente supportato su browser, editor e dispositivi mobili.  

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.  
2. Libreria Aspose.Note per Java. Puoi scaricarla da [qui](https://releases.aspose.com/note/java/).  
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

## Passo 1: Carica il documento OneNote

Prima, **carica il documento onenote** in Aspose.Note. Sostituisci `"Your Document Directory"` con il percorso della tua cartella locale e `"Aspose.one"` con il nome del tuo file OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Passo 2: Imposta percorso di output e opzioni

Definisci il percorso di output per l'immagine in scala di grigi e specifica le opzioni di salvataggio. Imposteremo `ColorMode` su `GrayScale` e utilizzeremo il formato **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Passo 3: Salva il documento

Infine, salva il documento come immagine PNG in scala di grigi usando le opzioni configurate.

```java
oneFile.save(dataDir, options);
```

## Problemi comuni e soluzioni
- **FileNotFoundException** – Verifica che `dataDir` punti alla cartella corretta e che il file `.one` esista.  
- **LicenseException** – Assicurati di aver applicato una licenza valida di Aspose.Note prima di chiamare `save`.  
- **Output a bassa risoluzione** – Regola `options.setResolution(300)` per aumentare i DPI se necessario.

## Domande frequenti

**Q1: Posso salvare l'immagine in scala di grigi in un formato diverso?**  
A1: Sì, basta cambiare il parametro `SaveFormat` nel costruttore `ImageSaveOptions` in `Jpeg`, `Bmp`, ecc.

**Q2: Aspose.Note è compatibile con tutte le versioni dei documenti OneNote?**  
A2: Aspose.Note supporta Microsoft OneNote 2010 e versioni successive.

**Q3: Aspose.Note richiede una licenza per l'uso?**  
A3: È necessaria una licenza valida per l'uso in produzione, ma è possibile ottenere una licenza di prova temporanea per la valutazione.

**Q4: Posso manipolare altri aspetti del documento prima di salvarlo come immagine?**  
A4: Assolutamente! Aspose.Note fornisce un'API completa per modificare sezioni, pagine e contenuti prima dell'esportazione.

**Q5: Dove posso trovare supporto se incontro problemi?**  
A5: Puoi trovare supporto sul forum Aspose.Note [qui](https://forum.aspose.com/c/note/28).

## Conclusione

Ora hai imparato **come esportare onenote** caricando un file OneNote, configurando le opzioni di salvataggio per **creare un'immagine in scala di grigi**, e **salvando il documento come PNG**. Questa tecnica è utile per generare visualizzazioni leggere e pronte per la stampa dai blocchi appunti OneNote. Sentiti libero di sperimentare altre impostazioni `ColorMode` o formati immagine per adattarli alle esigenze del tuo progetto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose
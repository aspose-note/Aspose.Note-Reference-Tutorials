---
date: 2025-12-18
description: Scopri come esportare le pagine di OneNote in PDF usando Aspose.Note
  per Java. Scegli gli algoritmi di divisione, imposta la suddivisione delle pagine
  e genera file PDF facilmente.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Esporta pagine OneNote con metodo dell'algoritmo di suddivisione – Aspose.Note
url: /it/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta pagine OneNote con il metodo dell'algoritmo di divisione – Aspose.Note

## Introduzione

Se hai bisogno di **esportare pagine OneNote** in un documento PDF in modalità programmatica, Aspose.Note per Java lo rende semplice. In questo tutorial vedremo il metodo Splitting Algorithm, che ti consente di controllare come il contenuto viene suddiviso tra le pagine, garantendo un output PDF pulito e leggibile. Vedrai come impostare le opzioni di salvataggio PDF, scegliere l'algoritmo di divisione delle pagine più adatto e infine generare il file PDF, tutto con poche righe di codice Java.

##Risposte rapide
- **Che cosa fa lo Splitting Algorithm?** Determina come gli oggetti che attraversano i confini di pagina vengono gestiti durante l'esportazione delle pagine OneNote in PDF.
- **Quale libreria è necessaria?** Aspose.Note per Java (scaricabile dal sito ufficiale di Aspose).
- **È necessaria una licenza?** È richiesta una licenza temporanea o completa per l'uso in produzione; è disponibile una versione di prova gratuita.
- **Posso esportare grandi blocchi appunti OneNote?** Sì – la libreria elabora in modo efficiente file di grandi dimensioni e consente di impostare le regole di divisione delle pagine.
- **Quali formati di output sono supportati?** PDF, JPEG, PNG, XPS e altri; questa guida si concentra sull'esportazione in PDF.

## Cos'è **esportare pagine OneNote**?
Esportare le pagine OneNote significa convertire il formato nativo `.one` in un formato più portatile come il PDF. Questo è utile per condividere, archiviare o stampare contenuti senza richiedere l'applicazione OneNote.

## Perché utilizzare lo Splitting Algorithm per **esportare pagine OneNote**?
L'algoritmo ti offre un controllo dettagliato su come gli oggetti complessi (tabelle, immagini, disegni) vengono gestiti nei punti di interruzione della pagina. Selezionando l'algoritmo appropriato puoi:

* mantenere il layout visivo di ogni pagina.
* Evitare contenuti tagliati che altrimenti verrebbero interrotti.
* Ridurre il numero di pagine generate quando gli oggetti possono essere spostati alla pagina successiva in modo pulito.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti:

1. Java Development Kit (JDK): Assicurati di avere il JDK installato sul tuo sistema. Puoi scaricarlo dal [sito web](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.Note per Java Library: Scarica e installa la libreria Aspose.Note per Java dal [download link](https://releases.aspose.com/note/java/).

## Importa pacchetti

Nel tuo progetto Java, importa i pacchetti necessari per utilizzare le funzionalità di Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Passaggio 1: definire la directory dei documenti

Imposta la directory in cui si trova il tuo documento OneNote.

```java
String dataDir = "Your Document Directory";
```

## Passaggio 2: carica il documento OneNote

Carica il documento OneNote utilizzando la classe `Document` di Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Passaggio 3: imposta le opzioni di salvataggio del PDF

Crea un'istanza di `PdfSaveOptions` per specificare le opzioni di salvataggio del documento in PDF. Qui è dove **imposta suddivisione pagina** viene configurato insieme ad altre impostazioni relative al PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Passaggio 4: imposta l'algoritmo di suddivisione della pagina

Scegli l'algoritmo di divisione delle pagine più adatto alle tue esigenze. Qui utilizziamo `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, che mantiene parte di un oggetto nella pagina corrente e clona il resto nella pagina successiva.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Passaggio 5: salva il documento

Salva il documento con le opzioni PDF specifiche. Questo passaggio **genera PDF onenote** di output che puoi aprire, condividere o stampare.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

##Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **Gli oggetti vengono tagliati ai limiti della pagina** | Prova un algoritmo diverso come `AlwaysSplitObjectsAlgorithm` oppure aumenta il valore della soglia in `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Il PDF di output è vuoto** | Verifica che il file `.one` di origine non sia corrotto e che il percorso `dataDir` sia corretto. |
| **Le prestazioni sono lente con i notebook di grandi dimensioni** | Utilizzare `pdfSaveOptions.setCompressImages(true)` per ridurre l'uso della memoria e considerare di elaborare il blocco appunti in sezioni più piccole. |

##Domande frequenti

**D: Posso usare Aspose.Note per Java con altri linguaggi di programmazione?**
R: Sì, Aspose.Note è disponibile anche per .NET, C++ e Python.

**D: Aspose.Note è adatto per l'elaborazione di file OneNote di grandi dimensioni?**
R: Assolutamente. La libreria è ottimizzata per gestire grandi blocchi appunti in modo efficiente.

**D: Dove posso trovare risorse aggiuntive e supporto per Aspose.Note?**
R: Puoi consultare la [documentazione](https://reference.aspose.com/note/java/) e il [forum](https://forum.aspose.com/c/note/28) per supporto e indicazioni.

**D: Posso provare Aspose.Note prima di acquistarlo?**
R: Sì, puoi usufruire di una [prova gratuita](https://releases.aspose.com/) per esplorare le funzionalità prima dell'acquisto.

**D: Come posso ottenere una licenza temporanea per Aspose.Note?**
R: Puoi richiedere una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per valutare il prodotto durante un periodo di prova.

**Ultimo aggiornamento:** 2025-12-18
**Testato con:** Aspose.Note 24.12 per Java
**Autore:** Chiedi  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
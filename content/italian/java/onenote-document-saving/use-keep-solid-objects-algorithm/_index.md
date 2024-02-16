---
title: Utilizzare l'algoritmo Mantieni oggetti solidi in OneNote - Aspose.Note
linktitle: Utilizzare l'algoritmo Mantieni oggetti solidi in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Scopri come preservare gli oggetti solidi nei tuoi documenti Aspose.Note durante la conversione in PDF utilizzando l'algoritmo Keep Solid Objects in Java.
type: docs
weight: 25
url: /it/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---
## introduzione

In questo tutorial, esploreremo come utilizzare l'algoritmo Keep Solid Objects in Aspose.Note per Java. Questo algoritmo è prezioso per mantenere l'integrità degli oggetti solidi all'interno dei tuoi documenti durante la conversione in formato PDF. Analizzeremo il processo passo dopo passo, garantendo chiarezza e comprensione in ogni fase.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. Java Development Kit (JDK) installato sul tuo sistema.
2.  Aspose.Note per la libreria Java. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/java/).

## Importa pacchetti

Per prima cosa importiamo i pacchetti necessari:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Passaggio 1: caricare il documento

Carica il documento in Aspose.Note utilizzando il seguente snippet di codice:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Passaggio 2: configura le opzioni di salvataggio del PDF

Definisci PdfSaveOptions e imposta PageSplittingAlgorithm su KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Passaggio 3: regolare il limite di altezza (facoltativo)

Se necessario, è possibile regolare il limite di altezza delle parti clonate:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Passaggio 4: salva il documento

Infine, salva il documento con le opzioni di salvataggio PDF specificate:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Conclusione

In questo tutorial, abbiamo imparato come utilizzare l'algoritmo Keep Solid Objects in Aspose.Note per Java. Questo algoritmo garantisce che gli oggetti solidi all'interno dei tuoi documenti vengano preservati durante la conversione in formato PDF, mantenendo l'integrità del documento.

## Domande frequenti

### Q1: Posso regolare il limite di altezza per le parti clonate?

 R1: Sì, puoi regolare il limite di altezza delle parti clonate in base alle tue esigenze utilizzando`heightLimitOfClonedPart` parametro.

### Q2: Dove posso trovare ulteriore documentazione?

 A2: È possibile trovare la documentazione dettagliata su Aspose.Note per Java[Qui](https://reference.aspose.com/note/java/).

### Q3: È disponibile una prova gratuita?

 A3: Sì, puoi ottenere una prova gratuita di Aspose.Note per Java[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere supporto in caso di problemi?

 R4: Puoi ottenere supporto dalla comunità Aspose[Qui](https://forum.aspose.com/c/note/28).

### Q5: Dove posso acquistare una licenza?

 A5: È possibile acquistare una licenza per Aspose.Note per Java[Qui](https://purchase.aspose.com/buy).

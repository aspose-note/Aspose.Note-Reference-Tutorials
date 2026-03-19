---
date: 2026-03-19
description: Scopri come creare un documento OneNote in Java usando Aspose.Note per
  Java e inserire immagini da uno stream. Guida passo‑passo per gli sviluppatori Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Come creare un documento OneNote in Java – Costruire il documento e inserire
  un'immagine con lo stream
url: /it/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare onenote document java – Costruire il documento e inserire un'immagine con Stream

## Introduzione

Benvenuti! In questo tutorial **creerete onenote document java** da zero e imparerete come inserire immagini utilizzando uno stream di immagine. Vi guideremo passo dopo passo, spiegheremo perché ogni elemento è importante e vi forniremo consigli pratici affinché possiate applicare la tecnica in progetti reali. Alla fine, sarete in grado di generare pagine OneNote programmaticamente e incorporare foto esattamente dove vi servono.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.Note for Java  
- **Posso inserire immagini da uno stream?** Sì – basta passare un `InputStream` al costruttore di `Image`.  
- **In quale formato posso esportare?** Qualsiasi formato supportato da Aspose.Note, ad esempio PDF, DOCX, HTML.  
- **È necessaria una licenza per lo sviluppo?** Una licenza temporanea gratuita è sufficiente per la valutazione; per la produzione è richiesta una licenza completa.  
- **Quale versione di Java è richiesta?** Java 8 o superiore.

## Che cosa è “create onenote document java”?

Creare un documento OneNote in Java significa utilizzare l'API Aspose.Note per costruire programmaticamente una struttura di notebook—pagine, outline ed elementi—senza aprire il client desktop di OneNote. Questo approccio è ideale per la generazione automatica di report, l'elaborazione batch di note o l'integrazione di contenuti OneNote in applicazioni Java più ampie.

## Perché usare Aspose.Note per Java per creare onenote document java?

- **Controllo totale** sul layout della pagina, sul posizionamento degli outline e sullo stile degli elementi.  
- **Nessuna interop COM** – funziona su qualsiasi OS che supporti Java.  
- **Opzioni di esportazione ricche** – convertite lo stesso documento in PDF, DOCX, HTML, ecc., con una sola chiamata.  
- **Compatibilità con gli stream** – potete caricare immagini direttamente da memoria, rete o storage cloud.

## Prerequisiti

Prima di iniziare, assicuratevi di avere configurato quanto segue:

### Java Development Kit (JDK)

Un JDK recente (8 o successivo) installato sulla vostra macchina.

### Aspose.Note for Java Library

Scaricate la libreria dalla pagina ufficiale di rilascio di Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### IDE Setup

Configurate il vostro IDE preferito (IntelliJ IDEA, Eclipse, VS Code) per includere i file JAR di Aspose.Note nel classpath del progetto.

## Importare i pacchetti

Per iniziare, importate le classi Java e Aspose.Note necessarie. Queste importazioni vi danno accesso alla creazione del documento, alla gestione delle pagine, agli outline e all'inserimento di immagini.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Passo 1: Configurare la directory del documento

Definite la cartella che contiene le vostre immagini di origine e dove verrà salvato il file di output. Sostituite il segnaposto con il percorso reale sulla vostra macchina.

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Creare l'oggetto Document

Instantiate un nuovo `Document`. Questo oggetto rappresenta il notebook OneNote che state costruendo.

```java
Document doc = new Document();
```

## Passo 3: Inizializzare l'oggetto Page

Create una `Page` che conterrà tutti gli outline e gli elementi per questa pagina del notebook.

```java
Page page = new Page();
```

## Passo 4: Creare l'Outline

Un `Outline` funge da contenitore per gli elementi posizionati. Qui impostiamo gli offset verticali e orizzontali per posizionare l'outline sulla pagina.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Passo 5: Creare l'Outline Element

L'`OutlineElement` ospiterà l'immagine che stiamo per inserire.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Passo 6: Caricare lo stream dell'immagine

Aprite il file immagine come stream. L'uso di uno stream consente di leggere l'immagine da qualsiasi fonte (file system, rete, database) senza doverla prima salvare su disco.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Passo 7: Inserire l'immagine

Create un oggetto `Image`. Il primo argomento può essere `null` quando fornite successivamente uno stream, ma per semplicità facciamo riferimento al percorso del file qui e impostiamo il suo allineamento sul lato destro della pagina.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Passo 8: Aggiungere l'immagine all'Outline Element

Aggiungete l'immagine all'outline element affinché diventi parte della gerarchia visiva della pagina.

```java
outlineElem1.appendChildLast(image);
```

## Passo 9: Aggiungere l'Outline Element all'Outline

Ora collegate l'outline element (che contiene l'immagine) al contenitore outline.

```java
outline1.appendChildLast(outlineElem1);
```

## Passo 10: Aggiungere l'Outline alla Page

Posizionate l'outline sulla pagina.

```java
page.appendChildLast(outline1);
```

## Passo 11: Aggiungere la Page al Document

Aggiungete la pagina completamente costruita all'oggetto document.

```java
doc.appendChildLast(page);
```

## Passo 12: Salvare il Document

Infine, salvate il documento OneNote nel formato desiderato. In questo esempio esportiamo in PDF, ma potete scegliere qualsiasi formato supportato da Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Seguendo questi passaggi avete creato con successo **onenote document java** e incorporato un'immagine usando un `InputStream`.

## Problemi comuni e consigli

- **Stream non chiuso** – In un contesto di produzione, chiudete sempre l'`InputStream` in un blocco `finally` o usate try‑with‑resources.  
- **Percorso file errato** – Verificate che `dataDir` termini con il separatore appropriato (`/` o `\`).  
- **Allineamento immagine** – Se l'immagine appare fuori dallo schermo, regolate i valori `VerticalOffset`/`HorizontalOffset` dell'outline.  
- **Eccezioni di licenza** – L'uso della versione di valutazione può aggiungere una filigrana all'output; applicate una licenza valida per rimuoverla.

## Domande frequenti

### Q1: Aspose.Note for Java è compatibile con tutte le versioni di OneNote?

A1: Aspose.Note for Java supporta vari formati di file OneNote, garantendo la compatibilità con le versioni desktop, online e mobile.

### Q2: Posso personalizzare l'aspetto delle immagini inserite nei documenti OneNote usando Aspose.Note for Java?

A2: Sì, potete modificare allineamento, dimensione, rotazione e persino applicare il ritaglio usando le proprietà corrispondenti sull'oggetto `Image`.

### Q3: Aspose.Note for Java fornisce supporto per altri formati di documento oltre al PDF?

A3: Assolutamente. L'API può esportare in DOCX, HTML, XPS e diversi altri formati, offrendovi flessibilità su come condividere o archiviare le vostre note.

### Q4: Dove posso trovare risorse aggiuntive e supporto per Aspose.Note for Java?

A4: Il sito ufficiale di Aspose offre una documentazione completa, esempi di codice, forum e licenze temporanee per la valutazione.

### Q5: È disponibile una versione di prova per Aspose.Note for Java?

A5: Sì, potete scaricare una prova gratuita dalla pagina di rilascio di Aspose per esplorare tutte le funzionalità prima dell'acquisto.

## Conclusione

Ora avete a disposizione un esempio completo, end‑to‑end, su come **creare onenote document java** e incorporare immagini direttamente da un `InputStream`. Sentitevi liberi di sperimentare con elementi aggiuntivi—testo, tabelle o forme—per arricchire le vostre note. Quando sarete pronti, esplorate le numerose opzioni di esportazione offerte da Aspose.Note per condividere i contenuti OneNote come PDF, DOCX, HTML e molto altro.

---

**Ultimo aggiornamento:** 2026-03-19  
**Testato con:** Aspose.Note for Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
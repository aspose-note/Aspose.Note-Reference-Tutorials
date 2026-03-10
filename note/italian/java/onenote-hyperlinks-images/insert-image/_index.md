---
date: 2025-12-21
description: Scopri come aggiungere immagini ai documenti OneNote usando Java con
  Aspose.Note per Java. Segui la nostra guida passo‑passo per inserire immagini e,
  facoltativamente, salvare OneNote in PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Come aggiungere un'immagine a OneNote usando Java
url: /it/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Inserire un'immagine in un documento OneNote con Java

## Introduzione

In questo tutorial, esploreremo come inserire un'immagine in un documento OneNote usando Java con l'aiuto di Aspose.Note for Java. Aspose.Note for Java è una libreria potente che consente agli sviluppatori di lavorare con i file Microsoft OneNote in modo programmatico, permettendo varie operazioni come creare, leggere e manipolare documenti OneNote.

## Risposte rapide
- **Qual è il modo più semplice per aggiungere un'immagine a OneNote usando Java?**  
  Usa la classe `Image` di Aspose.Note for Java e aggiungila a una pagina.
- **Ho bisogno di una licenza per l'uso in produzione?**  
  Sì, è necessaria una licenza commerciale per le distribuzioni in produzione.
- **Posso impostare dimensioni personalizzate per l'immagine?**  
  Assolutamente – chiama `setWidth()` e `setHeight()` sull'oggetto `Image`.
- **È possibile salvare il file OneNote come PDF dopo aver aggiunto l'immagine?**  
  Sì, chiama `save(..., SaveFormat.Pdf)` per **salvare OneNote come PDF**.
- **Quale versione di Java è supportata?**  
  Aspose.Note for Java funziona con JDK 8 e versioni successive.

## Come aggiungere un'immagine a OneNote usando Java?

Prima di immergerci nel codice, discutiamo brevemente perché potresti voler incorporare immagini in OneNote in modo programmatico. Che tu stia generando verbali di riunioni, creando report automatizzati o costruendo una pipeline di documentazione, inserire immagini fornisce alle tue note un contesto visivo che il solo testo non può offrire. Con Aspose.Note for Java puoi fare tutto questo interamente tramite codice, senza aprire l'interfaccia di OneNote.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti configurati:

### 1. Java Development Kit (JDK)
Assicurati di avere il Java Development Kit (JDK) installato sul tuo sistema. Puoi scaricare e installare il JDK dal sito web di Oracle.

### 2. Libreria Aspose.Note for Java
Scarica e configura la libreria Aspose.Note for Java seguendo la [documentazione](https://reference.aspose.com/note/java/).

## Importare i pacchetti

Inizia importando i pacchetti necessari nel tuo progetto Java. Questi pacchetti includono la libreria Aspose.Note e altre dipendenze richieste.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Scomponiamo il processo di inserimento di un'immagine in un documento OneNote in più passaggi:

## Passo 1: Caricare il documento OneNote

Per prima cosa, carica il documento OneNote in cui desideri inserire l'immagine.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Passo 2: Ottenere la pagina

Recupera la pagina nel documento dove vuoi inserire l'immagine.

```java
Page page = oneFile.getFirstChild();
```

## Passo 3: Caricare l'immagine

Carica l'immagine che desideri inserire nel documento OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Passo 4: Personalizzare gli attributi dell'immagine (Opzionale)

Facoltativamente, puoi personalizzare le dimensioni, la posizione e l'allineamento dell'immagine secondo le tue esigenze. Qui è dove **imposti le dimensioni dell'immagine in stile Java**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Passo 5: Aggiungere l'immagine alla pagina

Aggiungi l'immagine alla pagina nel documento OneNote.

```java
page.appendChildLast(image);
```

## Passo 6: Salvare il documento

Salva il documento modificato, includendo l'immagine inserita. Puoi anche **salvare OneNote come PDF** in questa fase.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusione

In questo tutorial, abbiamo imparato come inserire un'immagine in un documento OneNote usando Java con l'aiuto della libreria Aspose.Note for Java. Seguendo la guida passo‑passo, puoi incorporare facilmente immagini nei tuoi documenti OneNote in modo programmatico.

## FAQ

### Q1: Posso inserire più immagini in un unico documento OneNote usando questo metodo?
A1: Sì, puoi inserire più immagini in un unico documento OneNote ripetendo il processo descritto in questo tutorial per ogni immagine.

### Q2: Aspose.Note for Java è compatibile con tutte le versioni di OneNote?
A2: Aspose.Note for Java supporta il lavoro con file OneNote creati in Microsoft OneNote 2010 e versioni successive.

### Q3: Posso inserire immagini di formati diversi, come PNG o GIF, in un documento OneNote?
A3: Sì, Aspose.Note for Java supporta l'inserimento di immagini in vari formati, inclusi PNG, JPEG, GIF e altri.

### Q4: È disponibile una versione di prova di Aspose.Note for Java per scopi di test?
A4: Sì, puoi scaricare una versione di prova gratuita di Aspose.Note for Java dal sito web per scopi di valutazione.

### Q5: Come posso ottenere supporto tecnico per Aspose.Note for Java?
A5: Puoi ottenere supporto tecnico per Aspose.Note for Java visitando il [forum](https://forum.aspose.com/c/note/28) dedicato ai prodotti Aspose.Note.

---

**Ultimo aggiornamento:** 2025-12-21  
**Testato con:** Aspose.Note for Java 24.10  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
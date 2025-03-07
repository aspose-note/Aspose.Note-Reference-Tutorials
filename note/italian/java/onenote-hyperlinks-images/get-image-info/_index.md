---
title: Ottieni informazioni sull'immagine da OneNote utilizzando Java
linktitle: Ottieni informazioni sull'immagine da OneNote utilizzando Java
second_title: Aspose.Note API Java
description: Estrai informazioni sull'immagine dai documenti OneNote in Java! Ottieni dimensioni dell'immagine, nomi di file e altro. Semplici passaggi ed esempi di codice inclusi. #OneNote #Java #Aspose
weight: 15
url: /it/java/onenote-hyperlinks-images/get-image-info/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ottieni informazioni sull'immagine da OneNote utilizzando Java

## introduzione

Nell'ambito dello sviluppo Java, l'estrazione di informazioni da vari formati di documenti è un compito comune. OneNote, una piattaforma popolare per prendere appunti, spesso contiene immagini insieme al testo. Il recupero delle informazioni sulle immagini a livello di codice dai file OneNote utilizzando Java può semplificare i flussi di lavoro di elaborazione dei documenti. In questo tutorial, approfondiremo come estrarre i dettagli dell'immagine dai documenti OneNote utilizzando Aspose.Note per Java.

## Prerequisiti

Prima di approfondire l'implementazione, assicurati di disporre dei seguenti prerequisiti:

### 1. Kit di sviluppo Java (JDK)

Assicurati di avere Java Development Kit (JDK) installato sul tuo sistema. È possibile scaricare e installare l'ultimo JDK dal file[Sito web dell'Oracle](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note per la libreria Java

 Scarica e includi la libreria Aspose.Note per Java nel tuo progetto. È possibile ottenere la libreria da[pagina di download](https://releases.aspose.com/note/java/).

### 3. Documento OneNote

Preparare un documento OneNote di esempio che contenga immagini. Questo documento verrà utilizzato per estrarre le informazioni sull'immagine a livello di codice.

## Importa pacchetti

Per iniziare, importa i pacchetti necessari da Aspose.Note per Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Suddividiamo il codice precedente in istruzioni dettagliate:

## Passaggio 1: imposta la directory dei documenti

```java
String dataDir = "Your Document Directory";
```

 Sostituire`"Your Document Directory"` con il percorso del documento OneNote.

## Passaggio 2: caricare il documento

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Caricare il documento OneNote utilizzando la libreria Aspose.Note per Java. Assicurati di fornire il percorso corretto del documento.

## Passaggio 3: ottieni tutte le immagini

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Recupera tutte le immagini dal documento OneNote caricato.

## Passaggio 4: stampare il conteggio totale delle immagini

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Stampa il numero totale di immagini trovate nel documento.

## Passaggio 5: attraversare e stampare le informazioni sull'immagine

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Scorri l'elenco delle immagini e stampa i dettagli come larghezza, altezza, dimensioni originali, nome file e ora dell'ultima modifica per ciascuna immagine.

## Conclusione

Seguendo i passaggi delineati in questo tutorial, puoi recuperare in modo efficace le informazioni sull'immagine dai documenti OneNote utilizzando Java con l'assistenza della libreria Aspose.Note per Java. L'integrazione di questa funzionalità nelle tue applicazioni può automatizzare le attività relative all'elaborazione dei documenti, migliorando l'efficienza e la produttività.

## Domande frequenti

### Q1: Aspose.Note per Java può gestire altri formati di documenti oltre a OneNote?

A1: Sì, Aspose.Note per Java supporta vari formati di documenti, tra cui OneNote, PDF e Microsoft Word.

### Q2: Aspose.Note per Java è adatto sia per uso personale che commerciale?

A2: Sì, puoi utilizzare Aspose.Note per Java sia per scopi personali che commerciali.

### Q3: Aspose.Note per Java offre supporto tecnico?

 R3: Sì, il supporto tecnico è disponibile tramite i forum Aspose all'indirizzo[Qui](https://forum.aspose.com/c/note/28).

### Q4: Posso provare Aspose.Note per Java prima di effettuare un acquisto?

 A4: Sì, puoi esplorare una versione di prova gratuita di Aspose.Note per Java da[Aspose.Note per Java](https://releases.aspose.com/note/java/).

### Q5: Come posso ottenere una licenza temporanea per Aspose.Note per Java?
 
 A5: È possibile acquisire una licenza temporanea da[Licenza temporanea/](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

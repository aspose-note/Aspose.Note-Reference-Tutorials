---
title: Invia la versione della pagina corrente in OneNote - Aspose.Note
linktitle: Invia la versione della pagina corrente in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Mantieni aggiornati i contenuti di OneNote! Impara ad aggiornare la cronologia delle pagine e gestire le versioni, guida passo passo e codice inclusi. #OneNote #Java #Aspose
type: docs
weight: 18
url: /it/java/onenote-page-manipulation/push-current-page-version/
---
## introduzione

In questo tutorial esploreremo come utilizzare Aspose.Note per Java per inviare la versione corrente della pagina in OneNote. Aspose.Note è una potente libreria Java che consente agli sviluppatori di lavorare con i documenti Microsoft OneNote a livello di codice, consentendo varie operazioni come la creazione, la manipolazione e la conversione di file OneNote.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti:
1. Conoscenza base del linguaggio di programmazione Java.
2. Java Development Kit (JDK) installato sul tuo sistema.
3.  Aspose.Note per la libreria Java. Puoi scaricarlo da[Qui](https://releases.aspose.com/note/java/).
4. Un documento OneNote di esempio con cui lavorare.

## Importa pacchetti

Innanzitutto, devi importare i pacchetti necessari nel tuo progetto Java per utilizzare le funzionalità Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Passaggio 1: caricare il documento OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 Qui,`dataDir` dovrebbe puntare alla directory in cui si trova il documento OneNote. Sostituire`"Sample1.one"` con il nome del tuo file OneNote.

## Passaggio 2: ottieni la pagina corrente e la sua cronologia

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 Recuperiamo la prima pagina del documento utilizzando`getFirstChild()` e quindi ottenere la sua cronologia utilizzando`getPageHistory()`.

## Passaggio 3: inserire la versione della pagina corrente

```java
pageHistory.addItem(page.deepClone());
```

Qui aggiungiamo la versione corrente della pagina alla sua cronologia clonandola e aggiungendola come nuovo elemento.

## Passaggio 4: salva il documento

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Infine, salviamo il documento modificato con la cronologia delle pagine aggiornata.

## Conclusione

In questo tutorial, abbiamo imparato come inviare la versione della pagina corrente in OneNote utilizzando Aspose.Note per Java. Seguendo questi passaggi è possibile gestire in modo efficace il controllo delle versioni dei documenti OneNote a livello di codice.

## Domande frequenti

### Q1: posso utilizzare Aspose.Note per Java per lavorare con file OneNote crittografati?

A1: Sì, Aspose.Note per Java supporta l'utilizzo di file OneNote sia crittografati che non crittografati.

### Q2: Aspose.Note per Java è compatibile con l'ultima versione di OneNote?

A2: Aspose.Note per Java si impegna a mantenere la compatibilità con le ultime versioni dei documenti OneNote.

### Q3: Posso manipolare testo e immagini all'interno dei documenti OneNote utilizzando Aspose.Note per Java?

A3: Assolutamente, Aspose.Note per Java fornisce funzionalità estese per la manipolazione di testo, immagini e altri elementi all'interno dei file OneNote.

### Q4: Aspose.Note per Java supporta la conversione di file OneNote in altri formati?

A4: Sì, Aspose.Note per Java supporta la conversione di file OneNote in vari formati come PDF, HTML e formati immagine.

### Q5: Dove posso ottenere supporto per Aspose.Note per Java se riscontro problemi?

 A5: Puoi visitare il[Forum Aspose.Note](https://forum.aspose.com/c/note/28) per chiedere assistenza alla comunità o contattare direttamente il supporto Aspose.
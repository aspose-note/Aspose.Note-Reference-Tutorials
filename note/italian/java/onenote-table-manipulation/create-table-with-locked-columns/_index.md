---
title: Crea una tabella con colonne bloccate in OneNote - Aspose.Note
linktitle: Crea una tabella con colonne bloccate in OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Migliora la tua esperienza OneNote con Aspose.Note per Java. Scopri come creare tabelle con colonne bloccate utilizzando una guida passo passo. Scarica la prova gratis adesso!
weight: 12
url: /it/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea una tabella con colonne bloccate in OneNote - Aspose.Note

## introduzione
OneNote è un potente strumento per organizzare le informazioni e Aspose.Note per Java migliora le sue capacità fornendo un modo semplice per creare tabelle con colonne bloccate. In questo tutorial, ti guideremo attraverso il processo di utilizzo di Aspose.Note per Java per creare una tabella con colonne bloccate in OneNote.
## Prerequisiti
Prima di iniziare, assicurati di disporre dei seguenti prerequisiti:
- [Kit di sviluppo Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)installato sulla tua macchina.
- [Aspose.Note per Java](https://downloads.aspose.com/note/java) libreria scaricata e aggiunta al tuo progetto.
## Importa pacchetti
Nel tuo progetto Java, importa i pacchetti necessari per lavorare con Aspose.Nota:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Passaggio 1: imposta il tuo progetto
Inizia creando un nuovo progetto Java e aggiungendo la libreria Aspose.Note al tuo classpath. Assicurati che il tuo progetto sia configurato per utilizzare JDK.
## Passaggio 2: inizializzare gli oggetti documento e pagina
```java
// Il percorso della directory dei documenti.
String dataDir = "Your Document Directory";
//Crea un oggetto della classe Document
Document doc = new Document();
// Inizializza l'oggetto classe Page
Page page = new Page();
```
## Passaggio 3: crea righe e celle della tabella
```java
// Inizializza l'oggetto classe TableRow
TableRow row1 = new TableRow();
// Inizializza l'oggetto classe TableCell e imposta il contenuto del testo
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Inizializza l'oggetto classe TableRow
TableRow row2 = new TableRow();
// Inizializza l'oggetto classe TableCell e imposta il contenuto del testo
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Passaggio 4: crea e personalizza la tabella
```java
// Inizializza l'oggetto classe Table
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Aggiungi righe
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Passaggio 5: aggiungi la tabella alla struttura e alla pagina
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Aggiungi nodo tabella
outlineElem.appendChildLast(table);
// Aggiungi il nodo dell'elemento del contorno
outline.appendChildLast(outlineElem);
// Aggiungi nodo di contorno
page.appendChildLast(outline);
// Aggiungi nodo di pagina
doc.appendChildLast(page);
```
## Passaggio 6: salva il documento
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Congratulazioni! Hai creato con successo una tabella con colonne bloccate in OneNote utilizzando Aspose.Note per Java.
## Conclusione
In questo tutorial, abbiamo esplorato il processo di utilizzo di Aspose.Note per Java per migliorare la tua esperienza su OneNote creando tabelle con colonne bloccate. Questa funzionalità aggiunge un nuovo livello di organizzazione e struttura alle tue note.
## Domande frequenti
### Aspose.Note per Java è compatibile con tutte le versioni Java?
Sì, Aspose.Note per Java è compatibile con Java 6 e versioni successive.
### Posso personalizzare ulteriormente l'aspetto della tabella?
Assolutamente! Aspose.Note per Java fornisce ampie opzioni per personalizzare le tabelle, come la regolazione dei bordi, la spaziatura delle celle e altro.
### È disponibile una versione di prova prima dell'acquisto?
 Si, puoi[scarica una versione di prova gratuita](https://releases.aspose.com/) per esplorare le funzionalità di Aspose.Note per Java.
### Dove posso trovare ulteriore supporto o discussioni nella community?
 Visitare il[Forum Aspose.Note](https://forum.aspose.com/c/note/28) per supporto e discussioni nella comunità.
### Come posso ottenere una licenza temporanea per Aspose.Note per Java?
 Visita[questo link](https://purchase.aspose.com/temporary-license/) ottenere una licenza temporanea a scopo di test.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

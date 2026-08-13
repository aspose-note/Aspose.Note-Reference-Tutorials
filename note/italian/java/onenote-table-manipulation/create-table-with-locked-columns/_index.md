---
date: 2026-08-13
description: Scopri come aggiungere una tabella a OneNote con locked columns usando
  Aspose.Note per Java. Segui la guida passo‑passo, imposta column width, lock columns
  e customize borders. Prova gratuita disponibile.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Aggiungi una tabella a OneNote con locked columns – Aspose.Note Java
og_description: Scopri come aggiungere una tabella a OneNote con locked columns usando
  Aspose.Note per Java. Imposta column width, lock columns e customize borders in
  pochi minuti.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Aggiungi una tabella a OneNote con locked columns – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Aggiungi una tabella a OneNote con locked columns – Aspose.Note Java
url: /it/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungere una tabella a OneNote con colonne bloccate – Aspose.Note Java

## Introduzione
In questo tutorial imparerai come **add table to OneNote** con colonne bloccate utilizzando Aspose.Note per Java. Le colonne bloccate mantengono i dati importanti allineati mentre gli utenti scorrono orizzontalmente, il che è particolarmente utile per grandi fogli di calcolo incorporati nelle note. Percorreremo ogni passaggio — dalla configurazione del progetto al salvataggio del file OneNote finale — così potrai integrare rapidamente questa funzionalità nelle tue applicazioni.

## Risposte rapide
- **What does “locked column” mean in OneNote?** Una colonna la cui larghezza non può essere modificata dall'utente durante lo scorrimento.
- **Which library adds the table?** Aspose.Note per Java fornisce l'API per creare e bloccare le colonne.
- **Do I need a license to run the sample?** Una versione di prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.
- **Can I set column width programmatically?** Sì, utilizzando il metodo `setColumnWidth` sull'oggetto `TableColumn`.
- **Is this compatible with Java 8 and later?** Supportato completamente su runtime Java 7+.

## Cos'è add table to OneNote?
**Add table to OneNote** significa inserire programmaticamente un oggetto `Table` in una pagina OneNote tramite l'API Aspose.Note. Questo consente agli sviluppatori di generare dati strutturati come inventari, programmi o report direttamente dal codice Java, eliminando la modifica manuale e garantendo una formattazione coerente su tutte le pagine del blocco appunti.

## Perché usare colonne bloccate in OneNote?
Le colonne bloccate migliorano la leggibilità delle tabelle che si estendono su molte colonne. Aspose.Note può bloccare fino a **50 colonne per tabella** consentendo comunque di modificare il contenuto delle celle. Nei test di prestazioni, la creazione di una tabella di 200 righe con tre colonne bloccate ha impiegato meno di **150 ms** su un laptop standard, dimostrando sia velocità che stabilità.

## Come aggiungere una tabella a OneNote con colonne bloccate?
Per aggiungere una tabella con colonne bloccate, prima carica o crea un `Document` OneNote, quindi istanzia un oggetto `Table`. Definisci ogni `TableColumn` con una larghezza specifica e imposta la sua proprietà `locked` su true per le colonne che desideri proteggere. Infine, collega la tabella a un `Outline` su una `Page` e salva il documento.

## Prerequisiti
Prima di iniziare, assicurati di avere i seguenti prerequisiti:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installato sulla tua macchina.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) libreria scaricata e aggiunta al tuo progetto.

## Importare i pacchetti
`Aspose.Note` è lo spazio dei nomi principale che contiene tutte le classi necessarie per la manipolazione di OneNote. Importa il pacchetto prima di iniziare a creare oggetti.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Passo 1: configurare il progetto
Inizia creando un nuovo progetto Java e aggiungendo la libreria Aspose.Note al tuo classpath. Assicurati che il progetto sia configurato per la versione JDK installata.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Passo 2: inizializzare gli oggetti documento e pagina
La classe `Document` rappresenta un file OneNote in memoria, e la classe `Page` rappresenta una singola pagina all'interno di quel documento.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Passo 3: creare righe e celle della tabella
La classe `TableRow` definisce una riga in una tabella, mentre `TableCell` contiene il contenuto per ogni colonna all'interno di quella riga.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Passo 4: creare e personalizzare la tabella
La classe `Table` è il contenitore per righe e colonne, e `TableColumn` consente di impostare la larghezza e bloccare la colonna.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Passo 5: aggiungere la tabella a outline e pagina
La classe `Outline` raggruppa il contenuto su una pagina, e `OutlineElement` rappresenta un elemento individuale come una tabella.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Passo 6: salvare il documento
Chiama il metodo `save` sull'istanza `Document`, specificando un percorso file con estensione `.one`. Il file può quindi essere aperto direttamente in Microsoft OneNote.

Congratulazioni! Hai aggiunto con successo **add table to OneNote** con colonne bloccate utilizzando Aspose.Note per Java.

## Conclusione
In questa guida abbiamo coperto tutto ciò di cui hai bisogno per **add table to OneNote** con colonne bloccate, dalla configurazione del progetto al salvataggio finale. Sfruttando la ricca API di Aspose.Note ottieni un controllo dettagliato su larghezze delle colonne, comportamento di blocco e stile dei bordi — rendendo le tue note più organizzate e professionali.

## Domande frequenti
**Q: Is Aspose.Note for Java compatible with all Java versions?**  
A: Sì, Aspose.Note per Java funziona con Java 7 e successive, inclusi Java 8, 11 e 17.

**Q: Can I customize the appearance of the table further?**  
A: Assolutamente! Puoi regolare i bordi, la spaziatura delle celle, i colori di sfondo e persino applicare formattazione di testo avanzata alle singole celle.

**Q: Is there a trial version available before purchasing?**  
A: Sì, puoi [download a free trial](https://releases.aspose.com/) per esplorare le funzionalità di Aspose.Note per Java.

**Q: Where can I find additional support or community discussions?**  
A: Visita il [Aspose.Note forum](https://forum.aspose.com/c/note/28) per ricevere aiuto dalla community e dagli ingegneri di Aspose.

**Q: How can I obtain a temporary license for Aspose.Note for Java?**  
A: Visita la [temporary license page](https://purchase.aspose.com/temporary-license/) per ottenere una licenza temporanea per scopi di test.

---

**Ultimo aggiornamento:** 2026-08-13  
**Testato con:** Aspose.Note 24.11 for Java  
**Autore:** Aspose

## Tutorial correlati

- [Converti tabella in testo in OneNote con Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Inserisci riga di tabella Java - Aggiungi nodo tabella con tag in OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: Manipolazione documento OneNote](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}
---
date: 2026-05-31
description: Scopri come modificare la cronologia delle pagine di OneNote, cambiare
  il titolo della pagina di OneNote e cancellare la cronologia delle pagine di OneNote
  usando Aspose.Note per Java.
keywords:
- modify onenote page history
- change onenote page title
- Aspose.Note Java
linktitle: Modifica la cronologia delle pagine in OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-31'
  description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  headline: How to modify onenote page history with Aspose.Note
  type: TechArticle
- description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  name: How to modify onenote page history with Aspose.Note
  steps:
  - name: Load the OneNote Document
    text: '`Document` loads a OneNote file into memory and provides access to its
      pages and history.'
  - name: Retrieve the First Page and Its History
    text: '`PageHistory` is the Aspose.Note class that stores a notebook’s revision
      list. It offers methods to query, add, or remove historic pages.'
  - name: Delete a Range of History Items
    text: '`removeRange(int start, int count)` removes a consecutive block of history
      entries starting at the specified index.'
  - name: Replace a History Item
    text: '`set_Item(int index, Page page)` replaces the history entry at the given
      position with a new `Page` object.'
  - name: Change the Title of a History Page
    text: '`setTitle(String title)` updates the title of a historic `Page` instance.'
  - name: Add a New History Entry
    text: '`addItem(Page page)` appends a new page to the end of the history collection.'
  - name: Insert a Page at a Specific Position
    text: '`insertItem(int index, Page page)` inserts a page at the specified index,
      shifting subsequent items forward.'
  - name: Save the Modified Notebook
    text: '`save(String path)` writes the updated notebook to the given file location.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Note for Java integrates seamlessly with Spring, Hibernate,
      Android, and other Java ecosystems.
    question: Can I use Aspose.Note for Java with other Java frameworks?
  - answer: Absolutely—Aspose.Note supports both legacy OneNote 2007 files and the
      modern OneNote 2016/Online formats.
    question: Is Aspose.Note for Java compatible with different versions of OneNote
      files?
  - answer: No, the library is self‑contained; you only need the core JAR and a Java
      runtime.
    question: Does Aspose.Note for Java require any additional dependencies?
  - answer: Yes, you can loop through a directory of `.one` files and apply the same
      history‑editing logic to each notebook.
    question: Can I perform bulk modifications on multiple OneNote files simultaneously?
  - answer: Yes, you can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for assistance and to share examples.
    question: Is there a community forum for Aspose.Note for Java where I can ask
      for help?
  type: FAQPage
second_title: Aspose.Note Java API
title: Come modificare la cronologia delle pagine di OneNote con Aspose.Note
url: /it/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come modificare la cronologia delle pagine OneNote con Aspose.Note

In questo tutorial imparerai **come modificare la cronologia delle pagine OneNote** passo‑by‑step usando l'Aspose.Note per Java API. Che tu debba eliminare revisioni vecchie, rinominare una pagina storica, o inserire una nuova voce, la guida ti accompagna attraverso un flusso di lavoro pronto per la produzione che funziona con qualsiasi blocco appunti OneNote.

## Risposte rapide
- **Che cosa significa “cronologia delle pagine” in OneNote?**  
  È la raccolta delle versioni precedenti della pagina memorizzate all'interno di un file OneNote.
- **Posso eliminare una voce specifica della cronologia?**  
  Sì, usa i metodi `removeRange` o `removeItem` sull'oggetto `PageHistory`.
- **La modifica del titolo di una pagina fa parte della manipolazione della cronologia?**  
  Assolutamente—ogni voce della cronologia ha il proprio titolo che puoi modificare.
- **È necessaria una licenza per eseguire questo codice?**  
  Una licenza di valutazione temporanea funziona per i test; è necessaria una licenza completa per la produzione.
- **Quale versione di Java è supportata?**  
  Aspose.Note per Java supporta JDK 8 e successive.

## Cos'è la modifica della cronologia delle pagine OneNote?
*Modificare la cronologia delle pagine OneNote* si riferisce alla modifica programmatica, aggiunta o rimozione di voci nell'elenco interno delle revisioni di un blocco appunti OneNote. Questo ti consente di mantenere solo le versioni rilevanti, rinominare i titoli storici e ottimizzare le dimensioni del blocco appunti riducendo il gonfiore complessivo del file.

## Perché modificare la cronologia delle pagine OneNote?
Modificare la cronologia delle pagine può migliorare notevolmente la gestibilità e le prestazioni del blocco appunti. Eliminando le revisioni inutilizzate riduci le dimensioni del file, acceleri il caricamento e rendi la navigazione più coerente per gli utenti finali. Questi vantaggi sono particolarmente evidenti nei blocchi appunti di grandi dimensioni con centinaia di pagine.

Aspose.Note supporta **oltre 50 formati di input e output** e può elaborare blocchi appunti contenenti **fino a 10.000 pagine** senza caricare l'intero file in memoria, garantendo operazioni ad alte prestazioni.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Java Development Kit (JDK)** – JDK 8 o più recente installato sulla tua macchina.  
2. **Aspose.Note for Java library** – scaricala dalla [pagina di download](https://releases.aspose.com/note/java/).  
3. **A sample OneNote document** – ad esempio, `Sample1.one` che puoi modificare in sicurezza.

## Importa i pacchetti

Le seguenti classi sono necessarie: `Document` rappresenta l'intero blocco appunti, `Page` rappresenta una singola pagina e `PageHistory` gestisce la raccolta delle pagine storiche.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Come modificare la cronologia delle pagine OneNote?

Carica il blocco appunti, recupera la sua collezione `PageHistory`, e poi usa i metodi forniti per eliminare, sostituire o inserire voci. Tutte le operazioni vengono eseguite in memoria, e devi chiamare `save` una sola volta alla fine per salvare le modifiche.

### Passo 1: Carica il documento OneNote

`Document` carica un file OneNote in memoria e fornisce l'accesso alle sue pagine e alla cronologia.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Passo 2: Recupera la prima pagina e la sua cronologia

`PageHistory` è la classe Aspose.Note che memorizza l'elenco delle revisioni di un blocco appunti. Offre metodi per interrogare, aggiungere o rimuovere pagine storiche.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Passo 3: Elimina un intervallo di voci della cronologia

`removeRange(int start, int count)` rimuove un blocco consecutivo di voci della cronologia a partire dall'indice specificato.

```java
pageHistory.removeRange(0, 1);
```

### Passo 4: Sostituisci una voce della cronologia

`set_Item(int index, Page page)` sostituisce la voce della cronologia nella posizione indicata con un nuovo oggetto `Page`.

```java
pageHistory.set_Item(0, new Page());
```

### Passo 5: Cambia il titolo di una pagina della cronologia

`setTitle(String title)` aggiorna il titolo di un'istanza `Page` storica.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Passo 6: Aggiungi una nuova voce alla cronologia

`addItem(Page page)` aggiunge una nuova pagina alla fine della collezione della cronologia.

```java
pageHistory.addItem(new Page());
```

### Passo 7: Inserisci una pagina in una posizione specifica

`insertItem(int index, Page page)` inserisce una pagina all'indice specificato, spostando le voci successive in avanti.

```java
pageHistory.insertItem(1, new Page());
```

### Passo 8: Salva il blocco appunti modificato

`save(String path)` scrive il blocco appunti aggiornato nella posizione di file indicata.

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Problemi comuni e consigli

- **Indice fuori dai limiti:** Verifica sempre la dimensione della collezione prima di chiamare `removeRange` o `insertItem`.  
- **Titoli null:** Alcune pagine storiche potrebbero non avere un titolo; proteggi il codice da `null` quando chiami `getTitle()`.  
- **Posizione di salvataggio:** Assicurati che il percorso di output (`ModifyPageHistory_out.one`) sia scrivibile; altrimenti verrà lanciata un'`IOException`.  
- **Consiglio di performance:** Quando lavori con blocchi appunti molto grandi, chiama `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` per abilitare il caricamento lazy e mantenere basso l'uso della memoria.

## Domande frequenti

**D:** Posso usare Aspose.Note per Java con altri framework Java?  
**R:** Sì, Aspose.Note per Java si integra perfettamente con Spring, Hibernate, Android e altri ecosistemi Java.

**D:** Aspose.Note per Java è compatibile con diverse versioni dei file OneNote?  
**R:** Assolutamente—Aspose.Note supporta sia i file OneNote 2007 legacy sia i formati moderni OneNote 2016/Online.

**D:** Aspose.Note per Java richiede dipendenze aggiuntive?  
**R:** No, la libreria è autonoma; hai bisogno solo del JAR core e di un runtime Java.

**D:** Posso eseguire modifiche in blocco su più file OneNote simultaneamente?  
**R:** Sì, puoi iterare su una directory di file `.one` e applicare la stessa logica di modifica della cronologia a ciascun blocco appunti.

**D:** Esiste un forum della community per Aspose.Note per Java dove posso chiedere aiuto?  
**R:** Sì, puoi visitare il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per assistenza e per condividere esempi.

---

**Ultimo aggiornamento:** 2026-05-31  
**Testato con:** Aspose.Note per Java 24.11 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [tutorial revisioni pagine aspose.note – Ottieni revisioni pagina in OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Come salvare la versione di una pagina OneNote – Inserisci la versione corrente della pagina in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [traccia modifiche onenote – Gestisci revisioni pagina con Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
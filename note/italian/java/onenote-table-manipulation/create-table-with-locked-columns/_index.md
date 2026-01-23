---
date: 2026-01-23
description: Scopri come bloccare la larghezza delle colonne quando aggiungi una tabella
  a OneNote usando Aspose.Note per Java. Guida passo‑passo con codice, suggerimenti
  e FAQ.
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: Come bloccare la colonna in una tabella di OneNote – Aspose.Note
url: /it/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come bloccare una colonna in una tabella OneNote – Aspose.Note

## Introduzione
OneNote è una piattaforma versatile per prendere appunti, e Aspose.Note per Java semplifica **come bloccare la larghezza della colonna** quando aggiungi una tabella a OneNote. In questo tutorial vedrai un esempio completo, pratico, che mostra come impostare la larghezza della colonna della tabella, bloccarla e personalizzare i bordi della tabella OneNote—tutto con poche righe di codice Java.

## Risposte rapide
- **Cosa significa “bloccare la colonna”?** Fissa la larghezza della colonna in modo che l'utente non possa ridimensionarla in OneNote.  
- **Quale libreria fornisce questa funzionalità?** Aspose.Note per Java.  
- **È necessaria una licenza per eseguire il campione?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza commerciale per la produzione.  
- **Posso aggiungere altre righe dopo aver bloccato la colonna?** Sì, puoi continuare ad aggiungere righe; la larghezza bloccata rimane applicata.  
- **Quale versione di Java è supportata?** Java 6 e successive.

## Che cosa significa “come una colonna significa assegnare una larghezza fissa a un og larghezza della colonna report.

 iniziare, assicurati che quanto segue sia pronto:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installato sulla tua macchina.  
- Libreria [Aspose.Note per Java](https://downloads.aspose.com/note/java) scaricata e aggiunta al classpath del tuo progetto.

## Importare i pacchetti
Nel tuo progetto Java, importa i pacchetti necessari per lavorare con Aspose.Note:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Passo 1: Configurare il progetto
Crea un nuovo progetto Java (o utilizza uno esistente) e aggiungi i file JAR di Aspose.Note al percorso di compilazione. Assicurati che il progetto sia compilato con il JDK installato.

## Passo 2: Inizializzare gli oggetti Document e Page
Iniziamo creando un nuovo `Document` e una `Page` dove verrà inserita la tabella.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Passo 3: Creare righe e celle della tabella
Qui costruiamo due righe, ciascuna con una singola cella contenente del testo di esempio. Questo dimostra come la colonna bloccata si comporta con contenuti brevi e lunghi.

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

## Passo 4: Creare e personalizzare la tabella
Ora creiamo la tabella, **impostiamo la larghezza della colonna**, **blocchiamo la colonna** e **personalizziamo i bordi della tabella OneNote**.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Passo 5: Aggiungere la tabella a Outline e Page
Ora colleghiamo la tabella a un `OutlineElement` e infine la aggiungiamo alla pagina—questo è il passo **add outline element java**.

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

## Passo 6: Salvare il documento
Salva il file OneNote (`.one`) nella directory specificata in precedenza.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

Congratulazioni! Hai aggiunto con successo **add table to OneNote** con una colonna bloccata, larghezza fissa e bordi personalizzati usando Aspose.Note per Java.

## Problemi comuni e soluzioni
| Problema | Soluzione |
|----------|-----------|
| La tabella appare senza bordi | Assicurati di chiamare `table.setBordersVisible(true);`. |
| La larghezza della colonna cambia dopo aver aggiunto righe | Verifica che `col.setLockedWidth(true);` sia impostato **prima** di aggiungere le righe. |
| Il file non viene salvato | Controlla che `dataDir` punti a una cartella scrivibile e termini con un nome file valido. |

## Domande frequenti

**D: Aspose.Note per Java è compatibile con tutte le versioni di Java?**  
R: Sì, funziona con Java 6 e successive, incluse Java 11 e Java 17.

**D: Posso personalizzare ulteriormente l'aspetto della tabella?**  
R: Assolutamente! Puoi modificare gli stili dei bordi, il padding delle celle, i colori di sfondo e molto altro tramite le proprietà `Table` e `TableCell`.

**D: È disponibile una versione di prova prima dell'acquisto?**  
R: Sì, puoi [scaricare una prova gratuita](https://releases.aspose.com/) per esplorare le funzionalità di Aspose.Note per Java.

**D: Dove posso trovare supporto aggiuntivo o discussioni della community?**  
R: Visita il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per supporto e discussioni della community.

**D: Come posso ottenere una licenza temporanea per Aspose.Note per Java?**  
R: Visita [questo link](https://purchase.aspose.com/temporary-license/) per ottenere una licenza temporanea a scopo di test.

---

**Ultimo aggiornamento:** 2026-01-23  
**Testato con:** Aspose.Note per Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
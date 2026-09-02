---
date: 2026-01-12
description: Scopri come modificare la cronologia delle pagine di OneNote, cambiare
  il titolo di una pagina di OneNote e cancellare la cronologia delle pagine di OneNote
  usando Aspose.Note per Java.
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Come modificare la cronologia delle pagine di OneNote con Aspose.Note
url: /it/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come modificare la cronologia delle pagine OneNote con Aspose.Note

In questo tutorial scoprirai **come modificare i documenti OneNote** programmaticamente lavorando con la cronologia delle pagine. Vedremo come caricare un file OneNote, modificare le voci della cronologia, cambiare il titolo di una pagina e, infine, salvare il notebook aggiornato—tutto utilizzando l'API Aspose.Note per Java. Che tu debba pulire revisioni vecchie o rinominare pagine, i passaggi seguenti ti offrono una soluzione completa e pronta per la produzione.

## Risposte rapide
- **Cosa significa “cronologia della pagina” in OneNote?**  
  È la raccolta delle versioni precedenti della pagina memorizzate all'interno di un file OneNote.
- **Posso eliminare una voce specifica della cronologia?**  
  Sì, utilizza i metodi `removeRange` o `removeItem` sull'oggetto `PageHistory`.
- **La modifica del titolo di una pagina fa parte della manipolazione della cronologia?**  
  Assolutamente—ogni voce della cronologia ha il proprio titolo che può essere modificato.
- **È necessaria una licenza per eseguire questo codice?**  
  Una licenza di valutazione temporanea funziona per i test; è richiesta una licenza completa per la produzione.
- **Quale versione di Java è supportata?**  
  Aspose.Note per Java supporta JDK 8 e versioni successive.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Java Development Kit (JDK)** – JDK 8 o versioni successive installate sulla tua macchina.  
2. **Libreria Aspose.Note per Java** – scaricala dalla [pagina di download](https://releases.aspose.com/note/java/).  
3. **Un documento OneNote di esempio** – ad es. `Sample1.one` che puoi modificare in sicurezza.

## Importare i pacchetti

Per prima cosa, importa le classi necessarie. Il blocco di codice qui sotto deve rimanere esattamente così.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Guida passo‑passo

### Passo 1: Caricare il documento OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Passo 2: Recuperare la prima pagina e la sua cronologia

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Passo 3: Eliminare un intervallo di voci della cronologia

Se devi **eliminare voci della cronologia di OneNote**, chiama `removeRange`. L'esempio rimuove la prima voce.

```java
pageHistory.removeRange(0, 1);
```

### Passo 4: Sostituire una voce della cronologia

Puoi sostituire una voce esistente della cronologia con un nuovo oggetto `Page`.

```java
pageHistory.set_Item(0, new Page());
```

### Passo 5: Cambiare il titolo di una pagina della cronologia

Cambiare il titolo è una richiesta comune quando vuoi **cambiare il titolo di una pagina OneNote** per una revisione specifica.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Passo 6: Aggiungere una nuova voce alla cronologia

Aggiungi una pagina completamente nuova alla collezione della cronologia.

```java
pageHistory.addItem(new Page());
```

### Passo 7: Inserire una pagina in una posizione specifica

Inserisci una pagina all'indice 1, spostando gli elementi esistenti in avanti.

```java
pageHistory.insertItem(1, new Page());
```

### Passo 8: Salvare il notebook modificato

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Perché modificare la cronologia delle pagine OneNote?

- **Controllo di versione:** Conserva solo le revisioni rilevanti e scarta le bozze superflue.  
- **Coerenza:** Allinea i titoli delle pagine tra tutte le versioni storiche per una navigazione migliore.  
- **Prestazioni:** Collezioni di cronologia più piccole riducono le dimensioni del file e migliorano la velocità di caricamento.

## Problemi comuni e consigli

- **Indice fuori dai limiti:** Verifica sempre la dimensione della collezione prima di chiamare `removeRange` o `insertItem`.  
- **Titoli null:** Alcune pagine storiche potrebbero non avere un titolo; proteggi il codice da `null` quando chiami `getTitle()`.  
- **Posizione di salvataggio:** Assicurati che il percorso di output (`ModifyPageHistory_out.one`) sia scrivibile; altrimenti verrà sollevata un'`IOException`.

## Domande frequenti

**D: Posso usare Aspose.Note per Java con altri framework Java?**  
R: Sì, Aspose.Note per Java è compatibile con vari framework Java come Spring, Hibernate, ecc.

**D: Aspose.Note per Java è compatibile con diverse versioni di file OneNote?**  
R: Aspose.Note per Java supporta il lavoro sia con versioni vecchie sia con quelle nuove dei file OneNote.

**D: Aspose.Note per Java richiede dipendenze aggiuntive?**  
R: No, Aspose.Note per Java è una libreria autonoma e non richiede dipendenze aggiuntive.

**D: Posso eseguire modifiche in blocco su più file OneNote contemporaneamente?**  
R: Sì, Aspose.Note per Java fornisce API per gestire modifiche in blocco in modo efficiente.

**D: Esiste un forum della community per Aspose.Note per Java dove posso chiedere aiuto?**  
R: Sì, puoi visitare il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per qualsiasi assistenza o domanda relativa alla libreria.

---

**Ultimo aggiornamento:** 2026-01-12  
**Testato con:** Aspose.Note per Java 24.11 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
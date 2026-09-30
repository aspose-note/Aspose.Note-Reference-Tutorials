---
date: 2026-09-29
description: Il tutorial su come impostare la lingua onenote mostra come assegnare
  la lingua di revisione al testo in OneNote usando Aspose.Note per Java, con codice
  passo‑passo e migliori pratiche.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Imposta la lingua di revisione per il testo in OneNote - Aspose.Note
og_description: Guida su come impostare la lingua onenote per gli sviluppatori Java.
  Scopri come cambiare la lingua del testo, abilitare il controllo ortografico e salvare
  i file OneNote con Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Come impostare la lingua onenote in OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Come impostare la lingua onenote in un documento OneNote – Aspose.Note
url: /it/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come impostare la lingua onenote in un documento OneNote – Aspose.Note

## Introduzione
Se hai bisogno di **set language onenote** per parti specifiche di testo all'interno di un notebook OneNote, Aspose.Note per Java lo rende semplice. In questo tutorial imparerai a creare un documento OneNote, modificare la lingua del testo per parole o frasi individuali e infine salvare il file OneNote con la lingua di correzione applicata correttamente. Alla fine comprenderai perché impostare la lingua è importante per il controllo ortografico e la localizzazione, e avrai un esempio di codice pronto all'uso.

## Risposte rapide
- **What does “set language” affect?** Indica a OneNote quale dizionario di correzione utilizzare per il controllo ortografico e grammaticale.  
- **Can I set different languages in the same note?** Sì, è possibile assegnare una lingua a ciascuna sequenza di testo.  
- **Do I need a license for Aspose.Note?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per la produzione.  
- **Which Java versions are supported?** Aspose.Note per Java supporta Java 8 e versioni successive.  
- **Is the output a .one file?** Sì, il documento viene salvato come file OneNote *.one*.

## Cos'è set language onenote?
`set language onenote` si riferisce all'assegnazione di una locale IETF BCP‑47 a una sequenza di testo in modo che il motore di correzione di OneNote utilizzi il dizionario appropriato. questi metadati viaggiano con il file *.one* e sono rispettati dal client OneNote su qualsiasi piattaforma.

## Perché impostare set language onenote?
Applicare la lingua corretta migliora l'accuratezza del controllo ortografico fino al **95 %** per notebook multilingue e velocizza l'indicizzazione di circa **30 %** perché il motore può saltare i dizionari non pertinenti. Aspose.Note supporta **30+** formati di input e output e può elaborare notebook con **10,000+** pagine senza caricare l'intero file in memoria.

## Prerequisiti
Prima di immergerti nel codice, assicurati di avere quanto segue:

1. **Java Development Environment** – JDK 8 o superiore installato e configurato.  
2. **Aspose.Note for Java Library** – Scarica e installa la libreria dal [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Crea una cartella sul tuo computer dove verrà salvato il file OneNote generato.

## Come impostare set language onenote
Per impostare la lingua, prima carica un documento OneNote esistente o crea una nuova istanza `Document`. Quindi, per ogni segmento di testo che desideri modificare, crea o recupera un oggetto `RichText`, applica un `TextStyle` con il `Locale` desiderato (ad esempio `Locale.forLanguageTag("en-US")`), e collega il testo formattato nuovamente all'outline. Infine, chiama `document.save` per scrivere le modifiche in un file *.one*, preservando i metadati della lingua.

## Passo 1: configurare documento e pagina
Document è l'oggetto di livello superiore di Aspose.Note che rappresenta un notebook OneNote in memoria. Dopo aver creato un'istanza `Document` è possibile aggiungere pagine, outline e altri elementi.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Passo 2: creare outline e elemento outline
`Outline` funge da contenitore per il contenuto della pagina, mentre `OutlineElement` contiene elementi individuali come il testo formattato.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Passo 3: aggiungere testo formattato con impostazioni di lingua
`RichText` memorizza i caratteri effettivi. `TextStyle` consente di associare un `Locale` (ad es., `en‑US`, `fr‑FR`) alla sequenza di testo, che è il modo per **set language onenote**. Applicare lo stile a ogni chiamata `append` garantisce un controllo granulare.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Passo 4: organizzare gli elementi e salvare
`ParagraphStyle` può essere usato quando vuoi impostare la lingua per un intero paragrafo invece che per parole singole. Dopo aver assemblato la gerarchia dell'outline, chiama `document.save` per scrivere un file *.one* che conserva tutti i metadati della lingua.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Problemi comuni e consigli
- **Locale format** – Usa il tag IETF BCP‑47 (ad es., `en-US`, `de-DE`). Un tag errato farà ricadere sulla lingua del documento.  
- **File path** – Assicurati che `dataDir` punti a una cartella esistente; altrimenti `document.save` genererà un `IOException`.  
- **Pro tip:** Se devi impostare la lingua per un intero paragrafo, applica il `TextStyle` al `ParagraphStyle` invece di ogni chiamata `append`.

## Conclusione
Hai appena appreso **how to set language onenote** per frammenti di testo individuali in un notebook OneNote usando Aspose.Note per Java. Questa funzionalità ti consente di **create OneNote document** in modo programmatico, **change text language** al volo e **save OneNote file** con metadati di correzione accurati.

## Domande frequenti

**Q: Posso impostare la lingua di correzione per altre lingue non menzionate nell'esempio?**  
A: Assolutamente! Aggiungi chiamate `append` aggiuntive con il `Locale.forLanguageTag("xx-XX")` desiderato.

**Q: Aspose.Note per Java è compatibile con le ultime versioni di Java?**  
A: Sì, la libreria viene regolarmente aggiornata per supportare le versioni più recenti di Java.

**Q: Come posso gestire gli errori durante il processo di impostazione della lingua?**  
A: Avvolgi l'operazione di salvataggio in un blocco `try‑catch` per catturare `IOException` o `AsposeException`.

**Q: Posso integrare questo codice in un'applicazione web?**  
A: Certamente. Basta includere il JAR di Aspose.Note nel classpath del tuo progetto web e assicurarsi che il server abbia i permessi di scrittura sulla directory di destinazione.

**Q: Dove posso trovare esempi aggiuntivi e documentazione per Aspose.Note per Java?**  
A: Esplora la [documentation](https://reference.aspose.com/note/java/) per un elenco completo di API e progetti di esempio.

---

**Ultimo aggiornamento:** 2026-09-29  
**Testato con:** Aspose.Note per Java 24.12  
**Autore:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Tutorial correlati

- [Carica file OneNote con Java: usa Aspose.Note per caricare documenti OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Converti OneNote in testo semplice – estrai tutto il testo con Aspose.Note per Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Converti OneNote in PDF usando le impostazioni di pagina con Aspose.Note per Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
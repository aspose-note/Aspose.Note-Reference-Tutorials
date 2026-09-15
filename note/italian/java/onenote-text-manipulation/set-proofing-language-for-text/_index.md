---
date: 2026-03-29
description: Scopri come impostare la lingua del testo in OneNote usando Aspose.Note
  per Java. Questa guida passo passo ti mostra come creare un documento OneNote, modificare
  la lingua del testo e salvare il file OneNote in modo efficiente.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Come impostare la lingua del testo in OneNote – Aspose.Note
url: /it/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come impostare la lingua per il testo in OneNote – Aspose.Note

## Introduzione
Se hai bisogno di **impostare la lingua** per parti specifiche di testo all'interno di un notebook OneNote, Aspose.Note per Java lo rende semplice. In questo tutorial imparerai a creare un documento OneNote, cambiare la lingua del testo per parole o frasi individuali e, infine, salvare il file OneNote con la lingua di correzione corretta applicata. Alla fine comprenderai perché impostare la lingua è importante per il controllo ortografico e la localizzazione, e avrai a disposizione un esempio di codice pronto all'uso.

## Risposte rapide
- **Che cosa influenza “set language”?** Indica a OneNote quale dizionario di correzione utilizzare per ortografia e grammatica.  
- **Posso impostare lingue diverse nella stessa nota?** Sì, è possibile assegnare una lingua a ciascuna sequenza di testo.  
- **Ho bisogno di una licenza per Aspose.Note?** Una prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per la produzione.  
- **Quali versioni di Java sono supportate?** Aspose.Note per Java supporta Java 8 e versioni successive.  
- **L'output è un file .one?** Sì, il documento viene salvato come file OneNote *.one*.

## Prerequisiti
Prima di immergersi nel codice, assicurati di avere quanto segue:

1. **Ambiente di sviluppo Java** – JDK 8 o superiore installato e configurato.  
2. **Libreria Aspose.Note per Java** – Scarica e installa la libreria dal [download link](https://releases.aspose.com/note/java/).  
3. **Directory dei documenti** – Crea una cartella sul tuo computer dove verrà salvato il file OneNote generato.

## Perché impostare la lingua per il testo in OneNote?
Impostare la lingua di correzione garantisce che ortografia, suggerimenti grammaticali e indicizzazione della ricerca funzionino correttamente per contenuti multilingue. È particolarmente utile per:

- **Team globali** che collaborano su un unico notebook.  
- **Documentazione localizzata** in cui ogni sezione può essere in una lingua diversa.  
- **Applicazioni basate sui dati** che generano note programmaticamente per utenti in tutto il mondo.

## Importa pacchetti
Inizia importando le classi necessarie di Aspose.Note e le utility Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Passo 1: Configura documento e pagina
Crea un nuovo documento OneNote e una pagina che conterrà il tuo contenuto. Questo passo dimostra anche **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Passo 2: Crea outline e elemento outline
Un outline è il contenitore del contenuto del notebook. Qui costruiamo la struttura che in seguito conterrà il testo specifico per lingua.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Passo 3: Aggiungi testo formattato con impostazioni di lingua
Ora **cambiamo la lingua del testo** collegando un `TextStyle` con un `Locale` specifico a ciascun segmento di testo. Questo dimostra **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Passo 4: Organizza gli elementi e salva
Assembla la gerarchia dell'outline, collegala alla pagina e infine **save OneNote file** con le impostazioni di lingua applicate.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Problemi comuni e suggerimenti
- **Formato Locale** – Usa il tag IETF BCP‑47 (es., `en-US`, `de-DE`). Un tag errato farà ricadere sulla lingua del documento.  
- **Percorso file** – Assicurati che `dataDir` punti a una cartella esistente; altrimenti `document.save` genererà un `IOException`.  
- **Consiglio professionale:** Se devi impostare la lingua per un intero paragrafo, applica il `TextStyle` al `ParagraphStyle` invece di ogni chiamata `append`.

## Conclusione
Hai appena imparato **how to set language** per frammenti di testo individuali in un notebook OneNote usando Aspose.Note per Java. Questa funzionalità ti consente di **create OneNote document** programmaticamente, **change text language** al volo e **save OneNote file** con metadati di correzione accurati.

## Domande frequenti

**Q: Posso impostare la lingua di correzione per altre lingue non menzionate nell'esempio?**  
A: Assolutamente! Aggiungi chiamate `append` aggiuntive con il `Locale.forLanguageTag("xx-XX")` desiderato.

**Q: Aspose.Note per Java è compatibile con le versioni più recenti di Java?**  
A: Sì, la libreria è regolarmente aggiornata per supportare le ultime versioni di Java.

**Q: Come posso gestire gli errori durante il processo di impostazione della lingua?**  
A: Avvolgi l'operazione di salvataggio in un blocco `try‑catch` per catturare `IOException` o `AsposeException`.

**Q: Posso integrare questo codice in un'applicazione web?**  
A: Certamente. Basta includere il JAR di Aspose.Note nel classpath del tuo progetto web e assicurarsi che il server abbia i permessi di scrittura sulla directory di destinazione.

**Q: Dove posso trovare esempi aggiuntivi e documentazione per Aspose.Note per Java?**  
A: Esplora la [documentation](https://reference.aspose.com/note/java/) per un elenco completo di API e progetti di esempio.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
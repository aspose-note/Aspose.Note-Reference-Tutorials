---
date: 2026-01-05
description: Scopri come impostare la lingua predefinita, caricare un documento OneNote,
  impostare la licenza Aspose, convertire OneNote in PNG e salvare OneNote come immagine
  utilizzando Aspose.Note per Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Imposta locale predefinito in OneNote – Aspose.Note Java
url: /it/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta la locale predefinita in OneNote – Aspose.Note Java

## Introduzione

Se hai bisogno di **impostare la locale predefinita** durante l'elaborazione dei file OneNote, Aspose.Note per Java lo rende un gioco da ragazzi. In questo tutorial ti guideremo passo passo—dalla licenza del prodotto al caricamento di un documento OneNote, alla modifica della locale e infine alla conversione del file in un'immagine PNG. Alla fine, sarai in grado di personalizzare le impostazioni della lingua e generare output specifici per la locale con poche righe di codice.

## Risposte rapide
- **Cosa fa “impostare la locale predefinita”?** Definisce la lingua e la formattazione regionale usata da Aspose.Note durante la lettura o scrittura dei file OneNote.  
- **Ho bisogno di una licenza?** Sì—imposta la licenza Aspose per sbloccare tutte le funzionalità.  
- **Quale versione di Java è richiesta?** Qualsiasi JDK 8+ è supportato.  
- **Posso convertire OneNote in PNG?** Assolutamente; l'API consente di salvare le pagine come immagini.  
- **Il processo è thread‑safe?** L'impostazione della locale predefinita è globale, quindi configurala una sola volta all'avvio dell'applicazione.

## Cos'è “impostare la locale predefinita” in Aspose.Note?

Impostare la locale predefinita indica ad Aspose.Note quale lingua e convenzioni culturali applicare quando si analizzano date, numeri e testo. Questo è essenziale per applicazioni multi‑regionale che necessitano di una formattazione coerente tra le diverse locale degli utenti.

## Perché impostare la locale predefinita quando si lavora con OneNote?

- **Rappresentazione accurata dei dati:** Date e numeri appaiono correttamente per il pubblico di destinazione.  
- **Stringhe UI coerenti:** Il testo estratto da OneNote rispetta le impostazioni della lingua.  
- **Conversione semplificata:** Quando in seguito converti un file OneNote in PNG o altri formati, il layout visivo corrisponde alla locale prevista.

## Prerequisiti

- **Ambiente di sviluppo Java:** JDK installato e `JAVA_HOME` configurato.  
- **Libreria Aspose.Note:** Scarica l'ultimo JAR dal [download link](https://releases.aspose.com/note/java/).  
- **Un file di licenza Aspose valido** (la versione di prova gratuita funziona per i test).

## Importa pacchetti

Prima di scrivere qualsiasi codice, importa le classi che forniscono la funzionalità necessaria.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Passo 1: Imposta la licenza Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

Impostare la licenza Aspose sblocca tutte le funzionalità, inclusa la gestione della locale e la conversione delle immagini.

## Passo 2: Imposta la locale predefinita

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Qui **impostiamo la locale predefinita** su English (`en`) con il codice paese `rs`. Regola i codici lingua e paese per corrispondere alla tua regione di destinazione.

## Passo 3: Carica il documento OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Questo passo **carica il documento OneNote** nell'oggetto `Document` così da poter lavorare con il suo contenuto.

## Passo 4: Converti OneNote in PNG (conversione file OneNote)

```java
oneFile.save("sample.png");
```

Il metodo `save` esegue una **conversione del file onenote**, esportando il notebook (o una pagina specifica) come immagine PNG—effettivamente **converti onenote in png** e **salva onenote come immagine**.

## Problemi comuni e suggerimenti

- **Licenza non trovata:** Assicurati che il percorso di `licenseFile` sia corretto e che il file abbia i permessi di lettura.  
- **Locale non applicata:** Chiama `Locale.setDefault` **prima** di caricare il documento.  
- **Output immagine mancante:** Verifica che il file OneNote contenga effettivamente pagine renderizzabili; i notebook vuoti produrranno un PNG vuoto.

## Domande frequenti

**D: Aspose.Note è compatibile con diverse versioni di Java?**  
**R:** Sì, Aspose.Note supporta Java 8 e successive, garantendo ampia compatibilità con gli ambienti di sviluppo.

**D: Posso integrare Aspose.Note con altre librerie Java?**  
**R:** Assolutamente. L'API funziona senza problemi con librerie popolari come Apache POI, Jackson e Spring.

**D: Aspose.Note offre supporto per diversi formati di file?**  
**R:** Sebbene il suo focus principale siano i file OneNote, la libreria può esportare in PNG, JPEG, PDF e altri formati immagine.

**D: Esiste un forum della community per gli utenti di Aspose.Note dove chiedere aiuto e condividere conoscenze?**  
**R:** Sì, il forum della community Aspose fornisce una piattaforma per gli utenti per interagire con esperti, fare domande e collaborare su soluzioni. Visita il [support forum](https://forum.aspose.com/c/note/28) per assistenza.

**D: Posso provare Aspose.Note prima di acquistarlo?**  
**R:** Certamente, puoi esplorare le capacità di Aspose.Note usufruendo della prova gratuita offerta sul sito.

## Conclusione

Seguendo questi passaggi hai imparato come **impostare la locale predefinita**, **caricare il documento OneNote**, **impostare la licenza Aspose** e **convertire OneNote in PNG** usando Aspose.Note per Java. Questo flusso di lavoro ti consente di generare report e immagini sensibili alla locale che soddisfano un pubblico globale.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-01-05  
**Testato con:** Aspose.Note 24.11 for Java  
**Autore:** Aspose
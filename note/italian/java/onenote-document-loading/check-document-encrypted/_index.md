---
date: 2026-07-05
description: Scopri come controllare la crittografia di onenote usando Aspose.Note
  per Java. Rileva i file OneNote crittografati prima del caricamento per evitare
  errori e migliorare l'esperienza dell'utente.
keywords:
- check onenote encryption
- Aspose.Note encryption detection
- Java OneNote password check
linktitle: Verifica se il documento OneNote è crittografato - Java
second_title: Aspose.Note Java API
title: controlla la crittografia di onenote – Verifica la crittografia dei documenti
  OneNote con Java
url: /it/java/onenote-document-loading/check-document-encrypted/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# Verifica se il documento OneNote è crittografato – Java  

## Introduzione  

Quando lavori con file OneNote in un'applicazione Java, la prima cosa da sapere è **se il documento è crittografato**. Tentare di caricare un file crittografato senza la password corretta genererà eccezioni e interromperà il flusso di lavoro. In questo tutorial ti guideremo su **come verificare la crittografia di OneNote** con Aspose.Note per Java, così potrai decidere in modo sicuro se chiedere all'utente una password o continuare a elaborare il file.  

## Risposte rapide  

- **Quale metodo determina la crittografia?** `Document.isEncrypted`  
- **È necessaria una password per verificare?** No, è possibile interrogare lo stato senza una password.  
- **Quale versione dell'API funziona?** Qualsiasi versione recente di Aspise.Note per Java (testata con 26.4).  
- **Posso verificare sia gli stream che i percorsi file?** Sì – l'API supporta entrambi.  
- **Cosa succede se la password è errata?** Il metodo restituisce `true`, indicando che il file rimane crittografato.  

## Che cos'è la verifica della crittografia di OneNote?  

Verificare la crittografia di OneNote significa determinare programmaticamente se un file OneNote (`.one`) è protetto da una password prima di qualsiasi tentativo di leggere il suo contenuto. Questo rapido controllo di stato previene eccezioni a runtime, consente di richiedere la password agli utenti solo quando necessario e aiuta a rispettare le politiche di sicurezza.  

## Perché verificare la crittografia di OneNote prima del caricamento?  

Caricare un file OneNote crittografato senza fornire la password corretta genera un'eccezione che può far crashare il servizio o mostrare un errore confuso all'utente. Verificando prima il flag di crittografia, è possibile presentare una richiesta di password solo quando necessario, ridurre I/O non necessario e garantire che i contenuti protetti vengano gestiti secondo le regole di governance aziendale.  

## Prerequisiti  

1. **Java Development Kit (JDK)** – È richiesto Java 11 o successivo. Scaricalo da [qui](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note per Java** – ottieni la libreria dalla pagina di download ufficiale [qui](https://releases.aspose.com/note/java/).  

## Importa pacchetti  

La classe `Document` rappresenta un file OneNote e fornisce metodi per caricare e ispezionare il suo contenuto.  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

## Come verificare lo stato di crittografia per un documento caricato da uno stream?  

`Document.isEncrypted` è un metodo statico che restituisce un booleano indicando se un file OneNote è crittografato. Carica il tuo stream OneNote in stile PDF e chiama il metodo statico `Document.isEncrypted`. Il metodo restituisce un booleano che indica la crittografia e, quando il file non è crittografato, riempie un array di riferimento con l'istanza `Document` caricata così non è necessario un secondo caricamento.  

**Risposta diretta (40‑70 parole):**  
Chiama `Document.isEncrypted(inputStream, loadOptions, ref)` – ti dice immediatamente se lo stream è protetto da password. Se il risultato è `false`, `ref[0]` contiene l'oggetto `Document` pronto all'uso, permettendoti di continuare l'elaborazione senza I/O aggiuntivo. Se il risultato è `true`, lo stream è crittografato e devi richiedere una password prima di procedere.  

**Spiegazione**  

- `LoadOptions` ti consente di fornire opzionalmente una password (`setDocumentPassword`).  
- `Document.isEncrypted(stream, loadOptions, ref)` verifica lo stato di crittografia dello stream.  
- L'array `ref` riceve un riferimento al `Document` caricato quando il file **non** è crittografato, permettendoti di continuare l'elaborazione senza una seconda chiamata di caricamento.  

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```  

## Come verificare lo stato di crittografia per un documento caricato da un percorso file?  

`Document.isEncrypted` offre anche una sovraccarico che funziona direttamente con un percorso file e una stringa password. Questo sovraccarico segue lo stesso schema di ritorno booleano, popolando l'array di riferimento solo quando il file non è crittografato.  

**Risposta diretta (40‑70 parole):**  
Invoca `Document.isEncrypted(filePath, password, ref)` – la chiamata restituisce `true` se il file è crittografato (o la password è errata) e `false` altrimenti. Quando è `false`, `ref[0]` contiene il `Document` completamente caricato pronto per la manipolazione. Questo approccio evita un passaggio di caricamento separato e mantiene il codice conciso.  

**Spiegazione**  

- Questo sovraccarico funziona direttamente con un percorso file e una stringa password.  
- Se il file **non** è crittografato, `isEncrypted` restituisce `false` e il riferimento `ref[0]` contiene il documento caricato.  
- Se la password è errata, il metodo restituisce comunque `true`, indicando che il file rimane crittografato.  

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```  

## Problemi comuni e consigli  

- **Non inserire mai password in chiaro** nel codice di produzione; recuperale in modo sicuro (ad esempio, da un vault).  
- Chiudi sempre gli stream in un blocco `finally` o usa try‑with‑resources per evitare perdite di risorse.  
- Se ricevi `true` da `isEncrypted` e `ref[0]` è `null`, il file è crittografato **o** la password fornita è errata. Richiedi all'utente la password corretta e riprova.  

## Domande frequenti  

**Q: Posso verificare lo stato di crittografia senza fornire una password?**  
A: Sì. Chiama `Document.isEncrypted` con un'istanza `LoadOptions` che non imposta una password; il metodo segnalerà semplicemente se il file è crittografato.  

**Q: Cosa succede se fornisco una password errata?**  
A: Il metodo restituisce `true`, indicando che il documento è ancora crittografato, e `ref[0]` sarà `null`.  

**Q: Esiste un modo per decrittare il documento programmaticamente?**  
A: Sì. Una volta conosciuta la password corretta, passala a `LoadOptions` (o al sovraccarico che accetta una password) e carica il documento; l'API lo decritterà al volo.  

**Q: Aspose.Note funziona con altri formati Microsoft?**  
A: Aspose.Note è progettato esclusivamente per i file OneNote (`.one`). Per Word, Excel, PowerPoint, ecc., considera rispettivamente Aspose.Words, Aspose.Cells, Aspose.Slides.  

**Q: Dove posso trovare più esempi e supporto?**  
A: Visita il [forum Aspose.Note](https://forum.aspose.com/c/note/28) per l'aiuto della community e consulta la documentazione ufficiale per ulteriori esempi di codice.  

## Conclusione  

In questa guida abbiamo dimostrato **come verificare la crittografia di OneNote** usando Aspose.Note per Java, coprendo scenari sia basati su stream che su file. Integrando questi controlli nella tua applicazione puoi gestire elegantemente i file OneNote crittografati, migliorare l'esperienza utente e mantenere robusta la tua pipeline di elaborazione.  

---  

**Ultimo aggiornamento:** 2026-07-05  
**Testato con:** Aspose.Note 26.4 for Java  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Crea documento OneNote – Carica notebook con Aspose.Note](/note/java/onenote-notebook-operations/loading-notebook/)  
- [Proteggi con password OneNote con Aspose.Note per Java](/note/java/onenote-notebook-operations/write-password-protected-document/)  
- [Ottieni informazioni sul formato file Aspose Note da OneNote usando Java](/note/java/onenote-document-loading/get-file-format-info/)  


{{< /blocks/products/pf/tutorial-page-section >}}  
{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}
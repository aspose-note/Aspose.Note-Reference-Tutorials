---
date: 2026-07-05
description: Erfahren Sie, wie Sie die OneNote Encryption mit Aspose.Note für Java
  prüfen können. Erkennen Sie verschlüsselte OneNote-Dateien, bevor sie geladen werden,
  um Fehler zu vermeiden und die Benutzererfahrung zu verbessern.
keywords:
- check onenote encryption
- Aspose.Note encryption detection
- Java OneNote password check
linktitle: Prüfen, ob OneNote Document verschlüsselt ist – Java
second_title: Aspose.Note Java API
title: OneNote-Verschlüsselung prüfen – Überprüfen von OneNote Document Encryption
  mit Java
url: /de/java/onenote-document-loading/check-document-encrypted/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# Prüfen, ob OneNote-Dokument verschlüsselt ist – Java  

## Einführung  

Wenn Sie mit OneNote‑Dateien in einer Java‑Anwendung arbeiten, ist das Erste, was Sie wissen müssen, **ob das Dokument verschlüsselt ist**. Der Versuch, eine verschlüsselte Datei ohne das richtige Passwort zu laden, führt zu Ausnahmen und unterbricht Ihren Arbeitsablauf. In diesem Tutorial zeigen wir Ihnen **wie Sie die OneNote‑Verschlüsselung** mit Aspose.Note für Java prüfen können, damit Sie sicher entscheiden können, ob Sie den Benutzer nach einem Passwort fragen oder die Datei weiter verarbeiten.  

## Schnelle Antworten  

- **Welche Methode bestimmt die Verschlüsselung?** `Document.isEncrypted`  
- **Benötige ich ein Passwort, um zu prüfen?** Nein, Sie können den Status ohne Passwort abfragen.  
- **Welche API‑Version funktioniert?** Jede aktuelle Aspose.Note‑Version für Java (getestet mit 26.4).  
- **Kann ich sowohl Streams als auch Dateipfade prüfen?** Ja – die API unterstützt beides.  
- **Was passiert, wenn das Passwort falsch ist?** Die Methode gibt `true` zurück, was anzeigt, dass die Datei weiterhin verschlüsselt ist.  

## Was bedeutet das Prüfen der OneNote-Verschlüsselung?  

Das Prüfen der OneNote‑Verschlüsselung bedeutet, programmgesteuert festzustellen, ob eine OneNote‑(`.one`)-Datei mit einem Passwort geschützt ist, bevor ein Versuch unternommen wird, ihren Inhalt zu lesen. Diese schnelle Statusprüfung verhindert Laufzeitausnahmen, ermöglicht es Ihnen, Benutzer nur bei Bedarf zu fragen, und hilft Ihnen, Sicherheitsrichtlinien einzuhalten.  

## Warum die OneNote-Verschlüsselung vor dem Laden prüfen?  

Das Laden einer verschlüsselten OneNote‑Datei ohne das korrekte Passwort löst eine Ausnahme aus, die Ihren Dienst zum Absturz bringen oder dem Benutzer eine verwirrende Fehlermeldung anzeigen kann. Durch das vorherige Prüfen des Verschlüsselungsflags können Sie nur bei Bedarf eine Passwortabfrage anzeigen, unnötige I/O reduzieren und sicherstellen, dass geschützte Inhalte gemäß den Unternehmensrichtlinien behandelt werden.  

## Voraussetzungen  

1. **Java Development Kit (JDK)** – Java 11 oder höher ist erforderlich. Laden Sie es von [hier](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunter.  
2. **Aspose.Note für Java** – erhalten Sie die Bibliothek von der offiziellen Download‑Seite [hier](https://releases.aspose.com/note/java/).  

## Pakete importieren  

Die Klasse `Document` repräsentiert eine OneNote‑Datei und bietet Methoden zum Laden und Untersuchen ihres Inhalts.  

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

## Wie prüfe ich den Verschlüsselungsstatus für ein aus einem Stream geladenes Dokument?  

`Document.isEncrypted` ist eine statische Methode, die einen booleschen Wert zurückgibt, der angibt, ob eine OneNote‑Datei verschlüsselt ist. Laden Sie Ihren PDF‑ähnlichen OneNote‑Stream und rufen Sie die statische Methode `Document.isEncrypted` auf. Die Methode gibt einen booleschen Wert zurück, der die Verschlüsselung anzeigt, und füllt bei nicht verschlüsselten Dateien ein Referenz‑Array mit der geladenen `Document`‑Instanz, sodass kein zweiter Ladevorgang nötig ist.  

**Direkte Antwort (40‑70 Wörter):**  
Rufen Sie `Document.isEncrypted(inputStream, loadOptions, ref)` auf – es teilt Ihnen sofort mit, ob der Stream passwortgeschützt ist. Ist das Ergebnis `false`, enthält `ref[0]` das einsatzbereite `Document`‑Objekt, sodass Sie die Verarbeitung ohne zusätzlichen I/O fortsetzen können. Ist das Ergebnis `true`, ist der Stream verschlüsselt und Sie müssen vor dem Fortfahren ein Passwort anfordern.  

**Erklärung**  

- `LoadOptions` ermöglicht es Ihnen optional ein Passwort anzugeben (`setDocumentPassword`).  
- `Document.isEncrypted(stream, loadOptions, ref)` prüft den Verschlüsselungsstatus des Streams.  
- Das `ref`‑Array erhält eine Referenz auf das geladene `Document`, wenn die Datei **nicht** verschlüsselt ist, sodass Sie die Verarbeitung ohne einen zweiten Ladevorgang fortsetzen können.  

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

## Wie prüfe ich den Verschlüsselungsstatus für ein aus einem Dateipfad geladenes Dokument?  

`Document.isEncrypted` bietet zudem eine Überladung, die direkt mit einem Dateipfad und einem Passwort‑String arbeitet. Diese Überladung folgt dem gleichen booleschen Rückgabemuster und füllt das Referenz‑Array nur, wenn die Datei nicht verschlüsselt ist.  

**Direkte Antwort (40‑70 Wörter):**  
Rufen Sie `Document.isEncrypted(filePath, password, ref)` auf – der Aufruf gibt `true` zurück, wenn die Datei verschlüsselt ist (oder das Passwort falsch ist) und sonst `false`. Ist das Ergebnis `false`, enthält `ref[0]` das vollständig geladene `Document`, das zur Manipulation bereitsteht. Dieser Ansatz vermeidet einen separaten Ladeschritt und hält Ihren Code kompakt.  

**Erklärung**  

- Diese Überladung arbeitet direkt mit einem Dateipfad und einem Passwort‑String.  
- Wenn die Datei **nicht** verschlüsselt ist, gibt `isEncrypted` `false` zurück und die Referenz `ref[0]` enthält das geladene Dokument.  
- Ist das Passwort falsch, gibt die Methode **weiterhin `true`** zurück, was anzeigt, dass die Datei weiterhin verschlüsselt ist.  

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

## Häufige Fallstricke & Tipps  

- **Niemals Passwörter hart codieren** im Produktionscode; holen Sie sie sicher (z. B. aus einem Tresor).  
- Schließen Sie Streams immer in einem `finally`‑Block oder verwenden Sie try‑with‑resources, um Ressourcenlecks zu vermeiden.  
- Wenn Sie `true` von `isEncrypted` erhalten und `ref[0]` ist `null`, ist die Datei entweder verschlüsselt **oder** das angegebene Passwort ist **falsch**. Fordern Sie den Benutzer zum korrekten Passwort auf und versuchen Sie es erneut.  

## Häufig gestellte Fragen  

**Q: Kann ich den Verschlüsselungsstatus prüfen, ohne ein Passwort anzugeben?**  
A: Ja. Rufen Sie `Document.isEncrypted` mit einer `LoadOptions`‑Instanz auf, die kein Passwort setzt; die Methode gibt einfach an, ob die Datei verschlüsselt ist.  

**Q: Was passiert, wenn ich ein falsches Passwort angebe?**  
A: Die Methode gibt `true` zurück, was anzeigt, dass das Dokument weiterhin verschlüsselt ist, und `ref[0]` wird `null` sein.  

**Q: Gibt es eine Möglichkeit, das Dokument programmgesteuert zu entschlüsseln?**  
A: Ja. Sobald Sie das korrekte Passwort kennen, übergeben Sie es an `LoadOptions` (oder an die Überladung, die ein Passwort akzeptiert) und laden das Dokument; die API entschlüsselt es dann automatisch.  

**Q: Arbeitet Aspose.Note mit anderen Microsoft‑Formaten?**  
A: Aspose.Note ist ausschließlich für OneNote‑(`.one`)-Dateien konzipiert. Für Word, Excel, PowerPoint usw. sollten Sie jeweils Aspose.Words, Aspose.Cells, Aspose.Slides verwenden.  

**Q: Wo finde ich weitere Beispiele und Support?**  
A: Besuchen Sie das [Aspose.Note‑Forum](https://forum.aspose.com/c/note/28) für Community‑Hilfe und prüfen Sie die offizielle Dokumentation für weitere Code‑Beispiele.  

## Fazit  

In diesem Leitfaden haben wir **wie man die OneNote‑Verschlüsselung** mit Aspose.Note für Java prüft, sowohl für Stream‑ als auch für Dateibasiertes Szenario. Durch die Integration dieser Prüfungen in Ihre Anwendung können Sie verschlüsselte OneNote‑Dateien elegant handhaben, die Benutzererfahrung verbessern und Ihre Verarbeitungspipeline robust halten.  

---  

**Zuletzt aktualisiert:** 2026-07-05  
**Getestet mit:** Aspose.Note 26.4 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [OneNote-Dokument erstellen – Notebook mit Aspose.Note laden](/note/java/onenote-notebook-operations/loading-notebook/)
- [OneNote mit Aspose.Note für Java passwortgeschützt](/note/java/onenote-notebook-operations/write-password-protected-document/)
- [Aspose Note Dateiformatinformationen aus OneNote mit Java abrufen](/note/java/onenote-document-loading/get-file-format-info/)


{{< /blocks/products/pf/tutorial-page-section >}}  
{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}
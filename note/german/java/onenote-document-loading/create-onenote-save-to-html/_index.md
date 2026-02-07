---
date: 2026-02-07
description: Erfahren Sie, wie Sie Schriftarten exportieren, während Sie OneNote als
  HTML mit Aspose.Note für Java speichern. Dieser Leitfaden zeigt Ihnen, wie Sie OneNote
  programmgesteuert erstellen und Schriftarten, CSS und Bilder einbetten.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Wie man Schriftarten exportiert, wenn man OneNote als HTML speichert – Java
url: /de/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Schriftarten exportiert, wenn man OneNote als HTML speichert – Java

## Einführung

In diesem Tutorial erfahren Sie **wie man Schriftarten exportiert**, wenn Sie **OneNote als HTML speichern** mit Aspose.Note für Java. Wir führen Sie durch das programmgesteuerte Erstellen eines OneNote-Dokuments, das Konfigurieren der HTML‑Speicheroptionen und das Einbetten der erforderlichen Schriftdateien, sodass das resultierende HTML genau wie die ursprünglichen OneNote‑Seiten aussieht. Dieser Ansatz ist ideal, wenn Sie die visuelle Treue von OneNote‑Inhalten in einem web‑freundlichen Format bewahren müssen.

## Schnelle Antworten
- **Welche Bibliothek übernimmt den Export?** Aspose.Note für Java  
- **Können Schriftarten in das HTML eingebettet werden?** Ja – setzen Sie `ExportFonts` auf `ExportEmbedded`  
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.Note‑Lizenz ist für die kommerzielle Nutzung erforderlich  
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher  
- **Ist es möglich, Ressourcen in separate Dateien zu speichern?** Absolut – konfigurieren Sie `ResourceExportType` entsprechend  

## Was bedeutet „wie man Schriftarten exportiert“ im Kontext der OneNote‑HTML‑Konvertierung?

Wenn Sie ein OneNote‑Notizbuch in HTML konvertieren, hängt das visuelle Erscheinungsbild von CSS, Bildern und insbesondere den in den Originalseiten verwendeten Schriftarten ab. **Schriftarten exportieren** bedeutet, die Schriftdateien (z. B. TTF) direkt in das HTML‑Paket einzubetten, sodass Browser den Text exakt so darstellen können, wie er in OneNote erscheint, selbst wenn der Endbenutzer diese Schriftarten nicht lokal installiert hat.

## Warum OneNote programmgesteuert erstellen und als HTML speichern?

- **Automatisierung:** Berichte, Dokumentationen oder Wissensdatenbank‑Artikel aus OneNote generieren, ohne manuelles Kopieren‑Einfügen.  
- **Konsistenz:** Layout, Stil und benutzerdefinierte Schriftarten über Geräte hinweg bewahren.  
- **Portabilität:** HTML ist universell anzeigbar – kein OneNote‑Client erforderlich.  

## Voraussetzungen

1. Java Development Kit (JDK) 8 oder neuer installiert.  
2. Aspose.Note für Java‑Bibliothek – Download von [here](https://releases.aspose.com/note/java/).  
3. Eine Beispiel‑OneNote‑Datei (`.one`) zum Laden, oder Sie können programmgesteuert eine neue erstellen.  

## Pakete importieren

Zuerst importieren Sie die erforderlichen Klassen in Ihr Java‑Projekt:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Wie man Schriftarten exportiert, während man OneNote als HTML speichert?

Im Folgenden finden Sie eine Schritt‑für‑Schritt‑Anleitung, die Ihnen **zeigt, wie man Schriftarten exportiert** und andere Ressourcen.

### Schritt 1: OneNote‑Dokument programmgesteuert erstellen  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Diese Zeile lädt eine vorhandene `.one`‑Datei. Wenn Sie **OneNote programmgesteuert erstellen** müssen, können Sie ein neues `Document`‑Objekt instanziieren und über die API Abschnitte/Seiten hinzufügen (hier nicht gezeigt, um den Fokus auf das Exportieren von Schriftarten zu behalten).

### Schritt 2: In einen Speicher‑Stream mit eingebetteten Schriftarten speichern  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` weist Aspose.Note an, **Schriftarten** direkt in das HTML‑Paket zu **exportieren**.  
- `setFontFaceTypes(FontFaceType.Ttf)` stellt sicher, dass TrueType‑Schriftarten verwendet werden, die eine breite Browser‑Unterstützung besitzen.

### Schritt 3: Als HTML mit separaten Ressourcendateien speichern (schon Schriftarten exportierend)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Obwohl CSS und Bilder eingebettet sind, können Sie `ResourceExportType` auf `ExportExternal` ändern, wenn Sie separate Dateien für einfacheres Caching bevorzugen. Der entscheidende Teil – **Schriftarten exportieren** – bleibt unverändert.

### Schritt 4: Callbacks verwenden, um zu steuern, wo jede Ressource gespeichert wird  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Die Klasse `UserSavingCallbacks` (Sie müssen `ICssSavingCallback`, `IImageSavingCallback` und `IFontSavingCallback` implementieren) gibt Ihnen die volle Kontrolle über die Ordnerstruktur, sodass Sie Schriftarten in einem eigenen `fonts`‑Verzeichnis ablegen können, während Sie weiterhin **Schriftarten korrekt exportieren**.

## Wie man benutzerdefinierte Schriftarten beim Konvertieren von OneNote zu HTML einbettet

Das Einbetten benutzerdefinierter Schriftarten stellt sicher, dass die HTML‑Darstellung dem ursprünglichen OneNote‑Layout entspricht, selbst auf Geräten, die diese Schriftarten nicht installiert haben. Durch die Verwendung von `ExportEmbedded` zusammen mit `FontFaceType.Ttf` werden die TrueType‑Dateien base‑64‑kodiert und direkt in das erzeugte CSS eingefügt, wodurch die Notwendigkeit eines externen Font‑Hostings entfällt.

## Verwendung von ResourceExportType zur Steuerung des Ressourcenexports

`ResourceExportType` ermöglicht Ihnen zu entscheiden, ob CSS, Bilder und Schriftarten **innerhalb** der HTML‑Datei (`ExportEmbedded`) oder als **externe** Dateien (`ExportExternal`) gespeichert werden. Wählen Sie `ExportEmbedded` für eine Ein‑Datei‑Lösung oder `ExportExternal`, wenn Sie das Browser‑Caching für große Assets nutzen möchten.

## OneNote programmgesteuert für den HTML‑Export erstellen

Wenn Sie von Grund auf neu beginnen, können Sie ein OneNote‑Dokument vollständig im Code erstellen, Abschnitte, Seiten und Rich‑Text hinzufügen und dann dieselben `HtmlSaveOptions` wie oben anwenden. Das bietet Ihnen eine End‑zu‑End‑Automatisierung: von der Datengenerierung bis zu einer vollständig gestylten HTML‑Ausgabe mit eingebetteten benutzerdefinierten Schriftarten.

## Häufige Probleme & Tipps

- **Fehlende Schriftarten in der Ausgabe:** Stellen Sie sicher, dass `setExportFonts(ResourceExportType.ExportEmbedded)` gesetzt ist und dass die Quell‑OneNote‑Datei tatsächlich eingebettete Schriftarten verwendet.  
- **Große HTML‑Dateien:** Das Einbetten von Schriftarten kann die Größe erhöhen. Wenn die Bandbreite ein Problem darstellt, wechseln Sie `ExportFonts` zu `ExportExternal` und hosten Sie die Schriftarten auf einem CDN.  
- **Fehler bei der Callback‑Implementierung:** Stellen Sie sicher, dass Ihre Callback‑Klassen den Stream korrekt schreiben und Ressourcen schließen, um Dateikorruption zu vermeiden.  

## Häufig gestellte Fragen

**Q: Kann ich mehrere OneNote‑Dokumente auf einmal in HTML konvertieren?**  
A: Ja, iterieren Sie über jede `Document`‑Instanz und wenden Sie dieselben `HtmlSaveOptions` an.  

**Q: Unterstützt Aspose.Note für Java andere Ausgabeformate neben HTML?**  
A: Absolut. Sie können mit den entsprechenden Speicheroptionen nach PDF, DOCX, PNG, JPEG und mehr exportieren.  

**Q: Gibt es eine Testversion von Aspose.Note für Java?**  
A: Ja, laden Sie eine kostenlose Testversion von [here](https://releases.aspose.com/) herunter.  

**Q: Wo kann ich Support für Aspose.Note für Java erhalten?**  
A: Besuchen Sie das [Aspose.Note‑Forum](https://forum.aspose.com/c/note/28) für Community‑ und offiziellen Support.  

**Q: Wie kann ich eine Lizenz für Aspose.Note für Java erwerben?**  
A: Lizenzen sind auf der [Aspose‑Website](https://purchase.aspose.com/buy) erhältlich.  

## Fazit

Sie wissen jetzt **wie man Schriftarten exportiert**, während Sie **OneNote als HTML speichern** mit Aspose.Note für Java. Durch das Konfigurieren von `HtmlSaveOptions` und optional die Verwendung von Callbacks können Sie das genaue Aussehen Ihrer OneNote‑Seiten – einschließlich benutzerdefinierter Schriftarten – beim Bereitstellen im Web bewahren. Experimentieren Sie gern mit verschiedenen `ResourceExportType`‑Einstellungen, um die Leistungs‑ und Speicheranforderungen Ihres Projekts zu erfüllen.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
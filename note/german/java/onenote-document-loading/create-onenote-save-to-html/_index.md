---
date: 2025-12-02
description: Erfahren Sie, wie Sie Schriftarten exportieren, während Sie OneNote als
  HTML mit Aspose.Note für Java speichern. Dieser Leitfaden zeigt Ihnen, wie Sie OneNote
  programmgesteuert erstellen und Schriftarten, CSS und Bilder einbetten.
language: de
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Wie man Schriftarten exportiert, wenn man OneNote als HTML speichert – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Schriftarten exportiert, wenn man OneNote als HTML speichert – Java

## Einführung

In diesem Tutorial erfahren Sie **wie man Fonts exportiert**, wenn Sie **OneNote als HTML speichern** mit Aspose.Note für Java. Wir führen Sie durch das programmgesteuerte Erstellen eines OneNote‑Dokuments, das Konfigurieren der HTML‑Speicheroptionen und das Einbetten der erforderlichen Schriftdateien, sodass das resultierende HTML exakt wie die ursprünglichen OneNote‑Seiten aussieht. Dieser Ansatz ist ideal, wenn Sie die visuelle Treue von OneNote‑Inhalten in einem web‑freundlichen Format bewahren müssen.

## Schnelle Antworten
- **Welche Bibliothek übernimmt den Export?** Aspose.Note for Java  
- **Können Fonts in das HTML eingebettet werden?** Ja – setzen Sie `ExportFonts` auf `ExportEmbedded`  
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.Note‑Lizenz ist für die kommerzielle Nutzung erforderlich  
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher  
- **Ist es möglich, Ressourcen in separate Dateien zu speichern?** Absolut – konfigurieren Sie `ResourceExportType` entsprechend  

## Was bedeutet „wie man Fonts exportiert“ im Kontext der OneNote‑HTML‑Konvertierung?

Wenn Sie ein OneNote‑Notizbuch in HTML konvertieren, hängt das visuelle Erscheinungsbild von CSS, Bildern und insbesondere den in den Originalseiten verwendeten Fonts ab. **Fonts exportieren** bedeutet, die Schriftdateien (z. B. TTF) direkt in das HTML‑Paket einzubetten, sodass Browser den Text exakt so rendern können wie in OneNote, selbst wenn der End‑Benutzer diese Fonts nicht lokal installiert hat.

## Warum OneNote programmgesteuert erstellen und als HTML speichern?

- **Automatisierung:** Berichte, Dokumentationen oder Knowledge‑Base‑Artikel aus OneNote generieren, ohne manuelles Kopieren und Einfügen.  
- **Konsistenz:** Layout, Styling und benutzerdefinierte Fonts über Geräte hinweg erhalten.  
- **Portabilität:** HTML ist universell viewable — keine OneNote‑Client‑Installation nötig.  

## Voraussetzungen

1. Java Development Kit (JDK) 8 oder neuer installiert.  
2. Aspose.Note für Java‑Bibliothek – Download von [hier](https://releases.aspose.com/note/java/).  
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

## Wie man Fonts exportiert, während man OneNote als HTML speichert?

Im Folgenden finden Sie eine Schritt‑für‑Schritt‑Anleitung, die Ihnen **wie man Fonts exportiert** und weitere Ressourcen zeigt.

### Schritt 1: Ein OneNote‑Dokument programmgesteuert erstellen  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Diese Zeile lädt eine vorhandene `.one`‑Datei. Wenn Sie **OneNote programmgesteuert erstellen** möchten, können Sie ein neues `Document`‑Objekt instanziieren und über die API Abschnitte/Seiten hinzufügen (nicht gezeigt, um den Fokus auf das Exportieren von Fonts zu behalten).

### Schritt 2: In einen Memory‑Stream mit eingebetteten Fonts speichern  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` weist Aspose.Note an, **Fonts** direkt in das HTML‑Paket zu **exportieren**.  
- `setFontFaceTypes(FontFaceType.Ttf)` stellt sicher, dass TrueType‑Fonts verwendet werden, die von den meisten Browsern unterstützt werden.

### Schritt 3: Als HTML mit separaten Ressourcendateien speichern (Fonts weiterhin exportieren)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Obwohl CSS und Bilder eingebettet sind, können Sie `ResourceExportType` auf `ExportExternal` ändern, wenn Sie separate Dateien für einfacheres Caching bevorzugen. Der zentrale Teil — **Fonts exportieren** — bleibt unverändert.

### Schritt 4: Callbacks verwenden, um zu steuern, wo jede Ressource gespeichert wird  

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

Die Klasse `UserSavingCallbacks` (Sie müssen `ICssSavingCallback`, `IImageSavingCallback` und `IFontSavingCallback` implementieren) gibt Ihnen die volle Kontrolle über die Ordnerstruktur, sodass Sie Fonts in einem eigenen `fonts`‑Verzeichnis ablegen können, während Sie **Fonts korrekt exportieren**.

## Häufige Probleme & Tipps

- **Fonts fehlen in der Ausgabe:** Stellen Sie sicher, dass `setExportFonts(ResourceExportType.ExportEmbedded)` gesetzt ist und die Quell‑OneNote‑Datei tatsächlich eingebettete Fonts verwendet.  
- **Große HTML‑Dateien:** Das Einbetten von Fonts kann die Dateigröße erhöhen. Bei Bandbreiten‑Bedenken wechseln Sie `ExportFonts` zu `ExportExternal` und hosten die Fonts auf einem CDN.  
- **Fehler bei Callback‑Implementierungen:** Achten Sie darauf, dass Ihre Callback‑Klassen den Stream korrekt schreiben und Ressourcen schließen, um Dateikorruption zu vermeiden.  

## Häufig gestellte Fragen

**F: Kann ich mehrere OneNote‑Dokumente gleichzeitig in HTML konvertieren?**  
A: Ja, iterieren Sie über jede `Document`‑Instanz und wenden Sie dieselben `HtmlSaveOptions` an.  

**F: Unterstützt Aspose.Note für Java neben HTML noch andere Ausgabeformate?**  
A: Absolut. Sie können mit den entsprechenden Speicheroptionen nach PDF, DOCX, PNG, JPEG und mehr exportieren.  

**F: Gibt es eine Testversion von Aspose.Note für Java?**  
A: Ja, laden Sie eine kostenlose Testversion von [hier](https://releases.aspose.com/).  

**F: Wo bekomme ich Support für Aspose.Note für Java?**  
A: Besuchen Sie das [Aspose.Note‑Forum](https://forum.aspose.com/c/note/28) für Community‑ und offiziellen Support.  

**F: Wie kann ich eine Lizenz für Aspose.Note für Java erwerben?**  
A: Lizenzen sind auf der [Aspose‑Website](https://purchase.aspose.com/buy) erhältlich.  

## Fazit

Sie wissen jetzt **wie man Fonts exportiert**, während Sie **OneNote als HTML speichern** mit Aspose.Note für Java. Durch die Konfiguration von `HtmlSaveOptions` und optional die Nutzung von Callbacks können Sie das exakte Aussehen Ihrer OneNote‑Seiten — einschließlich benutzerdefinierter Fonts —  beim Bereitstellen im Web bewahren. Experimentieren Sie gern mit verschiedenen `ResourceExportType`‑Einstellungen, um die Leistungs‑ und Speicheranforderungen Ihres Projekts zu optimieren.

---

**Zuletzt aktualisiert:** 2025-12-02  
**Getestet mit:** Aspose.Note for Java 24.12  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

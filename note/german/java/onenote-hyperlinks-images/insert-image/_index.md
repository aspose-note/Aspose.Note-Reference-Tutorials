---
date: 2025-12-21
description: Erfahren Sie, wie Sie mit Java und Aspose.Note für Java Bilder zu OneNote‑Dokumenten
  hinzufügen. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung, um Bilder einzufügen
  und optional OneNote als PDF zu speichern.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Wie man ein Bild mit Java zu OneNote hinzufügt
url: /de/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ein Bild in ein OneNote-Dokument mit Java einfügen

## Einführung

In diesem Tutorial werden wir untersuchen, wie man ein Bild in ein OneNote-Dokument mit Java einfügt, mithilfe von Aspose.Note für Java. Aspose.Note für Java ist eine leistungsstarke Bibliothek, die Entwicklern ermöglicht, Microsoft OneNote-Dateien programmgesteuert zu bearbeiten, und verschiedene Vorgänge wie das Erstellen, Lesen und Manipulieren von OneNote-Dokumenten zu unterstützen.

## Schnelle Antworten
- **Was ist der einfachste Weg, ein Bild zu OneNote mit Java hinzuzufügen?**  
  Verwenden Sie die `Image`-Klasse von Aspose.Note für Java und hängen Sie sie an eine Seite an.
- **Benötige ich eine Lizenz für den Produktionseinsatz?**  
  Ja, für Produktionsbereitstellungen ist eine kommerzielle Lizenz erforderlich.
- **Kann ich benutzerdefinierte Abmessungen für das Bild festlegen?**  
  Natürlich – rufen Sie `setWidth()` und `setHeight()` am `Image`-Objekt auf.
- **Ist es möglich, die OneNote-Datei nach dem Hinzufügen des Bildes als PDF zu speichern?**  
  Ja, rufen Sie `save(..., SaveFormat.Pdf)` auf, um **OneNote als PDF zu speichern**.
- **Welche Java-Version wird unterstützt?**  
  Aspose.Note für Java funktioniert mit JDK 8 und höher.

## Wie fügt man ein Bild zu OneNote mit Java hinzu?

Bevor wir in den Code eintauchen, lassen Sie uns kurz besprechen, warum Sie möglicherweise programmatisch Bilder in OneNote einbetten möchten. Ob Sie Sitzungsprotokolle erstellen, automatisierte Berichte generieren oder eine Dokumentationspipeline aufbauen – das Einfügen von Bildern verleiht Ihren Notizen einen visuellen Kontext, den reiner Text nicht bieten kann. Mit Aspose.Note für Java können Sie dies vollständig im Code erledigen, ohne die OneNote-Oberfläche zu öffnen.

## Voraussetzungen

Stellen Sie vor Beginn sicher, dass die folgenden Voraussetzungen eingerichtet sind:

### 1. Java Development Kit (JDK)

Stellen Sie sicher, dass das Java Development Kit (JDK) auf Ihrem System installiert ist. Sie können das JDK von der Oracle-Website herunterladen und installieren.

### 2. Aspose.Note für Java Bibliothek

Laden Sie die Aspose.Note für Java-Bibliothek herunter und richten Sie sie ein, indem Sie der [Dokumentation](https://reference.aspose.com/note/java/) folgen.

## Pakete importieren

Beginnen Sie damit, die erforderlichen Pakete in Ihr Java-Projekt zu importieren. Diese Pakete umfassen die Aspose.Note-Bibliothek und weitere notwendige Abhängigkeiten.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Lassen Sie uns den Vorgang des Einfügens eines Bildes in ein OneNote-Dokument in mehrere Schritte aufteilen:

## Schritt 1: OneNote-Dokument laden

Laden Sie zunächst das OneNote-Dokument, in das Sie das Bild einfügen möchten.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Schritt 2: Seite abrufen

Rufen Sie die Seite im Dokument ab, in die Sie das Bild einfügen möchten.

```java
Page page = oneFile.getFirstChild();
```

## Schritt 3: Bild laden

Laden Sie das Bild, das Sie in das OneNote-Dokument einfügen möchten.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Schritt 4: Bildattribute anpassen (optional)

Optional können Sie Größe, Position und Ausrichtung des Bildes nach Ihren Anforderungen anpassen. Hier können Sie die **Bildabmessungen in Java** festlegen.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Schritt 5: Bild zur Seite hinzufügen

Fügen Sie das Bild zur Seite im OneNote-Dokument hinzu.

```java
page.appendChildLast(image);
```

## Schritt 6: Dokument speichern

Speichern Sie das geänderte Dokument, einschließlich des eingefügten Bildes. Sie können in diesem Schritt auch **OneNote als PDF speichern**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Fazit

In diesem Tutorial haben wir gelernt, wie man ein Bild in ein OneNote-Dokument mit Java mithilfe der Aspose.Note für Java-Bibliothek einfügt. Durch Befolgen der Schritt‑für‑Schritt‑Anleitung können Sie Bilder mühelos programmgesteuert in Ihre OneNote-Dokumente einbinden.

## FAQ

### Q1: Kann ich mehrere Bilder in ein einzelnes OneNote-Dokument mit dieser Methode einfügen?

A1: Ja, Sie können mehrere Bilder in ein einzelnes OneNote-Dokument einfügen, indem Sie den in diesem Tutorial beschriebenen Vorgang für jedes Bild wiederholen.

### Q2: Ist Aspose.Note für Java mit allen Versionen von OneNote kompatibel?

A2: Aspose.Note für Java unterstützt die Arbeit mit OneNote-Dateien, die in Microsoft OneNote 2010 und späteren Versionen erstellt wurden.

### Q3: Kann ich Bilder verschiedener Formate, wie PNG oder GIF, in ein OneNote-Dokument einfügen?

A3: Ja, Aspose.Note für Java unterstützt das Einfügen von Bildern in verschiedenen Formaten, einschließlich PNG, JPEG, GIF und mehr.

### Q4: Gibt es eine Testversion von Aspose.Note für Java zum Ausprobieren?

A4: Ja, Sie können eine kostenlose Testversion von Aspose.Note für Java von der Website für Evaluierungszwecke herunterladen.

### Q5: Wie kann ich technischen Support für Aspose.Note für Java erhalten?

A5: Sie können technischen Support für Aspose.Note für Java erhalten, indem Sie das dem Aspose.Note-Produkt gewidmete [Forum](https://forum.aspose.com/c/note/28) besuchen.

---

**Zuletzt aktualisiert:** 2025-12-21  
**Getestet mit:** Aspose.Note for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
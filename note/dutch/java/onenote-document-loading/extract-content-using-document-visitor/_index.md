---
date: 2025-12-04
description: Leer hoe je afbeeldingen uit OneNote‑bestanden kunt extraheren en OneNote
  naar tekst kunt converteren in Java met Aspose.Note. Stapsgewijze handleiding met
  codevoorbeelden.
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Afbeeldingen uit OneNote extraheren met Document Visitor - Java
url: /nl/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeeldingen extraheren uit OneNote met Document Visitor - Java

## Inleiding

Aspose.Note for Java maakt het eenvoudig om **afbeeldingen uit OneNote** notitieboeken te **extraheren** en het onderliggende `.one`-bestand in Java te lezen. In deze tutorial lopen we je stap voor stap door een volledig hands‑on voorbeeld dat laat zien hoe je een OneNote‑bestand laadt, de structuur doorloopt met een aangepaste `DocumentVisitor`, en zowel afbeeldingen als platte tekst haalt. Aan het einde weet je ook hoe je **OneNote naar tekst kunt converteren** als je alleen de tekstuele inhoud nodig hebt.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.Note for Java (downloadlink hieronder).  
- **Kan ik alleen afbeeldingen extraheren?** Ja – implementeer de `VisitImageStart`‑methode in een `DocumentVisitor`.  
- **Hoe lees ik een .one‑bestand in Java?** Gebruik `new Document(path, new LoadOptions())`.  
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist voor niet‑trial gebruik.  
- **Welke Java‑versie wordt ondersteund?** JDK 8 of hoger.

## Vereisten

Zorg ervoor dat je het volgende hebt voordat je begint:

1. Java Development Kit (JDK) 8 of nieuwer geïnstalleerd.  
2. Aspose.Note for Java‑bibliotheek gedownload. Je kunt deze **[here](https://releases.aspose.com/note/java/)** downloaden.  
3. Een OneNote‑document (`.one`‑bestand) waarvan je afbeeldingen wilt extraheren of wilt converteren naar tekst.

## Importeer pakketten

Importeer eerst de benodigde klassen van de Aspose.Note‑API.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Stap 1: Een aangepaste Document Visitor instellen

Maak een klasse die `DocumentVisitor` uitbreidt. Deze klasse wordt aangeroepen voor elke node in het OneNote‑document, waardoor je **afbeeldingen uit OneNote kunt extraheren** en optioneel tekst kunt verzamelen.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Stap 2: Visitor‑methoden implementeren

Voeg overrides toe voor de node‑typen waarin je geïnteresseerd bent. Hieronder behandelen we rich‑text, afbeeldingen, titels, pagina's, outlines en outline‑elementen. De `VisitImageStart`‑methode is waar de afbeeldingsextractie plaatsvindt.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Waarom deze methoden implementeren?

- **Afbeeldingen uit OneNote extraheren:** `VisitImageStart` geeft je directe toegang tot de ruwe afbeeldingsbytes.  
- **OneNote naar tekst converteren:** `VisitRichTextStart` verzamelt de tekstuele inhoud, waardoor een eenvoudige **convert OneNote to text**‑operatie mogelijk is.  
- **.one‑bestand lezen in Java:** Het visitor‑patroon abstraheert de onderliggende `.one`‑bestandstructuur, zodat je het binaire formaat niet zelf hoeft te parseren.

## Stap 3: Voer de Visitor uit vanuit je main‑methode

Laad het `.one`‑bestand, maak een instantie van je visitor, en start de traversatie.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Veelvoorkomende gebruikssituaties

- **Geautomatiseerde rapportage:** Haal afbeeldingen en tekst uit een OneNote‑vergadernotitieboek om een PDF‑ of HTML‑samenvatting te genereren.  
- **Inhoudsmigratie:** Converteer legacy OneNote‑archieven naar platte‑tekstbestanden voor indexering of zoekmachine‑invoer.  
- **Digitale assets extraheren:** Verzamel ingesloten screenshots, diagrammen of foto’s voor hergebruik in andere applicaties.

## Probleemoplossing & tips

- **Grote notitieboeken:** Als je geheugenproblemen ondervindt, verwerk pagina's afzonderlijk door `VisitPageStart` te controleren en paginaniveau‑resources alleen te laden wanneer nodig.  
- **Afbeeldingsformaten:** Het `Image`‑object retourneert ruwe bytes; je moet mogelijk het formaat (PNG, JPEG) detecteren voordat je opslaat.  
- **Licentiefouten:** Zorg ervoor dat je de Aspose‑licentie hebt ingesteld (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) voordat je het document in productie laadt.

## Veelgestelde vragen

**Q: Kan ik specifieke soorten inhoud uit het OneNote‑document extraheren?**  
A: Ja – door alleen de visitor‑methoden te overschrijven die je nodig hebt (bijv. `VisitImageStart` voor afbeeldingen, `VisitRichTextStart` voor tekst).

**Q: Is Aspose.Note for Java compatibel met verschillende versies van OneNote‑documenten?**  
A: Absoluut. De bibliotheek ondersteunt alle belangrijke OneNote‑bestandversies, dus je kunt veilig **read .one file Java**‑projecten uitvoeren, ongeacht de oorspronkelijke OneNote‑versie.

**Q: Kan ik dit extractieproces integreren in mijn Java‑applicatie?**  
A: Ja. Het visitor‑patroon werkt naadloos binnen elke Java‑codebase; voeg gewoon de bibliotheek‑JAR toe en roep het bovenstaande voorbeeld aan.

**Q: Biedt Aspose.Note for Java ondersteuning voor het verwerken van complexe OneNote‑documenten?**  
A: Ja. Geneste outlines, ingesloten media en aangepaste gegevens worden allemaal beschikbaar gesteld via de visitor‑API.

**Q: Is er een limiet aan de grootte van het OneNote‑document dat kan worden verwerkt?**  
A: Er is geen harde limiet, maar zeer grote notitieboeken kunnen meer heap‑geheugen vereisen; overweeg ze pagina voor pagina te verwerken.

**Q: Hoe converteer ik de geëxtraheerde tekst naar een platte‑tekstbestand?**  
A: Nadat `myConverter.GetText()` een `String` retourneert, schrijf je deze naar een bestand met standaard Java‑I/O (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Laatst bijgewerkt:** 2025-12-04  
**Getest met:** Aspose.Note for Java 24.10  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
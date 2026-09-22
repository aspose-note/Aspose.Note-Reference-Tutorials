---
date: 2026-08-18
description: Apprenez à exporter OneNote en PDF, à définir le formatage des paragraphes
  en Java et à enregistrer OneNote au format PDF à l'aide d'Aspose.Note pour Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Définir le style de paragraphe lors de la création d'un document OneNote
  en Java
og_description: Exportez OneNote en PDF et définissez le style de paragraphe en Java
  avec Aspose.Note. Suivez ce guide étape par étape pour générer des PDF soignés sans
  effort.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Exporter OneNote en PDF avec le style de paragraphe en Java (58 caractères)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Comment exporter OneNote en PDF avec le style de paragraphe en Java
url: /fr/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir le style de paragraphe lors de la création d'un document OneNote en Java

## Introduction

Exporter OneNote en PDF de manière programmatique est une exigence courante pour les moteurs de reporting, les services de prise de notes automatisés et les pipelines de conversion de documents. Dans ce tutoriel, vous apprendrez comment **exporter OneNote en PDF**, appliquer un formatage de paragraphe personnalisé et enregistrer le fichier OneNote — le tout en utilisant Aspose.Note pour Java. À la fin, vous disposerez d’un extrait Java prêt à l’emploi qui produit un PDF soigné avec l’apparence exacte que vous avez définie.

## Réponses rapides
- **Que signifie « set paragraph style » ?** Il applique la police, la taille, la couleur et d’autres attributs de formatage à un paragraphe de texte.  
- **Puis-je exporter le résultat en PDF ?** Oui – le guide se termine par l’enregistrement du fichier OneNote au format PDF.  
- **Ai-je besoin d’une licence pour Aspose.Note ?** Un essai gratuit suffit pour l’évaluation ; une licence commerciale est requise pour une utilisation en production.  
- **Quels IDE sont pris en charge ?** Tout IDE Java – Eclipse, IntelliJ IDEA, NetBeans, etc.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour un document basique.

## Comment exporter OneNote en PDF avec Java ?

`Document` représente un fichier OneNote contenant des pages, des contours et d’autres éléments. Chargez votre document OneNote avec `new Document()` (ou créez‑en un nouveau) et appelez `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note écrit le PDF en une seule passe, préservant les styles, les images et les contours sans nécessiter l’installation de Microsoft OneNote. Cette approche directe fonctionne sous Windows, Linux et macOS avec n’importe quel JDK 1.8+.

## Qu’est‑ce que « set paragraph style » dans Aspose.Note ?

`ParagraphStyle` est la classe qui stocke le nom de police, la taille, la couleur, l’alignement et d’autres paramètres typographiques pour un paragraphe. En attachant une instance de `ParagraphStyle` à un nœud `RichText`, vous contrôlez exactement l’apparence de ce paragraphe dans la page OneNote finale et le PDF exporté.

## Pourquoi exporter OneNote en PDF ?

Exporter OneNote en PDF garantit une cohérence de la marque en préservant les polices et couleurs d’entreprise, améliore la lisibilité en conservant la mise en page exacte pour l’impression ou l’archivage, et offre un accès multiplateforme afin que les destinataires puissent visualiser le document sur n’importe quel appareil sans avoir besoin de OneNote. Cela apporte également des avantages de performance, permettant de traiter rapidement de gros documents.

## Prérequis

1. **Java Development Kit (JDK) 1.8+** – tout JDK récent fonctionnera.  
2. **Aspose.Note for Java** – téléchargez le dernier JAR depuis la [page de téléchargement Aspose.Note](https://releases.aspose.com/note/java/).  
3. **Un IDE** (Eclipse, IntelliJ IDEA ou NetBeans) pour compiler et exécuter l’exemple.  

> **Astuce :** Ajoutez le JAR Aspose.Note au classpath de votre projet via Maven (`<dependency>`) ou en référencant manuellement le JAR dans votre IDE.

## Importer les packages

Tout d’abord, importez les espaces de noms requis. Ce bloc reste inchangé.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> La classe `ParagraphStyle` est la clé pour **set paragraph style** plus tard dans le tutoriel.

## Guide étape par étape

Voici un guide concis de chaque opération. Les blocs de code sont exactement comme dans l’exemple original ; nous ajoutons uniquement du texte explicatif.

### Étape 1 : définir le répertoire du document
Définissez où les fichiers générés seront enregistrés.

```java
String dataDir = "Your Document Directory";
```

Remplacez "Your Document Directory" par un chemin absolu ou relatif sur votre machine.

### Étape 2 : initialiser l’objet document
Créez le `Document` racine qui représente le fichier OneNote.

```java
Document doc = new Document();
```

**Ancre de définition :** `Document` est l’objet de niveau supérieur d’Aspose.Note qui contient une ou plusieurs pages en mémoire.

### Étape 3 : initialiser l’objet page
Un fichier OneNote se compose d’une ou plusieurs pages ; nous commençons avec une seule page.

```java
Page page = new Page();
```

**Ancre de définition :** `Page` représente une page OneNote unique, contenant des contours, des images et d’autres éléments.

### Étape 4 : initialiser l’objet contour
Les contours servent de conteneurs pour les éléments de contour (pensez-y comme des sections).

```java
Outline outline = new Outline();
```

**Ancre de définition :** `Outline` regroupe les objets `OutlineElement` liés et définit leur hiérarchie visuelle.

### Étape 5 : initialiser l’objet élément de contour
Ici nous **ajoutons un élément de contour** qui contiendra notre texte enrichi.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Ancre de définition :** `OutlineElement` est un nœud feuille à l’intérieur d’un `Outline` qui peut contenir du texte, des images ou d’autres médias.

### Étape 6 : définir le style du texte (set paragraph style)
`ParagraphStyle` définit la famille de police, la taille, la couleur et d’autres attributs typographiques pour un paragraphe.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

L’instance `ParagraphStyle` définit la police, la taille et la couleur — c’est ici que nous **set paragraph style** pour le nœud texte à venir.

### Étape 7 : initialiser l’objet texte enrichi
`RichText` est le nœud qui stocke le texte formaté au sein d’un `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Nous créons un nœud `RichText`, insérons une chaîne simple et attachons le style défini précédemment.

### Étape 8 : ajouter le nœud texte enrichi à l’élément de contour
```java
outlineElem.appendChildLast(text);
```

Le texte formaté se trouve maintenant à l’intérieur de l’élément de contour.

### Étape 9 : ajouter le nœud élément de contour au contour
```java
outline.appendChildLast(outlineElem);
```

Le contour contient maintenant l’élément qui détient notre paragraphe.

### Étape 10 : ajouter le nœud contour à la page
```java
page.appendChildLast(outline);
```

Nous plaçons le contour sur la page.

### Étape 11 : ajouter le nœud page au document
```java
doc.appendChildLast(page);
```

Le document possède maintenant une seule page avec notre texte formaté.

### Étape 12 : enregistrer le document (export OneNote PDF)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

La méthode `save` écrit le fichier OneNote et **exports OneNote to PDF** en une seule étape. Vous pouvez également enregistrer au format `.one` en utilisant `SaveFormat.One` si vous avez besoin du format natif.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **Fichier non trouvé** | `dataDir` pointe vers un dossier inexistant. | Assurez‑vous que le répertoire existe ou créez‑le programmatique (`new File(dataDir).mkdirs();`). |
| **PDF blanc** | Aucun contenu n’a été ajouté avant l’enregistrement. | Vérifiez que le nœud `RichText` est ajouté et que le style est défini. |
| **Police non prise en charge** | Le nom de police n’est pas installé sur le système. | Utilisez une police commune comme `"Arial"` ou intégrez la police dans le projet. |

## Questions fréquemment posées

**Q : Aspose.Note peut‑il gérer le formatage complexe tel que les tableaux ou les images ?**  
R : Oui, l’API prend en charge les tableaux, les images, les hyperliens et les fonctionnalités de mise en page avancées en plus du texte brut.

**Q : Est‑il possible de convertir un PDF OneNote en fichier OneNote ?**  
R : Une conversion directe n’est pas fournie, mais vous pouvez extraire le contenu du PDF et reconstruire un document OneNote à l’aide de l’API.

**Q : La bibliothèque fonctionne‑t‑elle sur les environnements Linux/macOS ?**  
R : Absolument. Aspose.Note pour Java est indépendant de la plateforme ; il suffit d’avoir un JDK compatible installé.

**Q : Comment ajouter plusieurs pages ou contours ?**  
R : Créez des objets `Page` et `Outline` supplémentaires, puis ajoutez‑les au `Document` comme dans l’exemple à page unique.

**Q : Où puis‑je trouver plus d’exemples ?**  
R : La documentation officielle d’Aspose.Note et le [forum d’assistance](https://forum.aspose.com/c/note/28) contiennent de nombreux exemples de code et scénarios réels.

## Conclusion

Vous avez maintenant vu comment **set paragraph style**, **add outline element**, et **export OneNote to PDF** avec Aspose.Note pour Java. Appliquer du texte formaté dès le départ garantit que le PDF final a un aspect professionnel, et l’opération `save` en un seul appel gère la conversion efficacement. Étendez cette base avec des images, des tableaux ou des métadonnées personnalisées pour répondre aux besoins spécifiques de votre application.

---

**Dernière mise à jour :** 2026-08-18  
**Testé avec :** Aspose.Note for Java 26.5 (dernière version)  
**Auteur :** Aspose

## Tutoriels associés

- [Comment enregistrer OneNote en PDF avec Aspose.Note pour Java](/note/java/onenote-document-loading/load-save-format/)
- [Apprendre à convertir OneNote en PDF avec Aspose.Note en utilisant PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Définir le style de paragraphe par défaut dans OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
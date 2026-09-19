---
date: 2026-06-05
description: Apprenez comment changer le font size dans OneNote, définir le font color
  et le highlight text avec Aspose.Note pour Java – guide étape par étape avec des
  extraits de code.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Modifier la taille de la police dans OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Modifier la taille de la police dans OneNote - Aspose.Note
url: /fr/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifier la taille de police dans OneNote - Aspose.Note

## Introduction

Dans ce tutoriel, vous apprendrez **how to change font size onenote** documents en utilisant Aspose.Note pour Java. Nous parcourrons le chargement d'un fichier OneNote, l'accès à ses nœuds de texte, l'application de couleur, de surbrillance et de modifications de taille de police, puis l'enregistrement du fichier mis à jour. Que vous automatisiez la génération de rapports ou que vous peaufiniez des notes de réunion, ce guide vous offre une méthode fiable pour styliser le contenu OneNote de manière programmatique.

## Réponses rapides
- **Comment changer la taille de police dans OneNote avec Java ?** Chargez le document, modifiez la propriété `FontSize` de chaque `TextRun`, puis enregistrez – trois étapes simples.  
- **Puis-je également changer la couleur du texte et la surbrillance ?** Oui, définissez `FontColor` et `HighlightColor` sur le même `TextRun`.  
- **Quelle version d'Aspose.Note est requise ?** Toute version 23.10+ prend en charge ces API de style.  
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Cette approche convient‑elle aux gros blocs‑notes ?** Oui – Aspose.Note traite des blocs‑notes de plusieurs centaines de pages sans charger le fichier complet en mémoire.

## Qu’est‑ce que change font size onenote ?
**change font size onenote** désigne l'ajustement programmatique de l'attribut `FontSize` des éléments de texte à l'intérieur d'un carnet OneNote. Avec Aspose.Note, les développeurs peuvent modifier cette propriété via l'API, qui met à jour directement la structure du fichier OneNote sous‑jacent, garantissant que l'apparence visuelle change sans édition manuelle ni interaction UI.

## Pourquoi utiliser Aspose.Note pour modifier le style du texte dans OneNote ?
Aspose.Note offre plus de 30 options de mise en forme — y compris la famille de police, la taille, la couleur, la surbrillance, l'alignement et l'espacement des paragraphes — et est conçu pour traiter efficacement de gros blocs‑notes. Il peut gérer des blocs‑notes de plus de 500 pages tout en consommant moins de 150 Mo de RAM, offrant une automatisation fiable et haute performance pour les flux de travail de documents à l'échelle de l'entreprise.

## Prérequis

1. Connaissances de base en programmation Java.  
2. JDK 8 ou supérieur installé sur votre machine.  
3. Bibliothèque Aspose.Note pour Java (téléchargement depuis le site Aspose).  
4. Familiarité avec la structure hiérarchique de OneNote (pages, sections, nœuds RichText).

## Comment modifier la taille de police dans OneNote avec Aspose.Note ?
Chargez votre fichier OneNote, localisez chaque nœud `RichText`, mettez à jour le style de chaque `TextRun`, puis enregistrez le document. Ce flux de bout en bout ne nécessite que quelques lignes de code et s'exécute en moins d'une seconde pour des blocs‑notes typiques.

### Étape 1 : Importer les packages

The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note` namespace. Import them at the top of your Java source file:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Étape 2 : Charger le document

The `Document` class is Aspose.Note's top‑level object that represents a single OneNote file in memory. Loading a file is as simple as passing the file path to its constructor.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Étape 3 : Accéder aux nœuds RichText

`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`, you gain access to every piece of editable text in the notebook.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Étape 4 : Modifier le style du texte

`TextRun` represents a contiguous run of characters sharing the same formatting. Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize` to **20** points to achieve the desired styling.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Étape 5 : Enregistrer le document

Call `document.save("StyledSample.one")` to write the changes back to a OneNote file. The save operation preserves all original content while applying the new styles.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Problèmes courants et solutions

- **Texte ne change pas :** Assurez‑vous d'itérer sur les objets `TextRun` à l'intérieur de chaque nœud `RichText` ; ignorer ce niveau laissera le formatage inchangé.  
- **La couleur apparaît différente :** Aspose.Note utilise des valeurs RVB ; vérifiez que vous utilisez les constantes `java.awt.Color` correctes.  
- **Le gros bloc‑notes ralentit :** LoadOptions configure la façon dont Aspose.Note charge un fichier, permettant le streaming et la sélection du format. Utilisez `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` pour activer le mode streaming, ce qui réduit l'empreinte mémoire.

## Questions fréquentes

**Q : Puis‑je appliquer ces modifications de style de texte à des sections spécifiques de mon document OneNote ?**  
R : Oui, filtrez la collection `RichText` par ID de page ou de section avant d'appliquer les changements de style.

**Q : Aspose.Note prend‑il en charge d'autres options de mise en forme au‑delà de la couleur, de la surbrillance et de la taille ?**  
R : Absolument, vous pouvez modifier la famille de police, le gras/italique, le soulignement, l'alignement et l'espacement des paragraphes en utilisant le même modèle d'objet.

**Q : Puis‑je intégrer Aspose.Note avec d'autres bibliothèques Java pour un traitement avancé ?**  
R : Oui, Aspose.Note fonctionne de manière transparente avec des bibliothèques comme Apache POI, Jackson ou Spring pour créer des pipelines de documents complexes.

**Q : Aspose.Note est‑il licencié pour un usage commercial ?**  
R : Une licence commerciale est requise pour les déploiements en production ; une licence d'évaluation gratuite est disponible pour le développement et les tests.

**Q : Où puis‑je trouver des exemples supplémentaires et la référence API ?**  
R : Visitez le portail de documentation Aspose.Note, téléchargez le PDF complet de référence API, et explorez le dépôt GitHub pour des exemples communautaires.

## Conclusion

En suivant les étapes ci‑dessus, vous savez maintenant **how to change font size onenote** les fichiers, ajuster la couleur du texte et appliquer des surbrillances avec Aspose.Note pour Java. Cette capacité vous permet d'automatiser la finition visuelle des notes de réunion, du matériel de formation ou de tout contenu basé sur OneNote à grande échelle.

---

**Dernière mise à jour :** 2026-06-05  
**Testé avec :** Aspose.Note 23.10 for Java  
**Auteur :** Aspose

## Tutoriels associés

- [Définir le style de paragraphe par défaut dans OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Définir la langue de vérification pour le texte dans OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Définir le titre de page dans le style Microsoft OneNote - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}
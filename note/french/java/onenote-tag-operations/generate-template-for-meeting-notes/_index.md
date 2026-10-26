---
date: 2026-10-26
description: Découvrez comment ajouter des cases à cocher OneNote lors de la génération
  d'un modèle de notes de réunion avec Aspose.Note for Java, et personnaliser facilement
  le font style OneNote.
keywords:
- add checkboxes onenote
- generate meeting notes template
- customize font style onenote
- create outline onenote
lastmod: 2026-10-26
linktitle: Générer un modèle de notes de réunion avec Aspose.Note for Java – Créer
  un plan dans OneNote
og_description: Découvrez comment ajouter des cases à cocher OneNote lors de la génération
  d'un modèle de notes de réunion avec Aspose.Note for Java, et personnaliser facilement
  le font style OneNote.
og_image_alt: 'Developer guide: add checkboxes onenote and generate meeting notes
  template using Aspose.Note for Java'
og_title: Ajouter des cases à cocher OneNote et créer un modèle de notes en Java
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to add checkboxes onenote while generating a meeting notes
    template with Aspose.Note for Java, and customize font style onenote easily.
  headline: Add checkboxes onenote and create notes template in Java
  type: TechArticle
- questions:
  - answer: You can create a bulleted list and manually mark items, but using `NoteCheckBox`
      provides interactive checkboxes that sync with OneNote’s UI.
    question: How do I add a checklist to OneNote without using checkboxes?
  - answer: Absolutely. Just change the date formatting or pass a custom title string
      to reuse the same structure for each week.
    question: Can I use this template to create a meeting agenda template for weekly
      repeats?
  - answer: Define `ParagraphStyle` objects with your corporate font name, size, and
      color, then apply them to each `RichText` element as shown in Step 1.
    question: What is the best way to customize font style onenote for branding?
  - answer: Yes. After saving the OneNote file, you can load it with Aspose.Note and
      export to PDF using `Document.save("output.pdf", SaveFormat.Pdf)`.
    question: Does Aspose.Note support exporting the outline to PDF?
  - answer: You can set the checkbox state by adding a `NoteCheckBox` tag with the
      `Checked` property set to `true`.
    question: Is there a way to programmatically mark a checkbox as completed?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java
- meeting notes template
- checkboxes
title: Ajouter des cases à cocher OneNote et créer un modèle de notes en Java
url: /fr/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter des cases à cocher onenote et créer un modèle de notes en Java

## Introduction
Dans les environnements collaboratifs modernes, **add checkboxes onenote** rapidement et générez un modèle de notes de réunion soigné sans mise en forme manuelle. Aspose.Note for Java vous donne un contrôle complet sur les titres de page, les structures hiérarchiques, le style de police et les cases à cocher interactives, vous permettant de produire un ordre du jour réutilisable en quelques secondes. Ce guide vous accompagne à chaque étape — de l’importation des classes requises à l’enregistrement du fichier OneNote final—afin que vous puissiez vous concentrer sur le contenu de la réunion, et non sur les tâches fastidieuses d’interface.

## Réponses rapides
- **What does “add checkboxes onenote” mean?** Cela signifie insérer programmétiquement des cases à cocher interactives dans une structure OneNote, exactement comme le fait l’interface utilisateur.  
- **Which library helps with this?** Aspose.Note for Java fournit l’API complète.  
- **Can I add checkboxes to the outline?** Oui – utilisez `NoteCheckBox.createBlueCheckBox()` ou d’autres variantes de couleur.  
- **Do I need a license?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **What Java version is supported?** Java 8 et versions ultérieures.

## Qu'est-ce que add checkboxes onenote ?
L’ajout de cases à cocher onenote insère une balise `NoteCheckBox` dans un élément `RichText`, transformant une ligne de texte ordinaire en une case à cocher interactive que les utilisateurs peuvent cocher ou décocher directement dans l’interface OneNote, tout en conservant l’état de la case sur tous les appareils.

## Pourquoi utiliser Aspose.Note pour générer un modèle de notes de réunion ?
Aspose.Note traite **plus de 50 formats d’entrée et de sortie** et peut gérer des pages contenant **jusqu’à 500 lignes** sans charger le document complet en mémoire, offrant ainsi une génération rapide et économique en mémoire de grands ordres du jour. Il propose également une API fluide pour le style, prend en charge les caractères Unicode et s’intègre parfaitement à d’autres bibliothèques Aspose, ce qui le rend idéal pour les flux de documentation de réunions à l’échelle de l’entreprise.

## Prérequis
- Bonne compréhension de la programmation Java.  
- Bibliothèque Aspose.Note for Java installée. Vous pouvez **download Aspose.Note for Java** depuis la page officielle de publication : [Aspose.Note for Java release page](https://releases.aspose.com/note/java/).  
- Un IDE tel qu’Eclipse ou IntelliJ IDEA.  

## Importer les packages
Les classes `Document`, `Outline`, `ParagraphStyle`, `RichText` et `NoteCheckBox` sont les blocs de construction essentiels.  

`Document` représente le fichier OneNote complet en mémoire, permettant d’ajouter ou de modifier des pages et du contenu.  
`Outline` modélise la structure hiérarchique affichée dans OneNote, permettant des puces et une numérotation imbriquées.  
`ParagraphStyle` définit des attributs de police et de paragraphe réutilisables pouvant être appliqués à plusieurs éléments `RichText`.  
`RichText` contient le texte réel d’un paragraphe et peut inclure des balises comme `NoteCheckBox`.  
`NoteCheckBox` crée une balise de case à cocher interactive pouvant être attachée à un paragraphe `RichText`.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Étape 1 : créer la structure du document
Tout d’abord, créez une instance de `Document`, définissez un titre de page et créez deux objets `ParagraphStyle` réutilisables — un pour les titres et un pour le corps du texte.  

Les objets `ParagraphStyle` vous permettent d’appliquer la même famille de police, taille et couleur à plusieurs paragraphes sans répéter le code.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Ce que nous avons fait :*  
- Défini `headerStyle` pour les titres et `bodyStyle` pour le texte normal.  
- Créé un `Document` et ajouté un `Title` incluant la date du jour, donnant à la page un titre clair.

## Étape 2 : structurer les points importants
Ensuite, ajoutez un objet `Outline` à la page et remplissez‑le avec des sections telles que « Agenda », « Discussion Items » et « Action Items ».  

L’objet `Outline` représente la liste hiérarchique que vous voyez dans OneNote. En utilisant `createListNumberingStyle` nous générons une liste numérotée qui peut être redémarrée pour chaque nouvelle section.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Pourquoi c'est important :*  
- La hiérarchie de l’outline reflète la structure manuelle que vous taperiez dans OneNote, garantissant la cohérence sur toutes les pages générées.  
- Les styles de numérotation maintiennent chaque section d’ordre du jour ordonnée et facile à suivre.

## Étape 3 : mettre en évidence les actions (comment ajouter des cases à cocher)
Les actions nécessitent un repère visuel. En attachant une balise `NoteCheckBox` à chaque élément `RichText`, vous activez **add checkboxes onenote** directement dans l’outline.  

`NoteCheckBox.createBlueCheckBox()` crée une case à cocher bleue ; d’autres couleurs sont disponibles pour le branding.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Astuce :* Utilisez `NoteCheckBox.createBlueCheckBox()` pour une case à cocher bleue ; d’autres couleurs sont disponibles si vous avez besoin d’un style visuel différent.

## Étape 4 : personnaliser le style de police onenote
Pour que les notes de réunion respectent votre identité visuelle, appliquez les objets `ParagraphStyle` définis précédemment à chaque élément `RichText`.  

Définir les propriétés `FontName`, `FontSize` et `FontColor` garantit que la page générée correspond à votre guide de style corporate.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Étape 5 : enregistrer le document
Enfin, écrivez le fichier OneNote sur le disque. Le fichier peut être ouvert directement dans l’application de bureau OneNote, et vous pouvez également le convertir en PDF ultérieurement si besoin.

*Réponse directe :* Appelez `document.save("MeetingTemplate.one")` — l’API écrit un fichier OneNote entièrement compatible qui s’ouvre instantanément dans le client OneNote.

## Problèmes courants et solutions
| Problème | Solution |
|----------|----------|
| **Checkboxes not appearing** | Assurez‑vous d’avoir appelé `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` après avoir défini le style du paragraphe. |
| **Fonts look different in OneNote** | Vérifiez que le nom de police (par ex., « Calibri ») est installé sur la machine où OneNote ouvre le fichier. |
| **Outline not indented** | Ajustez `setVerticalOffset` et `setHorizontalOffset` sur l’objet `Outline`. |
| **Numbering restarts unexpectedly** | Utilisez correctement le `restartFlag` ; réglez‑le sur `true` uniquement pour la première liste d’une nouvelle section. |

## Questions fréquemment posées
### Comment ajouter des cases à cocher onenote ?
Chargez un élément `RichText`, puis appelez `richText.getTags().add(NoteCheckBox.createBlueCheckBox())`. La balise transforme la ligne en une case à cocher interactive que les utilisateurs peuvent cocher dans OneNote.

### Puis-je personnaliser les styles de police dans mes notes de réunion ?
Oui. Créez des objets `ParagraphStyle` avec le `FontName`, `FontSize` et `FontColor` souhaités, puis affectez‑les à chaque élément `RichText` comme illustré à l’Étape 1.

### Aspose.Note est‑il compatible avec d’autres bibliothèques Java ?
Aspose.Note fonctionne avec les autres produits Aspose (PDF, Cells, Slides) ainsi qu’avec les bibliothèques Java standards, vous permettant de chaîner des opérations comme la conversion du fichier OneNote généré en PDF.

### Comment ajouter des sections supplémentaires à mes notes de réunion ?
Réutilisez le même schéma : créez un nouveau nœud `Outline`, appliquez un `ParagraphStyle` et, éventuellement, ajoutez des cases à cocher. L’API est entièrement réutilisable pour n’importe quel nombre de sections.

### Existe‑t‑il des considérations de licence pour Aspose.Note ?
Consultez la [documentation Aspose.Note](https://reference.aspose.com/note/java/) pour les détails complets sur la licence. Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour les déploiements en production.

### Une version d’essai d’Aspose.Note est‑elle disponible ?
Oui, vous pouvez accéder à la **page de téléchargement d’essai gratuit d’Aspose.Note** : [Aspose.Note trial download page](https://releases.aspose.com/).

## FAQ
**Q : Comment ajouter une checklist à OneNote sans utiliser de cases à cocher ?**  
R : Vous pouvez créer une liste à puces et marquer manuellement les éléments, mais `NoteCheckBox` fournit des cases interactives qui se synchronisent avec l’interface de OneNote.

**Q : Puis‑je utiliser ce modèle pour créer un agenda de réunion récurrent chaque semaine ?**  
R : Absolument. Il suffit de modifier le format de date ou de passer une chaîne de titre personnalisée pour réutiliser la même structure chaque semaine.

**Q : Quelle est la meilleure façon de personnaliser le style de police onenote pour le branding ?**  
R : Définissez des objets `ParagraphStyle` avec le nom, la taille et la couleur de police de votre entreprise, puis appliquez‑les à chaque élément `RichText` comme montré à l’Étape 1.

**Q : Aspose.Note prend‑il en charge l’exportation de l’outline vers PDF ?**  
R : Oui. Après avoir enregistré le fichier OneNote, vous pouvez le charger avec Aspose.Note et l’exporter en PDF via `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q : Existe‑t‑il un moyen de marquer programmétiquement une case à cocher comme terminée ?**  
R : Vous pouvez définir l’état de la case en ajoutant une balise `NoteCheckBox` avec la propriété `Checked` définie sur `true`.

---

**Last Updated:** 2026-10-26  
**Tested With:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## Tutoriels associés

- [Ajouter des balises à OneNote – Créer un document OneNote balisé avec Aspose.Note](/note/java/onenote-tag-operations/)
- [Comment personnaliser les styles OneNote avec Aspose.Note for Java](/note/java/onenote-styles/)
- [Créer un document OneNote Java – Tutoriel Aspose Note Java](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
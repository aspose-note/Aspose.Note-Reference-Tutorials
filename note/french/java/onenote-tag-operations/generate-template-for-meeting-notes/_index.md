---
date: 2026-03-03
description: Apprenez à créer un plan dans OneNote et à générer un modèle de notes
  de réunion avec Aspose.Note pour Java. Personnalisez le style de police et ajoutez
  facilement des cases à cocher.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: Créer un plan dans OneNote – Modèle de notes de réunion
url: /fr/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un plan dans OneNote – Modèle de notes de réunion

## Introduction
Dans le monde actuel au rythme rapide, **créer un plan dans OneNote** de manière efficace est essentiel pour une documentation claire des réunions. Aspose.Note for Java offre un moyen puissant de **générer un modèle de notes de réunion** que vous pouvez personnaliser, ajouter des cases à cocher et styliser les polices exactement comme vous le souhaitez. Dans ce guide étape par étape, nous allons construire un modèle d'ordre du jour réutilisable, en expliquant **comment ajouter des cases à cocher**, **ajouter une liste de contrôle à OneNote**, et **personnaliser le style de police onenote** pour un rendu soigné.

## Réponses rapides
- **Que signifie « créer un plan dans OneNote » ?** Cela signifie créer de manière programmatique une structure hiérarchique (titres, sections, puces) à l'intérieur d'un fichier OneNote.  
- **Quelle bibliothèque aide à cela ?** Aspose.Note for Java.  
- **Puis‑je ajouter des cases à cocher au plan ?** Oui – utilisez `NoteCheckBox.createBlueCheckBox()`.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit est disponible ; une licence commerciale est requise pour la production.  
- **Quelle version de Java est prise en charge ?** Java 8 et ultérieure.

## Qu’est‑ce que « créer un plan dans OneNote » ?
Créer un plan dans OneNote signifie définir une page avec un titre, plusieurs sections de plan, et éventuellement une numérotation de liste ou des cases à cocher. Cette structure reflète la façon dont vous taperiez manuellement des titres et des puces dans l'interface OneNote, mais elle est générée automatiquement par le code.

## Pourquoi utiliser Aspose.Note pour les modèles d'ordre du jour ?
- **Cohérence :** Chaque réunion commence avec la même mise en page épurée.  
- **Automatisation :** Réduisez la saisie manuelle et assurez‑vous que toutes les sections requises (ordre du jour, actions, notes) sont présentes.  
- **Personnalisation :** Modifiez les polices, les couleurs et ajoutez des cases à cocher interactives pour suivre les tâches.  
- **Intégration :** Fonctionne avec n'importe quel IDE Java et peut être combiné avec d'autres bibliothèques Aspose pour les PDF, les feuilles de calcul, etc.

## Prérequis
- Compréhension de base de la programmation Java.  
- Bibliothèque Aspose.Note for Java installée. Vous pouvez la télécharger [ici](https://releases.aspose.com/note/java/).  
- Un IDE tel qu'Eclipse ou IntelliJ IDEA.  

## Importer les packages
Tout d'abord, importez les classes dont nous aurons besoin. Cet extrait reste exactement le même que dans le tutoriel original.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Étape 1 : Créer la structure du document
Nous commençons par construire le document, définir un titre et préparer les styles de paragraphe qui nous aideront plus tard à **personnaliser le style de police onenote**.

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
- Défini deux objets `ParagraphStyle` (`headerStyle` pour les titres, `bodyStyle` pour le texte normal).  
- Créé un `Document` et ajouté un `Title` incluant la date actuelle, donnant à la page un en‑tête clair.

## Étape 2 : Structurer les points importants
Ensuite, nous **créons un plan dans OneNote** en ajoutant un objet `Outline` et en le remplissant avec des sections telles que « Important ». C’est ici que résident les éléments de l’ordre du jour.

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

*Pourquoi c’est important :*
- L'objet `Outline` représente la liste hiérarchique que vous voyez dans OneNote.  
- En utilisant `createListNumberingStyle`, nous générons une liste numérotée qui peut être redémarrée pour chaque nouvelle section.

## Étape 3 : Mettre en évidence les actions (Comment ajouter des cases à cocher)
Les éléments d'action nécessitent un repère visuel. En attachant une balise de case à cocher à chaque élément `RichText`, nous permettons **comment ajouter des cases à cocher** directement dans le plan.

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

## Étape 4 : Enregistrer le document
Enfin, écrivez le fichier OneNote sur le disque. Le fichier peut être ouvert directement dans l'application de bureau OneNote.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Problèmes courants et solutions
| Problème | Solution |
|----------|----------|
| **Les cases à cocher n’apparaissent pas** | Assurez‑vous d’avoir appelé `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` après avoir défini le style de paragraphe. |
| **Les polices apparaissent différemment dans OneNote** | Vérifiez que le nom de la police (par ex., « Calibri ») est installé sur la machine où OneNote ouvre le fichier. |
| **Le plan n’est pas indenté** | Ajustez `setVerticalOffset` et `setHorizontalOffset` sur l’objet `Outline`. |
| **La numérotation redémarre de façon inattendue** | Utilisez correctement le `restartFlag` ; définissez‑le à `true` uniquement pour la première liste d’une nouvelle section. |

## Questions fréquemment posées
### Puis‑je personnaliser les styles de police dans mes notes de réunion ?
Oui, Aspose.Note vous permet de définir des styles de police personnalisés pour les en‑têtes et le texte principal.

### Aspose.Note est‑il compatible avec d’autres bibliothèques Java ?
Aspose.Note peut être intégré de façon transparente avec d’autres bibliothèques Java pour des fonctionnalités étendues.

### Comment ajouter des sections supplémentaires à mes notes de réunion ?
Vous pouvez facilement étendre la structure du plan en suivant le même modèle présenté dans le tutoriel.

### Existe‑t‑il des considérations de licence pour Aspose.Note ?
Consultez la [documentation Aspose.Note](https://reference.aspose.com/note/java/) pour les détails de licence.

### Une version d’essai d’Aspose.Note est‑elle disponible ?
Oui, vous pouvez accéder à l’[essai gratuit ici](https://releases.aspose.com/).

## FAQ
**Q : Comment ajouter une liste de contrôle à OneNote sans utiliser de cases à cocher ?**  
R : Vous pouvez créer une liste à puces et marquer manuellement les éléments, mais l’utilisation de `NoteCheckBox` fournit des cases à cocher interactives qui se synchronisent avec l’interface de OneNote.

**Q : Puis‑je utiliser ce modèle pour créer un modèle d’ordre du jour de réunion récurrent chaque semaine ?**  
R : Absolument. Il suffit de modifier le format de la date ou de passer une chaîne de titre personnalisée pour réutiliser la même structure chaque semaine.

**Q : Quelle est la meilleure façon de **personnaliser le style de police onenote** pour le branding ?**  
R : Définissez des objets `ParagraphStyle` avec le nom, la taille et la couleur de votre police d’entreprise, puis appliquez‑les à chaque élément `RichText` comme montré à l’étape 1.

**Q : Aspose.Note prend‑il en charge l’exportation du plan au format PDF ?**  
R : Oui. Après avoir enregistré le fichier OneNote, vous pouvez le charger avec Aspose.Note et l’exporter en PDF en utilisant `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q : Existe‑t‑il un moyen de marquer programmétiquement une case à cocher comme terminée ?**  
R : Vous pouvez définir l’état de la case à cocher en ajoutant une balise `NoteCheckBox` avec la propriété `Checked` définie sur `true`.

**Dernière mise à jour :** 2026-03-03  
**Testé avec :** Aspose.Note for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
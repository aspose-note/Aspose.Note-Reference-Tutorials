---
date: 2026-01-18
description: Apprenez comment définir la couleur de police Java dans OneNote à l’aide
  d’Aspose.Note, mettre en surbrillance le texte, modifier la taille de la police
  et enregistrer OneNote au format PDF. Guide étape par étape avec du code.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Définir la couleur de la police Java dans OneNote – Aspose.Note
url: /fr/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la couleur de police Java dans OneNote – Aspose.Note

## Introduction

Dans ce tutoriel, vous découvrirez comment **set font color Java** pour le texte à l'intérieur d'un document OneNote avec l'API Aspose.Note for Java. Nous parcourrons le chargement d'un fichier `.one`, l'accès à ses nœuds RichText, l'application de changements de couleur, de surbrillance et de taille de police, et enfin **saving OneNote as PDF**. Que vous ayez besoin de **highlight text onenote**, **modify font size onenote**, ou simplement de modifier le style global du texte, les étapes ci‑dessous vous offrent une solution complète prête pour la production.

## Réponses rapides
- **Can I change the font color of specific words?** Oui – parcourez les objets `TextRun` et appelez `setFontColor`.
- **Does Aspose.Note let me save OneNote as PDF?** Absolument ; utilisez `document.save("output.pdf")`.
- **What Java version is required?** Java 8 ou version supérieure.
- **Is highlighting supported?** Utilisez `setHighlight(Color)` sur le `TextStyle`.
- **Can I convert OneNote to PDF in one line?** Pas directement, mais la méthode `save` gère la conversion.

## Qu’est‑ce que “set font color java” ?

L'expression fait référence à l'attribution programmatique d'une nouvelle couleur de police aux éléments de texte d'un fichier OneNote à l'aide de code Java. Avec Aspose.Note, vous obtenez un contrôle complet sur les attributs de style tels que la couleur de police, la surbrillance et la taille, sans ouvrir l'interface OneNote.

## Pourquoi changer le style du texte onenote ?

- **Lisibilité améliorée** – le texte coloré ou surligné attire l'attention sur les points clés.
- **Cohérence de la marque** – appliquer les couleurs d'entreprise à travers les notes de réunion.
- **Qualité d'exportation** – les notes stylisées ont un aspect soigné lorsque vous **convert onenote to pdf** pour le partage.

## Prérequis

1. Connaissances de base en programmation Java.  
2. JDK 8 ou version plus récente installé.  
3. Bibliothèque Aspose.Note for Java ajoutée à votre projet (Maven/Gradle ou JAR manuel).  
4. Un fichier OneNote d'exemple (`Sample1.one`) pour expérimenter.

## Importer les packages

Tout d'abord, importez les classes dont nous aurons besoin :

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Guide étape par étape

### Étape 1 : Charger le document

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Nous chargeons le fichier OneNote (`Sample1.one`) afin qu'Aspose.Note puisse travailler avec sa structure interne.

### Étape 2 : Accéder aux nœuds RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Les objets `RichText` contiennent les paragraphes réels. En récupérant le premier nœud, nous obtenons une référence au texte que nous voulons styliser.

### Étape 3 : Modifier le style du texte (set font color java)

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

À l'intérieur de la boucle, nous **set font color Java** en jaune, appliquons une surbrillance bleue (démontrant **highlight text onenote**), et augmentons la taille à 20 points, illustrant **modify font size onenote**.

### Étape 4 : Enregistrer le document (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Appeler `save` avec une extension `.pdf` convertit automatiquement **convert onenote to pdf**, vous fournissant un fichier prêt à être partagé.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| Aucun changement de couleur visible | Le document était ouvert dans OneNote avant l'enregistrement | Fermez OneNote ou rechargez le fichier après la fin du processus Java |
| Surbrillance non appliquée | Utilisation d'une couleur qui correspond à l'arrière‑plan | Choisissez une `Color` contrastante (par ex., `Color.yellow`) |
| `document.save` lance `IOException` | Chemin de sortie invalide | Assurez‑vous que le répertoire existe et que vous avez les permissions d'écriture |

## Questions fréquentes

**Q : Puis‑je appliquer ces changements de style uniquement à certaines sections de mon fichier OneNote ?**  
R : Oui – filtrez les nœuds `RichText` par leur parent `Section` ou `Page` avant d'itérer sur les `TextRun`s.

**Q : En plus de la couleur, de la surbrillance et de la taille, quels autres formats Aspose.Note peut‑il gérer ?**  
R : Vous pouvez modifier la famille de police, le gras/italique/souligné, l'alignement, et même l'espacement des paragraphes.

**Q : Est‑il possible de traiter par lots plusieurs fichiers OneNote ?**  
R : Absolument. Enveloppez la logique de chargement et de style dans une boucle qui traite chaque fichier `.one` d'un dossier.

**Q : La bibliothèque prend‑elle en charge l'enregistrement direct vers d'autres formats comme DOCX ?**  
R : Oui – Aspose.Note peut exporter vers PDF, DOCX, HTML et plusieurs formats d'image.

**Q : Où puis‑je trouver plus d'exemples et la référence API ?**  
R : Visitez le site officiel de documentation Aspose.Note, explorez la référence API, et téléchargez la version d'essai gratuite pour des tests pratiques.

## Conclusion

Vous disposez maintenant d'un exemple complet, de bout en bout, montrant comment **set font color Java**, surligner du texte, ajuster la taille de police, et **save OneNote as PDF** avec Aspose.Note. N'hésitez pas à adapter le code pour cibler des pages spécifiques, appliquer un style conditionnel, ou l'intégrer dans des pipelines de traitement de documents plus vastes.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-01-18  
**Testé avec :** Aspose.Note 24.11 for Java  
**Auteur :** Aspose
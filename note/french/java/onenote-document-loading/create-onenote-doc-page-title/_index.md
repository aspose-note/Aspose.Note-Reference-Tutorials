---
date: 2025-12-02
description: Apprenez à créer une page OneNote avec un titre en Java en utilisant
  Aspose.Note pour Java. Ce guide montre comment définir le titre d’une page OneNote
  et personnaliser la police du titre.
language: fr
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Comment créer une page OneNote avec titre - Java
url: /java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer une page OneNote avec titre - Java

## Introduction

Si vous devez **créer une page OneNote** programmatique, Aspose.Note for Java rend cela simple. Dans ce tutoriel, vous apprendrez à générer un fichier OneNote, à définir le titre de la page, et même à personnaliser la police du titre — le tout depuis du code Java. À la fin, vous disposerez d’un document OneNote prêt à l’emploi que vous pourrez intégrer à n’importe quelle application Java.

## Réponses rapides
- **Quelle bibliothèque est requise ?** Aspose.Note for Java.
- **Puis-je définir une police personnalisée pour le titre ?** Oui – utilisez `ParagraphStyle` pour définir le nom, la taille et la couleur de la police.
- **Quelle version de Java est prise en charge ?** Tout JDK 8+ (l’API est rétrocompatible).
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise en production.
- **Où le résultat est‑il enregistré ?** Vous définissez le chemin dans la variable `dataDir`.

## Qu’est‑ce qu’un titre de page OneNote ?
Un titre de page OneNote est l’en‑tête affiché en haut de chaque page. Il comprend généralement le nom de la page, la date de création et l’heure. Définir ce titre de façon programmatique vous aide à créer des carnets de notes cohérents et bien structurés.

## Pourquoi définir le titre d’une page OneNote programmatique ?
- **Automatisation :** Générer des rapports ou des notes de réunion sans édition manuelle.  
- **Cohérence :** Appliquer une convention de nommage sur toutes les pages.  
- **Intégration :** Combiner OneNote avec d’autres systèmes (par ex., CRM, outils de gestion de projet).  

## Prérequis

- **Java Development Kit (JDK)** – version 8 ou supérieure.  
- **Aspose.Note for Java** – téléchargez depuis le site officiel **[ici](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA, Eclipse ou NetBeans (au choix).

## Importer les packages

Tout d’abord, importez les classes dont nous aurons besoin depuis la bibliothèque Aspose.Note.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Étape 1 : Configurer le répertoire du document  
Définissez l’endroit où le fichier OneNote généré sera enregistré.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Étape 2 : Créer l’objet Document  
Instanciez un nouveau `Document` – il représente le fichier OneNote que vous allez créer.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Étape 3 : Initialiser l’objet Page  
Créez un objet `Page` qui contiendra le titre et tout le contenu.

```java
// Initialize Page class object
Page page = new Page();
```

### Étape 4 : Définir le style de texte par défaut  
Définissez un `ParagraphStyle` par défaut qui sera appliqué au texte du titre. C’est ici que nous **personnalisons la police du titre OneNote**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Étape 5 : Définir les propriétés du titre de la page  
Ici nous **définissons les détails du titre de la page OneNote** – le texte du titre, la date et l’heure. N’hésitez pas à modifier les chaînes pour correspondre à votre cas d’utilisation.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Étape 6 : Assigner le titre à la page  
Maintenant nous **ajoutons le titre à OneNote** en liant l’objet `Title` à la `Page`.

```java
page.setTitle(title);
```

### Étape 7 : Ajouter la page au document  
Ajoutez la page configurée à la structure du document.

```java
doc.appendChildLast(page);
```

### Étape 8 : Enregistrer le document OneNote  
Spécifiez le nom du fichier de sortie et enregistrez le bloc‑note. Cela complète le processus de **création de fichier OneNote en Java**.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Problèmes courants et astuces

| Problème | Solution |
|----------|----------|
| **Chemin de fichier invalide** | Assurez‑vous que `dataDir` se termine par un séparateur correct (`/` ou `\\`) et que le dossier existe. |
| **Titre non visible** | Vérifiez que le `ParagraphStyle` est appliqué à chaque élément `RichText`. |
| **Exception de licence** | Utilisez une licence d’essai pour les tests ; appliquez une licence complète avant le déploiement. |
| **La date indique le mauvais mois** | Les mois en Java sont indexés à zéro ; `cal.set(2018, 04, 03)` définit en fait mai. Ajustez en conséquence. |

## Questions fréquemment posées

**Q : Aspose.Note for Java est‑il compatible avec différentes versions de Java ?**  
R : Oui, la bibliothèque fonctionne avec Java 8 et les versions ultérieures, vous offrant ainsi une grande flexibilité.

**Q : Puis‑je personnaliser le style et la taille de la police du titre de la page ?**  
R : Absolument ! Utilisez `ParagraphStyle` (comme montré à l’étape 4) pour définir n’importe quel nom de police, taille et couleur.

**Q : Comment ajouter plus de contenu (par ex., paragraphes, images) à la page ?**  
R : Créez des objets supplémentaires `RichText` ou `Image`, définissez leurs styles, puis ajoutez‑les à la `Page` avec `page.appendChildLast(votreObjet)`.

**Q : Existe‑t‑il une version d’essai disponible pour Aspose.Note for Java ?**  
R : Oui, vous pouvez télécharger une version d’essai gratuite depuis le site Aspose pour évaluer toutes les fonctionnalités.

**Q : Où puis‑je obtenir de l’aide si je rencontre des problèmes ?**  
R : Consultez le [forum Aspose.Note](https://forum.aspose.com/c/note/28) pour obtenir de l’aide de la communauté ou ouvrez un ticket de support auprès d’Aspose.

**Dernière mise à jour :** 2025-12-02  
**Testé avec :** Aspose.Note for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
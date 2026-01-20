---
date: 2026-01-20
description: Apprenez à définir le style de paragraphe par défaut dans OneNote en
  utilisant Aspise.Note pour Java, et ajoutez la police par défaut à OneNote avec
  une police de paragraphe personnalisée.
linktitle: Set Default Paragraph Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Définir le style de paragraphe par défaut dans OneNote - Aspose.Note
url: /fr/java/onenote-styles/set-default-paragraph-style/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir le style de paragraphe par défaut dans OneNote - Aspose.Note

## Introduction

Dans ce tutoriel, vous apprendrez **comment définir le style de paragraphe par défaut** dans OneNote de manière programmatique avec Aspose.Note pour Java. Appliquer un style par défaut vous permet d'ajouter une police par défaut aux pages OneNote et de personnaliser la police des paragraphes sur l'ensemble d'un document, vous évitant ainsi de répéter le code de mise en forme pour chaque paragraphe.

## Quick Answers
- **Que fait « définir le style de paragraphe par défaut » ?** Il définit un modèle de mise en forme au niveau du paragraphe que chaque nouveau paragraphe hérite, sauf si vous le remplacez.  
- **Quelle bibliothèque est requise ?** Aspose.Note pour Java.  
- **Ai‑je besoin d’une licence ?** Une version d'essai gratuite suffit pour l'évaluation ; une licence commerciale est requise pour la production.  
- **Quelles sont les principales étapes ?** Initialiser le document, définir un `ParagraphStyle`, l'appliquer à `RichText` et enregistrer le fichier OneNote.  
- **Puis‑je changer la police plus tard ?** Oui – vous pouvez modifier le style ou appliquer un `TextStyle` différent aux portions individuelles.  

## Qu’est‑ce que « définir le style de paragraphe par défaut » ?
Définir un style de paragraphe par défaut signifie créer un objet `ParagraphStyle` (nom de police, taille, couleur, etc.) et l'assigner à un élément `RichText`. Une fois attaché, chaque ligne à l'intérieur de ce `RichText` utilise automatiquement la mise en forme définie, sauf si un `TextStyle` spécifique la remplace.

## Pourquoi personnaliser la police des paragraphes dans OneNote ?
- **Cohérence :** garantit une apparence uniforme dans toutes les sections d’un bloc‑note.  
- **Productivité :** supprime la nécessité de formater chaque paragraphe manuellement.  
- **Image de marque :** facilite l’application des directives de style de l’entreprise.  

## Prérequis

Avant de commencer, assurez‑vous de disposer de :

1. Java Development Kit (JDK) installé sur votre système.  
2. Bibliothèque Aspose.Note pour Java – téléchargez‑la depuis la [page de téléchargement](https://releases.aspose.com/note/java/).  
3. Un IDE tel qu’Eclipse ou IntelliJ IDEA pour écrire et exécuter du code Java.

## Import Packages

First, import the necessary packages to begin coding:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Now, let's break down the example code into multiple steps:

## Step 1: Initialize Document, Page, and Outline

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Step 2: Create an Outline Element

```java
OutlineElement outlineElem = new OutlineElement();
```

## Step 3: Define Default Paragraph Style

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Step 4: Create Rich Text with Default Style

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Step 5: Append Rich Text to Outline Element

```java
outlineElem.appendChildLast(text);
```

## Step 6: Append Outline Element to Outline

```java
outline.appendChildLast(outlineElem);
```

## Step 7: Append Outline to Page

```java
page.appendChildLast(outline);
```

## Step 8: Append Page to Document

```java
document.appendChildLast(page);
```

## Step 9: Save Document

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Ce code définira le style de paragraphe par défaut dans OneNote à l’aide d’Aspose.Note pour Java.

## Common Issues and Solutions
- **Police manquante sur la machine cible :** la police doit être installée sur le système où le fichier OneNote est ouvert ; sinon, OneNote revient à une police par défaut.  
- **Erreurs de chemin :** assurez‑vous que `dataDir` pointe vers un dossier existant et accessible en écriture ; sinon, `document.save` lèvera une `IOException`.  
- **Licence non définie :** si vous exécutez cela sans licence valide, le fichier généré contiendra un filigrane.

## Conclusion

Définir un style de paragraphe par défaut dans OneNote de manière programmatique peut être réalisé efficacement avec Aspose.Note pour Java. En suivant les étapes décrites dans ce tutoriel, vous pouvez intégrer cette fonctionnalité dans vos applications Java, ajouter une police par défaut aux pages OneNote et personnaliser la police des paragraphes pour correspondre à votre image de marque ou à vos normes de documentation.

## Frequently Asked Questions

**Q1 : Puis‑je personnaliser davantage le style de paragraphe par défaut ?**  
**R1 :** Oui, vous pouvez ajuster des paramètres tels que le nom de la police, la taille, la couleur, l'alignement et l'interligne selon vos besoins.

**Q2 : Aspose.Note prend‑il en charge d’autres opérations de mise en forme du texte ?**  
**R2 :** Absolument. Aspose.Note offre un support étendu pour la manipulation de la mise en forme du texte, y compris les styles de police, les puces, les retraits, etc.

**Q3 : Aspose.Note est‑il compatible avec toutes les versions de OneNote ?**  
**R3 :** Aspose.Note est conçu pour fonctionner avec les fichiers Microsoft OneNote sur différentes versions, assurant une large compatibilité.

**Q4 : Puis‑je intégrer Aspose.Note dans mon projet Java existant ?**  
**R4 :** Oui, vous pouvez facilement ajouter Aspose.Note à votre projet en incluant les fichiers JAR ou les dépendances Maven/Gradle et en important les packages requis.

**Q5 : Existe‑t‑il une version d’essai disponible pour Aspose.Note ?**  
**R5 :** Oui, vous pouvez accéder à une version d’essai gratuite d’Aspose.Note depuis le [site web](https://releases.aspose.com/).

**Q6 : Comment modifier le style par défaut après la création du document ?**  
**R6 :** Récupérez le `ParagraphStyle` de l’objet `RichText` existant, modifiez ses propriétés et ré‑attribuez‑le, ou créez un nouveau style et appliquez‑le aux paragraphes supplémentaires.

**Q7 : Le style par défaut affectera‑t‑il les paragraphes existants dans un document chargé ?**  
**R7 :** Non. Le style par défaut ne s’applique qu’aux nouveaux paragraphes que vous ajoutez après l’avoir défini. Les paragraphes existants conservent leur mise en forme d’origine, sauf si vous les modifiez explicitement.

**Dernière mise à jour :** 2026-01-20  
**Testé avec :** Aspose.Note 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
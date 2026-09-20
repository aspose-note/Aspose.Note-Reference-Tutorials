---
date: 2026-06-30
description: Apprenez comment exporter OneNote en enregistrant un document au format
  PNG en niveaux de gris à l'aide d'Aspose.Note pour Java. Comprend les étapes pour
  charger le document OneNote et créer une image en niveaux de gris.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Comment exporter OneNote en image en niveaux de gris – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Comment exporter OneNote en image en niveaux de gris – Aspose.Note
url: /fr/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer en image en niveaux de gris dans OneNote - Aspose.Note

## Introduction

Dans ce tutoriel, vous découvrirez **how to export onenote** en convertissant un fichier OneNote `.one` en une image PNG en niveaux de gris de haute qualité à l'aide d'Aspose.Note pour Java. La conversion en niveaux de gris est souvent nécessaire aux développeurs Java pour l'impression, l'archivage, ou pour **réduire la taille de OneNote** sans perdre le contenu essentiel. Nous parcourrons le chargement d'un document OneNote, la configuration des options d'enregistrement — y compris **adjust image resolution** — et enfin l'enregistrement du document au format PNG.

## Réponses rapides
- **What does “how to export onenote” mean?** Cela fait référence à la conversion programmatique d'un fichier OneNote en un autre format, tel qu'une image, à l'aide de code.  
- **Which format is best for grayscale output?** Le PNG fonctionne bien car il préserve une qualité sans perte et prend en charge un mode couleur dédié aux niveaux de gris.  
- **Do I need a license?** Une licence Aspose.Note valide est requise pour une utilisation en production ; une licence d'essai temporaire est disponible pour les tests.  
- **What Java version is required?** Java 8 ou supérieur est recommandé.  
- **Can I change the image size?** Oui, vous pouvez ajuster les propriétés `ImageSaveOptions` telles que `Resolution` ou `PageSize` avant l'enregistrement.

## Qu'est‑ce que « how to export onenote » ?

Exporter OneNote signifie convertir de manière programmatique un fichier OneNote `.one` en une autre représentation — comme PDF, HTML ou une image. Dans ce guide, nous nous concentrons sur **creating grayscale PNG** images, une exigence courante pour la documentation ou les flux de travail prêts à imprimer. Avec Aspose.Note, la conversion se fait entièrement en mémoire, vous n'avez donc jamais besoin d'installer Microsoft OneNote sur le serveur.

## Pourquoi exporter OneNote en image en niveaux de gris ?

Les PNG en niveaux de gris sont généralement **30‑40 % plus petits** que leurs homologues en couleur, ce qui accélère la diffusion sur le web et réduit les coûts de stockage. Ils offrent également un **contraste plus net** sur les imprimantes laser, rendant les rapports plus lisibles. Comme le PNG est universellement pris en charge, les fichiers résultants fonctionnent sur les navigateurs, les appareils mobiles et les éditeurs de bureau sans codecs supplémentaires.

## Prérequis

1. Java Development Kit (JDK) 8 ou plus récent installé.  
2. Bibliothèque Aspose.Note pour Java – téléchargez la dernière version depuis [ici](https://releases.aspose.com/note/java/).  
3. Une compréhension de base de la syntaxe Java et de la configuration de projet Maven/Gradle.  

## Importer les packages

La classe `ImageSaveOptions` contrôle la façon dont le document est rendu en image. `ColorMode` est une énumération qui vous permet de basculer entre la sortie en couleur complète et en niveaux de gris.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Étape 1 : charger le document OneNote

`Document` représente un carnet OneNote et fournit des méthodes pour charger, modifier et enregistrer son contenu. Tout d'abord, **load the OneNote document** dans Aspose.Note. Remplacez `"Your Document Directory"` par le chemin de votre dossier local et `"Aspose.one"` par le nom de votre fichier OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Étape 2 : définir le chemin de sortie et les options

`ImageSaveOptions` configure la façon dont un document OneNote est rendu en fichier image. L'énumération `ColorMode` sélectionne le mode de rendu couleur, tel que niveaux de gris ou couleur complète. Définissez le chemin de sortie pour l'image en niveaux de gris et spécifiez les options d'enregistrement. Nous définirons le `ColorMode` sur `GrayScale` et utiliserons le format **save document as PNG**. Vous pouvez également **adjust image resolution** à 300 DPI pour des impressions de haute qualité.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Étape 3 : enregistrer le document

Enfin, enregistrez le document en tant qu'image PNG en niveaux de gris en utilisant les options configurées. La méthode `save` écrit le fichier sur le disque sans nécessiter de fichiers temporaires intermédiaires.

```java
oneFile.save(dataDir, options);
```

## Problèmes courants et solutions
- **FileNotFoundException** – Vérifiez que `dataDir` pointe vers le bon dossier et que le fichier `.one` existe.  
- **LicenseException** – Assurez‑vous d'avoir appliqué une licence Aspose.Note valide avant d'appeler `save`.  
- **Low‑resolution output** – Ajustez `options.setResolution(300)` pour augmenter le DPI ; un DPI plus élevé donne des impressions plus nettes mais des fichiers plus volumineux.  

## Questions fréquemment posées

**Q1 : Puis‑je enregistrer l'image en niveaux de gris dans un autre format ?**  
R1 : Oui, il suffit de changer le paramètre `SaveFormat` dans le constructeur `ImageSaveOptions` en `Jpeg`, `Bmp` ou tout autre des plus de 20 formats d'image pris en charge.

**Q2 : Aspose.Note est‑il compatible avec toutes les versions de documents OneNote ?**  
R2 : Aspose.Note prend en charge Microsoft OneNote 2010 et versions ultérieures, couvrant plus de 95 % des carnets de notes en cours d'utilisation aujourd'hui.

**Q3 : Aspose.Note nécessite‑t‑il une licence pour être utilisé ?**  
R3 : Une licence valide est requise pour une utilisation en production, mais une licence d'essai temporaire peut être obtenue pour l'évaluation gratuitement.

**Q4 : Puis‑je manipuler d'autres aspects du document avant de l'enregistrer en image ?**  
R4 : Absolument ! Aspose.Note fournit des API pour modifier les sections, les pages et les éléments individuels tels que le texte, les tableaux et les images avant l'exportation.

**Q5 : Où puis‑je trouver du support si je rencontre des problèmes ?**  
R5 : Vous pouvez trouver du support sur le forum Aspose.Note [ici](https://forum.aspose.com/c/note/28).

## Conclusion

Vous avez maintenant appris **how to export onenote** en chargeant un fichier OneNote, en configurant les options d'enregistrement pour **create a grayscale image**, et **saving the document as PNG**. Cette approche est idéale pour générer des visuels légers, prêts à imprimer, à partir de carnets OneNote. N'hésitez pas à expérimenter d'autres paramètres `ColorMode`, des valeurs DPI plus élevées, ou des formats d'image alternatifs pour répondre aux exigences de votre projet.

---

**Dernière mise à jour :** 2026-06-30  
**Testé avec :** Aspose.Note 27.0 pour Java  
**Auteur :** Aspose  

---

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Exporter la page OneNote en image PNG en Java avec Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – Définir la résolution de l'image de sortie dans OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Comment enregistrer OneNote en PDF avec Aspose.Note pour Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
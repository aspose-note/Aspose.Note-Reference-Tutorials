---
date: 2025-12-17
description: Apprenez à exporter OneNote en enregistrant un document au format PNG
  en niveaux de gris à l’aide d’Aspose.Note pour Java. Comprend les étapes pour charger
  le document OneNote et créer une image en niveaux de gris.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
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

Dans ce tutoriel, nous vous montrerons **comment exporter onenote** en enregistrant un document sous forme d'image en niveaux de gris à l'aide d'Aspose.Note pour Java. Les images en niveaux de gris sont des images monochromes qui ne contiennent que des nuances de gris, ce qui peut être utile pour l'impression, l'archivage ou la réduction de la taille du fichier. Nous parcourrons le chargement d'un document OneNote, la configuration des options d'enregistrement pour **créer une image en niveaux de gris**, et enfin **enregistrer le document au format PNG**.

## Quick Answers
- **Que signifie « how to export onenote » ?** Cela fait référence à la conversion d'un fichier OneNote en un autre format, tel qu'une image, de manière programmatique.  
- **Quel format est le meilleur pour une sortie en niveaux de gris ?** Le PNG fonctionne bien car il préserve une qualité sans perte et prend en charge le mode couleur en niveaux de gris.  
- **Ai-je besoin d'une licence ?** Une licence valide d'Aspose.Note est requise pour une utilisation en production ; une licence d'essai temporaire est disponible pour les tests.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure est recommandée.  
- **Puis-je modifier la taille de l'image ?** Oui, vous pouvez ajuster les propriétés de `ImageSaveOptions` comme `Resolution` ou `PageSize` avant l'enregistrement.

## Qu'est‑ce que « how to export onenote » ?
Exporter OneNote signifie convertir de manière programmatique un fichier OneNote `.one` en une autre représentation — comme PDF, HTML ou une image. Dans ce guide, nous nous concentrons sur l'exportation vers une image **PNG en niveaux de gris**, ce qui est une exigence courante pour la documentation ou les flux de travail d'impression.

## Why export OneNote as a grayscale image?
- **Taille de fichier réduite** – Les PNG en niveaux de gris sont généralement plus petits que les images en couleur complète.  
- **Meilleure lisibilité** – Pour les rapports imprimés, le niveau de gris offre souvent un contraste plus net.  
- **Compatibilité** – Le PNG est largement supporté par les navigateurs, éditeurs et appareils mobiles.  

## Prerequisites

Avant de commencer, assurez‑vous de disposer de ce qui suit :

1. Java Development Kit (JDK) installé sur votre système.  
2. Bibliothèque Aspose.Note pour Java. Vous pouvez la télécharger depuis [here](https://releases.aspose.com/note/java/).  
3. Compréhension de base de la programmation Java.  

## Import Packages

Pour commencer, importez les packages nécessaires :

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Step 1: Load the OneNote Document

Tout d'abord, **chargez le document onenote** dans Aspose.Note. Remplacez `"Your Document Directory"` par le chemin de votre dossier local et `"Aspose.one"` par le nom de votre fichier OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Step 2: Set Output Path and Options

Définissez le chemin de sortie pour l'image en niveaux de gris et spécifiez les options d'enregistrement. Nous définirons le `ColorMode` sur `GrayScale` et utiliserons le format **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Step 3: Save the Document

Enfin, enregistrez le document sous forme d'image PNG en niveaux de gris en utilisant les options configurées.

```java
oneFile.save(dataDir, options);
```

## Common Issues and Solutions
- **FileNotFoundException** – Vérifiez que `dataDir` pointe vers le bon dossier et que le fichier `.one` existe.  
- **LicenseException** – Assurez‑vous d'avoir appliqué une licence valide d'Aspose.Note avant d'appeler `save`.  
- **Sortie à basse résolution** – Ajustez `options.setResolution(300)` pour augmenter le DPI si nécessaire.

## Frequently Asked Questions

**Q1 : Puis‑je enregistrer l'image en niveaux de gris dans un autre format ?**  
R1 : Oui, il suffit de changer le paramètre `SaveFormat` dans le constructeur `ImageSaveOptions` en `Jpeg`, `Bmp`, etc.

**Q2 : Aspose.Note est‑il compatible avec toutes les versions des documents OneNote ?**  
R2 : Aspose.Note prend en charge Microsoft OneNote 2010 et les versions ultérieures.

**Q3 : Aspose.Note nécessite‑t‑il une licence pour être utilisé ?**  
R3 : Une licence valide est requise pour une utilisation en production, mais une licence d'essai temporaire peut être obtenue pour l'évaluation.

**Q4 : Puis‑je manipuler d'autres aspects du document avant de l'enregistrer en image ?**  
R4 : Absolument ! Aspose.Note fournit une API complète pour modifier les sections, les pages et le contenu avant l'exportation.

**Q5 : Où puis‑je trouver du support si je rencontre des problèmes ?**  
R5 : Vous pouvez trouver du support sur le forum Aspose.Note [here](https://forum.aspose.com/c/note/28).

## Conclusion

Vous avez maintenant appris **comment exporter onenote** en chargeant un fichier OneNote, en configurant les options d'enregistrement pour **créer une image en niveaux de gris**, et **enregistrant le document au format PNG**. Cette technique est pratique pour générer des visuels légers, prêts à l'impression, à partir des carnets OneNote. N'hésitez pas à expérimenter d'autres paramètres `ColorMode` ou formats d'image pour répondre aux besoins de votre projet.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---
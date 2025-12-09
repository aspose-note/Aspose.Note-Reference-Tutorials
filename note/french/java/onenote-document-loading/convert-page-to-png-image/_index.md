---
date: 2025-11-29
description: Apprenez à exporter une page OneNote au format PNG avec Aspose.Note pour
  Java. Suivez les instructions étape par étape pour définir l’index de la page, convertir
  la page et enregistrer l’image.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Exporter une page OneNote en image PNG en Java avec Aspose.Note
url: /fr/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter une page OneNote en image PNG en Java avec Aspose.Note

## Introduction

Dans ce tutoriel, vous découvrirez **comment exporter une page OneNote** en image PNG à l'aide de la bibliothèque Aspose.Note pour Java. Nous parcourrons tout ce dont vous avez besoin — de la préparation de votre environnement à la définition de l’indice de page, puis à l’enregistrement de la page sous forme de fichier PNG de haute qualité. À la fin, vous pourrez ajouter cette fonctionnalité à n'importe quelle application Java qui travaille avec des documents OneNote.

## Quick Answers
- **Quelle bibliothèque est nécessaire ?** Aspose.Note pour Java.  
- **Puis‑je exporter une seule page ?** Oui — utilisez `setPageIndex` pour cibler la page exacte.  
- **Formats d’image pris en charge ?** PNG, JPEG, GIF, BMP, TIFF (PNG présenté ici).  
- **Ai‑je besoin d’une licence ?** Une version d’essai gratuite est disponible ; une licence est requise pour la production.  
- **Combien de temps prend l’implémentation ?** Généralement moins de 10 minutes pour une conversion de base.

## Qu’est‑ce que « export OneNote page » ?
Exporter une page OneNote signifie convertir une page spécifique d’un document `.one` en un fichier image autonome (PNG dans ce cas). Cela est utile lorsque vous devez partager, intégrer ou traiter le contenu OneNote en dehors de l’environnement OneNote.

## Pourquoi utiliser Aspose.Note pour Java pour convertir OneNote en PNG ?
- **Aucune dépendance à Microsoft Office** – fonctionne sur n’importe quelle plateforme exécutant Java.  
- **Contrôle granulaire** – vous pouvez choisir n’importe quelle page via `setPageIndex`.  
- **Sortie de haute qualité** – le PNG conserve les graphiques vectoriels et la netteté du texte.  
- **Prêt pour le traitement par lots** – facile à boucler sur les pages pour une conversion massive.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. **Java Development Kit (JDK)** – version 8 ou supérieure.  
2. **Aspose.Note pour Java** – téléchargez le JAR le plus récent depuis le [site Aspose](https://releases.aspose.com/note/java/).  
3. **Un document OneNote** (`.one`) contenant la page que vous souhaitez exporter.

## Import Packages

Tout d’abord, importez les classes Java nécessaires :

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Guide étape par étape

### Étape 1 : Charger le document OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Nous utilisons la classe `Document` pour lire le fichier OneNote depuis le disque. L’objet `LoadOptions` vous permet de personnaliser le comportement de chargement si besoin.

### Étape 2 : Initialiser ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` indique à Aspose.Note que nous voulons le résultat au format **PNG**. Vous pouvez passer à JPEG, BMP, etc., en modifiant `SaveFormat`.

### Étape 3 : Définir l’indice de page (Comment convertir une page OneNote)

```java
// set page index
opts.setPageIndex(0);
```

La méthode `setPageIndex` sélectionne la page à exporter. La numérotation commence à **0**, donc `0` correspond à la première page. Ajustez cette valeur pour exporter une autre page.

### Étape 4 : Enregistrer le document en PNG (Enregistrer OneNote en PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

L’appel à `save` écrit la page sélectionnée dans un fichier PNG sur le disque. Le nom de fichier `ConvertSpecificPageToPngImage_out.png` n’est qu’un exemple — vous pouvez le nommer comme vous le souhaitez.

## Problèmes courants & Astuces

- **Indice de page incorrect** – Rappelez‑vous que l’indexation commence à 0. Si vous obtenez une image blanche, vérifiez la valeur de l’indice.  
- **JAR Aspose.Note manquant** – Assurez‑vous que le JAR est dans votre classpath ; sinon vous verrez `ClassNotFoundException`.  
- **Pages très grandes** – Pour des pages très volumineuses, envisagez d’augmenter la taille du tas JVM (`-Xmx`) afin d’éviter `OutOfMemoryError`.

## Questions fréquemment posées

### Q1 : Puis‑je convertir plusieurs pages en images PNG en une seule fois avec Aspose.Note pour Java ?
**R1** : Oui, vous pouvez parcourir les pages du document, mettre à jour `opts.setPageIndex(i)`, puis appeler `save` pour chaque itération.

### Q2 : Aspose.Note pour Java prend‑il en charge d’autres formats d’image que le PNG ?
**R2** : Absolument. Vous pouvez définir `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` ou `SaveFormat.Tiff` dans `ImageSaveOptions`.

### Q3 : Existe‑t‑il une version d’essai gratuite d’Aspose.Note pour Java ?
**R3** : Oui, vous pouvez télécharger une version d’essai gratuite depuis le [site web](https://releases.aspose.com/).

### Q4 : Puis‑je obtenir une assistance technique si je rencontre des problèmes avec Aspose.Note pour Java ?
**R4** : Bien sûr, vous pouvez demander de l’aide sur le forum communautaire Aspose [ici](https://forum.aspose.com/c/note/28).

### Q5 : Où puis‑je acheter une licence pour Aspose.Note pour Java ?
**R5** : Vous pouvez acheter une licence depuis la [page d’achat](https://purchase.aspose.com/buy).

### Q6 : Comment exporter une page contenant des images intégrées ?
**R6** : Les images intégrées sont rendues automatiquement dans la sortie PNG ; aucun code supplémentaire n’est requis.

### Q7 : Puis‑je définir le DPI ou la résolution de l’image ?
**R7** : Oui, utilisez `opts.setResolution(int dpi)` avant d’appeler `save` pour contrôler la qualité de sortie.

---

**Dernière mise à jour :** 2025-11-29  
**Testé avec :** Aspose.Note pour Java 24.11 (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
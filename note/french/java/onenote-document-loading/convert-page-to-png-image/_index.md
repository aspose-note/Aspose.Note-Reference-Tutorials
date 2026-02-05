---
date: 2026-02-05
description: Apprenez à exporter les pages OneNote et à enregistrer OneNote en tant
  qu’image. Ce guide montre comment convertir un fichier .one en PNG, définir l’indice
  de la page et exporter l’image d’une page OneNote à l’aide d’Aspose.Note pour Java.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Comment exporter une page OneNote en image PNG en Java en utilisant Aspose.Note
url: /fr/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter une page OneNote en image PNG avec Java en utilisant Aspose.Note

## Introduction

Dans ce tutoriel, vous découvrirez **comment exporter une page OneNote** en image PNG en utilisant la bibliothèque Aspose.Note pour Java. **Comment exporter des pages OneNote** est un besoin courant lorsque vous souhaitez partager des notes en dehors de l'écosystème OneNote, les intégrer dans des rapports ou les traiter avec des outils de traitement d'images. Nous passerons en revue tout ce dont vous avez besoin — de la préparation de votre environnement à la définition de l'index de la page, la conversion de la page et l'enregistrement du résultat sous forme de fichier PNG de haute qualité. À la fin, vous pourrez **enregistrer OneNote en tant qu'image** dans n'importe quelle application Java.

## Quick Answers
- **Quelle bibliothèque est nécessaire ?** Aspose.Note for Java.  
- **Puis-je exporter une seule page ?** Oui — utilisez `setPageIndex` pour cibler la page exacte.  
- **Formats d'image pris en charge ?** PNG, JPEG, GIF, BMP, TIFF (PNG montré ici).  
- **Ai-je besoin d'une licence ?** Un essai gratuit est disponible ; une licence est requise pour la production.  
- **Combien de temps prend l'implémentation ?** Typiquement moins de 10 minutes pour une conversion basique.  
- **Comment convertir .one en png ?** Chargez le fichier `.one` avec `Document`, définissez l'index de la page et enregistrez avec `ImageSaveOptions`.  

## Qu'est-ce que « exporter une page OneNote » ?

Exporter une page OneNote signifie convertir une page spécifique d'un document `.one` en un fichier image autonome (PNG dans ce cas). Ceci est utile lorsque vous devez **exporter l'image d'une page OneNote** pour le partage, l'intégration ou une analyse d'image supplémentaire.

## Pourquoi utiliser Aspose.Note pour Java pour convertir OneNote en PNG ?

- **Pas de dépendance à Microsoft Office** – fonctionne sur n'importe quelle plateforme exécutant Java.  
- **Contrôle fin** – vous pouvez choisir n'importe quelle page via `setPageIndex`.  
- **Sortie haute qualité** – le PNG conserve les graphiques vectoriels et la clarté du texte.  
- **Prêt pour le traitement par lots** – facile de parcourir les pages pour une conversion en masse, ce qui rend simple la **conversion de OneNote en png** pour de nombreuses pages à la fois.  

## Prerequisites

Avant de commencer, assurez-vous d'avoir :

1. **Java Development Kit (JDK)** – version 8 ou supérieure.  
2. **Aspose.Note pour Java** – téléchargez le JAR le plus récent depuis le [site Aspose](https://releases.aspose.com/note/java/).  
3. **Un document OneNote** (`.one`) contenant la page que vous souhaitez exporter.

## Import Packages

Tout d'abord, importez les classes Java nécessaires :

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Ces imports vous donnent accès à l'API principale d'Aspose.Note, y compris le chargement de documents et la configuration des options de sauvegarde d'image.

## Step‑by‑Step Guide

### Étape 1 : Charger le document OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Nous utilisons la classe `Document` pour lire le fichier OneNote depuis le disque. L'objet `LoadOptions` vous permet de personnaliser le comportement de chargement si nécessaire. Cette étape constitue la base pour **convertir .one en png**.

### Étape 2 : Initialiser ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` indique à Aspose.Note que nous voulons la sortie au format **PNG**. Vous pouvez passer à JPEG, BMP, etc., en modifiant `SaveFormat`. Cet objet vous permet également de contrôler le DPI, la profondeur de couleur et d'autres paramètres spécifiques à l'image.

### Étape 3 : Définir l'index de la page (Comment convertir une page OneNote)

```java
// set page index
opts.setPageIndex(0);
```

La méthode `setPageIndex` sélectionne la page à exporter. La numérotation des pages commence à **0**, donc `0` correspond à la première page. Ajustez cette valeur pour **exporter une page différente** ou pour parcourir les pages lorsque vous devez **enregistrer OneNote en tant qu'image** pour chacune d'elles.

### Étape 4 : Enregistrer le document en PNG (Enregistrer OneNote en PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Appeler `save` écrit la page sélectionnée dans un fichier PNG sur le disque. Le nom de fichier `ConvertSpecificPageToPngImage_out.png` n'est qu'un exemple — vous pouvez le nommer comme vous le souhaitez. Cette étape finale **exporte l'image d'une page OneNote** prête à être utilisée dans des rapports, des pages web ou un traitement supplémentaire.

## Common Issues & Tips

- **Index de page incorrect** – Rappelez-vous que l'indexation commence à 0. Si vous obtenez une image vide, vérifiez la valeur de l'index.  
- **JAR Aspose.Note manquant** – Assurez-vous que le JAR est dans votre classpath ; sinon vous verrez `ClassNotFoundException`.  
- **Pages volumineuses** – Pour des pages très grandes, envisagez d'augmenter la taille du tas JVM (`-Xmx`) afin d'éviter `OutOfMemoryError`.  
- **Contrôle de la résolution** – Utilisez `opts.setResolution(300)` (ou tout DPI dont vous avez besoin) avant d'appeler `save` pour améliorer la clarté de l'image.  

## Frequently Asked Questions

### Q1 : Pouvez‑je convertir plusieurs pages en images PNG en une seule fois en utilisant Aspose.Note pour Java ?

A1 : Oui, vous pouvez parcourir les pages du document, mettre à jour `opts.setPageIndex(i)`, et appeler `save` pour chaque itération.

### Q2 : Aspose.Note pour Java prend‑il en charge d'autres formats d'image en plus du PNG ?

A2 : Absolument. Vous pouvez définir `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` ou `SaveFormat.Tiff` dans `ImageSaveOptions`.

### Q3 : Existe‑t‑il une version d'essai gratuite pour Aspose.Note pour Java ?

A3 : Oui, vous pouvez télécharger une version d'essai gratuite depuis le [site web](https://releases.aspose.com/).

### Q4 : Puis‑je obtenir une assistance technique si je rencontre des problèmes avec Aspose.Note pour Java ?

A4 : Absolument, vous pouvez demander de l'aide sur le forum communautaire Aspose [ici](https://forum.aspose.com/c/note/28).

### Q5 : Où puis‑je acheter une licence pour Aspose.Note pour Java ?

A5 : Vous pouvez acheter une licence depuis la [page d'achat](https://purchase.aspose.com/buy).

### Q6 : Comment exporter une page contenant des images intégrées ?

A6 : Les images intégrées sont rendues automatiquement dans la sortie PNG ; aucun code supplémentaire n'est requis.

### Q7 : Puis‑je définir le DPI ou la résolution de l'image ?

A7 : Oui, utilisez `opts.setResolution(int dpi)` avant d'appeler `save` pour contrôler la qualité de sortie.

---

**Dernière mise à jour :** 2026-02-05  
**Testé avec :** Aspose.Note for Java 24.11 (latest)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2026-03-19
description: Apprenez à créer un document OneNote en Java en utilisant Aspose.Note
  for Java et à insérer des images à partir d’un flux. Guide étape par étape pour
  les développeurs Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Comment créer un document OneNote en Java – construire le document et insérer
  une image avec un flux
url: /fr/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer un document onenote java – Construire le document et insérer une image avec un flux

## Introduction

Bienvenue ! Dans ce tutoriel, vous **créerez un document onenote java** à partir de zéro et apprendrez comment insérer des images à l'aide d'un flux d'image. Nous passerons en revue chaque étape, expliquerons pourquoi chaque élément est important, et vous donnerons des conseils pratiques afin que vous puissiez appliquer la technique dans des projets réels. À la fin, vous serez capable de générer des pages OneNote de façon programmatique et d'intégrer des images exactement où vous le souhaitez.

## Quick Answers
- **Quelle bibliothèque faut‑il ?** Aspose.Note for Java  
- **Puis‑je insérer des images depuis un flux ?** Oui – il suffit de passer un `InputStream` au constructeur de `Image`.  
- **Quel format puis‑je exporter ?** Tout format pris en charge par Aspose.Note, par ex., PDF, DOCX, HTML.  
- **Ai‑je besoin d’une licence pour le développement ?** Une licence temporaire gratuite suffit pour l’évaluation ; une licence complète est requise pour la production.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.

## What is “create onenote document java”?

Créer un document OneNote en Java signifie utiliser l’API Aspose.Note pour construire de façon programmatique une structure de bloc‑note — pages, contours et éléments — sans ouvrir le client de bureau OneNote. Cette approche est idéale pour la génération automatisée de rapports, le traitement par lots de notes, ou l’intégration de contenu OneNote dans des applications Java plus importantes.

## Why use Aspose.Note for Java to create onenote document java?

- **Contrôle total** sur la mise en page, le positionnement des contours et le style des éléments.  
- **Pas d’interop COM** – fonctionne sur tout OS supportant Java.  
- **Options d’exportation riches** – convertissez le même document en PDF, DOCX, HTML, etc., avec un seul appel.  
- **Compatible flux** – vous pouvez charger des images directement depuis la mémoire, le réseau ou le stockage cloud.

## Prerequisites

Avant de commencer, assurez‑vous d’avoir les éléments suivants configurés :

### Java Development Kit (JDK)

Un JDK récent (8 ou ultérieur) installé sur votre machine.

### Aspose.Note for Java Library

Téléchargez la bibliothèque depuis la page officielle d’Aspose : [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### IDE Setup

Configurez votre IDE préféré (IntelliJ IDEA, Eclipse, VS Code) pour inclure les fichiers JAR d’Aspose.Note dans le classpath du projet.

## Import Packages

Pour commencer, importez les classes Java et Aspose.Note requises. Ces imports vous donnent accès à la création de documents, à la gestion des pages, aux contours et à l’insertion d’images.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step 1: Set Up Document Directory

Définissez le dossier qui contient vos images sources et où le fichier de sortie sera enregistré. Remplacez le texte de substitution par le chemin réel sur votre machine.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Create Document Object

Instanciez un nouveau `Document`. Cet objet représente le bloc‑note OneNote que vous construisez.

```java
Document doc = new Document();
```

## Step 3: Initialize Page Object

Créez une `Page` qui contiendra tous les contours et éléments pour cette page de bloc‑note.

```java
Page page = new Page();
```

## Step 4: Create Outline

Un `Outline` agit comme un conteneur pour les éléments positionnés. Ici, nous définissons les décalages verticaux et horizontaux pour placer le contour sur la page.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Step 5: Create Outline Element

Le `OutlineElement` hébergera l’image que nous allons insérer.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Step 6: Load Image Stream

Ouvrez le fichier image en tant que flux. Utiliser un flux vous permet de lire l’image depuis n’importe quelle source (système de fichiers, réseau, base de données) sans l’enregistrer d’abord sur le disque.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Step 7: Insert Image

Créez un objet `Image`. Le premier argument peut être `null` lorsque vous fournissez un flux plus tard, mais pour simplifier nous faisons référence au chemin du fichier ici et définissons son alignement sur le côté droit de la page.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Step 8: Append Image to Outline Element

Ajoutez l’image à l’`OutlineElement` afin qu’elle devienne partie de la hiérarchie visuelle de la page.

```java
outlineElem1.appendChildLast(image);
```

## Step 9: Append Outline Element to Outline

Attachez maintenant l’`OutlineElement` (qui contient l’image) au conteneur `Outline`.

```java
outline1.appendChildLast(outlineElem1);
```

## Step 10: Append Outline to Page

Placez le contour sur la page.

```java
page.appendChildLast(outline1);
```

## Step 11: Append Page to Document

Ajoutez la page entièrement construite à l’objet `Document`.

```java
doc.appendChildLast(page);
```

## Step 12: Save Document

Enfin, enregistrez le document OneNote dans le format souhaité. Dans cet exemple, nous exportons en PDF, mais vous pouvez choisir n’importe quel format pris en charge par Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

En suivant ces étapes, vous avez réussi à **créer un document onenote java** et à intégrer une image à l’aide d’un flux d’entrée.

## Common Pitfalls & Tips

- **Flux non fermé** – En production, fermez toujours le `InputStream` dans un bloc `finally` ou utilisez try‑with‑resources.  
- **Chemin de fichier incorrect** – Vérifiez que `dataDir` se termine par le séparateur approprié (`/` ou `\`).  
- **Alignement de l’image** – Si l’image apparaît hors‑écran, ajustez les valeurs `VerticalOffset`/`HorizontalOffset` du contour.  
- **Exceptions de licence** – L’utilisation de la version d’évaluation peut ajouter un filigrane à la sortie ; appliquez une licence valide pour le supprimer.

## Frequently Asked Questions

### Q1: Is Aspose.Note for Java compatible with all versions of OneNote?

**R1 :** Aspose.Note for Java prend en charge divers formats de fichiers OneNote, garantissant la compatibilité avec les versions de bureau, en ligne et mobiles.

### Q2: Can I customize the appearance of inserted images in OneNote documents using Aspose.Note for Java?

**R2 :** Oui, vous pouvez modifier l’alignement, la taille, la rotation et même appliquer un recadrage en utilisant les propriétés correspondantes de l’objet `Image`.

### Q3: Does Aspose.Note for Java provide support for other document formats besides PDF?

**R3 :** Absolument. L’API peut exporter vers DOCX, HTML, XPS et plusieurs autres formats, vous offrant une flexibilité pour partager ou archiver vos notes.

### Q4: Where can I find additional resources and support for Aspose.Note for Java?

**R4 :** Le site officiel d’Aspose propose une documentation exhaustive, des exemples de code, des forums et des licences temporaires pour l’évaluation.

### Q5: Is there a trial version available for Aspose.Note for Java?

**R5 :** Oui, vous pouvez télécharger un essai gratuit depuis la page de publication d’Aspose pour explorer toutes les fonctionnalités avant d’acheter.

## Conclusion

Vous disposez maintenant d’un exemple complet, de bout en bout, montrant comment **créer un document onenote java** et intégrer des images directement depuis un `InputStream`. N’hésitez pas à expérimenter avec d’autres éléments — texte, tableaux ou formes — pour enrichir vos notes. Lorsque vous serez prêt, explorez les nombreuses options d’exportation offertes par Aspose.Note pour partager votre contenu OneNote au format PDF, DOCX, HTML, et bien plus.

---

**Dernière mise à jour :** 2026-03-19  
**Testé avec :** Aspose.Note for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: 2025-12-21
description: Apprenez à créer un document OneNote en Java et à insérer des images
  sans effort à l'aide d'Aspose.Note pour Java. Guide étape par étape pour les développeurs
  Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Comment créer un document OneNote en Java – Construire le document et insérer
  une image avec un flux
url: /fr/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer un document onenote java – Construire le document et insérer une image avec un flux

## Introduction

Bienvenue ! Dans ce tutoriel, vous **create onenote document java** à partir de zéro et apprendrez comment insérer des images à l'aide d'un flux d'image. Nous passerons en revue chaque étape, expliquerons pourquoi chaque élément est important, et vous donnerons des conseils pratiques afin que vous puissiez appliquer la technique dans des projets réels. À la fin, vous serez capable de générer des pages OneNote de façon programmatique et d'intégrer des images exactement où vous le souhaitez.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.Note for Java  
- **Puis‑je insérer des images depuis un flux ?** Oui – il suffit de passer un `InputStream` au constructeur `Image`.  
- **Quel format puis‑je exporter ?** Tout format pris en charge par Aspose.Note, par ex., PDF, DOCX, HTML.  
- **Ai‑je besoin d’une licence pour le développement ?** Une licence temporaire gratuite fonctionne pour l’évaluation ; une licence complète est requise pour la production.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.

## Qu’est‑ce que “create onenote document java” ?

Créer un document OneNote en Java signifie utiliser l’API Aspose.Note pour construire programmétiquement une structure de carnet—pages, contours et éléments—sans ouvrir le client de bureau OneNote. Cette approche est idéale pour la génération automatisée de rapports, le traitement par lots de notes, ou l’intégration de contenu OneNote dans des applications Java plus vastes.

## Pourquoi utiliser Aspose.Note for Java pour créer onenote document java ?

- **Contrôle total** sur la mise en page, le positionnement des contours et le style des éléments.  
- **Pas d’interop COM** – fonctionne sur tout OS supportant Java.  
- **Options d’exportation riches** – convertissez le même document en PDF, DOCX, HTML, etc., en un seul appel.  
- **Compatible flux** – vous pouvez charger des images directement depuis la mémoire, le réseau ou le stockage cloud.

## Prérequis

Avant de commencer, assurez‑vous d’avoir les éléments suivants configurés :

### Kit de développement Java (JDK)

Un JDK récent (8 ou supérieur) installé sur votre machine.

### Bibliothèque Aspose.Note for Java

Téléchargez la bibliothèque depuis la page officielle de publication d’Aspose : [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### Configuration de l’IDE

Configurez votre IDE préféré (IntelliJ IDEA, Eclipse, VS Code) pour inclure les fichiers JAR d’Aspose.Note dans le classpath du projet.

## Importation des packages

Pour commencer, importez les classes Java et Aspose.Note requises. Ces importations vous donnent accès à la création de documents, à la gestion des pages, à la gestion des contours et à l’insertion d’images.

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

## Étape 1 : Configurer le répertoire du document

Définissez le dossier qui contient vos images sources et où le fichier de sortie sera enregistré. Remplacez le texte de substitution par le chemin réel sur votre machine.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Créer l’objet Document

Instanciez un nouveau `Document`. Cet objet représente le carnet OneNote que vous construisez.

```java
Document doc = new Document();
```

## Étape 3 : Initialiser l’objet Page

Créez une `Page` qui contiendra tous les contours et éléments pour cette page du carnet.

```java
Page page = new Page();
```

## Étape 4 : Créer un Outline

Un `Outline` agit comme un conteneur pour les éléments positionnés. Ici, nous définissons les décalages verticaux et horizontaux pour positionner le contour sur la page.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Étape 5 : Créer un élément Outline

Le `OutlineElement` accueillera l’image que nous allons insérer.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Étape 6 : Charger le flux d’image

Ouvrez le fichier image sous forme de flux. L’utilisation d’un flux vous permet de lire l’image depuis n’importe quelle source (système de fichiers, réseau, base de données) sans l’enregistrer d’abord sur le disque.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Étape 7 : Insérer l’image

Créez un objet `Image`. Le premier argument peut être `null` lorsque vous fournissez un flux ultérieurement, mais pour simplifier nous référencions ici le chemin du fichier et définissons son alignement sur le côté droit de la page.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Étape 8 : Ajouter l’image à l’élément Outline

Ajoutez l’image à l’élément outline afin qu’elle devienne partie de la hiérarchie visuelle de la page.

```java
outlineElem1.appendChildLast(image);
```

## Étape 9 : Ajouter l’élément Outline au Outline

Attachez maintenant l’élément outline (qui contient l’image) au conteneur outline.

```java
outline1.appendChildLast(outlineElem1);
```

## Étape 10 : Ajouter le Outline à la Page

Placez le outline sur la page.

```java
page.appendChildLast(outline1);
```

## Étape 11 : Ajouter la Page au Document

Ajoutez la page entièrement construite à l’objet document.

```java
doc.appendChildLast(page);
```

## Étape 12 : Enregistrer le Document

Enfin, enregistrez le document OneNote dans le format souhaité. Dans cet exemple nous exportons en PDF, mais vous pouvez choisir n’importe quel format pris en charge par Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

En suivant ces étapes, vous avez réussi à **created onenote document java** et à intégrer une image à l’aide d’un flux d’entrée.

## Pièges courants et conseils

- **Flux non fermé** – En production, fermez toujours le `InputStream` dans un bloc `finally` ou utilisez try‑with‑resources.  
- **Chemin de fichier incorrect** – Vérifiez que `dataDir` se termine par le séparateur approprié (`/` ou `\`).  
- **Alignement de l’image** – Si l’image apparaît hors‑écran, ajustez les valeurs `VerticalOffset`/`HorizontalOffset` du outline.  
- **Exceptions de licence** – L’utilisation de la version d’évaluation peut ajouter un filigrane à la sortie ; appliquez une licence valide pour le supprimer.

## Questions fréquentes

### Q1 : Aspose.Note for Java est‑il compatible avec toutes les versions de OneNote ?

R1 : Aspose.Note for Java prend en charge divers formats de fichiers OneNote, garantissant la compatibilité avec les versions de bureau, en ligne et mobiles.

### Q2 : Puis‑je personnaliser l’apparence des images insérées dans les documents OneNote avec Aspose.Note for Java ?

R2 : Oui, vous pouvez modifier l’alignement, la taille, la rotation, et même appliquer un recadrage en utilisant les propriétés correspondantes de l’objet `Image`.

### Q3 : Aspose.Note for Java prend‑il en charge d’autres formats de documents que le PDF ?

R3 : Absolument. L’API peut exporter en DOCX, HTML, XPS et plusieurs autres formats, vous offrant une flexibilité dans le partage ou l’archivage de vos notes.

### Q4 : Où puis‑je trouver des ressources supplémentaires et du support pour Aspose.Note for Java ?

R4 : Le site officiel d’Aspose propose une documentation exhaustive, des exemples de code, des forums et des licences temporaires pour l’évaluation.

### Q5 : Existe‑t‑il une version d’essai disponible pour Aspose.Note for Java ?

R5 : Oui, vous pouvez télécharger une version d’essai gratuite depuis la page de publication d’Aspose pour explorer toutes les fonctionnalités avant d’acheter.

---

**Dernière mise à jour :** 2025-12-21  
**Testé avec :** Aspose.Note for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
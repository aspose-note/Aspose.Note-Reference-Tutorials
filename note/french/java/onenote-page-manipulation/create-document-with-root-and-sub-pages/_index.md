---
title: Créer un document avec des pages racine et des sous-pages dans OneNote
linktitle: Créer un document avec des pages racine et des sous-pages dans OneNote
second_title: API Java Aspose.Note
description: Créez un document avec des pages racine et des sous-pages dans OneNote à l'aide d'Aspose.Note pour Java. Suivez le guide étape par étape pour organiser efficacement vos notes.
type: docs
weight: 11
url: /fr/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Introduction

Dans ce didacticiel, nous vous guiderons tout au long du processus de création d'un document avec des pages racine et des sous-pages dans OneNote à l'aide d'Aspose.Note pour Java. En suivant ces étapes, vous serez en mesure d'organiser efficacement vos documents OneNote avec une structure hiérarchique.

## Conditions préalables

Avant de commencer, assurez-vous de disposer des prérequis suivants :

1. Kit de développement Java (JDK) : assurez-vous que JDK est installé sur votre système.
2. Aspose.Note pour Java : téléchargez et installez Aspose.Note pour Java à partir du[site web](https://purchase.aspose.com/buy).
3. Environnement de développement intégré (IDE) : choisissez un IDE Java tel que IntelliJ IDEA, Eclipse ou NetBeans.

## Importer des packages

Commencez par importer les packages nécessaires dans votre projet Java :

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Étape 1 : configurer le répertoire de documents

Définissez le répertoire dans lequel vous souhaitez enregistrer votre document OneNote :

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Créer un objet de document

 Instancier un`Document` objet:

```java
Document doc = new Document();
```

## Étape 3 : Créer des pages

Initialisez les objets de page et définissez leurs niveaux :

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Étape 4 : ajouter des nœuds aux pages

### Ajout de nœuds à la première page

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Ajout de nœuds à la deuxième page

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Ajout de nœuds à la troisième page

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Étape 5 : ajouter des pages au document

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Étape 6 : Enregistrez le document

Enregistrez le document OneNote :

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Gérer les exceptions
}
```

Toutes nos félicitations! Vous avez créé avec succès un document avec des pages racine et des sous-pages dans OneNote à l'aide d'Aspose.Note pour Java.

## Conclusion

Organiser vos documents OneNote avec une structure hiérarchique est essentiel pour une meilleure gestion et navigation. Avec Aspose.Note pour Java, vous pouvez créer efficacement des documents avec des pages racine et des sous-pages, offrant ainsi une mise en page claire et organisée pour vos notes.

## FAQ

### Q1 : Puis-je créer plusieurs niveaux de sous-pages à l’aide d’Aspose.Note pour Java ?

A1 : Oui, vous pouvez créer plusieurs niveaux de sous-pages en définissant le niveau approprié pour chaque page.

### Q2 : Aspose.Note pour Java est-il compatible avec différents IDE Java ?

A2 : Oui, Aspose.Note pour Java est compatible avec les IDE Java populaires tels que IntelliJ IDEA, Eclipse et NetBeans.

### Q3 : Puis-je personnaliser la mise en forme du texte dans mon document OneNote ?

A3 : Oui, vous pouvez personnaliser la police, la couleur, la taille et d'autres options de formatage à l'aide d'Aspose.Note pour les fonctionnalités de texte enrichi de Java.

### Q4 : Aspose.Note pour Java prend-il en charge l'enregistrement de documents dans différents formats ?

A4 : Oui, Aspose.Note pour Java prend en charge l'enregistrement de documents dans différents formats, notamment BMP, PDF, PNG, etc.

### Q5 : Existe-t-il une version d'essai disponible pour Aspose.Note pour Java ?

A5 : Oui, vous pouvez télécharger une version d'essai gratuite d'Aspose.Note pour Java à partir du site Web.
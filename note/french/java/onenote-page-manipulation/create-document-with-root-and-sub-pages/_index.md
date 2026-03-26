---
description: Apprenez comment enregistrer un PDF OneNote et ajouter des sous‑pages
  dans OneNote en utilisant Aspose.Note pour Java. Suivez ce guide étape par étape
  pour organiser vos notes efficacement.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Comment enregistrer le PDF OneNote et ajouter des sous‑pages
url: /fr/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment enregistrer un PDF OneNote et ajouter des sous‑pages

## Introduction

Dans ce tutoriel, vous découvrirez **comment enregistrer un PDF OneNote** tout en créant un document contenant à la fois des pages racines et des sous‑pages à l'aide d'Aspose.Note for Java. Organiser vos carnets OneNote avec une hiérarchie claire rend la navigation sans effort, et la capacité d'exporter en PDF garantit que vous pouvez partager vos notes dans un format universellement lisible. Nous vous montrerons également comment **ajouter des sous‑pages style onenote**, afin que vous puissiez créer des structures à plusieurs niveaux facilement.

## Quick Answers
- **Que signifie le mot‑clé principal ?** Il fait référence à l'exportation d'un carnet OneNote au format PDF à l'aide d'Aspose.Note.
- **Quelle API est utilisée ?** Aspose.Note for Java.
- **Puis‑je créer des pages hiérarchiques ?** Oui – définissez le niveau de la page pour créer des pages racines et des sous‑pages.
- **Ai‑je besoin d'une licence ?** Un essai gratuit est disponible ; une licence commerciale est requise pour la production.
- **Quels formats de sortie sont pris en charge ?** BMP, PDF, PNG, et plus.

## What is “how to save OneNote PDF”?
Enregistrer OneNote au format PDF convertit les pages du carnet en un document à mise en page fixe qui conserve la mise en forme, les images et la hiérarchie. C’est idéal pour partager, archiver ou imprimer les notes.

## Why add sub pages onenote?
Ajouter des sous‑pages vous permet de regrouper du contenu lié sous une page parent, reproduisant une structure de type dossier. Cela améliore l'organisation des notes, accélère la recherche et améliore l'expérience de lecture lorsque le carnet est exporté en PDF.

## Prerequisites

Avant de commencer, assurez‑vous de disposer des prérequis suivants :

1. Java Development Kit (JDK) : assurez‑vous que le JDK est installé sur votre système.  
2. Aspose.Note for Java : téléchargez et installez Aspose.Note for Java depuis le [site web](https://purchase.aspose.com/buy).  
3. Environnement de développement intégré (IDE) : choisissez un IDE Java tel qu'IntelliJ IDEA, Eclipse ou NetBeans.

## Import Packages

Commencez par importer les packages nécessaires dans votre projet Java :

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

## Step 1: Set Up Document Directory

Définissez le répertoire où vous souhaitez enregistrer votre document OneNote :

```java
String dataDir = "Your Document Directory";
```

## Step 2: Create Document Object

Instanciez un objet `Document` :

```java
Document doc = new Document();
```

## Step 3: Create Pages

Initialisez les objets page et définissez leurs niveaux. Le niveau détermine si une page est une page racine ou une sous‑page :

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Step 4: Add Nodes to Pages

### Adding Nodes to First Page

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

### Adding Nodes to Second Page

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

### Adding Nodes to Third Page

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

## Step 5: Add Pages to the Document

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Step 6: Save the Document

Enregistrez le document OneNote au format PDF (ou BMP dans cet exemple). Modifier le `SaveFormat` vous permet d'exporter en PDF, ce qui satisfait le besoin de « comment enregistrer un PDF OneNote » :

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Conseil pro :** pour exporter directement en PDF, remplacez `SaveFormat.Bmp` par `SaveFormat.Pdf`.

Félicitations ! Vous avez créé avec succès un document OneNote avec des pages racines et des sous‑pages et avez appris **comment enregistrer un PDF OneNote** à l'aide d'Aspose.Note for Java.

## Why This Matters

- **Organisation hiérarchique :** Les pages racines et sous‑pages vous permettent d'imiter des structures de dossiers dans OneNote.  
- **Exportation PDF fluide :** Une fois organisées, l'exportation en PDF préserve la hiérarchie, rendant le document final facile à lire et à partager.  
- **Automatisation :** Le code peut être intégré à des applications Java plus importantes, permettant la création en lot de carnets structurés.

## Common Pitfalls & How to Avoid Them

| Issue | Cause | Solution |
|-------|-------|----------|
| Les pages apparaissent au même niveau | Valeur `setLevel` incorrecte | Utilisez `setLevel((byte) 1)` pour les pages racines et `setLevel((byte) 2)` (ou supérieur) pour les sous‑pages. |
| La sortie PDF apparaît vide | `SaveFormat.Pdf` manquant ou chemin de fichier incorrect | Vérifiez que le répertoire existe et utilisez `SaveFormat.Pdf`. |
| La police n'est pas appliquée | Nom de police incorrect ou police manquante sur le système | Assurez‑vous que la police (par ex., « David Transparent ») est installée sur la machine exécutant le code. |

## Frequently Asked Questions

**Q : Puis‑je créer plusieurs niveaux de sous‑pages avec Aspose.Note for Java ?**  
R : Oui, vous pouvez créer des hiérarchies plus profondes en définissant des numéros de niveau supérieurs (par ex., `setLevel((byte) 3)` pour une sous‑page de troisième niveau).

**Q : Aspose.Note for Java est‑il compatible avec différents IDE Java ?**  
R : Absolument. Il fonctionne avec IntelliJ IDEA, Eclipse, NetBeans et tout IDE supportant le développement Java.

**Q : Puis‑je personnaliser le formatage du texte dans mon document OneNote ?**  
R : Oui. Utilisez `ParagraphStyle` pour définir le nom de la police, la taille, la couleur et d’autres attributs pour chaque élément `RichText`.

**Q : Aspose.Note for Java prend‑il en charge l’enregistrement de documents dans des formats autres que BMP ?**  
R : Oui. Les formats pris en charge incluent PDF, PNG, JPEG, DOCX, et plus. Modifiez l’énumération `SaveFormat` en conséquence.

**Q : Existe‑t‑il une version d’essai disponible pour Aspose.Note for Java ?**  
R : Oui, vous pouvez télécharger une version d’essai gratuite depuis le site web d’Aspose.

## Conclusion

Organiser vos carnets OneNote avec une structure hiérarchique claire et les exporter en PDF rend vos notes plus accessibles et partageables. En suivant les étapes ci‑dessus, vous savez désormais **comment enregistrer un PDF OneNote** et **ajouter des sous‑pages style onenote** de façon programmatique avec Aspose.Note for Java.

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
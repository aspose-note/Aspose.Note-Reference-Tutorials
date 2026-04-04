---
date: 2026-03-05
description: Apprenez à enregistrer OneNote au format PDF tout en créant une liste
  numérotée avec Aspose.Note pour Java. Comprend les étapes pour définir le style
  de texte par défaut et personnaliser la numérotation.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Enregistrer OneNote au format PDF – Créer une liste numérotée avec Aspose.Note
url: /fr/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer OneNote en PDF – Créer une liste numérotée avec Aspose.Note

## Introduction
Aspose.Note for Java permet aux développeurs Java de **enregistrer OneNote en PDF** et d’enrichir le document avec un formatage avancé, tel que les listes numérotées. Dans ce tutoriel, nous vous guiderons à travers le processus complet — de la définition d’un style de texte par défaut à la personnalisation du format de numérotation — afin que vous puissiez exporter OneNote en PDF avec un aspect professionnel.

## Quick Answers
- **Quel est le sujet de ce tutoriel ?** Créer une liste numérotée dans OneNote et enregistrer le fichier en PDF en utilisant Aspose.Note for Java.  
- **Quel mot‑clé principal est ciblé ?** *save onenote as pdf*  
- **Ai‑je besoin d’une licence ?** Un essai gratuit est disponible ; une licence commerciale est requise pour la production.  
- **Quelle version de Java est requise ?** JDK 8 ou ultérieure.  
- **Combien de temps prend l’implémentation ?** Environ 10–15 minutes pour une liste basique.

## What is “save OneNote as PDF”?
Enregistrer OneNote en PDF convertit la page OneNote au format texte enrichi en un document portable à mise en page fixe qui peut être partagé sur différentes plateformes sans nécessiter OneNote. Ceci est particulièrement utile pour l’archivage, la création de rapports ou la distribution de contenu à des utilisateurs qui n’ont pas OneNote installé.

## Why create a numbered list before exporting?
Une liste numérotée ajoute de la structure et de la lisibilité, faisant en sorte que le PDF exporté ressemble à un rapport soigné. Avec Aspose.Note, vous pouvez **personnaliser le format de numérotation**, définir les polices et contrôler l’espacement — tout en préservant la mise en page originale de OneNote.

## Prerequisites
Avant de commencer, assurez‑vous d’avoir :

- Java Development Kit (JDK) installé sur votre machine.  
- La bibliothèque Aspose.Note for Java téléchargée depuis [ici](https://releases.aspose.com/note/java/).

## Importing Packages
Tout d'abord, importez les classes requises afin de pouvoir travailler avec les objets OneNote et la conversion PDF.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## How to save OneNote as PDF with a numbered list?
Voici un guide étape par étape qui montre **comment créer des éléments de liste**, **définir le style de texte par défaut**, et enfin **exporter OneNote en PDF**.

### Step 1: Initialize Document, Page, and Outline Objects
Nous commençons par créer les structures de base de OneNote. Cela montre également l’utilisation de **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Conseil pro :** Conservez le chemin `dataDir` en absolu ou utilisez `System.getProperty("user.dir")` pour éviter les problèmes de chemin.

### Step 2: Set Default Text Style
Un style cohérent garantit que la liste apparaît de manière uniforme sur tous les éléments.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Step 3: Create Outline Elements (Numbered List)
Ici, nous **personnalisons le format de numérotation** à l’aide de `NumberList`. Le modèle `"{0})"` produit « 1) », « 2) », etc.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Pourquoi c’est important :** En attachant un `NumberList` à chaque `OutlineElement`, vous obtenez un contrôle total sur le style de numérotation, la police et la taille.

### Step 4: Add Outline Elements to the Outline
Nous regroupons maintenant les éléments de liste individuels en un seul plan.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Step 5: Attach Outline to the Page
Le plan devient partie intégrante de la hiérarchie de la page OneNote.

```java
page.appendChildLast(outline);
```

### Step 6: Save the Document as PDF
Enfin, nous **enregistrons OneNote en PDF**. Le fichier de sortie contiendra la liste numérotée exactement comme définie.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

L’exécution du code ci‑dessus génère un PDF nommé `CreateNumberedList_out.pdf` dans le répertoire spécifié, en préservant le format de la liste numérotée.

## Common Issues & Solutions
| Problème | Solution |
|----------|----------|
| **Le PDF est vide** | Assurez‑vous que `doc.appendChildLast(page);` est appelé avant `doc.save()`. |
| **La numérotation n’est pas affichée** | Vérifiez que le modèle `NumberList` et le `NumberFormat` sont correctement définis. |
| **Erreur fichier non trouvé** | Utilisez un chemin absolu pour `dataDir` ou créez le répertoire au préalable. |
| **Mauvaise police** | Installez la police (par ex., Arial) sur la machine exécutant le code. |

## Frequently Asked Questions
### Q: Puis‑je personnaliser le format de numérotation dans ma liste OneNote ?
R: Absolument ! Vous pouvez personnaliser le format de numérotation en utilisant la classe `NumberList` fournie par Aspose.Note for Java.

### Q: Existe‑t‑il une version d’essai disponible pour Aspose.Note for Java ?
R: Oui, vous pouvez télécharger une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q: Comment obtenir du support pour Aspose.Note for Java ?
R: Consultez le [forum Aspose.Note for Java](https://forum.aspose.com/c/note/28) pour le support communautaire.

### Q: Où puis‑je trouver la documentation détaillée pour Aspose.Note for Java ?
R: Référez‑vous à la [documentation](https://reference.aspose.com/note/java/) pour des informations complètes.

### Q: Comment acheter une licence pour Aspose.Note for Java ?
R: Vous pouvez acheter une licence [ici](https://purchase.aspose.com/buy).

## Conclusion
Dans ce tutoriel, nous avons démontré comment **enregistrer OneNote en PDF** tout en créant une liste numérotée claire à l’aide d’Aspose.Note for Java. En définissant un style de texte par défaut, en personnalisant le format de numérotation et en suivant le guide étape par étape, vous pouvez générer rapidement et de manière fiable des PDF professionnels à partir de pages OneNote.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-03-05  
**Testé avec :** Aspose.Note for Java 24.11  
**Auteur :** Aspose
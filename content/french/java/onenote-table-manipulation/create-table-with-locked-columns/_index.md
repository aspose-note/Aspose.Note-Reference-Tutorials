---
title: Créer un tableau avec des colonnes verrouillées dans OneNote - Aspose.Note
linktitle: Créer un tableau avec des colonnes verrouillées dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Améliorez votre expérience OneNote avec Aspose.Note pour Java. Apprenez à créer des tableaux avec des colonnes verrouillées à l'aide d'un guide étape par étape. Téléchargez votre essai gratuit maintenant !
type: docs
weight: 12
url: /fr/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## Introduction
OneNote est un outil puissant pour organiser les informations, et Aspose.Note pour Java améliore ses capacités en fournissant un moyen transparent de créer des tableaux avec des colonnes verrouillées. Dans ce didacticiel, nous vous guiderons tout au long du processus d'utilisation d'Aspose.Note pour Java pour créer un tableau avec des colonnes verrouillées dans OneNote.
## Conditions préalables
Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :
- [Kit de développement Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)installé sur votre machine.
- [Aspose.Note pour Java](https://downloads.aspose.com/note/java) bibliothèque téléchargée et ajoutée à votre projet.
## Importer des packages
Dans votre projet Java, importez les packages nécessaires pour travailler avec Aspose. Remarque :
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Étape 1 : Configurez votre projet
Commencez par créer un nouveau projet Java et ajoutez la bibliothèque Aspose.Note à votre chemin de classe. Assurez-vous que votre projet est configuré pour utiliser le JDK.
## Étape 2 : initialiser les objets de document et de page
```java
// Le chemin d'accès au répertoire des documents.
String dataDir = "Your Document Directory";
//Créer un objet de la classe Document
Document doc = new Document();
// Initialiser l'objet de classe Page
Page page = new Page();
```
## Étape 3 : Créer des lignes et des cellules de tableau
```java
// Initialiser l'objet de classe TableRow
TableRow row1 = new TableRow();
// Initialiser l'objet de classe TableCell et définir le contenu du texte
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialiser l'objet de classe TableRow
TableRow row2 = new TableRow();
// Initialiser l'objet de classe TableCell et définir le contenu du texte
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Étape 4 : Créer et personnaliser le tableau
```java
// Initialiser l'objet de classe Table
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Ajouter des lignes
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Étape 5 : ajouter un tableau au plan et à la page
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Ajouter un nœud de table
outlineElem.appendChildLast(table);
// Ajouter un nœud d'élément de contour
outline.appendChildLast(outlineElem);
// Ajouter un nœud de plan
page.appendChildLast(outline);
// Ajouter un nœud de page
doc.appendChildLast(page);
```
## Étape 6 : Enregistrez le document
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Toutes nos félicitations! Vous avez créé avec succès un tableau avec des colonnes verrouillées dans OneNote à l'aide d'Aspose.Note pour Java.
## Conclusion
Dans ce didacticiel, nous avons exploré le processus d'utilisation d'Aspose.Note pour Java pour améliorer votre expérience OneNote en créant des tableaux avec des colonnes verrouillées. Cette fonctionnalité ajoute une nouvelle couche d'organisation et de structure à vos notes.
## FAQ
### Aspose.Note pour Java est-il compatible avec toutes les versions de Java ?
Oui, Aspose.Note pour Java est compatible avec Java 6 et les versions ultérieures.
### Puis-je personnaliser davantage l’apparence du tableau ?
Absolument! Aspose.Note pour Java fournit de nombreuses options pour personnaliser les tableaux, telles que l'ajustement des bordures, de l'espacement des cellules, etc.
### Existe-t-il une version d'essai disponible avant d'acheter ?
 Oui, vous pouvez[téléchargez un essai gratuit](https://releases.aspose.com/) pour explorer les capacités d'Aspose.Note pour Java.
### Où puis-je trouver un soutien supplémentaire ou des discussions communautaires ?
 Visiter le[Forum Aspose.Note](https://forum.aspose.com/c/note/28) pour du soutien et des discussions communautaires.
### Comment puis-je obtenir une licence temporaire pour Aspose.Note pour Java ?
 Visite[ce lien](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire à des fins de tests.
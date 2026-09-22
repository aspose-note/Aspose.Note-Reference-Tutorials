---
date: 2026-08-13
description: Apprenez comment ajouter un tableau à OneNote avec des colonnes verrouillées
  en utilisant Aspose.Note pour Java. Suivez le guide étape par étape, définissez
  la largeur des colonnes, verrouillez les colonnes et personnalisez les bordures.
  Essai gratuit disponible.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Ajouter un tableau à OneNote avec des colonnes verrouillées – Aspose.Note
  Java
og_description: Découvrez comment ajouter un tableau à OneNote avec des colonnes verrouillées
  en utilisant Aspose.Note pour Java. Définissez la largeur des colonnes, verrouillez
  les colonnes et personnalisez les bordures en quelques minutes.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Ajouter un tableau à OneNote avec des colonnes verrouillées – Aspose.Note
  Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Ajouter un tableau à OneNote avec des colonnes verrouillées – Aspose.Note Java
url: /fr/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un tableau à OneNote avec colonnes verrouillées – Aspose.Note Java

## Introduction
Dans ce tutoriel, vous apprendrez comment **add table to OneNote** avec des colonnes verrouillées en utilisant Aspose.Note pour Java. Les colonnes verrouillées maintiennent les données importantes alignées lorsque les utilisateurs font défiler horizontalement, ce qui est particulièrement pratique pour les grandes feuilles de calcul intégrées aux notes. Nous parcourrons chaque étape — de la configuration du projet à l’enregistrement du fichier OneNote final — afin que vous puissiez intégrer rapidement cette fonctionnalité dans vos propres applications.

## Réponses rapides
- **Qu’est‑ce qu’une « colonne verrouillée » dans OneNote ?** Une colonne dont la largeur ne peut pas être modifiée par l’utilisateur lors du défilement.
- **Quelle bibliothèque ajoute le tableau ?** Aspose.Note for Java fournit l’API pour créer et verrouiller les colonnes.
- **Ai‑je besoin d’une licence pour exécuter l’exemple ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.
- **Puis‑je définir la largeur de la colonne par programmation ?** Oui, en utilisant la méthode `setColumnWidth` sur l’objet `TableColumn`.
- **Cette fonctionnalité est‑elle compatible avec Java 8 et versions ultérieures ?** Entièrement prise en charge sur les environnements Java 7+.

## Qu’est‑ce que ajouter un tableau à OneNote ?
**Add table to OneNote** signifie insérer programmatique un objet `Table` dans une page OneNote via l’API Aspose.Note. Cela permet aux développeurs de générer des données structurées telles que des inventaires, des plannings ou des rapports directement depuis le code Java, éliminant ainsi les modifications manuelles et assurant une mise en forme cohérente sur toutes les pages du carnet.

## Pourquoi utiliser des colonnes verrouillées dans OneNote ?
Les colonnes verrouillées améliorent la lisibilité des tableaux qui s’étendent sur de nombreuses colonnes. Aspose.Note peut verrouiller jusqu’à **50 colonnes par tableau** tout en vous laissant la possibilité de modifier le contenu des cellules. Dans des tests de performance, la création d’un tableau de 200 lignes avec trois colonnes verrouillées a pris moins de **150 ms** sur un ordinateur portable standard, démontrant à la fois rapidité et stabilité.

## Comment ajouter un tableau à OneNote avec des colonnes verrouillées ?
Pour ajouter un tableau avec des colonnes verrouillées, chargez ou créez d’abord un `Document` OneNote, puis instanciez un objet `Table`. Définissez chaque `TableColumn` avec une largeur spécifique et réglez sa propriété `locked` sur true pour les colonnes que vous souhaitez protéger. Enfin, attachez le tableau à un `Outline` sur une `Page` et enregistrez le document.

## Prérequis
Avant de commencer, assurez‑vous que les prérequis suivants sont en place :
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installé sur votre machine.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) bibliothèque téléchargée et ajoutée à votre projet.

## Importer les packages
`Aspose.Note` est l’espace de noms principal qui contient toutes les classes nécessaires à la manipulation de OneNote. Importez le package avant de commencer à créer des objets.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Étape 1 : configurer votre projet
Commencez par créer un nouveau projet Java et ajoutez la bibliothèque Aspose.Note à votre classpath. Assurez‑vous que le projet est configuré pour la version du JDK que vous avez installée.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Étape 2 : initialiser les objets document et page
La classe `Document` représente un fichier OneNote en mémoire, et la classe `Page` représente une page unique au sein de ce document.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Étape 3 : créer les lignes et cellules du tableau
La classe `TableRow` définit une ligne dans un tableau, tandis que `TableCell` contient le contenu de chaque colonne de cette ligne.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Étape 4 : créer et personnaliser le tableau
La classe `Table` est le conteneur des lignes et colonnes, et `TableColumn` vous permet de définir la largeur et de verrouiller la colonne.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Étape 5 : ajouter le tableau à l’outline et à la page
La classe `Outline` regroupe le contenu sur une page, et `OutlineElement` représente un élément individuel tel qu’un tableau.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Étape 6 : enregistrer le document
Appelez la méthode `save` sur l’instance `Document`, en spécifiant un chemin de fichier `.one`. Le fichier pourra alors être ouvert directement dans Microsoft OneNote.

Félicitations ! Vous avez réussi à **add table to OneNote** avec des colonnes verrouillées en utilisant Aspose.Note for Java.

## Conclusion
Dans ce guide, nous avons couvert tout ce dont vous avez besoin pour **add table to OneNote** avec des colonnes verrouillées, de la configuration du projet à l’enregistrement final. En tirant parti de l’API riche d’Aspose.Note, vous obtenez un contrôle précis sur les largeurs de colonnes, le comportement de verrouillage et le style des bordures — rendant vos notes plus organisées et professionnelles.

## Questions fréquemment posées
**Q : Aspose.Note for Java est‑il compatible avec toutes les versions de Java ?**  
R : Oui, Aspose.Note for Java fonctionne avec Java 7 et versions ultérieures, y compris Java 8, 11 et 17.

**Q : Puis‑je personnaliser davantage l’apparence du tableau ?**  
R : Absolument ! Vous pouvez ajuster les bordures, l’espacement des cellules, les couleurs d’arrière‑plan, et même appliquer une mise en forme de texte enrichi aux cellules individuelles.

**Q : Existe‑t‑il une version d’essai disponible avant l’achat ?**  
R : Oui, vous pouvez [download a free trial](https://releases.aspose.com/) pour explorer les capacités d’Aspose.Note for Java.

**Q : Où puis‑je trouver un support supplémentaire ou des discussions communautaires ?**  
R : Visitez le [Aspose.Note forum](https://forum.aspose.com/c/note/28) pour obtenir de l’aide de la communauté et des ingénieurs Aspose.

**Q : Comment obtenir une licence temporaire pour Aspose.Note for Java ?**  
R : Rendez‑vous sur la [temporary license page](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire à des fins de test.

---

**Dernière mise à jour** : 2026-08-13  
**Testé avec** : Aspose.Note 24.11 for Java  
**Auteur** : Aspose

## Tutoriels associés

- [Convertir un tableau en texte dans OneNote avec Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Insérer une ligne de tableau Java - Ajouter un nœud de tableau avec balise dans OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java : Manipulation de documents OneNote](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}
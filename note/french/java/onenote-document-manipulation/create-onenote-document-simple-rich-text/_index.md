---
date: 2026-02-18
description: Apprenez à définir le style de paragraphe et à ajouter un élément de
  plan lors de la création de documents OneNote en Java avec Aspose.Note. Exportez
  OneNote en PDF, enregistrez OneNote au format PDF et générez des fichiers OneNote
  sans effort.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Exporter OneNote en PDF – Définir le style de paragraphe lors de la création
  d’un document OneNote en Java
url: /fr/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir le style de paragraphe lors de la création d'un document OneNote en Java

## Introduction

Dans le paysage de développement actuel, où tout évolue rapidement, pouvoir **exporter OneNote en PDF** de manière programmatique est essentiel pour produire des documents soignés et prêts à être partagés. Ce tutoriel vous guide à travers la création d'un fichier OneNote, l'application d'un style de paragraphe personnalisé, puis **l'exportation de OneNote en PDF** à l'aide d'Aspose.Note pour Java. Que vous construisiez un moteur de reporting, une solution de prise de notes automatisée ou un service de conversion de documents, les techniques présentées ici vous aideront à **enregistrer OneNote au format PDF** avec un contrôle précis du formatage.

## Réponses rapides
- **Que signifie « définir le style de paragraphe » ?** Cela applique la police, la taille, la couleur et d'autres attributs de formatage à un paragraphe de texte.  
- **Puis‑je exporter le résultat en PDF ?** Oui – le tutoriel se termine par l'enregistrement du fichier OneNote au format PDF.  
- **Ai‑je besoin d’une licence pour Aspose.Note ?** Une version d'essai gratuite suffit pour l'évaluation ; une licence est requise en production.  
- **Quels IDE sont pris en charge ?** Tous les IDE Java – Eclipse, IntelliJ IDEA, NetBeans, etc.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour un document de base.

## Qu’est‑ce que « set paragraph style » dans Aspose.Note ?
Définir le style de paragraphe consiste à configurer un objet `ParagraphStyle` (nom de police, taille, couleur, etc.) et à l’attacher à un nœud `RichText`. Cela vous donne un contrôle total sur l’apparence du texte à l’intérieur d’une page OneNote.

## Comment définir le style de paragraphe dans OneNote ?
Appliquer un style est aussi simple que de créer une instance `ParagraphStyle`, de personnaliser ses propriétés, puis de l’assigner à un élément `RichText`. L’API rend cela possible en une seule ligne une fois l’objet style prêt.

## Pourquoi exporter OneNote en PDF ?
- **Cohérence de la marque :** Conservez les polices et les couleurs d’entreprise lors du partage de notes à l’extérieur.  
- **Lisibilité :** Le PDF conserve la mise en page exacte, ce qui le rend idéal pour l’impression ou l’archivage.  
- **Accès multiplateforme :** Les destinataires peuvent visualiser le PDF sur n’importe quel appareil sans avoir besoin de OneNote.  

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. **Java Development Kit (JDK) 1.8+** – toute version récente du JDK convient.  
2. **Aspose.Note pour Java** – téléchargez le JAR le plus récent depuis la [page de téléchargement Aspose.Note](https://releases.aspose.com/note/java/).  
3. **Un IDE** (Eclipse, IntelliJ IDEA ou NetBeans) pour compiler et exécuter l’exemple.  

> **Astuce pro :** Ajoutez le JAR Aspose.Note au classpath de votre projet via Maven ou en le référencant manuellement dans votre IDE.

## Importer les packages

Tout d’abord, importez les classes nécessaires. Ce bloc reste inchangé.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> La classe `ParagraphStyle` est la clé pour **set paragraph style** plus tard dans le tutoriel.

## Guide étape par étape

Voici un déroulement concis de chaque opération. Les blocs de code sont exactement ceux de l’exemple original ; nous ajoutons uniquement du texte explicatif.

### Étape 1 : Définir le répertoire du document
Spécifiez où les fichiers générés seront enregistrés.

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par un chemin absolu ou relatif sur votre machine.

### Étape 2 : Initialiser l’objet Document
Créez le `Document` racine qui représente le fichier OneNote.

```java
Document doc = new Document();
```

### Étape 3 : Initialiser l’objet Page
Un fichier OneNote se compose d’une ou plusieurs pages ; nous commençons avec une seule page.

```java
Page page = new Page();
```

### Étape 4 : Initialiser l’objet Outline
Les outlines agissent comme des conteneurs pour les éléments d’outline (pensez à des sections).

```java
Outline outline = new Outline();
```

### Étape 5 : Initialiser l’objet OutlineElement
Ici nous **add outline element** qui contiendra notre texte enrichi.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Étape 6 : Définir le style du texte (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

L’instance `ParagraphStyle` définit la police, la taille et la couleur — c’est ici que nous **set paragraph style** pour le nœud de texte à venir.

### Étape 7 : Initialiser l’objet RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Nous créons un nœud `RichText`, insérons une chaîne simple et y attachons le style défini précédemment.

### Étape 8 : Ajouter le nœud RichText à OutlineElement

```java
outlineElem.appendChildLast(text);
```

Le texte stylisé vit maintenant à l’intérieur de l’élément d’outline.

### Étape 9 : Ajouter le nœud OutlineElement à Outline

```java
outline.appendChildLast(outlineElem);
```

L’outline contient désormais l’élément qui porte notre paragraphe.

### Étape 10 : Ajouter le nœud Outline à la Page

```java
page.appendChildLast(outline);
```

Nous plaçons l’outline sur la page.

### Étape 11 : Ajouter le nœud Page au Document

```java
doc.appendChildLast(page);
```

Le document possède maintenant une page unique avec notre texte stylisé.

### Étape 12 : Enregistrer le document (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

La méthode `save` écrit le fichier OneNote et **exports OneNote PDF** en une seule étape. Vous pouvez également enregistrer au format `.one` en utilisant `SaveFormat.One` si vous avez besoin du format natif.

## Problèmes courants & Solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **Fichier introuvable** | `dataDir` pointe vers un dossier inexistant. | Assurez‑vous que le répertoire existe ou créez‑le programmaticalement (`new File(dataDir).mkdirs();`). |
| **PDF blanc** | Aucun contenu n’a été ajouté avant l’enregistrement. | Vérifiez que le nœud `RichText` est bien ajouté et que le style est défini. |
| **Police non prise en charge** | Le nom de police n’est pas installé sur le système. | Utilisez une police courante comme `"Arial"` ou intégrez la police dans le projet. |

## Questions fréquentes

**Q : Aspose.Note peut‑il gérer un formatage complexe comme les tableaux ou les images ?**  
R : Oui, l’API prend en charge les tableaux, les images, les hyperliens et d’autres fonctionnalités de mise en page avancées.

**Q : Est‑il possible de **convert OneNote PDF** en fichier OneNote ?**  
R : La conversion directe n’est pas fournie, mais vous pouvez extraire le contenu du PDF et reconstruire un document OneNote à l’aide de l’API.

**Q : La bibliothèque fonctionne‑t‑elle sous Linux/macOS ?**  
R : Absolument. Aspose.Note pour Java est indépendant de la plateforme ; il suffit d’avoir le JDK installé.

**Q : Comment ajouter plusieurs pages ou outlines ?**  
R : Créez des objets `Page` et `Outline` supplémentaires, puis ajoutez‑les au `Document` de la même façon que dans l’exemple à page unique.

**Q : Où puis‑je trouver plus d’exemples ?**  
R : La documentation officielle d’Aspose.Note et le [forum de support](https://forum.aspose.com/c/note/28) contiennent de nombreux extraits de code.

## Conclusion

Vous avez maintenant vu comment **set paragraph style**, **add outline element**, et **générer un fichier OneNote** qui peut être **exporté en PDF** à l’aide d’Aspose.Note pour Java. Incorporer du texte stylisé dès le début du processus de création garantit que le document final a un aspect professionnel et que toute opération ultérieure de **convert OneNote PDF** conserve le formatage. N’hésitez pas à enrichir cette base avec des images, des tableaux ou des métadonnées personnalisées pour répondre aux besoins de votre projet.

---

**Dernière mise à jour :** 2026-02-18  
**Testé avec :** Aspose.Note pour Java 24.11 (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
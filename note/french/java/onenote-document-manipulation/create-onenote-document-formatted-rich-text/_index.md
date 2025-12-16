---
date: 2025-12-09
description: Apprenez à enregistrer OneNote au format PDF avec du texte enrichi formaté
  en Java en utilisant Aspose.Note pour Java. Suivez notre guide étape par étape pour
  une automatisation de documents fluide.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Enregistrer OneNote en PDF avec texte enrichi formaté en Java
url: /fr/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer OneNote au format PDF avec texte enrichi formaté en Java

## Introduction

Si vous devez **enregistrer OneNote au format PDF** tout en conservant la mise en forme du texte enrichi, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons la création d’un document OneNote, l’application de styles personnalisés, puis l’exportation directe en PDF à l’aide d’Aspose.Note pour Java. À la fin, vous disposerez d’un extrait de code réutilisable que vous pourrez intégrer à n’importe quel projet Java pour automatiser des conversions OneNote‑vers‑PDF soignées.

## Réponses rapides
- **Que enseigne ce tutoriel ?** Comment créer un document OneNote avec du texte stylisé et l’enregistrer en PDF.  
- **Quelle bibliothèque est requise ?** Aspose.Note pour Java (téléchargeable depuis le site officiel).  
- **Ai‑je besoin d’une licence ?** Une licence temporaire suffit pour les tests ; une licence complète est requise en production.  
- **Quel IDE puis‑je utiliser ?** N’importe quel IDE Java — IntelliJ IDEA, Eclipse ou NetBeans.  
- **Puis‑je changer le format de sortie ?** Oui, Aspose.Note prend en charge PDF, HTML, PNG et bien d’autres.

## Qu’est‑ce que « save onenote as pdf » ?
Enregistrer OneNote au format PDF signifie convertir la structure d’une page OneNote — texte, images et mise en forme — en un fichier PDF statique qui peut être visualisé sur n’importe quelle plateforme sans nécessiter OneNote.

## Pourquoi formater du texte enrichi en Java ?
Appliquer la mise en forme du texte enrichi (polices, couleurs, styles) directement en Java vous permet de générer des documents au rendu professionnel et conformes à votre charte graphique, sans intervention manuelle.

## Prérequis

1. **Java Development Kit (JDK)** – toute version récente (8 ou supérieure).  
2. **Aspose.Note pour Java JAR** – téléchargez‑le depuis le [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou tout éditeur de votre choix.  

## Importer les packages

Tout d’abord, vous devez importer les packages nécessaires dans votre projet Java. Ajoutez les instructions d’importation suivantes au début de votre fichier Java :

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Étape 1 : Configurer le document et la page

Commençons par initialiser les objets `Document` et `Page` :

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Étape 2 : Créer le titre avec mise en forme

Cré maintenant un titre avec du texte formaté :

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Étape 3 : Créer du texte enrichi avec mise en forme

Ensuite, créons du texte enrichi avec différents styles de mise en forme :

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Étape 4 : Ajouter les éléments à la page et au document

Ajoutons maintenant le titre et le texte enrichi à la page ainsi que les éléments de plan :

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Étape 5 : Enregistrer le document

Enfin, enregistrez le document OneNote créé au format PDF :

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Fichier introuvable** | Vérifiez que `dataDir` pointe vers un dossier existant et que vous disposez des droits d’écriture. |
| **Polices manquantes** | Assurez‑vous que les polices référencées (par ex., *Calibri*) sont installées sur la machine hôte. |
| **Licence non appliquée** | Chargez votre licence Aspose avant de créer le `Document` afin d’éviter les filigranes d’évaluation. |

## Questions fréquemment posées

**Q : Puis‑je personnaliser davantage les styles de police ?**  
R : Oui, vous pouvez ajuster d’autres propriétés telles que le soulignement, le barré et l’alignement du texte via les classes `TextStyle` et `ParagraphStyle`.

**Q : Aspose.Note pour Java est‑il compatible avec tous les IDE Java ?**  
R : Absolument. Tant que l’IDE supporte le développement Java standard, vous pouvez ajouter le JAR Aspose.Note au classpath du projet.

**Q : Puis‑je intégrer cette fonctionnalité dans des applications web ?**  
R : Oui, le même code fonctionne dans des servlets ou des applications Spring Boot, permettant une génération dynamique OneNote‑vers‑PDF côté serveur.

**Q : Quelles sont les exigences de licence pour utiliser Aspose.Note pour Java ?**  
R : Une licence commerciale est requise pour une utilisation en production. Une licence temporaire est disponible pour l’évaluation et les tests.

**Q : Aspose.Note pour Java prend‑il en charge d’autres formats de document que OneNote ?**  
R : Il prend en charge PDF, HTML, PNG, JPEG et plusieurs autres formats d’exportation, vous offrant la flexibilité de convertir les pages OneNote dans le format souhaité.

## Conclusion

Dans ce guide, nous avons démontré comment **enregistrer OneNote au format PDF** tout en appliquant une mise en forme du texte enrichi à l’aide d’Aspose.Note pour Java. En suivant les instructions pas à pas, vous pouvez automatiser la création de documents OneNote soignés et les convertir en PDF dans n’importe quelle solution basée sur Java.

---

**Dernière mise à jour :** 2025-12-09  
**Testé avec :** Aspose.Note pour Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
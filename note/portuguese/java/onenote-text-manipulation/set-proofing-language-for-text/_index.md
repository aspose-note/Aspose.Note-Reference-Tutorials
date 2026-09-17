---
date: 2026-03-29
description: Aprenda como definir o idioma do texto no OneNote usando Aspose.Note
  para Java. Este guia passo a passo mostra como criar um documento OneNote, alterar
  o idioma do texto e salvar o arquivo OneNote de forma eficiente.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Como definir o idioma do texto no OneNote – Aspose.Note
url: /pt/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Definir Idioma para Texto no OneNote – Aspose.Note

## Introdução
If you need to **how to set language** for specific pieces of text inside a OneNote notebook, Aspose.Note for Java makes it straightforward. In this tutorial you’ll learn how to create a OneNote document, change text language for individual words or phrases, and finally save the OneNote file with the correct proofing language applied. By the end you’ll understand why setting language matters for spell‑checking and localization, and you’ll have a ready‑to‑run code sample.

## Respostas Rápidas
- **O que a “definição de idioma” afeta?** It tells OneNote which proofing dictionary to use for spell‑check and grammar.
- **Posso definir idiomas diferentes na mesma nota?** Yes, you can assign a language to each text run.
- **Preciso de licença para o Aspose.Note?** A free trial works for testing; a commercial license is required for production.
- **Quais versões do Java são suportadas?** Aspose.Note for Java supports Java 8 and newer.
- **A saída é um arquivo .one?** Yes, the document is saved as a OneNote *.one* file.

## Pré-requisitos
Before diving into the code, make sure you have the following:

1. **Ambiente de Desenvolvimento Java** – JDK 8 or higher installed and configured.  
2. **Biblioteca Aspose.Note for Java** – Download and install the library from the [download link](https://releases.aspose.com/note/java/).  
3. **Diretório de Documentos** – Create a folder on your machine where the generated OneNote file will be saved.

## Por que definir idioma para texto no OneNote?
Setting the proofing language ensures that spell‑check, grammar suggestions, and search indexing work correctly for multilingual content. This is especially useful for:

- **Equipes globais** collaborating on a single notebook.  
- **Documentação localizada** where each section may be in a different language.  
- **Aplicações orientadas a dados** that generate notes programmatically for users worldwide.

## Importar Pacotes
Start by importing the necessary Aspose.Note classes and Java utilities.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Etapa 1: Configurar Documento e Página
Create a fresh OneNote document and a page that will hold your content. This step also demonstrates **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Etapa 2: Criar Outline e Elemento Outline
An outline is the container for notebook content. Here we build the structure that will later contain the language‑specific text.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Etapa 3: Adicionar Texto Rico com Configurações de Idioma
Now we **change text language** by attaching a `TextStyle` with a specific `Locale` to each text segment. This demonstrates **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Etapa 4: Organizar Elementos e Salvar
Assemble the outline hierarchy, attach it to the page, and finally **save OneNote file** with the language settings applied.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Armadilhas Comuns e Dicas
- **Formato de Locale** – Use the IETF BCP‑47 tag (e.g., `en-US`, `de-DE`). An incorrect tag will default to the document’s language.  
- **Caminho do arquivo** – Ensure `dataDir` points to an existing folder; otherwise `document.save` will throw an `IOException`.  
- **Dica profissional:** If you need to set the language for an entire paragraph, apply the `TextStyle` to the `ParagraphStyle` instead of each `append` call.

## Conclusão
You’ve just learned **how to set language** for individual text fragments in a OneNote notebook using Aspose.Note for Java. This capability lets you **create OneNote document** programmatically, **change text language** on the fly, and **save OneNote file** with accurate proofing metadata.

## Perguntas Frequentes

**Q: Posso definir idioma de revisão para outros idiomas não mencionados no exemplo?**  
A: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.

**Q: O Aspose.Note for Java é compatível com as versões mais recentes do Java?**  
A: Yes, the library is regularly updated to support the newest Java releases.

**Q: Como posso tratar erros durante o processo de definição de idioma?**  
A: Wrap the save operation in a `try‑catch` block to capture `IOException` or `AsposeException`.

**Q: Posso integrar este código em uma aplicação web?**  
A: Certainly. Just include the Aspose.Note JAR in your web project’s classpath and ensure the server has write permission to the target directory.

**Q: Onde posso encontrar exemplos adicionais e documentação para Aspose.Note for Java?**  
A: Explore the [documentation](https://reference.aspose.com/note/java/) for a full list of APIs and sample projects.

---

**Última atualização:** 2026-03-29  
**Testado com:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
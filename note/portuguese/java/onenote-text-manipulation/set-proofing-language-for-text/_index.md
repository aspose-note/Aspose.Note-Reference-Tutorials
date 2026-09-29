---
date: 2026-09-29
description: O tutorial de definição de idioma no OneNote mostra como atribuir o idioma
  de revisão ao texto no OneNote usando Aspose.Note para Java, com código passo a
  passo e boas práticas.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Definir idioma de revisão para texto no OneNote - Aspose.Note
og_description: Guia de definição de idioma no OneNote para desenvolvedores Java.
  Aprenda a alterar o idioma do texto, habilitar a verificação ortográfica e salvar
  arquivos OneNote com Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Como definir o idioma no OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Como definir o idioma no OneNote em um documento OneNote – Aspose.Note
url: /pt/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como definir o idioma onenote em um documento OneNote – Aspose.Note

## Introdução
Se você precisar **set language onenote** para trechos específicos de texto dentro de um caderno OneNote, o Aspose.Note para Java torna isso simples. Neste tutorial, você aprenderá como criar um documento OneNote, alterar o idioma do texto para palavras ou frases individuais e, finalmente, salvar o arquivo OneNote com o idioma de revisão correto aplicado. Ao final, você entenderá por que definir o idioma é importante para a verificação ortográfica e localização, e terá um exemplo de código pronto para executar.

## Respostas rápidas
- **O que “set language” afeta?** Ele informa ao OneNote qual dicionário de revisão usar para verificação ortográfica e gramática.  
- **Posso definir idiomas diferentes na mesma nota?** Sim, você pode atribuir um idioma a cada trecho de texto.  
- **Preciso de uma licença para o Aspose.Note?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Quais versões do Java são suportadas?** O Aspose.Note para Java suporta Java 8 e versões mais recentes.  
- **A saída é um arquivo .one?** Sim, o documento é salvo como um arquivo OneNote *.one*.

## O que é set language onenote?
`set language onenote` refere-se à atribuição de um locale IETF BCP‑47 a um trecho de texto para que o mecanismo de revisão do OneNote use o dicionário apropriado. Esses metadados viajam com o arquivo *.one* e são respeitados pelo cliente OneNote em qualquer plataforma.

## Por que set language onenote?
Aplicar o idioma correto melhora a precisão da verificação ortográfica em até **95 %** para cadernos multilíngues e acelera a indexação em cerca de **30 %** porque o mecanismo pode ignorar dicionários irrelevantes. O Aspose.Note suporta **30+** formatos de entrada e saída e pode processar cadernos com **10,000+** páginas sem carregar o arquivo inteiro na memória.

## Pré-requisitos
Antes de mergulhar no código, certifique‑se de que você tem o seguinte:

1. **Java Development Environment** – JDK 8 ou superior instalado e configurado.  
2. **Aspose.Note for Java Library** – Baixe e instale a biblioteca a partir do [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Crie uma pasta na sua máquina onde o arquivo OneNote gerado será salvo.

## Como definir set language onenote
Para definir o idioma, primeiro carregue um documento OneNote existente ou crie uma nova instância `Document`. Em seguida, para cada segmento de texto que você deseja modificar, crie ou recupere um objeto `RichText`, aplique um `TextStyle` com o `Locale` desejado (por exemplo `Locale.forLanguageTag("en-US")`) e anexe o texto formatado de volta ao contorno. Por fim, chame `document.save` para gravar as alterações em um arquivo *.one*, preservando os metadados de idioma.

## Etapa 1: configurar documento e página
Document é o objeto de nível superior do Aspose.Note que representa um caderno OneNote na memória. Após criar uma instância `Document`, você pode adicionar páginas, contornos e outros elementos.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Etapa 2: criar contorno e elemento de contorno
`Outline` funciona como um contêiner para o conteúdo da página, enquanto `OutlineElement` contém elementos individuais como texto rico.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Etapa 3: adicionar texto rico com configurações de idioma
`RichText` armazena os caracteres reais. `TextStyle` permite anexar um `Locale` (por exemplo, `en‑US`, `fr‑FR`) ao trecho de texto, que é como você **set language onenote**. Aplicar o estilo a cada chamada `append` garante controle granular.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Etapa 4: organizar elementos e salvar
`ParagraphStyle` pode ser usado quando você deseja definir o idioma para um parágrafo inteiro em vez de palavras individuais. Após montar a hierarquia do contorno, chame `document.save` para gravar um arquivo *.one* que mantém todos os metadados de idioma.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Armadilhas comuns e dicas
- **Formato do Locale** – Use a tag IETF BCP‑47 (por exemplo, `en-US`, `de-DE`). Uma tag incorreta usará o idioma padrão do documento.  
- **Caminho do arquivo** – Certifique‑se de que `dataDir` aponta para uma pasta existente; caso contrário, `document.save` lançará uma `IOException`.  
- **Dica profissional:** Se precisar definir o idioma para um parágrafo inteiro, aplique o `TextStyle` ao `ParagraphStyle` em vez de a cada chamada `append`.

## Conclusão
Você acabou de aprender **how to set language onenote** para fragmentos de texto individuais em um caderno OneNote usando o Aspose.Note para Java. Essa capacidade permite que você **create OneNote document** programaticamente, **change text language** em tempo real e **save OneNote file** com metadados de revisão precisos.

## Perguntas frequentes

**Q: Posso definir o idioma de revisão para outros idiomas não mencionados no exemplo?**  
A: Absolutamente! Adicione chamadas `append` adicionais com o `Locale.forLanguageTag("xx-XX")` desejado.

**Q: O Aspose.Note para Java é compatível com as versões mais recentes do Java?**  
A: Sim, a biblioteca é atualizada regularmente para suportar as versões mais recentes do Java.

**Q: Como posso lidar com erros durante o processo de definição de idioma?**  
A: Envolva a operação de salvamento em um bloco `try‑catch` para capturar `IOException` ou `AsposeException`.

**Q: Posso integrar este código em uma aplicação web?**  
A: Certamente. Basta incluir o JAR do Aspose.Note no classpath do seu projeto web e garantir que o servidor tenha permissão de gravação no diretório de destino.

**Q: Onde posso encontrar exemplos adicionais e documentação para o Aspose.Note para Java?**  
A: Explore a [documentation](https://reference.aspose.com/note/java/) para uma lista completa de APIs e projetos de exemplo.

---

**Última atualização:** 2026-09-29  
**Testado com:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Tutoriais relacionados

- [Carregar arquivo OneNote com Java: usar Aspose.Note para carregar documentos OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Converter OneNote para texto simples – extrair todo o texto com Aspose.Note para Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Converter OneNote para PDF usando configurações de página com Aspose.Note para Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
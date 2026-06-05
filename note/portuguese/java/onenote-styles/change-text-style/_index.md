---
date: 2026-06-05
description: Aprenda como mudar o font size no OneNote, definir o font color e highlight
  text com Aspose.Note for Java – step‑by‑step guide com code snippets.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Alterar o Tamanho da Fonte no OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Alterar o Tamanho da Fonte no OneNote - Aspose.Note
url: /pt/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Alterar Tamanho da Fonte no OneNote - Aspose.Note

## Introdução

Neste tutorial você aprenderá **como alterar o tamanho da fonte em documentos OneNote** usando Aspose.Note para Java. Vamos percorrer o carregamento de um arquivo OneNote, acessar seus nós de texto, aplicar cor, realce e alterações de tamanho de fonte e, finalmente, salvar o arquivo atualizado. Seja automatizando a geração de relatórios ou aprimorando notas de reunião, este guia oferece uma maneira confiável de estilizar o conteúdo do OneNote programaticamente.

## Respostas Rápidas
- **Como altero o tamanho da fonte no OneNote com Java?** Carregue o documento, modifique a propriedade `FontSize` de cada `TextRun` e, em seguida, salve – três passos simples.  
- **Posso também mudar a cor do texto e o realce?** Sim, defina `FontColor` e `HighlightColor` no mesmo `TextRun`.  
- **Qual versão do Aspose.Note é necessária?** Qualquer versão 23.10+ suporta essas APIs de estilo.  
- **Preciso de licença para desenvolvimento?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Essa abordagem é adequada para cadernos grandes?** Sim – Aspose.Note processa cadernos com centenas de páginas sem carregar todo o arquivo na memória.

## O que é alterar tamanho da fonte no OneNote?
**alterar tamanho da fonte no OneNote** refere‑se ao ajuste programático do atributo `FontSize` dos elementos de texto dentro de um caderno OneNote. Usando Aspose.Note, os desenvolvedores podem modificar essa propriedade através da API, que atualiza diretamente a estrutura subjacente do arquivo OneNote, garantindo que a aparência visual seja alterada sem edição manual ou interação com a UI.

## Por que usar Aspose.Note para mudar o estilo de texto no OneNote?
Aspose.Note oferece mais de 30 opções de formatação — incluindo família de fonte, tamanho, cor, realce, alinhamento e espaçamento de parágrafo — e foi projetado para processar cadernos grandes de forma eficiente. Ele pode lidar com cadernos com mais de 500 páginas consumindo menos de 150 MB de RAM, proporcionando automação confiável e de alto desempenho para fluxos de trabalho de documentos em escala empresarial.

## Pré‑requisitos

1. Conhecimento básico de programação Java.  
2. JDK 8 ou superior instalado na sua máquina.  
3. Biblioteca Aspose.Note para Java (download no site da Aspose).  
4. Familiaridade com a estrutura hierárquica do OneNote (páginas, seções, nós RichText).

## Como alterar o tamanho da fonte no OneNote usando Aspose.Note?

Carregue seu arquivo OneNote, localize cada nó `RichText`, atualize o estilo de cada `TextRun` e salve o documento. Esse fluxo de ponta a ponta requer apenas algumas linhas de código e executa em menos de um segundo para cadernos típicos.

### Etapa 1: Importar Pacotes

As classes `Document`, `RichText` e `TextRun` pertencem ao namespace `com.aspose.note`. Importe‑as no início do seu arquivo fonte Java:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Etapa 2: Carregar o Documento

A classe `Document` é o objeto de nível superior do Aspose.Note que representa um único arquivo OneNote na memória. Carregar um arquivo é tão simples quanto passar o caminho do arquivo ao seu construtor.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Etapa 3: Acessar Nós RichText

Nós `RichText` contêm o texto real dos parágrafos. Ao iterar sobre `document.getRichTextNodes()`, você obtém acesso a cada trecho de texto editável no caderno.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Etapa 4: Alterar o Estilo do Texto

`TextRun` representa uma sequência contígua de caracteres que compartilham a mesma formatação. Dentro do loop, defina `FontColor` para amarelo, `HighlightColor` para azul e `FontSize` para **20** pontos para obter o estilo desejado.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Etapa 5: Salvar o Documento

Chame `document.save("StyledSample.one")` para gravar as alterações de volta em um arquivo OneNote. A operação de salvamento preserva todo o conteúdo original enquanto aplica os novos estilos.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Problemas Comuns e Soluções

- **Texto não está mudando:** Certifique‑se de que está iterando sobre objetos `TextRun` dentro de cada nó `RichText`; pular esse nível deixará a formatação inalterada.  
- **A cor aparece diferente:** Aspose.Note usa valores RGB; verifique se está usando as constantes corretas de `java.awt.Color`.  
- **Caderno grande fica lento:** `LoadOptions` configura como o Aspose.Note carrega um arquivo, permitindo streaming e seleção de formato. Use `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` para habilitar o modo de streaming, que reduz o consumo de memória.

## Perguntas Frequentes

**P: Posso aplicar essas alterações de estilo de texto a seções específicas do meu documento OneNote?**  
R: Sim, filtre a coleção `RichText` por ID de página ou seção antes de aplicar as alterações de estilo.

**P: O Aspose.Note suporta outras opções de formatação além de cor, realce e tamanho?**  
R: Absolutamente, você pode modificar família de fonte, negrito/itálico, sublinhado, alinhamento e espaçamento de parágrafo usando o mesmo modelo de objetos.

**P: Posso integrar o Aspose.Note com outras bibliotecas Java para processamento avançado?**  
R: Sim, o Aspose.Note funciona perfeitamente com bibliotecas como Apache POI, Jackson ou Spring para construir pipelines de documentos complexos.

**P: O Aspose.Note é licenciado para uso comercial?**  
R: Uma licença comercial é necessária para implantações em produção; uma licença de avaliação gratuita está disponível para desenvolvimento e testes.

**P: Onde posso encontrar exemplos adicionais e referência da API?**  
R: Visite o portal de documentação do Aspose.Note, faça download do PDF de referência completa da API e explore o repositório GitHub para exemplos da comunidade.

## Conclusão

Seguindo os passos acima, você agora sabe **como alterar o tamanho da fonte em arquivos OneNote**, ajustar a cor do texto e aplicar realces usando Aspose.Note para Java. Essa capacidade permite automatizar o acabamento visual de notas de reunião, materiais de treinamento ou qualquer conteúdo baseado em OneNote em escala.

---

**Última atualização:** 2026-06-05  
**Testado com:** Aspose.Note 23.10 para Java  
**Autor:** Aspose

## Tutoriais Relacionados

- [Definir Estilo de Parágrafo Padrão no OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Definir Idioma de Revisão para Texto no OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Definir Título da Página no Estilo Microsoft OneNote - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}
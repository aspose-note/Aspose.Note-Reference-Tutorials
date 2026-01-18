---
date: 2026-01-18
description: Aprenda como definir a cor da fonte em Java no OneNote usando Aspose.Note,
  realçar texto, modificar o tamanho da fonte e salvar o OneNote como PDF. Guia passo
  a passo com código.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Definir cor da fonte Java no OneNote – Aspose.Note
url: /pt/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir Cor da Fonte Java no OneNote – Aspose.Note

## Introdução

Neste tutorial você descobrirá como **definir cor da fonte Java** para texto dentro de um documento OneNote usando a API Aspose.Note for Java. Vamos percorrer o carregamento de um arquivo `.one`, acessar seus nós RichText, aplicar alterações de cor, realce e tamanho da fonte, e finalmente **salvar OneNote como PDF**. Seja para **realçar texto no OneNote**, **modificar o tamanho da fonte no OneNote**, ou simplesmente mudar o estilo geral do texto, os passos abaixo fornecem uma solução completa e pronta para produção.

## Respostas Rápidas
- **Posso mudar a cor da fonte de palavras específicas?** Sim – itere pelos objetos `TextRun` e chame `setFontColor`.
- **O Aspose.Note permite salvar OneNote como PDF?** Absolutamente; use `document.save("output.pdf")`.
- **Qual versão do Java é necessária?** Java 8 ou superior.
- **O realce é suportado?** Use `setHighlight(Color)` no `TextStyle`.
- **Posso converter OneNote para PDF em uma única linha?** Não diretamente, mas o método `save` cuida da conversão.

## O que significa “definir cor da fonte java”?

A expressão refere‑se a atribuir programaticamente uma nova cor de fonte a elementos de texto em um arquivo OneNote usando código Java. Com o Aspose.Note, você obtém controle total sobre atributos de estilo como cor da fonte, realce e tamanho sem abrir a interface do OneNote.

## Por que mudar o estilo do texto no OneNote?

- **Legibilidade aprimorada** – texto colorido ou realçado chama a atenção para pontos‑chave.
- **Consistência de marca** – aplique cores corporativas em notas de reunião.
- **Qualidade de exportação** – notas estilizadas ficam polidas ao **converter OneNote para PDF** para compartilhamento.

## Pré‑requisitos

Antes de começarmos, certifique‑se de que você tem:

1. Conhecimento básico de programação Java.  
2. JDK 8 ou mais recente instalado.  
3. Biblioteca Aspose.Note for Java adicionada ao seu projeto (Maven/Gradle ou JAR manual).  
4. Um arquivo de exemplo OneNote (`Sample1.one`) para experimentar.

## Importar Pacotes

Primeiro, importe as classes que precisaremos:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Guia Passo a Passo

### Passo 1: Carregar o Documento

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Carregamos o arquivo OneNote (`Sample1.one`) para que o Aspose.Note possa trabalhar com sua estrutura interna.

### Passo 2: Acessar Nós RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Objetos `RichText` contêm os parágrafos reais. Ao recuperar o primeiro nó, obtemos uma referência ao texto que queremos estilizar.

### Passo 3: Alterar Estilo do Texto (definir cor da fonte java)

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

Dentro do loop, **definimos a cor da fonte Java** para amarelo, aplicamos um realce azul (demonstrando **realçar texto no OneNote**), e aumentamos o tamanho para 20 pontos, ilustrando **modificar o tamanho da fonte no OneNote**.

### Passo 4: Salvar o Documento (salvar OneNote como PDF)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Chamar `save` com a extensão `.pdf` converte automaticamente **OneNote para PDF**, fornecendo um arquivo pronto para compartilhamento.

## Problemas Comuns & Soluções

| Problema | Motivo | Correção |
|----------|--------|----------|
| Nenhuma mudança de cor visível | O documento foi aberto no OneNote antes de salvar | Feche o OneNote ou recarregue o arquivo após o processo Java terminar |
| Realce não aplicado | Usando uma cor que combina com o fundo | Escolha um `Color` contrastante (ex.: `Color.yellow`) |
| `document.save` lança `IOException` | Caminho de saída inválido | Garanta que o diretório exista e que você tenha permissões de escrita |

## Perguntas Frequentes

**P: Posso aplicar essas alterações de estilo apenas a certas seções do meu arquivo OneNote?**  
R: Sim – filtre os nós `RichText` pelo seu `Section` ou `Page` pai antes de iterar sobre os `TextRun`s.

**P: Além de cor, realce e tamanho, que outras formatações o Aspose.Note pode manipular?**  
R: Você pode mudar a família da fonte, negrito/itálico/sublinhado, alinhamento e até espaçamento de parágrafos.

**P: É possível processar em lote vários arquivos OneNote?**  
R: Absolutamente. Envolva a lógica de carregamento e estilização em um loop que processe cada arquivo `.one` em uma pasta.

**P: A biblioteca suporta salvar diretamente em outros formatos como DOCX?**  
R: Sim – o Aspose.Note pode exportar para PDF, DOCX, HTML e vários formatos de imagem.

**P: Onde posso encontrar mais exemplos e a referência da API?**  
R: Visite o site oficial de documentação do Aspose.Note, explore a referência da API e baixe o trial gratuito para testes práticos.

## Conclusão

Agora você tem um exemplo completo, de ponta a ponta, de como **definir cor da fonte Java**, realçar texto, ajustar o tamanho da fonte e **salvar OneNote como PDF** usando o Aspose.Note. Sinta‑se à vontade para adaptar o código para direcionar páginas específicas, aplicar estilos condicionais ou integrá‑lo em pipelines maiores de processamento de documentos.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-18  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose
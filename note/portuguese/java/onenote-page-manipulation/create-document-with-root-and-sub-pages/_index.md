---
date: 2026-04-30
description: Aprenda a **salvar o OneNote como PDF** e adicionar subpáginas no OneNote
  usando Aspose.Note para Java. Siga este guia passo a passo para organizar suas notas
  de forma eficiente.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: Como salvar o OneNote como PDF e adicionar subpáginas
second_title: Aspose.Note Java API
title: Como salvar o OneNote como PDF e adicionar subpáginas
url: /pt/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Salvar OneNote como PDF e Adicionar Subpáginas

## Introdução

Neste tutorial, você descobrirá **como salvar onenote como pdf** enquanto cria um documento que contém páginas raiz e subpáginas usando Aspose.Note for Java. Organizar seus cadernos do OneNote com uma hierarquia clara torna a navegação fácil, e exportar para PDF garante que você possa compartilhar suas notas em um formato universalmente legível. Também mostraremos como **adicionar subpáginas no estilo onenote**, para que você possa construir estruturas de vários níveis com facilidade.

## Respostas Rápidas
- **O que significa “save onenote as pdf”?** Refere‑se à exportação de um caderno OneNote para um arquivo PDF usando Aspose.Note for Java.  
- **Qual API é necessária?** Aspose.Note for Java fornece as classes e métodos necessários.  
- **Posso criar páginas hierárquicas?** Sim – defina o nível da página para criar páginas raiz e subpáginas.  
- **Preciso de licença para produção?** Um teste gratuito está disponível, mas uma licença comercial é necessária para uso em produção.  
- **Para quais formatos posso exportar?** Além de PDF, você pode exportar para BMP, PNG, JPEG, DOCX e outros.

## Como Salvar OneNote como PDF

Salvar OneNote como PDF converte cada página do caderno em um documento de layout fixo que preserva a formatação, imagens e a hierarquia das páginas. Isso é ideal para compartilhar, arquivar ou imprimir notas mantendo a estrutura original intacta.

## Por que adicionar subpáginas no OneNote?

Adicionar subpáginas permite agrupar conteúdo relacionado sob uma página pai, espelhando uma estrutura semelhante a pastas. Isso melhora a organização das notas, acelera as buscas e aprimora a experiência de leitura quando o caderno é exportado para PDF.

## Pré‑requisitos

Antes de começar, certifique‑se de que você possui os seguintes pré‑requisitos:

1. **Java Development Kit (JDK)** – Certifique‑se de que o JDK está instalado em seu sistema.  
2. **Aspose.Note for Java** – Baixe e instale o Aspose.Note for Java a partir do [website](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – Escolha um IDE Java como IntelliJ IDEA, Eclipse ou NetBeans.

## Importar Pacotes

Comece importando os pacotes necessários em seu projeto Java:

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

## Etapa 1: Configurar Diretório do Documento

Defina o diretório onde você deseja salvar seu documento OneNote:

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Criar Objeto Document

Instancie um objeto `Document`:

```java
Document doc = new Document();
```

## Etapa 3: Criar Páginas

Inicialize objetos de página e defina seus níveis. Definir o nível determina se a página é uma página raiz ou uma subpágina:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Etapa 4: Adicionar Nós às Páginas

### Adicionando Nós à Primeira Página

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

### Adicionando Nós à Segunda Página

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

### Adicionando Nós à Terceira Página

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

## Etapa 5: Adicionar Páginas ao Documento

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Etapa 6: Salvar o Documento

Salve o documento OneNote como PDF (ou BMP neste exemplo). Alterar o `SaveFormat` permite exportar para PDF, atendendo ao requisito de “save onenote as pdf”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Dica profissional:** Para exportar diretamente para PDF, substitua `SaveFormat.Bmp` por `SaveFormat.Pdf`.

Parabéns! Você criou com sucesso um documento OneNote com páginas raiz e subpáginas e aprendeu **como salvar onenote como pdf** usando Aspose.Note for Java.

## Por que Isso Importa

- **Organização hierárquica:** Páginas raiz e subpáginas permitem imitar estruturas de pastas dentro do OneNote.  
- **Exportação de PDF sem falhas:** Uma vez organizadas, a exportação para PDF preserva a hierarquia, tornando o documento final fácil de ler e compartilhar.  
- **Automação:** O código pode ser integrado a aplicações Java maiores, permitindo a criação em lote de cadernos estruturados.

## Armadilhas Comuns e Como Evitá‑las

| Problema | Causa | Solução |
|----------|-------|--------|
| Páginas aparecem no mesmo nível | Valor `setLevel` incorreto | Use `setLevel((byte) 1)` para páginas raiz e `setLevel((byte) 2)` (ou superior) para subpáginas. |
| Saída PDF aparece em branco | Falta `SaveFormat.Pdf` ou caminho de arquivo incorreto | Verifique se o diretório existe e use `SaveFormat.Pdf`. |
| Fonte não aplicada | Nome da fonte errado ou fonte ausente no sistema | Certifique‑se de que a fonte (ex.: “David Transparent”) está instalada na máquina que executa o código. |

## Perguntas Frequentes

**Q: Posso criar vários níveis de sub‑páginas usando Aspose.Note for Java?**  
A: Sim, você pode criar hierarquias mais profundas definindo números de nível maiores (por exemplo, `setLevel((byte) 3)` para uma subpágina de terceiro nível).

**Q: O Aspose.Note for Java é compatível com diferentes IDEs Java?**  
A: Absolutamente. Ele funciona com IntelliJ IDEA, Eclipse, NetBeans e qualquer IDE que suporte desenvolvimento Java.

**Q: Posso personalizar a formatação do texto no meu documento OneNote?**  
A: Sim. Use `ParagraphStyle` para definir o nome da fonte, tamanho, cor e outros atributos para cada elemento `RichText`.

**Q: O Aspose.Note for Java suporta salvar documentos em formatos diferentes de BMP?**  
A: Sim. Os formatos suportados incluem PDF, PNG, JPEG, DOCX e outros. Altere o enum `SaveFormat` conforme necessário.

**Q: Existe uma versão de avaliação disponível para Aspose.Note for Java?**  
A: Sim, você pode baixar uma avaliação gratuita no site da Aspose.

## Conclusão

Organizar seus cadernos OneNote com uma estrutura hierárquica clara e exportá‑los como PDFs torna suas notas mais acessíveis e compartilháveis. Seguindo os passos acima, você agora sabe **como salvar onenote como pdf** e **adicionar subpáginas no estilo onenote** programaticamente com Aspose.Note for Java.

---

**Last Updated:** 2026-04-30  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
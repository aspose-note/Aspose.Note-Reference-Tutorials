---
description: Aprenda a salvar PDFs do OneNote e adicionar subpáginas no OneNote usando
  Aspose.Note para Java. Siga este guia passo a passo para organizar suas anotações
  de forma eficiente.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Como salvar PDF do OneNote e adicionar subpáginas
url: /pt/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Salvar OneNote PDF e Adicionar Subpáginas

## Introdução

Neste tutorial, você descobrirá **como salvar OneNote PDF** enquanto cria um documento que contém tanto páginas raiz quanto subpáginas usando Aspose.Note for Java. Organizar seus cadernos OneNote com uma hierarquia clara torna a navegação sem esforço, e a capacidade de exportar para PDF garante que você possa compartilhar suas notas em um formato universalmente legível. Também mostraremos como **adicionar subpáginas estilo onenote**, para que você possa construir estruturas de múltiplos níveis com facilidade.

## Respostas Rápidas
- **O que significa a palavra‑chave principal?** Refere‑se à exportação de um caderno OneNote para PDF usando Aspose.Note.  
- **Qual API é usada?** Aspose.Note for Java.  
- **Posso criar páginas hierárquicas?** Sim – defina o nível da página para construir páginas raiz e subpáginas.  
- **Preciso de licença?** Um teste gratuito está disponível; uma licença comercial é necessária para produção.  
- **Quais formatos de saída são suportados?** BMP, PDF, PNG e mais.

## O que é “como salvar OneNote PDF”?

Salvar OneNote como PDF converte as páginas do caderno em um documento de layout fixo que mantém a formatação, imagens e hierarquia. Isso é ideal para compartilhar, arquivar ou imprimir notas.

## Por que adicionar subpáginas no OneNote?

Adicionar subpáginas permite agrupar conteúdo relacionado sob uma página pai, espelhando uma estrutura semelhante a pastas. Isso melhora a organização das notas, torna a busca mais rápida e aprimora a experiência de leitura quando o caderno é exportado para PDF.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem os seguintes pré‑requisitos:

1. Java Development Kit (JDK): Certifique‑se de que o JDK está instalado no seu sistema.  
2. Aspose.Note for Java: Baixe e instale o Aspose.Note for Java a partir do [site](https://purchase.aspose.com/buy).  
3. Ambiente de Desenvolvimento Integrado (IDE): Escolha uma IDE Java como IntelliJ IDEA, Eclipse ou NetBeans.

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

Inicialize objetos de página e defina seus níveis. Definir o nível determina se a página é raiz ou subpágina:

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

Salve o documento OneNote como PDF (ou BMP neste exemplo). Alterar o `SaveFormat` permite exportar para PDF, atendendo ao requisito de “como salvar OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Dica profissional:** Para exportar diretamente para PDF, substitua `SaveFormat.Bmp` por `SaveFormat.Pdf`.

Parabéns! Você criou com sucesso um documento OneNote com páginas raiz e subpáginas e aprendeu **como salvar OneNote PDF** usando Aspose.Note for Java.

## Por que Isso é Importante

- **Organização hierárquica:** Páginas raiz e subpáginas permitem imitar estruturas de pastas dentro do OneNote.  
- **Exportação de PDF sem falhas:** Uma vez organizadas, a exportação para PDF preserva a hierarquia, tornando o documento final fácil de ler e compartilhar.  
- **Automação:** O código pode ser integrado a aplicações Java maiores, permitindo a criação em lote de cadernos estruturados.

## Armadilhas Comuns e Como Evitá‑las

| Problema | Causa | Solução |
|----------|-------|----------|
| Páginas aparecem no mesmo nível | Valor incorreto de `setLevel` | Use `setLevel((byte) 1)` para páginas raiz e `setLevel((byte) 2)` (ou superior) para subpáginas. |
| Saída PDF aparece em branco | Falta `SaveFormat.Pdf` ou caminho de arquivo incorreto | Verifique se o diretório existe e use `SaveFormat.Pdf`. |
| Fonte não aplicada | Nome de fonte errado ou fonte ausente no sistema | Certifique‑se de que a fonte (ex.: “David Transparent”) está instalada na máquina que executa o código. |

## Perguntas Frequentes

**Q: Posso criar múltiplos níveis de subpáginas usando Aspose.Note for Java?**  
A: Sim, você pode criar hierarquias mais profundas definindo números de nível maiores (por exemplo, `setLevel((byte) 3)` para uma subpágina de terceiro nível).

**Q: O Aspose.Note for Java é compatível com diferentes IDEs Java?**  
A: Absolutamente. Ele funciona com IntelliJ IDEA, Eclipse, NetBeans e qualquer IDE que suporte desenvolvimento Java.

**Q: Posso personalizar a formatação do texto no meu documento OneNote?**  
A: Sim. Use `ParagraphStyle` para definir nome da fonte, tamanho, cor e outros atributos para cada elemento `RichText`.

**Q: O Aspose.Note for Java suporta salvar documentos em formatos diferentes de BMP?**  
A: Sim. Os formatos suportados incluem PDF, PNG, JPEG, DOCX e mais. Altere o enum `SaveFormat` conforme necessário.

**Q: Existe uma versão de avaliação disponível para Aspose.Note for Java?**  
A: Sim, você pode baixar uma avaliação gratuita no site da Aspose.

## Conclusão

Organizar seus cadernos OneNote com uma estrutura hierárquica clara e exportá‑los como PDFs torna suas notas mais acessíveis e compartilháveis. Seguindo os passos acima, agora você sabe **como salvar OneNote PDF** e **adicionar subpáginas estilo onenote** programaticamente com Aspose.Note for Java.

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
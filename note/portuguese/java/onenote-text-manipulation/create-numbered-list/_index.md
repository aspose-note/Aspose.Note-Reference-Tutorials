---
date: 2026-03-05
description: Aprenda a salvar o OneNote como PDF enquanto cria uma lista numerada
  usando Aspose.Note para Java. Inclui etapas para definir o estilo de texto padrão
  e personalizar a numeração.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Salvar OneNote como PDF – Criar lista numerada com Aspose.Note
url: /pt/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar OneNote como PDF – Criar Lista Numerada com Aspose.Note

## Introdução
Aspose.Note for Java capacita desenvolvedores Java a **salvar OneNote como PDF** e enriquecer o documento com formatação avançada, como listas numeradas. Neste tutorial, vamos guiá‑lo através do processo completo — desde a definição de um estilo de texto padrão até a personalização do formato de numeração — para que você possa exportar OneNote para PDF com um aspecto profissional.

## Respostas Rápidas
- **O que este tutorial aborda?** Criação de uma lista numerada no OneNote e salvamento do arquivo como PDF usando Aspose.Note for Java.  
- **Qual palavra‑chave principal é alvo?** *save onenote as pdf*  
- **Preciso de uma licença?** Uma avaliação gratuita está disponível; uma licença comercial é necessária para produção.  
- **Qual versão do Java é necessária?** JDK 8 ou posterior.  
- **Quanto tempo leva a implementação?** Aproximadamente 10–15 minutos para uma lista básica.

## O que é “salvar OneNote como PDF”?
Salvar OneNote como PDF converte a página rica em texto do OneNote em um documento portátil de layout fixo que pode ser compartilhado entre plataformas sem exigir o OneNote. Isso é especialmente útil para arquivamento, relatórios ou distribuição de conteúdo a usuários que não têm o OneNote instalado.

## Por que criar uma lista numerada antes de exportar?
Uma lista numerada adiciona estrutura e legibilidade, fazendo com que o PDF exportado pareça um relatório bem elaborado. Com Aspose.Note você pode **personalizar o formato de numeração**, definir fontes e controlar espaçamentos — tudo preservando o layout original do OneNote.

## Pré‑requisitos
Antes de começar, certifique‑se de que você tem:

- Java Development Kit (JDK) instalado na sua máquina.  
- Biblioteca Aspose.Note for Java baixada de [here](https://releases.aspose.com/note/java/).  

## Importando Pacotes
Primeiro, importe as classes necessárias para trabalhar com objetos OneNote e conversão para PDF.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## Como salvar OneNote como PDF com uma lista numerada?
A seguir, um guia passo a passo que mostra **como criar elementos de lista**, **definir estilo de texto padrão** e, finalmente, **exportar OneNote para PDF**.

### Etapa 1: Inicializar Objetos Document, Page e Outline
Começamos criando as estruturas principais do OneNote. Isso também demonstra o uso de **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Dica profissional:** Mantenha o caminho `dataDir` absoluto ou use `System.getProperty("user.dir")` para evitar problemas de caminho.

### Etapa 2: Definir Estilo de Texto Padrão
Um estilo consistente garante que a lista tenha aparência uniforme em todos os itens.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Etapa 3: Criar Elementos Outline (Lista Numerada)
Aqui **personalizamos o formato de numeração** usando `NumberList`. O padrão `"{0})"` produz “1)”, “2)”, etc.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Por que isso importa:** Ao anexar um `NumberList` a cada `OutlineElement`, você obtém controle total sobre o estilo de numeração, fonte e tamanho.

### Etapa 4: Adicionar Elementos Outline ao Outline
Agora agrupamos os itens individuais da lista em um único outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Etapa 5: Anexar Outline à Página
O outline passa a fazer parte da hierarquia da página OneNote.

```java
page.appendChildLast(outline);
```

### Etapa 6: Salvar o Documento como PDF
Finalmente, **salvamos OneNote como PDF**. O arquivo de saída conterá a lista numerada exatamente como definida.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Executar o código acima gera um PDF chamado `CreateNumberedList_out.pdf` no diretório especificado, preservando o formato da lista numerada.

## Problemas Comuns & Soluções
| Problema | Solução |
|----------|---------|
| **PDF está vazio** | Certifique‑se de que `doc.appendChildLast(page);` seja chamado antes de `doc.save()`. |
| **Numeração não exibida** | Verifique se o padrão `NumberList` e `NumberFormat` estão configurados corretamente. |
| **Erro de arquivo não encontrado** | Use um caminho absoluto para `dataDir` ou crie o diretório previamente. |
| **Incompatibilidade de fonte** | Instale a fonte (por exemplo, Arial) na máquina que executa o código. |

## Perguntas Frequentes
### P: Posso personalizar o formato de numeração na minha lista OneNote?
R: Absolutamente! Você pode personalizar o formato de numeração usando a classe `NumberList` fornecida pelo Aspose.Note for Java.

### P: Existe uma versão de avaliação disponível para Aspose.Note for Java?
R: Sim, você pode baixar uma avaliação gratuita [here](https://releases.aspose.com/).

### P: Como posso obter suporte para Aspose.Note for Java?
R: Visite o [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) para suporte da comunidade.

### P: Onde posso encontrar documentação detalhada para Aspose.Note for Java?
R: Consulte a [documentation](https://reference.aspose.com/note/java/) para informações abrangentes.

### P: Como faço para comprar uma licença para Aspose.Note for Java?
R: Você pode comprar uma licença [here](https://purchase.aspose.com/buy).

## Conclusão
Neste tutorial demonstramos como **salvar OneNote como PDF** enquanto criamos uma lista numerada limpa usando Aspose.Note for Java. Definindo um estilo de texto padrão, personalizando o formato de numeração e seguindo o guia passo a passo, você pode gerar PDFs profissionais a partir de páginas OneNote de forma rápida e confiável.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-03-05  
**Testado com:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

---
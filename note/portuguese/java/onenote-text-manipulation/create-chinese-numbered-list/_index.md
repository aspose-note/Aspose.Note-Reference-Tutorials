---
date: 2026-03-08
description: Aprenda como salvar o OneNote como PDF com uma lista numerada em chinês
  usando Aspose.Note para Java. Guia passo a passo que cobre numeração, contornos
  e exportação para PDF.
linktitle: Save OneNote as PDF with Chinese Numbered List – Aspose.Note
second_title: Aspose.Note Java API
title: Salvar OneNote como PDF com lista numerada em chinês – Aspose.Note
url: /pt/java/onenote-text-manipulation/create-chinese-numbered-list/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar OneNote como PDF com Lista Numerada em Chinês – Aspose.Note

## Introdução
Se você deseja **salvar OneNote como PDF** enquanto adiciona uma lista numerada em chinês, o Aspose.Note for Java torna isso simples. Neste tutorial, vamos guiá‑lo pelos passos exatos para criar um contorno no estilo chinês, aplicar numeração e exportar o documento OneNote para PDF. Ao final, você entenderá **como adicionar numeração**, **adicionar contorno ao OneNote**, e verá por que **Aspose.Note Java** é a biblioteca ideal para essa tarefa.

## Respostas Rápidas
- **O que este tutorial cobre?** Criar uma lista numerada em chinês no OneNote e salvá‑la como PDF com Aspose.Note for Java.  
- **Preciso de uma licença?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Quais IDEs são suportadas?** Qualquer IDE Java, como Eclipse, IntelliJ IDEA ou NetBeans.  
- **Posso personalizar o estilo da lista?** Sim – fonte, tamanho, cor e formato de numeração são totalmente configuráveis.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para uma lista básica.

## O que é “salvar OneNote como PDF”?
Salvar OneNote como PDF converte a página interativa do bloco de notas em um documento estático e amplamente compatível. Isso é útil para compartilhamento, arquivamento ou impressão, preservando o layout original e qualquer numeração personalizada que você tenha aplicado.

## Por que usar Aspose.Note para Java?
Aspose.Note fornece uma API rica e de alto desempenho que permite criar programaticamente estruturas OneNote, aplicar numeração complexa (incluindo contagem chinesa) e exportar diretamente para PDF sem etapas manuais na interface. Funciona em várias plataformas, não requer instalação do Office e oferece controle total de estilo.

## Pré‑requisitos
1. **Ambiente de Desenvolvimento Java** – JDK 8+ e sua IDE favorita.  
2. **Biblioteca Aspose.Note** – Baixe o JAR mais recente no site oficial [here](https://releases.aspose.com/note/java/).  
3. **Familiaridade básica** com a sintaxe Java e conceitos orientados a objetos.

## Importar Pacotes
Comece importando os pacotes necessários para o seu projeto Java. Essas importações dão acesso aos recursos de criação de documentos, estilo e numeração.

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

Agora, vamos detalhar a implementação passo a passo.

## Como salvar OneNote como PDF com Lista Numerada em Chinês
A seguir, um guia detalhado e numerado. Cada passo inclui uma breve explicação seguida do código exato que você deve copiar.

### Etapa 1: Criar o Objeto Document
Começamos criando uma instância vazia de `Document` que armazenará o conteúdo do OneNote.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### Etapa 2: Inicializar o Objeto Page
Uma página do OneNote funciona como uma tela para contornos e outros elementos.

```java
// initialize Page class object
Page page = new Page();
```

### Etapa 3: Inicializar o Objeto Outline
Outlines são os contêineres para itens de lista. Pense neles como o “detentor de marcadores/números”.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### Etapa 4: Inicializar o Objeto TextStyle
Defina um estilo de parágrafo padrão que será aplicado a cada entrada da lista.

```java
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

### Etapa 5: Inicializar Objetos OutlineElement e Aplicar Numeração
Aqui criamos três elementos outline, cada um representando um item de lista. Usamos `NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10)` para obter a contagem chinesa (一、二、三…).

```java
// initialize OutlineElement class objects and apply numbering
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement();
outlineElem2.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text2 = new RichText().append("Second");
text2.setParagraphStyle(defaultStyle);
outlineElem2.appendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement();
outlineElem3.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text3 = new RichText().append("Third");
text3.setParagraphStyle(defaultStyle);
outlineElem3.appendChildLast(text3);
```

### Etapa 6: Adicionar Elementos Outline
Anexe cada elemento numerado ao contêiner outline.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Etapa 7: Adicionar Nó Outline à Página
Agora colocamos o outline completo na página.

```java
// add Outline node
page.appendChildLast(outline);
```

### Etapa 8: Adicionar Nó de Página ao Documento
A página torna‑se parte do documento OneNote geral.

```java
// add Page node
doc.appendChildLast(page);
```

### Etapa 9: Salvar o Documento como PDF
Finalmente, exportamos o documento OneNote para PDF usando o método `save`. Esta é a etapa onde **salvamos OneNote como PDF**.

```java
// save the document
doc.save(dataDir + "CreateChineseNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateChineseNumberedList_out.pdf");
```

Executar o código acima gera um arquivo PDF (`CreateChineseNumberedList_out.pdf`) que contém uma lista numerada em chinês, exatamente como você veria em uma página do OneNote.

## Problemas Comuns e Soluções
- **Formato de numeração incorreto:** Certifique‑se de usar `NumberFormat.ChineseCounting`. Outros formatos (Árabe, Romano) gerarão resultados diferentes.  
- **Erro de arquivo não encontrado:** Verifique se `dataDir` aponta para uma pasta existente e gravável.  
- **Fonte ausente:** Se a fonte especificada (por exemplo, "Arial") não estiver instalada no servidor, o PDF pode usar uma fonte padrão. Instale a fonte ou escolha outra.

## Perguntas Frequentes

### O Aspose.Note é compatível com diferentes IDEs Java?
Sim, o Aspose.Note é compatível com IDEs Java populares como Eclipse e IntelliJ IDEA.

### Posso personalizar a formatação da lista numerada?
Absolutamente. Conforme mostrado no tutorial, você pode ajustar a fonte, cor e tamanho para atender aos seus requisitos específicos.

### Existe uma versão de avaliação disponível para Aspose.Note?
Sim, você pode explorar a versão de avaliação [here](https://releases.aspose.com/).

### Onde posso encontrar documentação detalhada para Aspose.Note?
Consulte a documentação [here](https://reference.aspose.com/note/java/).

### Como posso obter suporte para Aspose.Note?
Visite o fórum de suporte [here](https://forum.aspose.com/c/note/28) para qualquer assistência ou dúvidas.

## FAQ Adicional (Otimizado por IA)

**Q: Posso usar este código para adicionar numeração de outros idiomas?**  
A: Sim, substitua `NumberFormat.ChineseCounting` pelo valor enum `NumberFormat` apropriado (por exemplo, `NumberFormat.RomanUpper`).

**Q: O PDF mantém a hierarquia do outline?**  
A: O PDF exportado preserva a hierarquia visual, mas a navegação interativa de outline não está disponível em PDFs estáticos.

**Q: Como mudar o estilo de marcador em vez de números?**  
A: Use `NumberList` com uma string de formato personalizada como "• " e defina `NumberFormat.None`.

**Q: É possível adicionar imagens à mesma página?**  
A: Sim, você pode inserir objetos `Image` na página antes de salvar como PDF.

**Q: Qual versão do Aspose.Note é necessária?**  
A: A versão estável mais recente (a partir de 2026) suporta todos os recursos demonstrados aqui.

---

**Última atualização:** 2026-03-08  
**Testado com:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
title: Crie uma lista numerada no OneNote - Aspose.Note
linktitle: Crie uma lista numerada no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como criar facilmente uma lista numerada no OneNote com Aspose.Note para Java. Baixe uma avaliação gratuita e mergulhe no mundo do desenvolvimento Java!
weight: 14
url: /pt/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crie uma lista numerada no OneNote - Aspose.Note

## Introdução
Aspose.Note for Java capacita os desenvolvedores Java a trabalhar perfeitamente com arquivos do Microsoft OneNote. Neste tutorial, orientaremos você no processo de criação de uma lista numerada no OneNote com a poderosa biblioteca Aspose.Note para Java.
## Pré-requisitos
Antes de mergulhar no tutorial, certifique-se de que os seguintes pré-requisitos estejam atendidos:
- Instalado o Java Development Kit (JDK) em sua máquina.
-  Biblioteca Aspose.Note para Java baixada de[aqui](https://releases.aspose.com/note/java/).
## Importando Pacotes
Primeiro, vamos importar os pacotes necessários em seu projeto Java para aproveitar ao máximo as funcionalidades do Aspose.Note. Inclua o seguinte código em seu projeto:
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
## Etapa 1: inicializando objetos de documento, página e estrutura de tópicos
```java
// Seu diretório de documentos
String dataDir = "Your Document Directory";
// Criar objetos Documento, Página e Contorno
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Definir estilo de texto padrão
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Etapa 2: definir o estilo de texto padrão
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Etapa 3: Criando Elementos de Contorno
Agora, vamos criar os elementos da sua lista numerada.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repita para outros elementos (outlineElem2 e OutlineElem3)
```
## Passo 4: Adicionando Elementos de Contorno ao Contorno
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Etapa 5: adicionar contorno à página
```java
page.appendChildLast(outline);
```
## Etapa 6: salvando o documento
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Siga estas etapas meticulosamente e você criará facilmente uma lista numerada no OneNote usando Aspose.Note para Java.
## Conclusão
Neste tutorial, exploramos o processo contínuo de criação de uma lista numerada no OneNote usando Aspose.Note para Java. Os recursos robustos da biblioteca a tornam uma ferramenta inestimável para desenvolvedores Java que trabalham com arquivos do Microsoft OneNote.
## perguntas frequentes
### P: Posso personalizar o formato de numeração na minha lista do OneNote?
R: Absolutamente! Você pode personalizar o formato de numeração usando a classe NumberList fornecida por Aspose.Note para Java.
### P: Existe uma versão de teste disponível para Aspose.Note for Java?
 R: Sim, você pode baixar uma versão de avaliação gratuita[aqui](https://releases.aspose.com/).
### P: Como posso obter suporte para Aspose.Note para Java?
 R: Visite o[Fórum Aspose.Note para Java](https://forum.aspose.com/c/note/28) para apoio comunitário.
### P: Onde posso encontrar documentação detalhada para Aspose.Note for Java?
 R: Consulte o[documentação](https://reference.aspose.com/note/java/) para obter informações abrangentes.
### P: Como faço para adquirir uma licença do Aspose.Note para Java?
 R: Você pode comprar uma licença[aqui](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

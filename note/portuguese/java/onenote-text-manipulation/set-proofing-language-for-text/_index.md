---
title: Definir idioma de revisão de texto no OneNote - Aspose.Note
linktitle: Definir idioma de revisão de texto no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Desbloqueie o potencial do Aspose.Note para Java! Aprenda como definir perfeitamente o idioma de revisão de texto no OneNote com nosso guia passo a passo.
weight: 22
url: /pt/java/onenote-text-manipulation/set-proofing-language-for-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Definir idioma de revisão de texto no OneNote - Aspose.Note

## Introdução
No mundo dinâmico do desenvolvimento de software, Aspose.Note for Java se destaca como uma ferramenta poderosa para gerenciar e manipular documentos do OneNote de forma programática. Se você deseja aprimorar seus aplicativos Java com a capacidade de definir uma linguagem de revisão de texto no OneNote, você veio ao lugar certo. Este tutorial irá guiá-lo através do processo passo a passo, garantindo que você compreenda cada conceito claramente.
## Pré-requisitos
Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
1. Ambiente de desenvolvimento Java: certifique-se de ter um ambiente de desenvolvimento Java configurado em sua máquina.
2.  Biblioteca Aspose.Note para Java: Baixe e instale a biblioteca Aspose.Note para Java do[Link para Download](https://releases.aspose.com/note/java/).
3. Diretório de documentos: crie um diretório para seus documentos para armazenar o arquivo de saída.
## Importar pacotes
Comece importando os pacotes necessários para iniciar seu processo de desenvolvimento. Aqui está um trecho de código para ajudá-lo a começar:
```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```
## Etapa 1: configurar documento e página
Crie um novo documento e página para trabalhar. Isso servirá de base para a manipulação do OneNote.
```java
// O caminho para o diretório de documentos.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```
## Etapa 2: criar contorno e elemento de contorno
Construa um esboço e um elemento de esboço dentro da estrutura da sua página. É aqui que residirá o seu texto com as configurações de idioma de revisão.
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```
## Etapa 3: adicionar rich text com configurações de idioma
Integre rich text em seu elemento de estrutura de tópicos, especificando o idioma de revisão para cada segmento de texto.
```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```
## Etapa 4: organizar os elementos e salvar
Monte os elementos que você criou e salve seu documento no diretório especificado.
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```
## Conclusão
Parabéns! Você definiu com êxito a linguagem de revisão de texto no OneNote usando Aspose.Note para Java. Este tutorial equipou você com o conhecimento e trechos de código para aprimorar seus aplicativos Java de maneira integrada.
## Perguntas frequentes
### P: Posso definir o idioma de revisão para outros idiomas não mencionados no exemplo?
 R: Absolutamente! Modifique o código adicionando as tags de idioma desejadas no`setLanguage` método.
### P: O Aspose.Note for Java é compatível com as versões mais recentes do Java?
R: Sim, o Aspose.Note for Java é atualizado regularmente para garantir compatibilidade com as versões mais recentes do Java.
### P: Como posso lidar com erros durante o processo de configuração do idioma de revisão?
R: Implemente mecanismos de tratamento de erros usando blocos try-catch para resolver possíveis problemas.
### P: Posso integrar este código em aplicações web?
R: Certamente! Certifique-se de ter a biblioteca Aspose.Note para Java configurada corretamente em seu projeto web.
### P: Onde posso encontrar exemplos e documentação adicionais para Aspose.Note for Java?
 R: Explore o[documentação](https://reference.aspose.com/note/java/) para recursos abrangentes.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

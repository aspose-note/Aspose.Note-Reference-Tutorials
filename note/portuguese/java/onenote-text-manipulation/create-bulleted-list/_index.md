---
date: 2026-03-03
description: Aprenda a criar listas com marcadores no OneNote usando Aspose.Note para
  Java e também a salvar o documento do OneNote como PDF. Guia passo a passo com marcadores
  em Java.
linktitle: Create Bulleted List OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Criar lista com marcadores no OneNote - Aspose.Note
url: /pt/java/onenote-text-manipulation/create-bulleted-list/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar Lista com Marcadores OneNote - Aspose.Note

## Introdução
Se você precisa **criar lista com marcadores OneNote** programaticamente, o Aspose.Note para Java oferece uma API limpa e fluente que cuida de todos os detalhes internos do OneNote para você. Neste tutorial vamos percorrer os passos exatos para definir marcadores em Java, adicioná‑los a um outline e, finalmente, **salvar o documento OneNote como PDF**. Ao final, você terá um trecho pronto‑para‑usar que pode ser inserido em qualquer projeto Java.

## Respostas Rápidas
- **O que o Aspose.Note faz?** Ele permite gerar, editar e converter arquivos OneNote sem instalar o OneNote.  
- **Posso definir marcadores com Java?** Sim – use `NumberList` para definir o estilo do marcador.  
- **Como exportar para PDF?** Chame `doc.save(...".pdf")` após montar a página.  
- **Preciso de licença para desenvolvimento?** Um teste gratuito funciona para testes; uma licença é necessária para produção.  
- **Quais IDEs são suportadas?** Qualquer IDE Java, como Eclipse, IntelliJ IDEA ou VS Code.

## O que é “criar lista com marcadores OneNote”?
Criar uma lista com marcadores no OneNote significa adicionar uma série de elementos de outline onde cada elemento começa com um caractere de marcador (por exemplo, “*”). Essa estrutura melhora a legibilidade e imita a forma como os usuários adicionam listas manualmente na interface do OneNote.

## Por que usar Aspose.Note for Java para definir marcadores?
- **Nenhuma instalação do OneNote necessária** – funciona em servidores e pipelines de CI.  
- **Controle total sobre o estilo** – fonte, tamanho, cor e caractere do marcador são todos configuráveis.  
- **Exportação direta para PDF** – gere um PDF em uma única linha, perfeito para relatórios ou arquivamento.  

## Pré‑requisitos
Antes de começar, certifique‑se de que você tem:

- Conhecimento básico de programação Java.  
- Biblioteca Aspose.Note for Java instalada – faça o download em [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/).  
- Uma IDE Java (Eclipse, IntelliJ IDEA, etc.) configurada em sua máquina.

## Importar Pacotes
Comece importando os pacotes necessários para o seu projeto Java. Isso lhe dá acesso a todas as classes Aspose.Note que usaremos.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Import Aspose.Note for Java packages
```

## Etapa 1: Inicializar Documento e Página
Crie uma instância `Document` e uma `Page` onde o outline viverá.

```java
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
// initialize Page class object
Page page = new Page();
```

## Etapa 2: Inicializar Outline e TextStyle (definir marcadores java)
Vamos configurar um contêiner `Outline` e definir um `ParagraphStyle` padrão. É aqui que **definimos a formatação de marcadores java**.

```java
// initialize Outline class object
Outline outline = new Outline();
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

## Etapa 3: Criar Elementos de Lista com Marcadores
Crie objetos individuais `OutlineElement`, anexe um `NumberList` que define o caractere do marcador e adicione o texto.

```java
// initialize OutlineElement class objects and apply bullets
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// initialize RichText class object and apply text style
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```

*Repita o bloco acima para cada marcador adicional que precisar (por exemplo, `outlineElem2`, `outlineElem3`).*

## Etapa 4: Adicionar Elementos de Outline ao Outline
Agrupe todos os elementos de marcador no `Outline` pai.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

## Etapa 5: Adicionar Outline à Página e Salvar (salvar documento OneNote como PDF)
Anexe o `Outline` à `Page`, adicione a página ao `Document` e, finalmente, **salve o documento OneNote como PDF**.

```java
// add Outline node
page.appendChildLast(outline);
// add Page node
doc.appendChildLast(page);
// save the document
doc.save(dataDir + "CreateBulletedList_out.pdf");
```

Parabéns! Você acabou de **criar lista com marcadores OneNote** programaticamente e exportá‑la para PDF usando Aspose.Note for Java.

## Problemas Comuns e Soluções
| Problema | Solução |
|----------|---------|
| `outlineElem2` ou `outlineElem3` não definido | Certifique‑se de duplicar o bloco de código da Etapa 3 para cada marcador adicional e renomear as variáveis adequadamente. |
| Arquivo PDF não criado | Verifique se `dataDir` aponta para uma pasta com permissão de gravação e se você tem direitos de escrita. |
| O estilo do marcador parece diferente | Ajuste os parâmetros do construtor `NumberList` (fonte, tamanho ou caractere) para corresponder à aparência desejada. |

## Perguntas Frequentes

**Q: O Aspose.Note for Java é compatível com todas as IDEs Java?**  
A: Sim, funciona com Eclipse, IntelliJ IDEA, NetBeans e qualquer IDE que suporte projetos Java padrão.

**Q: Posso personalizar a formatação da lista com marcadores?**  
A: Absolutamente! Você pode mudar a fonte, cor, tamanho e até usar símbolos Unicode personalizados modificando os parâmetros do `NumberList`.

**Q: Onde posso encontrar suporte adicional para Aspose.Note for Java?**  
A: Visite o [Aspose.Note for Java support forum](https://forum.aspose.com/c/note/28) para ajuda da comunidade e assistência oficial.

**Q: Existe uma versão de teste gratuita do Aspose.Note for Java?**  
A: Sim, você pode explorar a versão de teste gratuito [aqui](https://releases.aspose.com/).

**Q: Como obter uma licença temporária para Aspose.Note for Java?**  
A: Obtenha uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

## Conclusão
Aspose.Note for Java torna simples **criar lista com marcadores OneNote**, estilizar cada marcador e **salvar o documento OneNote como PDF** em poucos passos concisos. Sinta‑se à vontade para experimentar diferentes caracteres de marcador, fontes e cores para combinar com a linguagem de design da sua aplicação. Explore outros recursos do Aspose.Note, como tabelas, imagens e hyperlinks, para construir conteúdo OneNote ainda mais rico.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-03-03  
**Testado com:** Aspose.Note for Java 24.11  
**Autor:** Aspose
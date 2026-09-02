---
date: 2026-03-03
description: Aprenda como criar esboço no OneNote e gerar um modelo de notas de reunião
  com Aspose.Note para Java. Personalize o estilo da fonte e adicione caixas de seleção
  facilmente.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: Criar Esboço no OneNote – Modelo de Notas de Reunião
url: /pt/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar Estrutura no OneNote – Modelo de Notas de Reunião

## Introdução
No mundo acelerado de hoje, **criar estrutura no OneNote** de forma eficiente é essencial para uma documentação clara das reuniões. Aspose.Note for Java oferece uma maneira poderosa de **gerar modelo de notas de reunião** que você pode personalizar, adicionar caixas de seleção e estilizar as fontes exatamente como precisar. Neste guia passo a passo, vamos percorrer a construção de um modelo reutilizável de agenda de reunião, explicando **como adicionar caixas de seleção**, **adicionar lista de verificação ao OneNote** e **personalizar estilo de fonte onenote** para um visual refinado.

## Respostas Rápidas
- **O que significa “criar estrutura no OneNote”?** Significa construir programaticamente uma estrutura hierárquica (títulos, seções, marcadores) dentro de um arquivo OneNote.  
- **Qual biblioteca ajuda com isso?** Aspose.Note for Java.  
- **Posso adicionar caixas de seleção à estrutura?** Sim – use `NoteCheckBox.createBlueCheckBox()`.  
- **Preciso de licença?** Uma versão de avaliação gratuita está disponível; uma licença comercial é necessária para produção.  
- **Qual versão do Java é suportada?** Java 8 ou superior.

## O que é “criar estrutura no OneNote”?
Criar uma estrutura no OneNote significa definir uma página com um título, várias seções de estrutura e numeração de lista ou caixas de seleção opcionais. Essa estrutura reflete a forma como você digitariam manualmente cabeçalhos e marcadores na interface do OneNote, mas é gerada automaticamente por código.

## Por que usar Aspose.Note para modelos de agenda de reunião?
- **Consistência:** Cada reunião começa com o mesmo layout limpo.  
- **Automação:** Reduza a digitação manual e garanta que todas as seções necessárias (agenda, itens de ação, notas) estejam presentes.  
- **Personalização:** Altere fontes, cores e adicione caixas de seleção interativas para rastrear tarefas.  
- **Integração:** Funciona com qualquer IDE Java e pode ser combinada com outras bibliotecas Aspose para PDFs, planilhas, etc.

## Pré‑requisitos
- Noções básicas de programação Java.  
- Biblioteca Aspose.Note for Java instalada. Você pode baixá‑la [aqui](https://releases.aspose.com/note/java/).  
- Uma IDE como Eclipse ou IntelliJ IDEA.  

## Importar Pacotes
Primeiro, importe as classes que precisaremos. Este trecho permanece exatamente o mesmo do tutorial original.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Etapa 1: Criar Estrutura do Documento
Começamos construindo o documento, definindo um título e preparando estilos de parágrafo que mais tarde ajudarão a **personalizar estilo de fonte onenote**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*O que fizemos:*  
- Definimos dois objetos `ParagraphStyle` (`headerStyle` para cabeçalhos, `bodyStyle` para texto normal).  
- Criamos um `Document` e adicionamos um `Title` que inclui a data atual, dando à página um cabeçalho claro.

## Etapa 2: Estruturar Pontos Importantes
Em seguida, **criar estrutura no OneNote** adicionando um objeto `Outline` e preenchendo‑o com seções como “Importante”. É aqui que os itens da agenda vivem.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Por que isso importa:*  
- O objeto `Outline` representa a lista hierárquica que você vê no OneNote.  
- Usando `createListNumberingStyle` geramos uma lista numerada que pode ser reiniciada para cada nova seção.

## Etapa 3: Destacar Itens de Ação (Como adicionar caixas de seleção)
Itens de ação precisam de um indicativo visual. Ao anexar uma tag de caixa de seleção a cada elemento `RichText`, habilitamos **como adicionar caixas de seleção** diretamente dentro da estrutura.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Dica profissional:* Use `NoteCheckBox.createBlueCheckBox()` para uma caixa de seleção azul; outras cores estão disponíveis se precisar de um estilo visual diferente.

## Etapa 4: Salvar o Documento
Por fim, grave o arquivo OneNote no disco. O arquivo pode ser aberto diretamente no aplicativo desktop do OneNote.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Problemas Comuns e Soluções
| Problema | Solução |
|----------|---------|
| **Caixas de seleção não aparecem** | Certifique‑se de ter chamado `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` após definir o estilo do parágrafo. |
| **Fontes aparecem diferentes no OneNote** | Verifique se o nome da fonte (ex.: “Calibri”) está instalado na máquina onde o OneNote abre o arquivo. |
| **Estrutura não está recuada** | Ajuste `setVerticalOffset` e `setHorizontalOffset` no objeto `Outline`. |
| **Numeração reinicia inesperadamente** | Use a `restartFlag` corretamente; defina‑a como `true` apenas para a primeira lista em uma nova seção. |

## Perguntas Frequentes
### Posso personalizar os estilos de fonte nas minhas notas de reunião?
Sim, o Aspose.Note permite definir estilos de fonte personalizados para cabeçalhos e texto do corpo.

### O Aspose.Note é compatível com outras bibliotecas Java?
O Aspose.Note pode ser integrado com outras bibliotecas Java de forma fluida para funcionalidades estendidas.

### Como posso adicionar seções adicionais às minhas notas de reunião?
Você pode estender facilmente a estrutura da estrutura seguindo o mesmo padrão demonstrado no tutorial.

### Existem considerações de licenciamento para o Aspose.Note?
Consulte a [documentação do Aspose.Note](https://reference.aspose.com/note/java/) para detalhes sobre licenciamento.

### Há uma versão de avaliação disponível para o Aspose.Note?
Sim, você pode acessar a [versão de avaliação gratuita aqui](https://releases.aspose.com/).

## FAQ
**Q: Como adiciono uma lista de verificação ao OneNote sem usar caixas de seleção?**  
A: Você pode criar uma lista com marcadores e marcar os itens manualmente, mas usar `NoteCheckBox` fornece caixas de seleção interativas que sincronizam com a UI do OneNote.

**Q: Posso usar este modelo para criar um modelo de agenda de reunião para repetições semanais?**  
A: Absolutamente. Basta alterar a formatação da data ou passar uma string de título personalizada para reutilizar a mesma estrutura a cada semana.

**Q: Qual é a melhor forma de **customizar font style onenote** para branding?**  
A: Defina objetos `ParagraphStyle` com o nome, tamanho e cor da fonte corporativa, depois aplique‑os a cada elemento `RichText` conforme mostrado na Etapa 1.

**Q: O Aspose.Note suporta exportar a estrutura para PDF?**  
A: Sim. Após salvar o arquivo OneNote, você pode carregá‑lo com Aspose.Note e exportar para PDF usando `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q: Existe uma maneira de marcar programaticamente uma caixa de seleção como concluída?**  
A: Você pode definir o estado da caixa de seleção adicionando uma tag `NoteCheckBox` com a propriedade `Checked` definida como `true`.

---

**Última atualização:** 2026-03-03  
**Testado com:** Aspose.Note for Java 24.11 (mais recente no momento da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}
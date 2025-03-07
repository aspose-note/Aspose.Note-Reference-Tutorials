---
title: Alterar o estilo da tabela no OneNote - Aspose.Note
linktitle: Alterar o estilo da tabela no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprimore suas tabelas do OneNote sem esforço com Aspose.Note para Java. Siga nosso guia passo a passo para alterar estilos de tabela. Baixe a biblioteca agora!
weight: 10
url: /pt/java/onenote-table-manipulation/change-table-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Alterar o estilo da tabela no OneNote - Aspose.Note

## Introdução
Aspose.Note for Java é uma biblioteca poderosa que permite aos desenvolvedores manipular arquivos do OneNote sem esforço. Neste tutorial, vamos nos concentrar em alterar o estilo da tabela em um documento do OneNote usando Aspose.Note para Java. Siga o guia passo a passo para aprimorar o apelo visual de suas mesas.
## Pré-requisitos
Antes de começar, certifique-se de ter o seguinte em vigor:
- Ambiente de Desenvolvimento Java: Certifique-se de ter um ambiente de desenvolvimento Java configurado em sua máquina.
-  Biblioteca Aspose.Note para Java: Baixe e instale a biblioteca Aspose.Note para Java do[página de download](https://releases.aspose.com/note/java/).
- Diretório de documentos: prepare um diretório para armazenar seus documentos do OneNote.
## Importar pacotes
Em seu projeto Java, importe os pacotes necessários para trabalhar com Aspose.Nota:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## Etapa 1: configurar o documento
Carregue o documento OneNote no Aspose.Note e recupere a lista de nós da tabela
```java
// Configure o documento e obtenha a lista de nós da tabela
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## Etapa 2: definir estilos de linha
Itere em cada tabela, definindo o estilo de cada linha, inclusive destacando a primeira linha após o cabeçalho.

```java
// Defina estilos de linha para cada tabela do documento
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Destaque a primeira linha após a cabeça.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## Método setRowStyle
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```
## Etapa 3: salve o documento
Salve o documento modificado com os novos estilos de tabela.
Seguindo essas etapas, você pode alterar facilmente o estilo da tabela em um documento do OneNote usando Aspose.Note para Java.

```java
// Salve o documento modificado
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## Conclusão
Aspose.Note para Java simplifica o processo de manipulação de arquivos do OneNote. Ao aproveitar os recursos da biblioteca, você pode aprimorar a apresentação visual de suas tabelas sem esforço.

## Perguntas frequentes
### Onde posso encontrar a documentação do Aspose.Note para Java?
 Visite a[documentação](https://reference.aspose.com/note/java/) para orientação abrangente.
### Como posso obter uma licença temporária do Aspose.Note for Java?
 Siga isso[link](https://purchase.aspose.com/temporary-license/) para adquirir uma licença temporária.
### Existe uma avaliação gratuita disponível para Aspose.Note para Java?
 Sim, você pode baixar uma versão de avaliação gratuita em[aqui](https://releases.aspose.com/).
### Onde posso obter suporte para Aspose.Note para Java?
 Junte-se a[Fórum Aspose.Note](https://forum.aspose.com/c/note/28) buscar ajuda da comunidade.
### Como faço para adquirir o Aspose.Note para Java?
 Você pode comprar a biblioteca[aqui](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

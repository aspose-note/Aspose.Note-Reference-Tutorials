---
title: Crie tabela com colunas bloqueadas no OneNote - Aspose.Note
linktitle: Crie tabela com colunas bloqueadas no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprimore sua experiência no OneNote com Aspose.Note para Java. Aprenda como criar tabelas com colunas bloqueadas usando um guia passo a passo. Baixe o seu teste gratuito agora!
type: docs
weight: 12
url: /pt/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## Introdução
O OneNote é uma ferramenta poderosa para organizar informações, e o Aspose.Note for Java aprimora seus recursos, fornecendo uma maneira perfeita de criar tabelas com colunas bloqueadas. Neste tutorial, iremos guiá-lo através do processo de uso do Aspose.Note for Java para criar uma tabela com colunas bloqueadas no OneNote.
## Pré-requisitos
Antes de começar, certifique-se de ter os seguintes pré-requisitos em vigor:
- [Kit de Desenvolvimento Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)instalado em sua máquina.
- [Aspose.Note para Java](https://downloads.aspose.com/note/java) biblioteca baixada e adicionada ao seu projeto.
## Importar pacotes
Em seu projeto Java, importe os pacotes necessários para trabalhar com Aspose.Nota:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Etapa 1: configure seu projeto
Comece criando um novo projeto Java e adicionando a biblioteca Aspose.Note ao seu classpath. Certifique-se de que seu projeto esteja configurado para usar o JDK.
## Etapa 2: inicializar documentos e objetos de página
```java
// O caminho para o diretório de documentos.
String dataDir = "Your Document Directory";
//Crie um objeto da classe Document
Document doc = new Document();
// Inicializar objeto de classe Page
Page page = new Page();
```
## Etapa 3: criar linhas e células da tabela
```java
// Inicializar objeto de classe TableRow
TableRow row1 = new TableRow();
// Inicialize o objeto da classe TableCell e defina o conteúdo do texto
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Inicializar objeto de classe TableRow
TableRow row2 = new TableRow();
// Inicialize o objeto da classe TableCell e defina o conteúdo do texto
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Etapa 4: crie e personalize a tabela
```java
// Inicializar objeto de classe Table
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Adicionar linhas
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Etapa 5: adicionar tabela ao esboço e à página
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Adicionar nó de tabela
outlineElem.appendChildLast(table);
// Adicionar nó de elemento de contorno
outline.appendChildLast(outlineElem);
// Adicionar nó de estrutura de tópicos
page.appendChildLast(outline);
// Adicionar nó de página
doc.appendChildLast(page);
```
## Etapa 6: salve o documento
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Parabéns! Você criou com êxito uma tabela com colunas bloqueadas no OneNote usando Aspose.Note para Java.
## Conclusão
Neste tutorial, exploramos o processo de utilização do Aspose.Note para Java para aprimorar sua experiência no OneNote criando tabelas com colunas bloqueadas. Esta funcionalidade adiciona uma nova camada de organização e estrutura às suas notas.
## Perguntas frequentes
### O Aspose.Note for Java é compatível com todas as versões Java?
Sim, Aspose.Note for Java é compatível com Java 6 e versões posteriores.
### Posso personalizar ainda mais a aparência da tabela?
Absolutamente! Aspose.Note for Java oferece amplas opções para personalizar tabelas, como ajuste de bordas, espaçamento de células e muito mais.
### Existe uma versão de teste disponível antes de comprar?
 Sim você pode[baixe um teste gratuito](https://releases.aspose.com/) para explorar os recursos do Aspose.Note para Java.
### Onde posso encontrar suporte adicional ou discussões na comunidade?
 Visite a[Fórum Aspose.Note](https://forum.aspose.com/c/note/28) para suporte e discussões na comunidade.
### Como posso obter uma licença temporária do Aspose.Note for Java?
 Visita[esse link](https://purchase.aspose.com/temporary-license/) para obter uma licença temporária para fins de teste.
---
title: Extraia o texto da linha da tabela no documento do OneNote - Aspose.Note
linktitle: Extraia o texto da linha da tabela no documento do OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda a extrair texto de linha de tabelas do OneNote sem esforço com Aspose.Note para Java. Siga nosso guia passo a passo para uma integração perfeita.
weight: 13
url: /pt/java/onenote-table-manipulation/extract-row-text-from-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extraia o texto da linha da tabela no documento do OneNote - Aspose.Note

## Introdução
Bem-vindo a este tutorial abrangente sobre como extrair texto de linha de tabelas em documentos do OneNote usando Aspose.Note para Java. Aspose.Note é uma biblioteca Java poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote perfeitamente. Neste tutorial, guiaremos você pelo processo passo a passo, demonstrando como extrair com eficiência texto de linha de tabelas em seus documentos do OneNote.
## Pré-requisitos
Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:
-  Biblioteca Aspose.Note para Java: Certifique-se de ter a biblioteca Aspose.Note para Java instalada. Você pode baixá-lo no[Link para Download](https://releases.aspose.com/note/java/).
- Ambiente de desenvolvimento Java: certifique-se de ter um ambiente de desenvolvimento Java configurado em sua máquina.
- Documento do OneNote: prepare um documento de amostra do OneNote (por exemplo, "Sample1.one") contendo tabelas das quais você deseja extrair o texto da linha.
## Importar pacotes
Em seu projeto Java, importe os pacotes Aspose.Note necessários. Isso garante que você tenha acesso às classes e aos métodos necessários para trabalhar com documentos do OneNote.
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## Etapa 1: definir diretório de documentos
```java
// O caminho para o diretório de documentos.
String dataDir = "Your Document Directory";
```
## Etapa 2: carregar o documento do OneNote
```java
// Carregue o documento no Aspose.Note.
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## Etapa 3: obter nós de tabela
```java
// Obtenha uma lista de nós de tabela
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## Etapa 4: iterar por meio de tabelas e linhas
```java
// Definir contagem de linhas
int rowCount = 0;
for (Table table : nodes) {
    // Iterar pelas linhas da tabela
    for (TableRow row : table) {
        rowCount++;
        // Recuperar texto
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // Imprimir texto na tela de saída
        System.out.println(text);
    }
}
```
Repita essas etapas para cada tabela do documento do OneNote e você extrairá o texto da linha com êxito.
## Conclusão
Parabéns! Você aprendeu como extrair texto de linha de tabelas em documentos do OneNote usando Aspose.Note para Java. Este tutorial fornece uma base para aproveitar os poderosos recursos do Aspose.Note em seus aplicativos Java.
## perguntas frequentes
### O Aspose.Note é compatível com a versão mais recente do Microsoft OneNote?
 Aspose.Note oferece suporte a várias versões do OneNote, incluindo a mais recente. Consulte o[documentação](https://reference.aspose.com/note/java/) para detalhes de compatibilidade.
### Posso experimentar o Aspose.Note para Java antes de comprar?
Sim, você pode explorar uma avaliação gratuita do Aspose.Note em[esse link](https://releases.aspose.com/).
### Onde posso encontrar suporte e assistência adicionais?
 Visite a[Fórum Aspose.Note](https://forum.aspose.com/c/note/28) para apoio e discussões da comunidade.
### Como obtenho uma licença temporária do Aspose.Note?
 Obtenha uma licença temporária de[esse link](https://purchase.aspose.com/temporary-license/).
### Há algum requisito de sistema específico para usar o Aspose.Note para Java?
Consulte a documentação para obter requisitos detalhados do sistema.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

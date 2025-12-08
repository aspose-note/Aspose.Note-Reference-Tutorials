---
date: 2025-12-04
description: Aprenda como extrair imagens de arquivos OneNote e converter OneNote
  em texto em Java usando Aspose.Note. Guia passo a passo com exemplos de código.
language: pt
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Extrair imagens do OneNote usando Document Visitor - Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrair Imagens do OneNote usando Document Visitor - Java

## Introdução

Aspose.Note for Java facilita **extrair imagens do OneNote** cadernos, bem como ler o arquivo `.one` subjacente em Java. Neste tutorial, vamos guiá‑lo através de um exemplo completo e prático que mostra como carregar um arquivo OneNote, percorrer sua estrutura com um `DocumentVisitor` personalizado e extrair tanto imagens quanto texto simples. Ao final, você também saberá como **converter OneNote para texto** se precisar apenas do conteúdo textual.

## Respostas Rápidas
- **Qual biblioteca eu preciso?** Aspose.Note for Java (link de download abaixo).  
- **Posso extrair apenas imagens?** Sim – implemente o método `VisitImageStart` em um `DocumentVisitor`.  
- **Como leio um arquivo .one em Java?** Use `new Document(path, new LoadOptions())`.  
- **Preciso de uma licença para produção?** É necessária uma licença comercial para uso não‑trial.  
- **Qual versão do Java é suportada?** JDK 8 ou superior.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

1. Java Development Kit (JDK) 8 ou mais recente instalado.  
2. Biblioteca Aspose.Note for Java baixada. Você pode baixá‑la **[aqui](https://releases.aspose.com/note/java/)**.  
3. Um documento OneNote (arquivo `.one`) do qual você deseja extrair imagens ou converter para texto.

## Importar Pacotes

Primeiro, importe as classes necessárias da API Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Etapa 1: Configurar um Document Visitor Personalizado

Crie uma classe que estenda `DocumentVisitor`. Esta classe será chamada para cada nó no documento OneNote, permitindo que você **extraia imagens do OneNote** e, opcionalmente, colete texto.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Etapa 2: Implementar Métodos do Visitor

Adicione substituições (overrides) para os tipos de nó que lhe interessam. Abaixo tratamos de rich‑text, imagens, títulos, páginas, outlines e elementos de outline. O método `VisitImageStart` é onde ocorre a extração da imagem.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Por que implementar esses métodos?

- **Extrair imagens do OneNote:** `VisitImageStart` fornece acesso direto aos bytes brutos da imagem.  
- **Converter OneNote para texto:** `VisitRichTextStart` coleta o conteúdo textual, permitindo uma operação simples de **converter OneNote para texto**.  
- **Ler arquivo .one em Java:** O padrão visitor abstrai a estrutura subjacente do arquivo `.one`, de modo que você não precisa analisar o formato binário manualmente.

## Etapa 3: Executar o Visitor a partir do Seu Método Main

Carregue o arquivo `.one`, instancie seu visitor e inicie a travessia.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Casos de Uso Comuns

- **Relatórios automatizados:** Extraia imagens e texto de um caderno de reunião do OneNote para gerar um resumo em PDF ou HTML.  
- **Migração de conteúdo:** Converta arquivos legados do OneNote para arquivos de texto simples para indexação ou ingestão por mecanismos de busca.  
- **Extração de ativos digitais:** Colha capturas de tela, diagramas ou fotos incorporadas para reutilização em outras aplicações.

## Solução de Problemas e Dicas

- **Cadernos grandes:** Se encontrar problemas de memória, processe as páginas individualmente verificando `VisitPageStart` e carregando recursos de nível de página somente quando necessário.  
- **Formatos de imagem:** O objeto `Image` retorna bytes brutos; pode ser necessário detectar o formato (PNG, JPEG) antes de salvar.  
- **Erros de licença:** Certifique‑se de que definiu a licença Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) antes de carregar o documento em produção.

## Perguntas Frequentes

**Q: Posso extrair tipos específicos de conteúdo do documento OneNote?**  
A: Sim – sobrescrevendo apenas os métodos do visitor que você precisa (por exemplo, `VisitImageStart` para imagens, `VisitRichTextStart` para texto).

**Q: O Aspose.Note for Java é compatível com diferentes versões de documentos OneNote?**  
A: Absolutamente. A biblioteca suporta todas as principais versões de arquivos OneNote, de modo que você pode **ler arquivo .one em Java** com segurança, independentemente da versão original do OneNote.

**Q: Posso integrar esse processo de extração na minha aplicação Java?**  
A: Sim. O padrão visitor funciona perfeitamente dentro de qualquer base de código Java; basta adicionar o JAR da biblioteca e chamar o exemplo mostrado acima.

**Q: O Aspose.Note for Java oferece suporte para lidar com documentos OneNote complexos?**  
A: Sim. Outlines aninhados, mídia incorporada e dados personalizados são todos expostos através da API do visitor.

**Q: Existe algum limite para o tamanho do documento OneNote que pode ser processado?**  
A: Não há limite rígido, mas cadernos extremamente grandes podem exigir mais memória heap; considere processá‑los página por página.

**Q: Como converto o texto extraído em um arquivo de texto simples?**  
A: Após `myConverter.GetText()` retornar uma `String`, escreva‑a em um arquivo usando I/O padrão do Java (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Última atualização:** 2025-12-04  
**Testado com:** Aspose.Note for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
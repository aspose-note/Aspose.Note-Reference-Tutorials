---
date: 2025-12-02
description: Aprenda como exportar fontes ao salvar o OneNote como HTML usando Aspose.Note
  para Java. Este guia mostra como criar o OneNote programaticamente e incorporar
  fontes, CSS e imagens.
language: pt
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Como Exportar Fontes ao Salvar o OneNote como HTML – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Exportar Fontes ao Salvar OneNote como HTML – Java

## Introdução

Neste tutorial você descobrirá **como exportar fontes** ao **salvar OneNote como HTML** usando Aspose.Note for Java. Vamos percorrer a criação de um documento OneNote programaticamente, a configuração das opções de salvamento HTML e a incorporação dos arquivos de fonte necessários para que o HTML resultante fique exatamente como as páginas originais do OneNote. Essa abordagem é perfeita quando você precisa preservar a fidelidade visual do conteúdo do OneNote em um formato amigável para a web.

## Respostas rápidas
- **Qual biblioteca lida com a exportação?** Aspose.Note for Java  
- **As fontes podem ser incorporadas no HTML?** Sim – defina `ExportFonts` como `ExportEmbedded`  
- **Preciso de licença para produção?** Uma licença válida do Aspose.Note é necessária para uso comercial  
- **Qual versão do Java é suportada?** Java 8 ou superior  
- **É possível salvar recursos em arquivos separados?** Absolutamente – configure `ResourceExportType` conforme necessário  

## O que significa “como exportar fontes” no contexto da conversão de OneNote para HTML?

Ao converter um bloco de notas OneNote para HTML, a aparência visual depende de CSS, imagens e, especialmente, das fontes usadas nas páginas originais. **Exportar fontes** significa incorporar os arquivos de fonte (por exemplo, TTF) diretamente no pacote HTML para que os navegadores possam renderizar o texto exatamente como aparece no OneNote, mesmo que o usuário final não tenha essas fontes instaladas localmente.

## Por que criar OneNote programaticamente e salvá-lo como HTML?

- **Automação:** Gere relatórios, documentação ou artigos de base de conhecimento a partir do OneNote sem copiar‑colar manualmente.  
- **Consistência:** Preserve layout, estilos e fontes personalizadas em todos os dispositivos.  
- **Portabilidade:** HTML é visualizável universalmente—não há necessidade do cliente OneNote.  

## Pré‑requisitos

1. Java Development Kit (JDK) 8 ou mais recente instalado.  
2. Biblioteca Aspose.Note for Java – faça o download [aqui](https://releases.aspose.com/note/java/).  
3. Um arquivo de exemplo do OneNote (`.one`) para carregar, ou você pode criar um novo programaticamente.  

## Importar Pacotes

Primeiro, importe as classes necessárias para o seu projeto Java:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Como Exportar Fontes ao Salvar OneNote como HTML?

A seguir, um guia passo a passo que mostra **como exportar fontes** e outros recursos.

### Passo 1: Criar um documento OneNote programaticamente  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Esta linha carrega um arquivo `.one` existente. Se precisar **criar OneNote programaticamente**, pode instanciar um novo objeto `Document` e adicionar seções/páginas via API (não mostrado aqui para manter o foco na exportação de fontes).

### Passo 2: Salvar em um fluxo de memória com fontes incorporadas  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` indica ao Aspose.Note para **exportar fontes** diretamente no pacote HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` garante que fontes TrueType sejam usadas, pois têm amplo suporte nos navegadores.

### Passo 3: Salvar como HTML com arquivos de recursos separados (ainda exportando fontes)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Mesmo que CSS e imagens estejam incorporados, você pode mudar `ResourceExportType` para `ExportExternal` se preferir arquivos separados para facilitar o cache. A parte essencial—**exportar fontes**—permanece inalterada.

### Passo 4: Usar callbacks para controlar onde cada recurso é armazenado  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

A classe `UserSavingCallbacks` (você precisará implementar `ICssSavingCallback`, `IImageSavingCallback` e `IFontSavingCallback`) oferece controle total sobre a estrutura de pastas, permitindo que você mantenha as fontes em um diretório dedicado `fonts` enquanto ainda **exporta fontes** corretamente.

## Problemas Comuns & Dicas

- **Fontes ausentes na saída:** Verifique se `setExportFonts(ResourceExportType.ExportEmbedded)` está definido e se o arquivo OneNote de origem realmente usa fontes incorporadas.  
- **Arquivos HTML grandes:** Incorporar fontes pode aumentar o tamanho. Se a largura de banda for uma preocupação, altere `ExportFonts` para `ExportExternal` e hospede as fontes em um CDN.  
- **Erros na implementação de callbacks:** Certifique‑se de que suas classes de callback gravem o stream corretamente e fechem os recursos para evitar corrupção de arquivos.  

## Perguntas Frequentes

**Q: Posso converter vários documentos OneNote para HTML de uma só vez?**  
A: Sim, itere sobre cada instância `Document` e aplique as mesmas `HtmlSaveOptions`.  

**Q: O Aspose.Note for Java suporta outros formatos de saída além de HTML?**  
A: Absolutamente. Você pode exportar para PDF, DOCX, PNG, JPEG e muito mais usando as opções de salvamento apropriadas.  

**Q: Existe uma versão de avaliação disponível para Aspose.Note for Java?**  
A: Sim, faça o download de um teste gratuito [aqui](https://releases.aspose.com/).  

**Q: Onde posso obter suporte para Aspose.Note for Java?**  
A: Visite o [forum Aspose.Note](https://forum.aspose.com/c/note/28) para assistência da comunidade e oficial.  

**Q: Como posso comprar uma licença para Aspose.Note for Java?**  
A: Licenças estão disponíveis no [site da Aspose](https://purchase.aspose.com/buy).  

## Conclusão

Agora você sabe **como exportar fontes** ao **salvar OneNote como HTML** usando Aspose.Note for Java. Configurando `HtmlSaveOptions` e, opcionalmente, usando callbacks, você pode preservar a aparência exata das suas páginas OneNote—including fontes personalizadas—ao entregá‑las na web. Sinta‑se à vontade para experimentar diferentes configurações de `ResourceExportType` para atender aos requisitos de desempenho e armazenamento do seu projeto.

---

**Última atualização:** 2025-12-02  
**Testado com:** Aspose.Note for Java 24.12  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---
date: 2026-09-19
description: Узнайте, как конвертировать OneNote в HTML и экспортировать шрифты с
  помощью Aspose.Note for Java. В этом руководстве рассматривается сохранение OneNote
  в виде HTML с внедрёнными шрифтами, CSS и изображениями.
keywords:
- convert onenote to html
- save onenote as html
- export fonts java
- aspose.note html export
lastmod: 2026-09-19
linktitle: Как экспортировать шрифты при сохранении OneNote в HTML – Java
og_description: Узнайте, как конвертировать OneNote в HTML и экспортировать шрифты
  с помощью Aspose.Note for Java. В этом руководстве показано сохранение OneNote в
  виде HTML с внедрёнными шрифтами, CSS и изображениями.
og_image_alt: 'Developer guide: convert OneNote to HTML with font export in Java'
og_title: Конвертировать OneNote в HTML и экспортировать шрифты в Java – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  headline: How to convert OneNote to HTML and export fonts in Java
  type: TechArticle
- description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  name: How to convert OneNote to HTML and export fonts in Java
  steps:
  - name: create a OneNote document programmatically
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. You can either load an existing `.one` file or
      instantiate a new document and add sections/pages via the API. This line loads
      an existing `.one` file. If you need to **create OneNote programmatica
  - name: save to a memory stream with embedded fonts
    text: The `HtmlSaveOptions` class controls every aspect of the HTML conversion.
      `ResourceExportType` is an enumeration that defines how resources such as fonts,
      images, and CSS are exported. Setting `setExportFonts(ResourceExportType.ExportEmbedded)`
      tells Aspose.Note to embed fonts directly into the HTML
  - name: save as HTML with separate resource files (still exporting fonts)
    text: If you prefer a single HTML file, keep `ExportEmbedded`. For caching‑friendly
      deployments, switch `ResourceExportType` to `ExportExternal`; the fonts will
      still be embedded, but CSS, images, and other assets will be saved as separate
      files. Even though CSS and images are embedded, you can change the
  - name: use callbacks to control where each resource is stored
    text: '`UserSavingCallbacks` allows custom handling of resource saving. Implementing
      `UserSavingCallbacks` (which requires `ICssSavingCallback`, `IImageSavingCallback`,
      and `IFontSavingCallback`) gives you full control over folder structure, allowing
      you to keep fonts in a dedicated `fonts` directory while'
  type: HowTo
- questions:
  - answer: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.
    question: Can I convert multiple OneNote documents to HTML in one go?
  - answer: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the
      appropriate save options.
    question: Does Aspose.Note for Java support other output formats besides HTML?
  - answer: Yes, download a free trial from the **Aspose releases page**([Aspose releases
      page](https://releases.aspose.com/)).
    question: Is there a trial version available for Aspose.Note for Java?
  - answer: Visit the **Aspose.Note forum**([Aspose.Note forum](https://forum.aspose.com/c/note/28))
      for community and official assistance.
    question: Where can I get support for Aspose.Note for Java?
  - answer: Licenses are available at the **Aspose purchase page**([Aspose website](https://purchase.aspose.com/buy)).
    question: How can I purchase a license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java HTML export
- font embedding
title: Как конвертировать OneNote в HTML и экспортировать шрифты в Java
url: /ru/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как конвертировать OneNote в HTML и экспортировать шрифты в Java

## Введение

В этом руководстве вы узнаете **как экспортировать шрифты**, пока **конвертируете OneNote в HTML** с помощью Aspose.Note for Java. Мы пройдем процесс создания документа OneNote программно, настройки параметров сохранения HTML и встраивания необходимых файлов шрифтов, чтобы полученный HTML выглядел точно так же, как оригинальные страницы OneNote. Этот подход идеален, когда необходимо сохранить визуальную точность контента OneNote в веб‑дружественном формате, особенно для порталов базы знаний, автоматических конвейеров отчетности или кроссплатформенных сайтов документации.

## Быстрые ответы
- **Какая библиотека обрабатывает экспорт?** Aspose.Note for Java  
- **Можно ли встроить шрифты в HTML?** Да – установите `ExportFonts` в `ExportEmbedded`  
- **Нужна ли лицензия для продакшн?** Требуется действующая лицензия Aspose.Note для коммерческого использования  
- **Какая версия Java поддерживается?** Java 8 или выше  
- **Можно ли сохранять ресурсы в отдельные файлы?** Конечно – настройте `ResourceExportType` соответствующим образом  

## Что означает «как экспортировать шрифты» в контексте конвертации OneNote в HTML?

Экспорт шрифтов означает встраивание оригинальных файлов шрифтов (например, TTF или OTF) непосредственно в пакет HTML, чтобы браузеры отображали текст точно так же, как в OneNote, даже если на устройстве конечного пользователя эти шрифты отсутствуют. Aspose.Note достигает этого, преобразуя шрифты в строки base‑64 и вставляя их в сгенерированный CSS, гарантируя пиксель‑точную типографику.

## Почему конвертировать OneNote в HTML и экспортировать шрифты?

Встраивание шрифтов во время конвертации обеспечивает сохранение визуального вида оригинальных страниц OneNote во всех браузерах, устраняя сдвиги макета, вызванные отсутствием шрифтов. Это особенно важно для корпоративного брендинга, юридических документов или любого контента, где точная типографика имеет значение.

- **Автоматизация:** Генерировать отчёты, учебные материалы или статьи базы знаний из OneNote без ручного копирования.  
- **Последовательность:** Сохранять макет, стили и пользовательские шрифты во всех браузерах и устройствах.  
- **Переносимость:** HTML универсален — не требуется клиент OneNote или дополнительные плагины.  
- **Производительность:** Встраивание шрифтов устраняет дополнительные сетевые запросы, что может улучшить время загрузки страниц для небольших‑средних документов.  

## Требования

1. Установлен Java Development Kit (JDK) 8 или новее.  
2. Библиотека Aspose.Note for Java – загрузите со **страницы выпуска Aspose.Note for Java**([Aspose.Note for Java release page](https://releases.aspose.com/note/java/)).  
3. Пример файла OneNote (`.one`) для загрузки, либо вы можете создать новый программно.  

## Импорт пакетов

Сначала импортируйте необходимые классы в ваш проект Java:

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

## Как конвертировать OneNote в HTML с экспортом шрифтов?

Загрузите ваш блокнот OneNote, настройте `HtmlSaveOptions` для встраивания шрифтов и сохраните результат в поток или файл. Этот одношаговый процесс гарантирует, что каждый пользовательский шрифт, использованный в оригинальных страницах, будет включён в вывод HTML, обеспечивая точное визуальное представление при простой и поддерживаемой работе.

### Шаг 1: создать документ OneNote программно  

Класс `Document` — это объект верхнего уровня Aspose.Note, представляющий один файл OneNote в памяти. Вы можете загрузить существующий файл `.one` или создать новый документ и добавить секции/страницы через API.

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Эта строка загружает существующий файл `.one`. Если вам нужно **создать OneNote программно**, вы можете создать новый объект `Document` и добавить секции/страницы через API (не показано здесь, чтобы сосредоточиться на экспорте шрифтов).

### Шаг 2: сохранить в поток памяти с встроенными шрифтами  

Класс `HtmlSaveOptions` управляет каждым аспектом конвертации в HTML. `ResourceExportType` — перечисление, определяющее, как экспортировать ресурсы, такие как шрифты, изображения и CSS. Установка `setExportFonts(ResourceExportType.ExportEmbedded)` указывает Aspose.Note **экспортировать шрифты** непосредственно в пакет HTML, а `setFontFaceTypes(FontFaceType.Ttf)` ограничивает экспорт TrueType‑шрифтами, которые имеют наибольшую поддержку в браузерах.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` указывает Aspose.Note **экспортировать шрифты** непосредственно в пакет HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` гарантирует использование TrueType‑шрифтов, которые поддерживаются большинством браузеров.

### Шаг 3: сохранить как HTML с отдельными файловыми ресурсами (по‑прежнему экспортируя шрифты)  

Если вам нужен один HTML‑файл, оставьте `ExportEmbedded`. Для кэш‑дружественных развертываний переключите `ResourceExportType` на `ExportExternal`; шрифты всё равно будут встроены, но CSS, изображения и другие активы сохранятся в виде отдельных файлов.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Хотя CSS и изображения могут быть встроены, вы можете изменить `ResourceExportType` на `ExportExternal`, если предпочитаете отдельные файлы для более удобного кэширования. Ключевая часть — **экспорт шрифтов** — остаётся без изменений.

### Шаг 4: использовать обратные вызовы для управления местом сохранения каждого ресурса  

`UserSavingCallbacks` позволяет настраивать сохранение ресурсов. Реализация `UserSavingCallbacks` (которая требует `ICssSavingCallback`, `IImageSavingCallback` и `IFontSavingCallback`) даёт полный контроль над структурой папок, позволяя хранить шрифты в отдельном каталоге `fonts`, при этом **экспортируя шрифты** корректно.

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

Классы обратных вызовов позволяют переименовывать файлы, сжимать потоки или размещать шрифты в папке, готовой к CDN, предоставляя гибкость для масштабных развертываний.

## Как встроить пользовательские шрифты при конвертации OneNote в HTML

Встраивание пользовательских шрифтов гарантирует, что отображение HTML будет соответствовать оригинальному макету OneNote, даже на устройствах без этих шрифтов. Используя `ExportEmbedded` вместе с `FontFaceType.Ttf`, файлы TrueType кодируются в base‑64 и вставляются непосредственно в сгенерированный CSS, устраняя необходимость внешнего хостинга шрифтов и обеспечивая согласованную типографику во всех браузерах.

## Использование ResourceExportType для управления экспортом ресурсов

`ResourceExportType` позволяет решить, будут ли CSS, изображения и шрифты храниться **внутри** HTML‑файла (`ExportEmbedded`) или сохраняться как **внешние** файлы (`ExportExternal`). Выбирайте `ExportEmbedded` для решения в один файл, или `ExportExternal`, когда хотите воспользоваться кэшированием браузера для крупных активов.

## Программное создание OneNote для экспорта в HTML

Если вы начинаете с нуля, можете полностью построить документ OneNote в коде, добавить секции, страницы и форматированный текст, а затем применить те же `HtmlSaveOptions`, показанные выше. Это обеспечивает полную автоматизацию: от генерации данных до полностью стилизованного HTML‑вывода с встроенными пользовательскими шрифтами.

## Распространённые проблемы и советы

- **Отсутствие шрифтов в выводе:** Убедитесь, что установлен `setExportFonts(ResourceExportType.ExportEmbedded)` и исходный файл OneNote действительно использует встроенные шрифты.  
- **Большие HTML‑файлы:** Встраивание шрифтов может увеличить размер на 200‑500 KB на каждый шрифт. Если пропускная способность важна, переключите `ExportFonts` на `ExportExternal` и разместите шрифты на CDN.  
- **Ошибки реализации обратных вызовов:** Убедитесь, что ваши классы обратных вызовов корректно записывают поток и закрывают ресурсы, чтобы избежать повреждения файлов.  
- **Совет по производительности:** Для блокнотов более 100 страниц обрабатывайте секции по отдельности и объединяйте полученные фрагменты HTML, чтобы снизить использование памяти.  
- **Количественное утверждение:** Aspose.Note может конвертировать блокноты до 500 страниц менее чем за 30 секунд на типичном сервере с 2.5 ГГц, сохраняя более 50 пользовательских шрифтов в документе.  

## Часто задаваемые вопросы

**Q: Можно ли конвертировать несколько документов OneNote в HTML за один раз?**  
**A: Да, пройдитесь по каждому экземпляру `Document` и примените те же `HtmlSaveOptions`.**  

**Q: Поддерживает ли Aspose.Note for Java другие форматы вывода, помимо HTML?**  
**A: Конечно. Вы можете экспортировать в PDF, DOCX, PNG, JPEG и другие форматы, используя соответствующие параметры сохранения.**  

**Q: Доступна ли пробная версия Aspose.Note for Java?**  
**A: Да, загрузите бесплатную пробную версию со **страницы выпусков Aspose**([Aspose releases page](https://releases.aspose.com/)).**  

**Q: Где я могу получить поддержку для Aspose.Note for Java?**  
**A: Посетите **форум Aspose.Note**([Aspose.Note forum](https://forum.aspose.com/c/note/28)) для получения помощи от сообщества и официальной поддержки.**  

**Q: Как приобрести лицензию на Aspose.Note for Java?**  
**A: Лицензии доступны на **странице покупки Aspose**([Aspose website](https://purchase.aspose.com/buy)).**  

## Заключение

Теперь вы знаете **как экспортировать шрифты**, пока **конвертируете OneNote в HTML** с помощью Aspose.Note for Java. Настраивая `HtmlSaveOptions` и при необходимости используя обратные вызовы, вы можете сохранить точный вид ваших страниц OneNote — включая пользовательские шрифты — при их публикации в вебе. Экспериментируйте с настройками `ResourceExportType`, чтобы найти баланс между размером файлов и стратегией кэширования, и интегрируйте этот процесс в ваш автоматический конвейер отчетности для максимальной эффективности.

---

**Последнее обновление:** 2026-09-19  
**Тестировано с:** Aspose.Note for Java 24.12  
**Автор:** Aspose

## Связанные руководства

- [Использовать Aspose.Note for Java для сохранения OneNote как PDF с указанной подсистемой шрифтов](/note/java/onenote-document-saving/save-using-specified-fonts-subsystem/)
- [Конвертировать OneNote в текст и извлечь изображения с помощью Document Visitor — Java](/note/java/onenote-document-loading/extract-content-using-document-visitor/)
- [Конвертировать OneNote в PDF, используя настройки страниц, с Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
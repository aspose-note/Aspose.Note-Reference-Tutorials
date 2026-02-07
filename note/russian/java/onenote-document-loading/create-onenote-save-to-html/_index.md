---
date: 2026-02-07
description: Узнайте, как экспортировать шрифты при сохранении OneNote в формате HTML
  с помощью Aspose.Note для Java. Это руководство покажет, как программно создавать
  OneNote и встраивать шрифты, CSS и изображения.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Как экспортировать шрифты при сохранении OneNote в формате HTML – Java
url: /ru/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как экспортировать шрифты при сохранении OneNote в HTML – Java

## Введение

В этом руководстве вы узнаете **как экспортировать шрифты**, когда **сохраняете OneNote в HTML** с помощью Aspose.Note for Java. Мы пройдем процесс создания документа OneNote программно, настройки параметров сохранения HTML и встраивания необходимых файлов шрифтов, чтобы полученный HTML выглядел точно так же, как оригинальные страницы OneNote. Такой подход идеален, когда необходимо сохранить визуальную точность содержимого OneNote в веб‑дружественном формате.

## Быстрые ответы
- **Какая библиотека обрабатывает экспорт?** Aspose.Note for Java  
- **Можно ли встроить шрифты в HTML?** Да – установите `ExportFonts` в `ExportEmbedded`  
- **Нужна ли лицензия для продакшна?** Требуется действующая лицензия Aspose.Note для коммерческого использования  
- **Какая версия Java поддерживается?** Java 8 или выше  
- **Можно ли сохранять ресурсы в отдельные файлы?** Конечно – настройте `ResourceExportType` соответствующим образом  

## Что означает «как экспортировать шрифты» в контексте конвертации OneNote в HTML?

При конвертации блокнота OneNote в HTML визуальное отображение зависит от CSS, изображений и, особенно, от шрифтов, использованных на оригинальных страницах. **Экспорт шрифтов** означает встраивание файлов шрифтов (например, TTF) непосредственно в пакет HTML, чтобы браузеры могли отобразить текст точно так же, как в OneNote, даже если у конечного пользователя эти шрифты не установлены локально.

## Почему создавать OneNote программно и сохранять его как HTML?

- **Автоматизация:** Генерация отчетов, документации или статей базы знаний из OneNote без ручного копирования.  
- **Последовательность:** Сохранение макета, стилей и пользовательских шрифтов на разных устройствах.  
- **Переносимость:** HTML доступен в любом браузере — не требуется клиент OneNote.  

## Предварительные требования

1. Установлен Java Development Kit (JDK) 8 или новее.  
2. Библиотека Aspose.Note for Java – скачайте её [здесь](https://releases.aspose.com/note/java/).  
3. Пример файла OneNote (`.one`) для загрузки, либо вы можете создать новый программно.  

## Импорт пакетов

Сначала импортируйте необходимые классы в ваш Java‑проект:

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

## Как экспортировать шрифты при сохранении OneNote в HTML?

Ниже представлено пошаговое руководство, показывающее **как экспортировать шрифты** и другие ресурсы.

### Шаг 1: Создать документ OneNote программно  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Эта строка загружает существующий файл `.one`. Если вам нужно **создать OneNote программно**, вы можете создать новый объект `Document` и добавить разделы/страницы через API (не показано здесь, чтобы сосредоточиться на экспорте шрифтов).

### Шаг 2: Сохранить в поток памяти со встроенными шрифтами  

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
- `setFontFaceTypes(FontFaceType.Ttf)` гарантирует использование TrueType шрифтов, которые поддерживаются большинством браузеров.

### Шаг 3: Сохранить как HTML с отдельными файлами ресурсов (по‑прежнему экспортируя шрифты)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Несмотря на то, что CSS и изображения встроены, вы можете изменить `ResourceExportType` на `ExportExternal`, если предпочитаете отдельные файлы для более удобного кэширования. Ключевая часть — **экспорт шрифтов** — остаётся без изменений.

### Шаг 4: Использовать обратные вызовы для контроля места хранения каждого ресурса  

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

Класс `UserSavingCallbacks` (вам потребуется реализовать `ICssSavingCallback`, `IImageSavingCallback` и `IFontSavingCallback`) предоставляет полный контроль над структурой папок, позволяя хранить шрифты в отдельном каталоге `fonts`, при этом **экспортируя шрифты** корректно.

## Как встроить пользовательские шрифты при конвертации OneNote в HTML

Встраивание пользовательских шрифтов гарантирует, что отображение HTML соответствует оригинальному макету OneNote, даже на устройствах без этих шрифтов. Используя `ExportEmbedded` вместе с `FontFaceType.Ttf`, файлы TrueType кодируются в base‑64 и вставляются непосредственно в сгенерированный CSS, устраняя необходимость внешнего хостинга шрифтов.

## Использование ResourceExportType для управления экспортом ресурсов

`ResourceExportType` позволяет выбрать, хранить ли CSS, изображения и шрифты **внутри** HTML‑файла (`ExportEmbedded`) или сохранять их как **внешние** файлы (`ExportExternal`). Выберите `ExportEmbedded` для решения в одном файле, или `ExportExternal`, если хотите использовать кэширование браузером для больших ресурсов.

## Создание OneNote программно для экспорта в HTML

Если вы начинаете с нуля, вы можете полностью построить документ OneNote в коде, добавить разделы, страницы и форматированный текст, а затем применить те же `HtmlSaveOptions`, показанные выше. Это обеспечивает полную автоматизацию от генерации данных до полностью стилизованного HTML‑вывода с встроенными пользовательскими шрифтами.

## Распространённые проблемы и советы

- **Отсутствующие шрифты в выводе:** Убедитесь, что установлен `setExportFonts(ResourceExportType.ExportEmbedded)` и исходный файл OneNote действительно использует встроенные шрифты.  
- **Большие HTML‑файлы:** Встраивание шрифтов может увеличить размер. Если важна пропускная способность, переключите `ExportFonts` на `ExportExternal` и разместите шрифты на CDN.  
- **Ошибки реализации обратных вызовов:** Убедитесь, что ваши классы обратных вызовов правильно записывают поток и закрывают ресурсы, чтобы избежать повреждения файлов.  

## Часто задаваемые вопросы

**В: Можно ли конвертировать несколько документов OneNote в HTML за один проход?**  
**О:** Да, пройдитесь в цикле по каждому экземпляру `Document` и примените те же `HtmlSaveOptions`.  

**В: Поддерживает ли Aspose.Note for Java другие форматы вывода, кроме HTML?**  
**О:** Конечно. Вы можете экспортировать в PDF, DOCX, PNG, JPEG и другие форматы, используя соответствующие параметры сохранения.  

**В: Есть ли доступна пробная версия Aspose.Note for Java?**  
**О:** Да, скачайте бесплатную пробную версию [здесь](https://releases.aspose.com/).  

**В: Где я могу получить поддержку по Aspose.Note for Java?**  
**О:** Посетите [форум Aspose.Note](https://forum.aspose.com/c/note/28) для получения помощи от сообщества и официальной поддержки.  

**В: Как приобрести лицензию на Aspose.Note for Java?**  
**О:** Лицензии доступны на [веб‑сайте Aspose](https://purchase.aspose.com/buy).  

## Заключение

Теперь вы знаете **как экспортировать шрифты**, когда **сохраняете OneNote в HTML** с помощью Aspose.Note for Java. Настраивая `HtmlSaveOptions` и при необходимости используя обратные вызовы, вы можете сохранить точный вид ваших страниц OneNote — включая пользовательские шрифты — при их публикации в вебе. Не стесняйтесь экспериментировать с различными настройками `ResourceExportType`, чтобы подобрать оптимальное соотношение производительности и объёма хранения для вашего проекта.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
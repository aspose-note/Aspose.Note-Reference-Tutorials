---
title: Создание документа OneNote и сохранение в HTML — Java
linktitle: Создание документа OneNote и сохранение в HTML — Java
second_title: Aspose.Note Java API
description: Научитесь создавать и сохранять документы OneNote в формате HTML с помощью Aspose.Note для Java. Интеграция с приложениями Java для программной обработки файлов OneNote.

type: docs
weight: 18
url: /ru/java/onenote-document-loading/create-onenote-save-to-html/
---
## Введение

Aspose.Note для Java — это мощная библиотека, которая позволяет разработчикам программно работать с файлами Microsoft OneNote. В этом уроке мы рассмотрим, как создать документ OneNote и сохранить его в формате HTML с помощью Aspose.Note для Java.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующее:

1. В вашей системе установлен Java Development Kit (JDK).
2.  Aspose.Note для библиотеки Java. Вы можете скачать его с[здесь](https://releases.aspose.com/note/java/).
3. Базовые знания Java-программирования.

## Импортировать пакеты

Сначала импортируйте необходимые пакеты в ваш Java-проект:

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

## Шаг 1. Создайте объект документа OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Этот код инициализирует`Document` объект, загрузив образец файла OneNote.

## Шаг 2. Сохраните как HTML в поток памяти.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Здесь мы настраиваем параметры сохранения HTML и сохраняем документ в поток памяти.

## Шаг 3. Сохраните в формате HTML с ресурсами в отдельных файлах.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

На этом этапе документ сохраняется в формате HTML с такими ресурсами, как CSS, шрифты и изображения, в отдельных файлах.

## Шаг 4. Сохранение в формате HTML в потоке памяти с обратными вызовами для экономии ресурсов.

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

Здесь мы сохраняем документ в формате HTML в поток памяти, используя обратные вызовы для экономии ресурсов.

## Заключение

Поздравляем! Вы узнали, как создать документ OneNote и сохранить его в формате HTML с помощью Aspose.Note для Java. Теперь вы можете интегрировать эту функцию в свои приложения Java для программной работы с файлами OneNote.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я преобразовать несколько документов OneNote в HTML за один раз?

О1: Да, вы можете просмотреть несколько документов и применить процесс сохранения итеративно.

### Вопрос 2. Поддерживает ли Aspose.Note for Java другие форматы вывода, кроме HTML?

О2: Да, Aspose.Note для Java поддерживает различные форматы вывода, включая PDF, DOCX и форматы изображений.

### Вопрос 3: Доступна ли пробная версия Aspose.Note для Java?

О3: Да, вы можете загрузить бесплатную пробную версию с сайта[здесь](https://releases.aspose.com/).

### Вопрос 4. Где я могу получить поддержку Aspose.Note для Java?

 A4: Вы можете получить поддержку от[Форум Aspose.Note](https://forum.aspose.com/c/note/28).

### Вопрос 5: Как я могу приобрести лицензию на Aspose.Note для Java?

 О5: Вы можете приобрести лицензию на сайте[Веб-сайт Aspose](https://purchase.aspose.com/buy).
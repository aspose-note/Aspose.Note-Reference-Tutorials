---
date: 2026-06-30
description: Узнайте, как экспортировать OneNote, сохранив документ в виде PNG‑изображения
  в градации серого с помощью Aspose.Note для Java. Включает шаги по загрузке документа
  OneNote и созданию изображения в градации серого.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Как экспортировать OneNote в изображение в градации серого – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Как экспортировать OneNote в изображение в градации серого – Aspose.Note
url: /ru/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранить в градациях серого в OneNote — Aspose.Note

## Введение

В этом руководстве вы узнаете **how to export onenote**, преобразуя файл OneNote `.one` в высококачественное PNG‑изображение в градациях серого с помощью Aspose.Note для Java. Преобразование в градации серого часто требуется разработчикам Java для печати, архивирования или **уменьшения размера OneNote** без потери важного содержимого. Мы пройдём процесс загрузки документа OneNote, настройки параметров сохранения — включая **регулировку разрешения изображения** — и, наконец, сохранения документа в формате PNG.

## Быстрые ответы
- **Что означает “how to export onenote”?** Это относится к программному преобразованию файла OneNote в другой формат, например изображение, с помощью кода.  
- **Какой формат лучше всего подходит для вывода в градациях серого?** PNG подходит, потому что сохраняет без потерь и поддерживает отдельный режим градаций серого.  
- **Нужна ли лицензия?** Для использования в продакшене требуется действующая лицензия Aspose.Note; временная пробная лицензия доступна для тестирования.  
- **Какая версия Java требуется?** Рекомендуется Java 8 или новее.  
- **Можно ли изменить размер изображения?** Да, вы можете настроить свойства `ImageSaveOptions`, такие как `Resolution` или `PageSize`, перед сохранением.

## Что такое “how to export onenote”?

Экспорт OneNote означает программное преобразование файла OneNote `.one` в другое представление — например PDF, HTML или изображение. В этом руководстве мы сосредоточимся на **создании PNG‑изображений в градациях серого**, что часто требуется для документации или печати. С помощью Aspose.Note преобразование происходит полностью в памяти, поэтому вам не понадобится установленный Microsoft OneNote на сервере.

## Почему экспортировать OneNote в виде изображения в градациях серого?

PNG‑изображения в градациях серого обычно **на 30‑40 % меньше**, чем их полноцветные аналоги, что ускоряет доставку в веб и снижает затраты на хранение. Они также обеспечивают **более чёткий контраст** на лазерных принтерах, делая отчёты легче читаемыми. Поскольку PNG поддерживается практически везде, полученные файлы работают в браузерах, мобильных устройствах и настольных редакторах без дополнительных кодеков.

## Требования

Перед началом убедитесь, что у вас есть:

1. Установлен Java Development Kit (JDK) 8 или новее.  
2. Библиотека Aspose.Note для Java — скачайте последнюю версию [здесь](https://releases.aspose.com/note/java/).  
3. Базовые знания синтаксиса Java и настройка проекта Maven/Gradle.  

## Импорт пакетов

Класс `ImageSaveOptions` управляет тем, как документ рендерится в изображение.  
`ColorMode` — перечисление, позволяющее переключаться между полноцветным и градациями серого выводом.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Шаг 1: Загрузка документа OneNote

`Document` представляет блокнот OneNote и предоставляет методы для загрузки, редактирования и сохранения его содержимого. Сначала **загрузите документ OneNote** в Aspose.Note. Замените `"Your Document Directory"` на путь к вашей локальной папке и `"Aspose.one"` на имя вашего файла OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Шаг 2: Установка пути вывода и параметров

`ImageSaveOptions` настраивает, как документ OneNote будет отрисован в файл изображения. Перечисление `ColorMode` выбирает режим рендеринга цвета, например градации серого или полноцветный. Укажите путь вывода для изображения в градациях серого и задайте параметры сохранения. Мы установим `ColorMode` в `GrayScale` и используем формат **сохранения документа как PNG**. Вы также можете **регулировать разрешение изображения** до 300 DPI для печати высокого качества.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Шаг 3: Сохранение документа

Наконец, сохраните документ как PNG‑изображение в градациях серого, используя настроенные параметры. Метод `save` записывает файл на диск без необходимости создания промежуточных временных файлов.

```java
oneFile.save(dataDir, options);
```

## Распространённые проблемы и решения
- **FileNotFoundException** – Убедитесь, что `dataDir` указывает на правильную папку и файл `.one` существует.  
- **LicenseException** – Убедитесь, что вы применили действующую лицензию Aspose.Note перед вызовом `save`.  
- **Низкое разрешение вывода** – Установите `options.setResolution(300)`, чтобы увеличить DPI; более высокое DPI даёт более чёткую печать, но увеличивает размер файла.  

## Часто задаваемые вопросы

**Q1: Можно ли сохранить изображение в градациях серого в другом формате?**  
A1: Да, просто измените параметр `SaveFormat` в конструкторе `ImageSaveOptions` на `Jpeg`, `Bmp` или любой из более чем 20 поддерживаемых форматов изображений.

**Q2: Совместим ли Aspose.Note со всеми версиями документов OneNote?**  
A2: Aspose.Note поддерживает Microsoft OneNote 2010 и новее, охватывая более 95 % блокнотов, активно используемых сегодня.

**Q3: Требуется ли лицензия для использования Aspose.Note?**  
A3: Для продакшена необходима действующая лицензия, но временную пробную лицензию можно получить для оценки бесплатно.

**Q4: Можно ли изменить другие аспекты документа перед сохранением его как изображения?**  
A4: Конечно! Aspose.Note предоставляет API для редактирования разделов, страниц и отдельных элементов, таких как текст, таблицы и изображения, перед экспортом.

**Q5: Где можно получить поддержку, если возникнут проблемы?**  
A5: Поддержку можно получить на форуме Aspose.Note [здесь](https://forum.aspose.com/c/note/28).

## Заключение

Теперь вы знаете **how to export onenote**, загрузив файл OneNote, настроив параметры сохранения для **создания изображения в градациях серого** и **сохранив документ в формате PNG**. Этот подход идеален для создания лёгких, готовых к печати визуалов из блокнотов OneNote. Не стесняйтесь экспериментировать с другими настройками `ColorMode`, более высокими значениями DPI или альтернативными форматами изображений, чтобы соответствовать требованиям вашего проекта.

---

**Last Updated:** 2026-06-30  
**Tested With:** Aspose.Note 27.0 for Java  
**Author:** Aspose  

---

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Экспортировать страницу OneNote в PNG‑изображение на Java с помощью Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – Установить разрешение выходного изображения в OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Как сохранить OneNote в PDF с помощью Aspose.Note для Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
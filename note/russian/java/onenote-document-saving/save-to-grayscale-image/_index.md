---
date: 2025-12-17
description: Узнайте, как экспортировать OneNote, сохранив документ в виде градаций
  серого PNG‑изображения с помощью Aspose.Note для Java. Включает шаги по загрузке
  документа OneNote и созданию изображения в градациях серого.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Как экспортировать OneNote в изображение в градациях серого – Aspose.Note
url: /ru/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранить в градациях серого в OneNote - Aspose.Note

## Introduction

В этом руководстве мы покажем, **как экспортировать onenote**, сохранив документ в виде изображения в градациях серого с помощью Aspose.Note for Java. Изображения в градациях серого — это монохромные картинки, содержащие только оттенки серого, что может быть полезно для печати, архивирования или уменьшения размера файла. Мы пройдем процесс загрузки документа OneNote, настройки параметров сохранения для **создания изображения в градациях серого**, и, наконец, **сохранения документа как PNG**.

## Quick Answers
- **Что означает «how to export onenote»?** Это преобразование файла OneNote в другой формат, например изображение, программным способом.  
- **Какой формат лучше всего подходит для вывода в градациях серого?** PNG подходит, потому что сохраняет без потерь качество и поддерживает режим градаций серого.  
- **Нужна ли лицензия?** Для использования в продакшене требуется действующая лицензия Aspose.Note; временная пробная лицензия доступна для тестирования.  
- **Какая версия Java требуется?** Рекомендуется Java 8 или выше.  
- **Можно ли изменить размер изображения?** Да, можно настроить свойства `ImageSaveOptions`, такие как `Resolution` или `PageSize`, перед сохранением.

## What is “how to export onenote”?

Экспорт OneNote означает программное преобразование файла OneNote `.one` в другое представление — например PDF, HTML или изображение. В этом руководстве мы сосредоточимся на экспорте в **градации серого PNG** изображение, что часто требуется для документации или печати.

## Why export OneNote as a grayscale image?
- **Уменьшенный размер файла** – PNG в градациях серого обычно меньше, чем полноцветные изображения.  
- **Лучшая читаемость** – Для печатных отчетов градации серого часто обеспечивают более четкий контраст.  
- **Совместимость** – PNG широко поддерживается в браузерах, редакторах и мобильных устройствах.  

## Prerequisites

Перед началом убедитесь, что у вас есть следующее:

1. Установленный Java Development Kit (JDK).  
2. Библиотека Aspose.Note for Java. Вы можете скачать её [здесь](https://releases.aspose.com/note/java/).  
3. Базовые знания программирования на Java.  

## Import Packages

Чтобы начать, импортируйте необходимые пакеты:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Step 1: Load the OneNote Document

Сначала **загрузите документ onenote** в Aspose.Note. Замените `"Your Document Directory"` на путь к вашей локальной папке и `"Aspose.one"` на имя вашего файла One.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Step 2: Set Output Path and Options

Определите путь вывода для изображения в градациях серого и укажите параметры сохранения. Мы установим `ColorMode` в `GrayScale` и используем формат **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Step 3: Save the Document

Наконец, сохраните документ как изображение PNG в градациях серого, используя настроенные параметры.

```java
oneFile.save(dataDir, options);
```

## Common Issues and Solutions
- **FileNotFoundException** – Убедитесь, что `dataDir` указывает на правильную папку и файл `.one` существует.  
- **LicenseException** – Убедитесь, что вы применили действующую лицензию Aspose.Note перед вызовом `save`.  
- **Низкое разрешение вывода** – При необходимости увеличьте DPI, изменив `options.setResolution(300)`.

## Frequently Asked Questions

**В1: Можно ли сохранить изображение в градациях серого в другом формате?**  
О1: Да, просто измените параметр `SaveFormat` в конструкторе `ImageSaveOptions` на `Jpeg`, `Bmp` и т.д.

**В2: Совместим ли Aspose.Note со всеми версиями документов OneNote?**  
О2: Aspose.Note поддерживает Microsoft OneNote 2010 и более новые версии.

**В3: Требуется ли лицензия для использования Aspose.Note?**  
О3: Для продакшн‑использования требуется действующая лицензия, но временную пробную лицензию можно получить для оценки.

**В4: Можно ли изменить другие аспекты документа перед сохранением его как изображения?**  
О4: Конечно! Aspose.Note предоставляет обширный API для редактирования разделов, страниц и содержимого перед экспортом.

**В5: Где можно получить поддержку, если возникнут проблемы?**  
О5: Поддержку можно найти на форуме Aspose.Note [здесь](https://forum.aspose.com/c/note/28).

## Conclusion

Теперь вы знаете **как экспортировать onenote**, загрузив файл OneNote, настроив параметры сохранения для **создания изображения в градациях серого** и **сохранив документ как PNG**. Эта техника полезна для создания легковесных, готовых к печати визуалов из блокнотов OneNote. Не стесняйтесь экспериментировать с другими настройками `ColorMode` или форматами изображений, чтобы соответствовать требованиям вашего проекта.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

---
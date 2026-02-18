---
date: 2026-02-18
description: Узнайте, как создать документ OneNote, отформатировать богатый текст
  и сохранить его в PDF в Java с помощью Aspose.Note. Пошаговое руководство для бесшовной
  автоматизации.
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: Создать документ OneNote и сохранить его в PDF в Java
url: /ru/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

Translate bullet lists.

Translate table content.

Translate Q/A.

Make sure not to translate URLs.

Also keep the "Aspose.Note for Java" unchanged.

Let's craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создать документ OneNote и сохранить как PDF на Java

## Введение

Если вам нужно **создать документ OneNote** и **сохранить OneNote как PDF**, сохранив форматирование rich‑text, вы попали по адресу. В этом руководстве мы пройдем процесс создания документа OneNote, применения пользовательских стилей и экспорта его напрямую в PDF с помощью Aspose.Note for Java. К концу вы получите переиспользуемый фрагмент кода, который можно добавить в любой Java‑проект для автоматизации качественного преобразования OneNote‑в‑PDF.

## Быстрые ответы
- **Что изучает это руководство?** Как создать документ OneNote со стилизованным текстом и сохранить его как PDF.  
- **Какая библиотека требуется?** Aspose.Note for Java (скачивается с официального сайта).  
- **Нужна ли лицензия?** Временная лицензия подходит для тестирования; полная лицензия требуется для продакшна.  
- **Какую IDE можно использовать?** Любую Java‑IDE — IntelliJ IDEA, Eclipse или NetBeans.  
- **Можно ли изменить формат вывода?** Да, Aspose.Note поддерживает PDF, HTML, PNG и другие форматы.

## Что такое «save onenote pdf»?
Сохранение OneNote как PDF означает преобразование структуры страницы OneNote — включая текст, изображения и форматирование — в статический PDF‑файл, который можно просматривать на любой платформе без необходимости установки OneNote.

## Почему форматировать rich text в Java?
Прямое **format rich text** в Java позволяет генерировать документы, выглядящие профессионально и соответствующие фирменному стилю, без ручного редактирования.

## Предварительные требования

1. **Java Development Kit (JDK)** — любая современная версия (8 или выше).  
2. **Aspose.Note for Java JAR** — скачайте его по [download link](https://releases.aspose.com/note/java/).  
3. **IDE** — IntelliJ IDEA, Eclipse или любой другой редактор по вашему выбору.  

## Импорт пакетов

Прежде чем начать, импортируйте необходимые классы в ваш Java‑файл:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Как создать документ OneNote — пошаговое руководство

### Шаг 1: Настройка документа и страницы

Инициализируйте объекты `Document` и `Page`, которые будут содержать весь контент:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Шаг 2: Создание заголовка с форматированием

Добавьте элемент заголовка и примените **set paragraph style** для управления его внешним видом:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### Шаг 3: Создание rich text с форматированием

Здесь мы формируем rich‑text контент, используя несколько объектов `TextStyle`, чтобы продемонстрировать **rich text formatting**:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### Шаг 4: Добавление элементов на страницу и в документ

Объедините заголовок и rich text в иерархии страницы:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Шаг 5: Сохранение документа — экспорт OneNote в PDF

Наконец, экспортируйте документ OneNote как PDF‑файл:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Распространённые проблемы и решения

| Проблема | Решение |
|----------|----------|
| **File not found** | Убедитесь, что `dataDir` указывает на существующую папку и у вас есть права на запись. |
| **Missing fonts** | Убедитесь, что шрифты, которые вы используете (например, *Calibri*), установлены на машине. |
| **License not applied** | Загрузите вашу лицензию Aspose перед созданием `Document`, чтобы избежать водяных знаков оценки. |

## Часто задаваемые вопросы

**В: Можно ли дальше настраивать стили шрифтов?**  
О: Да, вы можете изменить дополнительные свойства, такие как подчеркивание, зачеркивание и выравнивание текста, используя классы `TextStyle` и `ParagraphStyle`.

**В: Совместима ли Aspose.Note for Java со всеми Java‑IDE?**  
О: Абсолютно. Пока IDE поддерживает стандартную разработку на Java, вы можете добавить JAR‑файл Aspose.Note в classpath проекта.

**В: Можно ли интегрировать эту функциональность в веб‑приложения?**  
О: Да, тот же код работает в servlet‑базированных или Spring Boot приложениях, позволяя динамически генерировать OneNote‑в‑PDF на стороне сервера.

**В: Какие лицензионные требования у Aspose.Note for Java?**  
О: Для продакшн‑использования требуется коммерческая лицензия. Временная лицензия доступна для оценки и тестирования.

**В: Поддерживает ли Aspose.Note for Java другие форматы документов, помимо OneNote?**  
О: Да, он поддерживает PDF, HTML, PNG, JPEG и несколько других форматов экспорта, предоставляя гибкость при конвертации страниц OneNote в нужный вам формат.

## Заключение

В этом руководстве мы продемонстрировали, как **создать документ OneNote**, применить **rich text formatting** и **сохранить OneNote как PDF** с помощью Aspose.Note for Java. Следуя пошаговым инструкциям, вы сможете автоматизировать создание качественных документов OneNote и их конвертацию в PDF в любой Java‑решении.

---

**Последнее обновление:** 2026-02-18  
**Тестировано с:** Aspose.Note for Java 24.11 (последняя на момент написания)  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
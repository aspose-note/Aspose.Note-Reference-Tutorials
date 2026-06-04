---
description: Узнайте, как сохранять PDF‑файлы OneNote и добавлять подстраницы в OneNote
  с помощью Aspose.Note для Java. Следуйте этому пошаговому руководству, чтобы эффективно
  организовать свои заметки.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Как сохранить PDF из OneNote и добавить подстраницы
url: /ru/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как сохранить OneNote в PDF и добавить подстраницы

## Введение

В этом руководстве вы узнаете, **как сохранить OneNote в PDF**, создав документ, содержащий как корневые, так и подстраницы, с помощью Aspose.Note for Java. Организация блокнотов OneNote с чёткой иерархией упрощает навигацию, а возможность экспорта в PDF гарантирует, что ваши заметки можно будет поделиться в универсальном читаемом формате. Мы также покажем, как **добавить подстраницы в стиле onenote**, чтобы легко строить многоуровневые структуры.

## Быстрые ответы
- **Что означает основной ключевой запрос?** Он относится к экспорту блокнота OneNote в PDF с использованием Aspose.Note.
- **Какой API используется?** Aspose.Note for Java.
- **Можно ли создавать иерархические страницы?** Да — задайте уровень страницы, чтобы построить корневые и подстраницы.
- **Нужна ли лицензия?** Доступна бесплатная пробная версия; для продакшн‑использования требуется коммерческая лицензия.
- **Какие форматы вывода поддерживаются?** BMP, PDF, PNG и другие.

## Что такое «как сохранить OneNote PDF»?
Сохранение OneNote в PDF преобразует страницы блокнота в документ фиксированного макета, сохраняющий форматирование, изображения и иерархию. Это идеально для обмена, архивирования или печати заметок.

## Почему стоит добавлять подстраницы onenote?
Добавление подстраниц позволяет группировать связанный контент под родительской страницей, имитируя структуру папок. Это улучшает организацию заметок, ускоряет поиск и повышает удобство чтения при экспорте блокнота в PDF.

## Предварительные требования

Перед началом убедитесь, что у вас есть следующие требования:

1. Java Development Kit (JDK): Убедитесь, что JDK установлен в вашей системе.  
2. Aspose.Note for Java: Скачайте и установите Aspose.Note for Java с [веб‑сайта](https://purchase.aspose.com/buy).  
3. Интегрированная среда разработки (IDE): Выберите Java IDE, например IntelliJ IDEA, Eclipse или NetBeans.

## Импорт пакетов

Начните с импорта необходимых пакетов в ваш Java‑проект:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Шаг 1: Настройка каталога документа

Определите каталог, в котором вы хотите сохранить документ OneNote:

```java
String dataDir = "Your Document Directory";
```

## Шаг 2: Создание объекта Document

Создайте объект `Document`:

```java
Document doc = new Document();
```

## Шаг 3: Создание страниц

Инициализируйте объекты страниц и задайте их уровни. Уровень определяет, является ли страница корневой или подстраницей:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Шаг 4: Добавление узлов на страницы

### Добавление узлов на первую страницу

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Добавление узлов на вторую страницу

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Добавление узлов на третью страницу

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Шаг 5: Добавление страниц в документ

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Шаг 6: Сохранение документа

Сохраните документ OneNote в PDF (или BMP в этом примере). Изменение `SaveFormat` позволяет экспортировать в PDF, что удовлетворяет требованию «как сохранить OneNote PDF»:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Полезный совет:** Чтобы экспортировать напрямую в PDF, замените `SaveFormat.Bmp` на `SaveFormat.Pdf`.

Поздравляем! Вы успешно создали документ OneNote с корневыми и подстраницами и узнали, **как сохранить OneNote PDF** с помощью Aspose.Note for Java.

## Почему это важно

- **Иерархическая организация:** Корневые и подстраницы позволяют имитировать структуру папок внутри OneNote.  
- **Бесшовный экспорт в PDF:** После организации экспорт в PDF сохраняет иерархию, делая итоговый документ удобным для чтения и обмена.  
- **Автоматизация:** Код можно интегрировать в более крупные Java‑приложения, позволяя пакетно создавать структурированные блокноты.

## Распространённые ошибки и способы их избежать

| Проблема | Причина | Решение |
|----------|---------|----------|
| Страницы отображаются на одном уровне | Неправильное значение `setLevel` | Используйте `setLevel((byte) 1)` для корневых страниц и `setLevel((byte) 2)` (или выше) для подстраниц. |
| PDF‑вывод пустой | Отсутствует `SaveFormat.Pdf` или неверный путь к файлу | Убедитесь, что каталог существует, и используйте `SaveFormat.Pdf`. |
| Шрифт не применяется | Неправильное имя шрифта или шрифт не установлен в системе | Убедитесь, что шрифт (например, “David Transparent”) установлен на машине, где выполняется код. |

## Часто задаваемые вопросы

**В: Можно ли создавать несколько уровней подстраниц с помощью Aspose.Note for Java?**  
О: Да, можно создавать более глубокие иерархии, задавая более высокие номера уровней (например, `setLevel((byte) 3)` для подстраницы третьего уровня).

**В: Совместим ли Aspose.Note for Java с различными Java‑IDE?**  
О: Абсолютно. Он работает с IntelliJ IDEA, Eclipse, NetBeans и любой IDE, поддерживающей разработку на Java.

**В: Можно ли настроить форматирование текста в моём документе OneNote?**  
О: Да. Используйте `ParagraphStyle` для установки имени шрифта, размера, цвета и других атрибутов для каждого элемента `RichText`.

**В: Поддерживает ли Aspose.Note for Java сохранение документов в форматах, отличных от BMP?**  
О: Да. Поддерживаемые форматы включают PDF, PNG, JPEG, DOCX и другие. Измените соответствующее значение перечисления `SaveFormat`.

**В: Есть ли пробная версия Aspose.Note for Java?**  
О: Да, бесплатную пробную версию можно скачать с сайта Aspose.

## Заключение

Организация блокнотов OneNote с чёткой иерархической структурой и их экспорт в PDF делает ваши заметки более доступными и удобными для совместного использования. Следуя приведённым шагам, вы теперь знаете, **как сохранить OneNote PDF** и **добавить подстраницы в стиле onenote** программно с помощью Aspose.Note for Java.

---

**Последнее обновление:** 2026-01-07  
**Тестировано с:** Aspose.Note for Java 24.11 (latest)  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
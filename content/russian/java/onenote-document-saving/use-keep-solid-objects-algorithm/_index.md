---
title: Использование алгоритма сохранения твердых объектов в OneNote — Aspose.Note
linktitle: Использование алгоритма сохранения твердых объектов в OneNote — Aspose.Note
second_title: Aspose.Note Java API
description: Узнайте, как сохранить твердые объекты в документах Aspose.Note при преобразовании в PDF с помощью алгоритма сохранения твердых объектов в Java.
type: docs
weight: 25
url: /ru/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---
## Введение

В этом уроке мы рассмотрим, как использовать алгоритм Keep Solid Objects в Aspose.Note для Java. Этот алгоритм имеет неоценимое значение для сохранения целостности твердых объектов в ваших документах при их преобразовании в формат PDF. Мы разберем процесс шаг за шагом, обеспечивая ясность и понимание на каждом этапе.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующее:

1. В вашей системе установлен Java Development Kit (JDK).
2.  Aspose.Note для библиотеки Java. Вы можете скачать его с[здесь](https://releases.aspose.com/note/java/).

## Импортировать пакеты

Для начала импортируем необходимые пакеты:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Шаг 1. Загрузите документ

Загрузите документ в Aspose.Note, используя следующий фрагмент кода:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Шаг 2. Настройте параметры сохранения PDF

Определите PdfSaveOptions и установите для PageSplittingAlgorithm значение KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Шаг 3. Отрегулируйте ограничение высоты (необязательно).

При необходимости вы можете настроить ограничение высоты клонированных деталей:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Шаг 4. Сохраните документ

Наконец, сохраните документ с указанными параметрами сохранения PDF:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Заключение

В этом уроке мы узнали, как использовать алгоритм Keep Solid Objects в Aspose.Note для Java. Этот алгоритм гарантирует сохранение твердых объектов в ваших документах при их преобразовании в формат PDF, обеспечивая целостность документа.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я настроить ограничение высоты для клонированных деталей?

 О1: Да, вы можете настроить предел высоты клонированных деталей в соответствии с вашими требованиями, используя`heightLimitOfClonedPart` параметр.

### Вопрос 2. Где я могу найти дополнительную документацию?

 A2: Вы можете найти подробную документацию по Aspose.Note для Java.[здесь](https://reference.aspose.com/note/java/).

### В3: Есть ли бесплатная пробная версия?

 О3: Да, вы можете получить бесплатную пробную версию Aspose.Note для Java.[здесь](https://releases.aspose.com/).

### Вопрос 4. Как я могу получить поддержку, если у меня возникнут какие-либо проблемы?

 О4: Вы можете получить поддержку от сообщества Aspose.[здесь](https://forum.aspose.com/c/note/28).

### В5: Где я могу приобрести лицензию?

 A5: Вы можете приобрести лицензию на Aspose.Note для Java.[здесь](https://purchase.aspose.com/buy).

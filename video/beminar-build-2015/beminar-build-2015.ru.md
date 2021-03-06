# Видео вебинара по БЭМ: сборка и оптимизация проекта

30 апреля 2015 года мы провели **второй вебинар по БЭМ**, в котором подробно показали процесс сборки БЭМ-проекта. 

Как мы знаем, методология БЭМ рекомендует сохранять каждый блок в отдельный файл. Но потом их ещё нужно собрать. 

В ходе вебинара на примере [Gulp](http://gulpjs.com/) мы наглядно показали, как это делается — сами вы сможете затем использовать 
практически любой сборщик. Возможно, кто-то из вас даже пробовал [bem-tools](https://ru.bem.info/tools/bem/bem-tools/) или 
[ENB](https://ru.bem.info/tools/bem/enb-bem-examples/), и это здорово. В будущем мы обязательно расскажем, почему для сборки 
проектов в Яндексе используем именно их.

Это вебинар для тех, кто уже немного знаком с БЭМ. Вам будут необходимы базовые знания HTML и CSS, понимание общих процессов 
веб-разработки и умение пользоваться командной строкой. Для выполнения заданий понадобится терминал с установленными 
git, Node.js и npm, а также знания, полученные на прошлом вебинаре. 

Если вы пропустили его, обязательно посмотрите [видео](https://ru.bem.info/talks/beminar-css-2015/).

## Содержание вебинара

Краткий повтор: основы методологии БЭМ и именование сущностей в CSS, HTML и файловой системе.

Сборка БЭМ-проекта с помощью Gulp:

- сборка блоков в технологии CSS и изображений;
- сборка только нужных блоков, используемых в html-файлах;
- оптимизация рабочего процесса с помощью browser-sync и postCSS.

Автоматизация рутинной работы с помощью командной строки.

Видео вебинара, презентацию и ответы на ваши вопросы мы собрали в этом посте.

##  Видео вебинара

<iframe width="450" height="225" src="https://video.yandex.ru/iframe/ya-events/vuvreu3orq.6137/" frameborder="0" allowfullscreen="1"></iframe>

##  Презентация вебинара

<iframe src="https://www.slideshare.net/slideshow/embed_code/key/iDv4gVl8hEFwJ4" width="476" height="400" frameborder="0" marginwidth="0" marginheight="0" scrolling="no"></iframe>

## Ответы на вопросы

------

**Вопрос**: А зачем несколько тасков? Почему нельзя все в дефолт написать и пользоваться одной командой?

**Ответ**: Для универсальности использования задачи делаются настолько маленькими, насколько возможно. Потом можно запустить 
пересборку только html или только css, например.

------

**Вопрос**: Как сделать так, что бы при сбое в процессе сборки ничего не ломалось и watch на тасках продолжал работать? Как 
обрабатывать ошибки в настройках gulp?

**Ответ**: Например, воспользоваться модулем https://github.com/floatdrop/gulp-plumber

------

**Вопрос**: Как сделать так, что бы gulp watch подтягивал автоматически новосозданные файлы?

**Ответ**: Использовать floatdrop/gulp-watch

------

**Вопрос**: Можете оформить html2bl как плагин?

**Ответ**: Присылайте issue https://github.com/dab/html2bl

------

**Вопрос**: С SASS нормально все работать будет? В смысле, ходить по файлам, собирать css?

**Ответ**: Конечно, можно использовать пре- и пост-процессоры.

------

**Вопрос**: С копированием картинок явная проблема, если в разных блоках лежат картинки с одинаковыми именами. Как разруливать?

**Ответ**: Можно не использовать одинаковые имена, а задавать имена с использованием имени блока. Можно инлайнить картинки 
с помощью postcss.

------

**Вопрос**: Что с адаптивностью у блоков? У каждого блока могут быть свои правила адаптивности, как их группировать?

**Ответ**: Можно воспользоваться модулями Gulp.js для группировки стилей по media-queries.

------

**Вопрос**: Такая файловая структура у блоков подразумевает наличие отдельных файлов для стилей элементов и модификаторов? 
В данном примере всё стили в одном файле.

**Ответ**: Такая файловая структура и наш процесс сборки подразумевают, что все стили блоков, элементов и модификаторов 
находятся в одном файле. Для того, чтобы элементы и модификаторы лежали отдельно, надо дописать сборку соответствующим образом.

------

**Вопрос**: А можно сделать так, чтобы собирать модификации pink, potter и так далее через командную строку и не переписывать 
постоянно gulp.js? К примеру, сделать команду gulp build pink и на выходе получить pink.

**Ответ**: Конечно, можно. Можно сделать для каждого файла свою задачу и вызывать ее. А можно добавить обработку аргументов 
командной строки и брать имя html-файла и название уровня из этих аргументов.

------

Надеемся, что видео и ответы на вопросы помогают вам в ходе обучения. 

До встречи на следующих «БЭМинарах» и **Stay BEMed**!

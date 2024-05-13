---
title: 'Отложенное чтение: OpenSource-альтернатива / Хабр'
date: 2022-04-28
src_link: https://www.notion.so/OpenSource-b9886dd37361443b87d3e877bfcb5d11
src_date: '2022-04-28 09:09:00'
gold_link: https://habr.com/ru/articles/229883/
gold_link_hash: 9cdfd8ff1a5754ab89cca3ff7723fdf0
tags:
- '#host_habr_com'
---

![](https://habrastorage.org/r/w780q1/getpro/habr/post_images/61e/259/763/61e2597631a706761741bb986d289f11.jpg)  

  

Недавно я открыл для себя удобство отложенного чтения — когда заинтересовавшую статью в сети можно прочитать в любое время, комфортно расположившись c любимым девайсом на диване / пляже / под одиноким деревцем на тропе, ведущей к базовому лагерю у подножья Эвереста. И хотя проприетарных решений для этого хватает (Instapaper, Pocket, Readability), душа настойчиво требовала OpenSource. И вот к какому решению я пришёл после исследования возможных вариантов.  

  

  

  

#### Каталог

  

В качества каталога, в который собираются статьи, я использую приложение [Wallabag](https://www.wallabag.org/) (бывший Poshe, Github-страничка проекта [здесь](https://github.com/wallabag/wallabag)), позволяющее быстро и просто сохранить выбранный контент с оригинальным форматированием, таблицами и картинками (но при этом аккуратно вырезанной рекламой и лишними элементами) для последующего чтения его онлайн или на мобильном устройстве. Приложение предназначено для развертывания на собственном сервере, однако можно бесплатно зарегистрироваться на дружественном проекту сайте [Framabag](http://www.framabag.org/) и начать пользоваться уже установленным и настроенным инстансом. Для тестирования мной был заведен аккаунт там, однако приложение настолько понравилось, что сейчас я задумываюсь о переезде на своё оборудование. Процесс установки на свой сервер подробно описан [здесь](https://www.wallabag.org/frequently-asked-questions/#How_can_I_install_wallabag_and_what_are_the_requirements).  

  

  

#### Сохранение статей

  

Статьи в каталог я забираю с помощью расширения для [Firefox](https://addons.mozilla.org/firefox/addon/wallabag/), которое также поддерживает и мобильную версию браузера. Еще можно утаскивать тексты из активных вкладок, используя Java-Script-строку, сохраненную в закладках:  

  


```
javascript:if(top['bookmarklet-url@wallabag.org']){top['bookmarklet-url@wallabag.org'];}else{(function(){var url = location.href || url;window.open('http://ссылка_на_инстанс_wallabag/?action=add&url=' + btoa(url),'_self');})();void(0);}

```
  

Также доступно расширение для [Chrome](https://chrome.google.com/webstore/detail/wallabag/bepdcjnnkglfjehplaogpoonpffbdcdj) и приложения для [iOS](https://itunes.apple.com/us/app/wallabag/id828331015) и [Windows Phone](http://www.windowsphone.com/en-us/store/app/wallabag/ff890514-348c-4d0b-9b43-153fff3f7450).  

  

  

#### Чтение

  

Wallabag отдаёт список статей в виде RSS-ленты, поэтому удобно использовать для отложенного чтения любимый RSS-агрегатор. Для этого в настройках каталога генерируется личный маркер (token) и появившаяся ссылка на «Ленту непрочитанного» скармливается приложению для работы с RSS.  

  

[![](https://habrastorage.org/r/w780q1/getpro/habr/post_images/e76/393/f42/e76393f423e47f7c4ed5869e9f2337c7.jpg)](https://habrastorage.org/getpro/habr/post_images/e76/393/f42/e76393f423e47f7c4ed5869e9f2337c7.jpg)  

  

Для чтения на Android я использую:  

  

* [FeedEx](https://f-droid.org/repository/browse/?fdfilter=sparse&fdid=net.fred.feedex) (Android 4.0.3+) для смартфона и планшета;
* [Sparse rss](https://f-droid.org/repository/browse/?fdfilter=sparse&fdid=de.shandschuh.sparserss) (Android 1.5+) для Nook Simple Touch, листание кнопками dpad «вверх» и «вниз» (кнопки с правой стороны экрана в прошивке [ZeroLab Nooter](http://4pda.ru/forum/index.php?showtopic=253792&st=8860#entry17904246)).

  

  

Обе программы имеют лицензию open-source, умеют загружать статьи вместе с картинками для дальнейшего чтения оффлайн и синхронизировать ленту через установленный интервал времени. Официальное приложение для Android [существует](https://f-droid.org/repository/browse/?fdid=fr.gaulupeau.apps.InThePoche), однако оно развивается медленно и пока не умеет добавлять новые ссылки, подгружать картинки, да и вообще требует Android 2.2 (Nook Simple Touch отпадает).  

  

  

#### Минусы решения:

  

* бо́льшее количество времени, требуемого для настройки, чем при использовании проприетарных решений;
* при чтении статьи через RSS на мобильном устройстве нет возможности отметить ее как «прочитанную» в каталоге Wallabag, при посещении веб-интерфейса приходится дополнительно ставить там галку на этой статье.

  

  

#### Плюсы:

  

* удобный и эффективный инструмент для отложенного чтения, в том числе оффлайн;
* возможность экспорта статей в ePub (отдельных текстов и всего каталога сразу);
* поддержка нескольких пользователей — один инстанс на всю семью и друзей;
* возможность миграции своего профиля из других сервисов отложенного чтения (Instapaper и иже с ними) и экспорта своего Wallabag-каталога в json;
* избранное, поиск, темы и теги в веб-интерфейсе;
* возможность отложенного чтения на старых версиях Android;
* открытый код, бесплатность;
* приватность (в случае использования собственного сервера).

  

  

#### Вместо заключения

  

[Александр Зиновьев](https://ru.wikipedia.org/wiki/%C7%E8%ED%EE%E2%FC%E5%E2,_%C0%EB%E5%EA%F1%E0%ED%E4%F0_%C0%EB%E5%EA%F1%E0%ED%E4%F0%EE%E2%E8%F7) говорил об обучении: «Когда человек перестает учиться, он вступает в стадию старения». Надеюсь, эта небольшая статья поможет тебе, хабровчанин, читать, учиться и узнавать что-то новое проще, эффективнее и удобнее, дольше оставаясь молодыми и полными сил для дел, которые по-настоящему важны.   

  

  

  

  

#### P.S.:

  

1) Уважаемый [pred8or](http://habrahabr.ru/users/pred8or/) [подсказывает](http://habrahabr.ru/post/229883/#comment_7781703) как настроить инстанс Wallabag для локального сохранения картинок: нужно в файле конфигурации (inc/poche/config.inc.php) исправить строчку:  


```
define ('DOWNLOAD_PICTURES', TRUE);

```
  

2) Достопочтенный [subvillion](http://habrahabr.ru/users/subvillion/) [делится](http://habrahabr.ru/post/229883/#comment_7781999) в комментариях информацией об еще одной альтернативе — [Astatum](https://github.com/x0x01/astatum).  

  

  

  

  

#### P.P.S.: Немного скриншотов:

  



|  |  |
| --- | --- |

  



|  |  |  |
| --- | --- | --- |
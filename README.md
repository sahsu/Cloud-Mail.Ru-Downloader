# Cloud.Mail.Ru Downloader from https://github.com/Geograph-us/Cloud-Mail.Ru-Downloader
* this is modify version with Ubuntu friendly
* you need install php, aria2 stuff
```
cd `YOUR_DIRECTORY_OF_CLOUD_MAIL_RU_DOWNLOADER`
ln -s `which aria2c` .
ls -al 
lrwxrwxrwx 1 root root    21 Sep  5 16:34 aria2c -> /usr/local/bin/aria2c
```
* update your download link into links.txt
```
php mail.ru_downloader.php
```
* and you will see downloads/ with your files.


# Cloud&#64;Mail.Ru Downloader

Многопоточное скачивание из облака [Mail.Ru](http://cloud.mail.ru/) по публичной ссылки. Авторизация в Mail.Ru не требуется.

- Скрипт консольный, написан на PHP.
- Для скачивания используется консольный загрузчик [Aria2c](https://aria2.github.io/).
- Скрипт умеет корректно обрабатывать папки в облаке любой вложенности.
- Поддерживается докачка файлов.
- Для работы скрипта нужно установить php на компьютер, например отсюда http://windows.php.net/download/ (если уже установлен какой-нибудь Веб-сервер, например, [Denwer](http://www.denwer.ru/) или [OpenServer](http://open-server.ru/), то php от него тоже подойдет).
- Скрипт работает в PHP версий *5.x.x-7.2.x*.

## Порядок работы

- Скачать релиз скрипта, в который уже включена минимальная версия php
- В файл `links.txt` записать публичные ссылки на скачивание с облака вида https://cloud.mail.ru/public/9bFs/gVzxjU5uC по одной на строку.
- Запустить `start.bat`
- Скрипт сформирует файл с прямыми ссылками на скачивание `input.txt`.
- После чего запустится Aria2c Downloader, который скачает файлы из `input.txt`.
- Остаётся наблюдать за закачкой и ждать её завершения. Скачанные файлы окажутся в папке `downloads`.

[![Скрипт за работой](image.png)](image.png)

## Настройка PHP, если используете уже установленный
В `php.ini` должно быть активировано openssl-расширение:
>extension_dir = "ext"\
>extension=php_openssl.dll

### Видео-пример:
[![Cloud.MailRu.Downloader Video example](https://img.youtube.com/vi/WnJyXEdEqfI/0.jpg)](https://www.youtube.com/watch?v=WnJyXEdEqfI)

***
#### Надеюсь этот скрипт Вам пригодится!

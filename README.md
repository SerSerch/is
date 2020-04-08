# Information Security

## lesson 1
``` bash
sudo apt install git
sudo apt install curl
sudo apt install nginx
sudo nginx
// проверка запуска
ps aux | grep nginx
// редактирование файла
sudo gedit [file_name]
// настройка сервера
cd /etc/nginx/sites-available/
// скопирование файла
sudo cp default test.conf
cd /etc/nginx/sites-enabled/
// создание ссылки
sudo ln -s ../sites-available/test.conf test.conf
cd /var/log/nginx/
// просмотр логов
tail access.log
// установка php
sudo apt install php-fpm
// установка burp suite
bash burpsuite.sh
// остановка nginx
sudo nginx -s stop
// перезапуск nginx
sudo nginx -s reload
```

## lesson 2
* //mail.ru
* /blog/post.txt
* ?post=1
* #post1
* http://localhost
* https://geekbrains.ru
* mailto:test@mail.ru
* tel:+79808080808
* file:///var/www/html/index.html
* javascript:alert("XSS")
* data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4=
``` bash
// декодирование base64
echo "PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4=" | base64 -d
// получение IP
host geekbrains.ru
// получение информации об IP
whois 5.61.239.22
// изменение hosts
sudo gedit /etc/hosts
```

## lesson 3
``` bash
// подключение к серверу по порту
telnet [host] [port]
// запрос
[method] [path]?[params] [protocol]
Host: [host]
Referer: [url]
// вывод закоровков запросов и ответов
curl -i [host] | less
// вывод запросов больше информации
curl -v [host] 2>&1 | less
```

* 1** - информационная
* 2** - успешный
* 3** - перенаправление
* 4** - ошибка в запросе
* 5** - ошибка на сервере

``` html
// запрет передачи url ref
<meta name="referrer" content="no-referrer">
```
# ДЗ №38 Динамический веб
```
развернуть веб портал на выбор в vagrant
Варианты стенда
nginx + php-fpm (laravel/wordpress) + python (flask/django) + js(react/angular)
nginx + java (tomcat/jetty/netty) + go + ruby
можно свои комбинации

Реализации на выбор
- на хостовой системе через конфиги в /etc
- деплой через docker-compose

Для усложнения можно попросить проекты у коллег с курсов по разработке
```

## Практическая часть

Настроен Vagrantfile и плейбук ansible для развертки следующей конфигурации:
1) проект https://github.com/Rafael-99-spec/django-helloworld висит на порту localhost:8000 и проксирутся nginx с порта 83
2) проект https://github.com/Rafael-99-spec/go-http-hello-world висит на порту localhost:8800 и проксирутся nginx с порта 81
3) проект https://github.com/Rafael-99-spec/react-helloworld висит на порту localhost:7777 и проксирутся nginx с порта 82


- Для развертывания стенда необходимо скачать репозиторий на локальное хранилищье, войти в директорию с Vagrantfile и запустить стенд - ```vagrant up```.

- Проверка работоспособности:
Можно перейти по ссылкам после разворачивания стенда: 

http://192.168.100.20:83 

http://192.168.100.20:82 

http://192.168.100.20:81 

---

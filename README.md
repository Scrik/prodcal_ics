# Как использовать?
Ссылка на подписной календарь: https://prodcal.nikitastupin.com/prodcal.ics (http://prodcal.nikitastupin.com/prodcal.ics на случай, если я не обновлю TLS сертификат)

### Настройка подписного календаря на iOS
![Шаг 1](doc/iphone-guide.jpg)
### Настройка подписного календаря на MacOS
...
### Настройка подписного календаря в Google Calendar
...

# Как поднять у себя на сервере
1. Установить необходимые модули для Python:
```
$ pip3 install -r requirements.txt
```
1. Настроить автообновление календаря:
```
$ crontab -l
0 1 * * * python3 /home/ubuntu/prodcal_ics.py --start-year=2018 -o /home/ubuntu/www/prodcal.ics
```
1. Отдавать файл любым сервером prodcal.ics (например, nginx)

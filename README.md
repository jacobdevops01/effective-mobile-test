# Effective Mobile - тестовое задание 

## 1. запуск проекта

Клонируем репозиторию

```bash
git clone https://github.com/jacobdevops01/effective-mobile-test.git
```
Переходим в директориию проекта:
```bash
cd effective-mobile-test
```

## 2. запускаем контейнер

```bash
docker-compose up -d

Без фона (если хотите сразу видеть логи в терминале):

docker-compose up
``` 
если docker-compose up -d просит sudo, это значит, что у вашей учётной записи нет прав на работу с Docker без sudo. Есть два варианта:

1-вариант
```bash
Использовать sudo прямо командой
sudo docker-compose up -d
```

2-вариант

Добавляем своего пользователя в группу Docker:

```bash
sudo usermod -aG docker $USER
```

## Проверка работы - выполняем команду в терминале 
```bash
curl http://localhost 
```

Мы должны увидеть :

```bash
Hello from Effective Mobile!
```

как работает схема:

**Nginx** принимает внешние запросы и перенаправляет их на backend а **Backend** отвечает только внутри Docker-сети текстом `Hello from Effective Mobile!`.

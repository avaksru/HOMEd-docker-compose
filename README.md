
# Быстрое развертывание  HOMEd docker-compose

### Обновим систему
```bash
sudo apt update
sudo apt upgrade
```
### Ставим пакеты 
```bash
sudo apt install docker docker.io docker-compose mc
```
### Создаем каталог проекта и скачиваем файлы конфигурации
```bash
cd /opt
git clone https://github.com/avaksru/HOMEd-docker-compose.git services
cd services
```
### Меняем в файле conf\homed\homed-zigbee.conf настройки MQTT сервера на свои.

### Запускаем HOMEd. Переходим в каталог /opt/services
```bash
./start.sh
```
### Посмотреть логи:
```bash
sudo docker-compose logs homed
```
### Остановить / запустить  / рестартовать HOMEd:
```bash
sudo docker-compose stop/start/restart homed
```
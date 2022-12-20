
Быстрое развертывание  HOMEd docker-compose

# Обновим систему
sudo apt update
sudo apt upgrade

# Ставим пакеты 
sudo apt install docker docker.io docker-compose mc

# Создаем каталог проекта и скачиваем файлы конфигурации
cd /opt
git clone https://github.com/avaksru/-HOMEd-docker-compose.git services
cd services

# Меняем в файле conf\homed\homed.conf настройки MQTT сервера на свои.

# Запускаем HOMEd. Переходим в каталог /opt/services
./start.sh

# Посмотреть логи:
sudo docker-compose logs homed

# Остановить / запустить  / рестартовать HOMEd:
sudo docker-compose stop/start/restart homed
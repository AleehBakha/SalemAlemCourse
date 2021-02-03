# Установка необходимого ПО

### В данном курсе нам понадобятся:
* Visual Studio Code - наш основной редоктор кода
* OpenJDK 11 - набор инструментов для разработки на Java

### [Установка на Windows 10](https://www.youtube.com/)
### [Установка на Ubuntu 20.04](https://www.youtube.com/)
### Установка на Linux Mint/Kali Linux:

* Установим для начала Visual Studio Code:
    1. Переходим на сайт: https://code.visualstudio.com/Download
    2. Скачиваем .deb версию 
    3. Переходим в каталог со скачанным пакетом
    4. Запускаем в терминале команду:
       
            sudo apt install ./<pkg-name>.deb
    
* Установим OpenJDK 11:
    1. Откроем терминал
    2. Обновляемся командой:
       
            sudo apt update
    3. Проверим установлена ли Java и, если установлена, посмотрим её версию командой:
    
            java -version
        Если Java не установлена мы увидим следующий вывод:
            
            Command 'java' not found, but can be installed with:

            sudo apt install openjdk-11-jre-headless  # version 11.0.9.1+1-0ubuntu1~20.04, or
            sudo apt install default-jre              # version 2:1.11-72
            sudo apt install openjdk-8-jre-headless   # version 8u275-b01-0ubuntu1~20.04
            sudo apt install openjdk-13-jre-headless  # version 13.0.4+8-1~20.04
            sudo apt install openjdk-14-jre-headless  # version 14.0.2+12-1~20.04

    4. Установим Java следующей командой:
    
            sudo apt install default-jdk
        Проверим версию следующей командой:
       
            javac -version
        Мы должны увидеть подобную строку:
            
            javac 11.0.7
    
### Установка на Manjaro Linux:

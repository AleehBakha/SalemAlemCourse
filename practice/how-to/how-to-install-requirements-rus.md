# Қажетті БЖ-ны орнату

### Курс барысында қолданылатын программалар:
* Visual Studio Code - біздің негізгі код редакторы
* OpenJDK 11 -  Java тілімен код жазуға қажетті құралдар жиынтығы

### [Windows 10 жүйесіне орнату](https://www.youtube.com/)
### [Ubuntu 20.04 серверіне орнату](https://www.youtube.com/)
### Linux Mint/Kali Linux-ке орнату:

Осы тармақта біз тек қана орнату процессін қарастырамыз! \
Орнату процессі Ubuntu 20.04 серверіне арналған видеосабағында көрсетілген.

* Ең алдымен Visual Studio Code программасын орнатамыз:
    1. https://code.visualstudio.com/Download сілтемесі арқылы өтеміз
    2. .deb нұсқасын жүктейміз.
    3. Жүктелген құжат арқылы каталогке отеміз.
    4. Команданы терминалда іске асырамыз:
       
            sudo apt install ./<pkg-name>.deb
            Мұндағы <pkg-name> - әрдайым жүктелген құжаттың аты
    
* OpenJDK 11 -ді орнатайық:
    1. Терминалды ашамыз.
    2. Төмендегі команданы қолданып парақшамызды жаңартамыз:
       
            sudo apt update
    3. Java орнатылған жағдайда, орнатылған нұсқасын тексеруіміз жөн:
    
            java -version
            Java  орнатылмаған жағдайда шығарылатын жазба:
            
            Command 'java' not found, but can be installed with:

            sudo apt install openjdk-11-jre-headless  # version 11.0.9.1+1-0ubuntu1~20.04, or
            sudo apt install default-jre              # version 2:1.11-72
            sudo apt install openjdk-8-jre-headless   # version 8u275-b01-0ubuntu1~20.04
            sudo apt install openjdk-13-jre-headless  # version 13.0.4+8-1~20.04
            sudo apt install openjdk-14-jre-headless  # version 14.0.2+12-1~20.04

    4. Java программалау тілін төменде берілген команда арқылы орнатамыз:
    
            sudo apt install default-jdk
        Нұсқаны осы команда арқылы тексереміз:
       
            javac -version
        Мынадай жол көрінуі тиіс:
            
            javac 11.0.7


### Fedora Linux-қа орнату:
Бұл бөлімде біз тек орнатылым барысын қарастырамыз! \
Орнату процессі Ubuntu 20.04-ке арналған бейнероликте сипатталған.

* Алдымен Visual Studio Code орнатамыз:
    1. Терминалда Microsoft-қа yum репозитоорийлерін қосатын команданы іске қосамыз:

           sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
           sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
    2. Пакеттік кэшті жаңартып, бағдарламаны dnf (Fedora 22 және жоғары нұсқалары үшін) арқылы орнатыңыз:
            
            sudo dnf check-update
            sudo dnf install code
    3. Алдыңғы нұсқалары үшін yum қолданылады.
* OpenJDK 11 орнатамыз:
    1. Терминалды іске қосамыз.
    2. Келесі командамен жаңартыламыз:

           sudo dnf update
    3. Java орнатылғанын тексерейік, егер орнатылған болса, оның нұсқасын командалар бойынша көрейік:

            java -version
       Егер Java орнатылмаған болса, біз келесі нәтижені көреміз:

            Command 'java' not found
        
    4. Java-ны келесі командамен орнатыңыз:

            sudo dnf install java-11-openjdk.x86_64
       Нұсқасын келесі команда арқылы тексереміз:

            javac -version
       Біз осындай жолды көруіміз керек:

            javac 11.0.7

### Manjaro Linux-те орнату:

Бұл бөлімде біз тек орнату процесін сипаттаймыз! \
Орнату процессі Ubuntu 20.04-ке арналған бейнероликте сипатталған.

* Алдымен Visual Studio Code орнатамыз:
  
        Маңызды ескерту! Нұсқаулықта AUR (Arch user repository) қолданылады.
        Амалдарды мұқият әрекет ете отырып орындаңыз.
    1. Құрастырманы AUR-дан жүктейміз:
    
            curl -L -O https://aur.archlinux.org/cgit/aur.git/snapshot/visual-studio-code-bin.tar.gz
    2. Жүктелген мұрағаттың орамасын шешеміз:
       
            tar -xvf visual-studio-code-bin.tar.gz
    3. Қаптамадан шыққан каталогқа өтеміз:
       
            cd visual-studio-code-bin
    4. Пакет құрастырамыз:
    
            makepkg -si
    
* OpenJDK 11 орнатыңыз:
    1. Терминалды іске қосамыз.
    2. Келесі командамен жаңартыламыз:

            sudo pacman -Syu
                
    3. Java орнатылғанын тексерейік, егер орнатылған болса, оның нұсқасын командалар бойынша көрейік:
    
            java -version
       Егер Java орнатылмаған болса, біз келесі нәтижені көреміз:

            Command 'java' not found
  4. Java-ны келесі командамен орнатыңыз:
     
            sudo pacman -S jre11-openjdk-headless jre11-openjdk jdk11-openjdk openjdk11-doc openjdk11-src

     Нұсқасын келесі команда арқылы тексереміз:

          javac -version
     Біз осындай жолды көруіміз керек:

          javac 11.0.7

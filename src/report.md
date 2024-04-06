# Linux_01

## Part 1. Установка ОС

- ``Смотрим версию Ubuntu после установки ``<br>
![Alt text](./screen/1.png "Optional Title")<br>


---

## Part 2. Создание пользователя

- ``Создаём пользователя и назначаем ему группу adm``<br>
![Alt text](./screen/2.png "Optional Title")<br>


- ``Вывод списка пользователей (новый юзер в конце списка)``<br>
![Alt text](./screen/2.1.png "Optional Title")<br>

---


## Part 3. Настройка сети ОС

- ``Новое имя устройства: hostnamectl set-hostname user-1``<br>
![Alt text](./screen/3.1.1.png "Optional Title")<br>

- ``Меняем тайм зону sudo timedatectl set-timezone Europe/Moscow``<br>
![Alt text](./screen/3.2.png "Optional Title")<br>

- ``Установка net-tools``<br>
- ``sudo apt install net-tools``<br>

- ``Вывели информацию о сетевых интерфейсах``<br>
![Alt text](./screen/3.3.1.png)<br>
- ``**lo (loopback device)** – виртуальный интерфейс, присутствующий по умолчанию в любом Linux. Он используется для отладки сетевых программ и запуска серверных приложений на локальной машине. С этим интерфейсом всегда связан адрес 127.0.0.1.``<br>


- ``Получили ip от dhcp сервера``<br>
![Alt text](./screen/3.4.1.png)<br> 
- ``DHCP (Dynamic Host Configuration Protocol) - это протокол сетевого уровня, который позволяет устройствам автоматически получать IP-адрес, подсеть, шлюз по умолчанию и другие сетевые настройки от специального сервера, известного как DHCP-сервер.``<br>

- ``Выводим внешний IP-адрес``<br>
![Alt text](./screen/3.5.1.png "Optional Title")<br>

 - ``Выводим внутренний IP-адрес``<br>
![Alt text](./screen/3.5.2.png "Optional Title")<br>

- ``Меняем настройки сети вимом: sudo vim /etc/netplan/00-installer-config.yaml``<br>
![Alt text](./screen/3.6.2.png "Optional Title")<br>

- ``Сохраняем изменения, перезагружаем машину``<br>
![Alt text](./screen/3.6.3.png "Optional Title")<br>

- ``Проверяем настройки, и успешно ли пингуются удаленные хосты 1.1.1.1``<br>
![Alt text](./screen/3.7.1.png "Optional Title")<br>
- ``и ya.ru``<br>
![Alt text](./screen/3.7.2.png "Optional Title")<br>


---


## Part 4. Обновление ОС

- ``Обновляем ОС``<br>
![Alt text](./screen/4.png "Optional Title")<br>


---


## Part 5. Использование команды **sudo**

- ``Выдаем права sudo второму пользователю``<br>
![Alt text](./screen/5.1.png "Optional Title")<br>
- ``Меняем hostname OS от его имени``<br>
![Alt text](./screen/5.2.png "Optional Title")<br>


---


## Part 6. Установка и настройка службы времени

- ``Выводим время, часового пояса, в котором мы сейчас находимся``<br>
![Alt text](./screen/6.png "Optional Title")<br>

---


## Part 7. Установка и использование текстовых редакторов 

- ``Используя каждый из трех редакторов - Vim, Nano, Joe, создаем файл *test_X.txt*, где X -- название редактора, в котором создан файл. В нём пишем свой никнейм, и закрываем файл с сохранением изменений.``<br>
- ``$ sudo apt update; $ sudo apt install vim; $ sudo apt install nano; $ sudo apt install joe; ``<br>


- `` Vim. Режим редактирования - I. Для выхода из режима редактирования Esc. Для сохранения изменений Shift + Z + Z либо :wq Чтобы изменения не сохранялись :q!``<br>
![Alt text](./screen/7.1vim.png "Optional Title")<br>

- ``Nano. Для сохранения изменений Ctrl + O > Enter. Для выхода Ctrl + X. После нажатия Ctrl+X откроется меню и на экране появится вопрос Save modified buffer?. Чтобы выйти без сохранения изменений, нажимаем клавишу N``<br>
![Alt text](./screen/7.1nano.png "Optional Title")<br>

- ``Joe. Для выхода с сохранением из Joe Ctrl + K затем X.``<br>
![Alt text](./screen/7.1joe.png "Optional Title")<br>


- ``Используя каждый из трех выбранных редакторов, открываем файл на редактирование, редактируем файл, заменив никнейм на строку "21 School 21", закрываем файл без сохранения изменений.``<br>

- ``Vim``<br>
![Alt text](./screen/7.2vim.png "Optional Title")<br>


- ``Nano``<br>
![Alt text](./screen/7.2nano.png "Optional Title")<br>


- ``Joe``<br>
![Alt text](./screen/7.2joe.png "Optional Title")<br>
- ``Для выхода без сохранения можно также использовать комбинацию клавиш Ctrl+K и затем Q (символ "Q") для выхода из редактора. Если в файл были внесены изменения, Joe спросит: (Save modified buffer?). Чтобы выйти без сохранения изменений, нажмите клавишу N (символ 'N'). ``<br>


- ``Используя каждый из трех выбранных редакторов, отредактируем файл ещё раз, а затем освоим функции поиска по содержимому файла (слово) и замены слова на любое другое.``<br>

- ``В Vim для поиска слова в файле мы можем использовать команду /<word>``<br>
![Alt text](./screen/7.3.2vim.png "Optional Title")<br>


- ``После того, как Vim найдет первое совпадение, можно заменить это слово на другое с помощью команды :%s/old_word/new_word/g, где old_word - заменяемое, а new_word - заменяющее``<br>
![Alt text](./screen/7.3.1vim.png "Optional Title")<br>


- ``Ctrl + W, чтобы открыть поиск по содержимому файла. Введите слово или фразу, которую вы хотите найти, и нажмите Enter.``<br>
![Alt text](./screen/7.3.1nano.png "Optional Title")<br>


- ``Чтобы заменить найденное слово или фразу на другое, используем комбинацию Alt + R или Option + R``<br>
![Alt text](./screen/7.3.1nano.png "Optional Title")<br>
- ``Затем вводим новое слово или фразу. Для замены - Enter.``<br>
![Alt text](./screen/7.3.2nano.png "Optional Title")<br>


- ``Нажимаем Ctrl + K, затем клавишу F. Откроется строка поиска в нижней части экрана``
![Alt text](./screen/7.3.1joe.png "Optional Title")<br>


- ``Для замены нажимаем клавишу Ctrl + K, затем клавишу F. Откроется строка поиска в нижней части экрана.``<br>
![Alt text](./screen/7.3.2joe.png "Optional Title")<br>
- ``Вводим искомое слово, затем Enter. Joe предложит выбор, нажимаем R для замены слова, затем вводим новое слово.``<br>
- ``Enter, чтобы заменить найденные совпадения.``<br>
![Alt text](./screen/7.3.2joe.png "Optional Title")<br>

---



## Part 8. Установка и базовая настройка сервиса **SSHD**


- ``Сначала устанавливаем службу SSHD: $ sudo apt-get install ssh``<br>

- ``Затем настраиваем автозапуск служб при перезапуске системы ``<br>
![Alt text](./screen/8.2.png "Optional Title")<br>

- ``Переконфигурируем службу SSHd на порт 2022``<br>
![Alt text](./screen/8.3.2.png "Optional Title")<br>


- ``Перезапускаем систему : $ systemctl restart sshd``<br>

- ``Используя команду ps, показываем наличие процесса sshd``<br>
![Alt text](./screen/8.4.png "Optional Title")<br>
- ``* ps (показывает запущенные процессы, выполняемые пользователем в окне терминала); * ps -e или ps -A (Для просмотра всех запущенных процессов); * ps -d (Чтобы показать все процессы,кроме лидеров сессий); * ps -d -N (Вы можете инвертировать вывод с помощью переключателя -N. Например, если я хочу отобразить только лидеров сессий) * ps T (показывает только процессы,связанные с этим терминалом); * ps r (посмотреть все запущенные (running) процессы); * ps -p 'pid' (если вы знаете PID процесса, вы можете просто использовать следующую команду, чтобы вывести процесс с этим 'pid'); * ps -p 'pid1' 'pid2' * ps U 'userlist' (найти все процессы, выполняемые определенным пользователем); * ps -ef (получить полный список).``<br>


- ``Перезагружаем систему : $ reboot;`` <br>
![Alt text](./screen/8.5.2.png "Optional Title")<br>
- ``Выводим команду: $ netstat -tan;`` <br>
![Alt text](./screen/8.5.3.png "Optional Title")<br>
- `` Флаги для netstat : -t (--tcp) отображает только tcp соединения; -a (--all) отображает все активные TCP соединения; -n (--numeric) отображает активные TCP соединения с адресами и номерами портов в числовом формате; Proto: имя протокола (протокол TCP или протокол UDP); recv-Q: очередь на получение сети; end-Q: очередь на отправку сети; Local Address адрес локального компьютера и номер используемого порта; Foreign Address адрес и номер удаленного компьютера, к которому подключен сокет; State состояние сокета; 0.0.0.0 означает IP-адрес локального компьютера.`` <br>


---



## Part 9. Установка и использование утилит **top**, **htop**

- ``top`` <br>
![Alt text](./screen/9.png "Optional Title")<br>
- ``Время работы  - 15 минут. Количество авторизованных пользователей - 1. Общая нагрузка на систему - 0.00 0.00 0.00. Общее количество процессов - 94. Загрузка процессора - 0.0%. Загрузка памяти - 145/1971мб. PID процесса, использующего больше всего памяти - 1.   PID процесса, занимающего больше всего процессорного времени - 1091``<br>

- ``htop`` <br>

- ``Sort by PID`` <br>
![Alt text](./screen/9PID.png "Optional Title")<br>

- ``Sort by Percent CPU`` <br>
![Alt text](./screen/9PERCENT.png "Optional Title")<br>

- ``Sort by Percent MEM`` <br>
![Alt text](./screen/9MEM.png "Optional Title")<br>

- ``Sort by Percent TIME`` <br>
![Alt text](./screen/9TIME.png "Optional Title")<br>

- ``Filtered by sshd`` <br>
![Alt text](./screen/9ssh.png "Optional Title")<br>

- ``Searched by syslog`` <br>
![Alt text](./screen/9syslog.png "Optional Title")<br>

- ``С добавленным выводом hostname, clock и uptime`` <br>
- ``Перенаправление в файл`` <br>
![Alt text](./screen/9.1.png "Optional Title")<br>
- ``Вывод из файла`` <br>
![Alt text](./screen/9.2.png "Optional Title")<br>


---



## Part 10. Использование утилиты **fdisk**

- ``$ sudo fdisk -l; $ swapon``<br>
![Alt text](./screen/10.png "Optional Title")<br>
- ``Имя диска - VBOX HARDDISK, Размер диска - 30 GiB, Количество секторов - 62914560, Размер свопа - 1G``<br>

---



## Part 11. Использование утилиты **df** 

- ``$ df``<br>
![Alt text](./screen/11.png "Optional Title")<br>
- ``df Отчет для корневого раздела (/): * размер раздела - 8408452 Кбайт; * размер занятого пространства - 5099468 Кбайт; * размер свободного пространства - 8489432 Кбайт; * процент использования - 38%. ****  
![Alt text](./screen/11.2.png "Optional Title")<br>
- ``df -Th Отчет для корневого раздела (/): * размер раздела - 14 Гбайт; * размер занятого пространства - 4,9 Г; * размер свободного пространства - 8.1 Г; * процент использования - 38%; * тип файловой системы для раздела - ext4.``<br>

---


## Part 12. Использование утилиты **du**

- ``$ sudo du -sh /var/log /var /home ``<br>
![Alt text](./screen/12.1.png "Optional Title")<br>
- ``$ sudo du -s --block-size=1 /var/log /var /home`` <br>
![Alt text](./screen/12.1.2.png "Optional Title")<br>

- ``$ sudo du -sh /var/log/*`` <br>
![Alt text](./screen/12.2.png "Optional Title")<br>


---



## Part 13. Установка и использование утилиты **ncdu**

- ``Устанавливаем ncdu`` <br>
- ``sudo apt install ncdu`` <br>

- ``Выводим размер папки /home`` <br>
![Alt text](./screen/13home.png "Optional Title")<br>

- ``Выводим размер папки /var`` <br>
![Alt text](./screen/13var.png "Optional Title")<br>

- ``Выводим размер папки /var/log.`` <br>
![Alt text](./screen/13log.png "Optional Title")<br>


---



## Part 14. Работа с системными журналами

- ``$ sudo nano /var/log/auth.log`` <br>
![Alt text](./screen/14auth.log.png "Optional Title")<br>
- ``* Последняя успешная авторизация: Aug 27 12:24:48; * Имя пользователя: albettge; * Метод входа: pam-unix.`` <br>
- ``$ sudo nano /var/log/dmesg; <br>
![Alt text](./screen/14dmesg.png "Optional Title")<br>
- `` $ sudo nano /var/log/syslog; <br>
![Alt text](./screen/14syslog.png "Optional Title")<br>
- `` $ sudo systemctl restart ssh; $ cat /var/log/syslog ``<br>
![Alt text](./screen/14sshd.png "Optional Title")<br>
- ``Скрин с сообщением о рестарте службы`` <br>

---



## Part 15. Использование планировщика заданий **CRON**

- `` Используя планировщик заданий, запускаем команду uptime через каждые 2 минуты: $  sudo crontab -e ``<br>
![Alt text](./screen/15.1.png "Optional Title")<br>

- `` Скрин со списком текущих заданий для CRON после удаления``<br>
![Alt text](./screen/15.3.png "Optional Title")<br>
- `` Нет текущих задач``<br>
![Alt text](./screen/15.4.png "Optional Title")<br>


---









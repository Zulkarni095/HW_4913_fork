# Краткое руководство по работе с Git

## 1.Основные команды
* git init - **инициализация локального репозитория**
* git commit - **создание commit**

## 2.Работа с ветками  
* git branch branch_name - **создает ветку с именем branch_name**
* git branch - **выводит список веток**

## 3. Как сделать pull request
1. Делаем (fork) интересующего нас репозитория
2. Мы делаем git clone для нашей версии этого репозитория
3. СОздаем ветку с предлагаемыми изменениями
4. Производим все изменения только в этой ветке
5. Далее отправляем все изменения к себе в аккаунт (push)
6. В окне на Github появляется возможность отправить pull request

## 4. Как работать с GitHub
1. Создали аккаунт на Github.com
2. Создать локальный репозиторий
3. "подружить" ваш локальный и удаленный репозиторий. Github присоздании нового репозитория подскажет как это можно сделать)
4. Отправить (push) ваш локальный репозиторий в удаленный на (на Github), при этом вам, возможно, нужно будет авторизовться на удаленном репозитории.
5. Провести изменения "с другого компьютера"
6. Выкачать (pull) актуальное состояние 
## Терминология
Некоторые термины, которые будут встречаться далее, и значение которых нужно понимать

* __Репозиторий__ - это проще говоря - папка.
* __Удаленный репозиторий__ - это папка на Gitlab, ваш проект на Gitlab.
* __Локальный репозиторий__ - это папка на вашем компьютере.
* __Коммит__ - это некая совокупность изменений, сделанных вами, которая будет отправлена в удаленный репозиторий. Коммитить - по сути значит сохранять изменения.
* __Проиндексировать изменения__ - выполнить команду, которая выберет какие файлы мы будем коммитить. Сначала мы индексируем изменения, потом их коммитим.
* __Запушить изменения__ - отправить ваш коммит на удаленный репозиторий.
* __Спулиться__ - забрать себе в локальный репозиторий изменения, которые были запушены в удаленный репозиторий другим человеком.*

## Плюсы использования Git
 С открытым исходным кодом — можно использовать бесплатно. Вы можете загрузить его исходный код и изменить его в соответствии с вашими потребностями. Кроме того, в Интернете доступно множество ресурсов для изучения лучших практик Git.
Быстрый и легкий — основная часть Git и большинство его операций записываются и выполняются локально, что делает его быстрее, чем централизованная система контроля версий.
Умеренная аппаратная мощность — Git не требует мощного оборудования, так как членам команды нужно взаимодействовать с сервером только при отправке или извлечении изменений в основном репозитории. Это также полезно для растущих команд, поскольку Git не требует дополнительных требований к оборудованию, независимо от того, сколько людей его использует.
Безопасная среда — он использует SHA1, криптографическую хеш-функцию, для идентификации объектов в своей базе данных. Он проверяет каждый файл и фиксацию во время операции извлечения, поэтому невозможно изменить данные в базе данных без сохранения Git изменений.
Более безопасное резервное копирование — Git создает несколько копий ваших данных, отражая репозиторий для всех клиентов, что позволяет создавать больше резервных копий. Кроме того, Git может делать моментальные снимки, которые являются представлениями файловой системы, что позволяет вам вернуться к состоянию, в котором был сделан моментальный снимок. Это может быть полезным решением для восстановления в случае сбоя.
Более простое ветвление — создание, удаление и объединение ветвей занимает всего несколько секунд, что делает его более эффективным по времени и менее сложным, чем централизованная система контроля версий.

## Коммиты
Основы работы с Git предполагают понимание коммитов. Команда git commit откроет текстовый редактор для ввода сообщения коммита. Также эта команда принимает несколько аргументов:

-m позволяет написать сообщение вместе с командой, не открывая редактор. Например git commit -m "Пофиксил баг";
-a переносит все отслеживаемые файлы в область подготовленных файлов и включает их в коммит (позволяет пропустить git add перед коммитом);
--amend заменяет последний коммит новым изменённым коммитом, что бывает полезно, если вы неправильно набрали сообщение последнего коммита или забыли включить в него какие-то файлы.
## Советы для эффективного введения в Git:

Коммитьте как можно чаще.
Одно изменение — один коммит: не помещайте все не связанные между собой изменения в один коммит, разделите их, чтобы было проще откатиться.
Формат сообщений: заголовок должен быть в повелительном наклонении, меньше 50 символов в длину и должен логически дополнять фразу this commit will ___(this commit will fix bugs — этот коммит исправит баги). Сообщение должно пояснять, почему был сделан коммит, а сам коммит показывает, что изменилось.
Если у вас много незначительных изменений, хорошим тоном считается делать небольшие коммиты при разработке, а при добавлении в большой репозиторий объединять их в один коммит.
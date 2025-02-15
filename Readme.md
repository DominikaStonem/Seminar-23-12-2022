# Инструкция по работе с Git

## Что такое Git?
***Git*** - сама популярная реализация распределенной системы контроля версий (версионность поддерживается и на сервере, и у каждого клиента). Самой распространненой реализацией ***Git*** является (GitHub)[https://github.com]

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Для этого необходимо открыть в теринале папку с будущем репозиторием и написать *git init*.

## Создание коммита
Для создания новой фиксации (коммита) используется команда *git commit*. Для этого в терминале с папкой-репозиторием пишем *git commit -m "<сообщение коммиту>*. Сообщение к коммиту писать ***Обязательно!***

## Добавление файлов к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Используется она следующим образом: в терминале с папкой-репозиторием пишем *git add <название файла>*.

## Журнал изменений
Для просмотра историй изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.

## Перемещение между коммитами
Для переещения на другую фиксацию (коммит) используется команда *git checkout*. Для этого необходимо, как показона в прошлом пункте, в журнале изменений найти необходимый коммит и его хеш (номер), после чего в терминале с папкой-репозиторием написать *git checkout <хеш коммита>*. После выполения этой команды мы попадаем в состояние **detached head**, в котором никаие следующие коммиты сохраняться не будут. Для выхода из этого состояние необходимо писать *git checkout master*.

## Ветки в Git

### Создание веток в Git
Для создания веток  в Git используем команду *git branch <название ветки>*.
Далле можем вызвать данную ветку команой *git checkout <название ветки>* и продолжать работу в ней.

### Просмотр списка веток
Для просмотра списка веток используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch*. Выделенная зеленым со звездочкой ветка - это ветка, на которой мы находимся в данный момент.

### Перемещение между ветками
Для перехода на другую ветку используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название ветки>*.Такая ветка должна **существовать**.

### Слияние веток и разрешение конфликтов
Для слияния веток юзерам необходимо ввести *git branch merge <название ветки>*
Если вы уверены в правильности информации в данной ветке и хотите внести данную информацию в свой "чистовик", то вам необходимо для этого перейти в ветку "мастер" (*git checkout master*) и затем ввести команду, укаанную выше.

## Удаление веток
Если вы хотите удалить ветку, которую слили, необходимо ввести *git delete -d <название ветки>*.

##  Добавление нового удаленного репозитория
Чтобы добавить новый удаленный репозиторий, выполните команду git remote add в терминале в каталоге, в котором обнаружен репозиторий.
Команда git remote add принимает два аргумента:
имя удаленного репозитория, например, происхождение;
URL-адрес удаленного репозитория, например, https://github.com/user/repo.git.

##  Удаление удаленного репозитория
Чтобы удалить удаленный URL-адрес из репозитория, використовуйте команду git remote rm.
Команда git remote rm принимает один аргумент:
имя удаленного репозитория, например, пункт назначения.
При удалении удаленного URL-адреса из репозитория высокая только отмена привязки для случаев и удаленных репозиториев. Сам удаленный репозиторий не проходит.

##  Выбор URL-адреса для удаленного репозитория
Существует несколько вариантов клонирования репозиториев, доступных на GitHub.com.
При просмотре репозитория во время входа в учетную запись под сведениями о репозитории показа URL-адреса, который можно использовать для клонирования проекта на компьютер.
Сведения о возможности использования удаленного URL-адреса см. в разделе Управление удаленными репозиториями.

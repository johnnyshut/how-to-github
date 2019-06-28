
# How to GitHub
Тестовый репозиторий, упоминается в инструкции телеграмм канала https://t.me/YellowHummer 

*Перед работай с Git зарегистрируйся на github.com и создайте репозиторий*

## Как начать работать с Git!
Здесь я хочу собрать и описать самые простые команды, чтобы при получении ишуза (issues) от Алóиса Альцгéймера не забыть ключевые команды и ответить "git reset HEAD --hard"

**Установи GIT**
```no-highlight
для Windows > http://msysgit.github.io/
для RPM > yum install git-core
для DEB > apt-get install git
```

**Настрой Git, так Git связывает Ваш аккаунт и Ваши изменения**
```no-highlight
git config --global user.name JohnnyDoe         // Ваше имя
git config --global user.email jshut@yandex.ru  // Ваш Email
```

**Настрой Git для Windows**
```no-highlight
git config --global core.autocrlf true
git config --global core.safecrlf false
git config --global core.eol native
```

**Создай локальный GIT репозиторий для своего продукта**
```no-highlight
cd ./git                    // открываем каталог "git" в папке пользователя OS
git init ./PROJECTNAME      // инициализируем каталог проекта. <PROJECTNAME> - любое имя вашего проекта, может не совпадать с именем удаленного репозитория.
cd ./PROJECTNAME            // открываем каталог проекта
```

**Подключи стандартные каталоги**
```no-highlight
git remote add origin https://github.com/johnnyshut/HowToGitHub     // создаем ветвь разработки "origin" в удаленном репозитории
git fetch origin                                                    // получение изменений и вывод их на экран
git merge origin/master                                             // объединяет изменений и локального проекта
```

**Создай файл в локальном репозитории**
```no-highlight
mkdir hello             // создадим каталог в локальном репозитории
cd hello                // перейдем в созданный каталог "hello"
touch helloWorld.txt    // создадим файл "helloWorld.txt"!
```

**Свяжи новый файл с удаленным репозиторием**
```no-highlight
git add helloWorld.txt          // отмечаем файл для отправки или команда "git add .", чтобы отметить все файлы 
git commit -m "First Commit"    // помечаем все новые и измененные файлы сообщением (commit)
```

**Отправь код на удаленный репозиторий**
```no-highlight
git push -u origin master   // флаги используются только в первый раз, потом используем команду без флагов "git push"
git status                  // вывод информации об изменениях которые были сделаны
git pull                    // скачивание репозитория, полностью. Выполняет последовательно fetch и merge, без вывода на экран статусов
```

**Как вызвать справку?**
```no-highlight
git help <команда>
git <команда> --help
man git-<команда>
```

## Для использования репозитория на другом компьютере:

**Клонирование репозитория**
```no-highlight
git clone https://github.com/johnnyshut/HowToGitHub     // git скачает удаленный репозиторий в новую папку HowToGitHub и создаст локальный репозиторий
```

**После изменений в локальном репозитории, выполняем команды описанные выше**
```no-highlight
git add .
git commit -m "I changed the my life!"
git push
```

**Откат изменений**
```no-highlight
git reset HEAD --hard           // полный откат до предыдущего коммита
git checkout helloWorld.txt     // сброс изменений в файле на версию коммита 
git checkout v1                 // откат до установленного тега, например v1
```

*P.S. Все команды актуальны для любого сервиса Git
Инструкция по созданию репозитория https://help.github.com/en/articles/creating-a-new-repository*


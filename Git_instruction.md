# Работа с Git

## 1. Проверка наличия установленного Git:
В терминале выполнить команду ***`git version`***. 
Если Git установлен, то появится сообщение с информацией о версии программы. Иначе будет сообщение об ошибке.

## 2. Установка Git
Загружаем последнюю версию Git с сайта https://git-scm.com/downloads.
Устанавливаем с настройками по умолчанию

## 3. Настройка Git
При первом использовании Git необходимо представиться. Для этого нужно ввести в терминале две команды:
```
    git config --global user.name «Ваше имя английскими буквами»
    git config --global user.email ваша почта@example.com
```

## 4. Инициализация репозитория
Для инициализации репозитория необходимо перейти в локальную папку, планируемую для использования в качестве репозитория, и выполнить команду ***`git init`*** в терминале. После выполнения этой команды локальный репозиторий будет инциализирован.

## 5. Запись изменений в репозиторий
Команды терминала, применяемые для записи изменений в репозиторий Git, это:
```
1. git status
2. git add
3. git commit
4. git diff
```

### 5.1 git status
Команда ***`git status`*** является основным инструментом просмотра состояния файлов в репозитории. При этом в зависимости от различных состояний файлов может быть несколько вариантов вывода.

Если в терминале после ввода данной команды появилось следующее:
```
$ git status
On branch master
nothing to commit, working tree clean
```

то такой вывод означает, что в репозитории либо нет отслеживаемых файлов, либо все отслеживаемые файлы репозитория не изменялись.

Если в терминале после ввода данной команды появилось следующее:
```
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        <filename>

no changes added to commit (use "git add" and/or "git commit -a")
```

то такой вывод означает, то в репозитории существует неотслеживаемый файл с именем *\<filename>*.

Если в терминале после ввода данной команды появилось следующее:
```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   <filename>

no changes added to commit (use "git add" and/or "git commit -a")
```

то такой вывод означает, то в репозитории изменен отслеживаемый файл с именем *\<filename>*.

### 5.2 git add
Команда ***`git add`*** используется для начала отслеживания за новым файлом. Для файла с именем *\<filename>*, чтобы начать его отслеживание в репозитории, необходимо ввести:
```
git add <filename>
```

При этом команда ***`git status`*** покажет, что файл стал отслеживаемым:
```
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   <filename>
```


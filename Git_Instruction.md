## Основные команды Git

## Урок 1 - Основные команды Git

_**"git config --global user.name(user.email) <user_name(email)>"**_ - регистрирует имя(почту) пользователя в Git.

_**"Git init"**_ - создаёт репозиторий (папку в которой настроена система контроля версий)

_**"Git add <file.name>"**_ - даёт команду Git'у отслеживать указанный файл, чтобы можно было его закоммитить.

_**"commit -m"**_ - сохраняет текущую версию файла. Приставка "-m" позволяет дать название этому сохранению, чтобы было удобнее ориентироваться среди других коммитов.

_**git diff**_ - показывает отличия между текущим состоянием файла и его последним коммитом.

_**git log**_ - показывает историю коммитов файла.

_**"git status"**_ - показывает статус документа, наличие отслеживаемых, неотслеживаемых, модифицированных(отредактированных несохранённых) файлов.

_**"git checkout <name_branch(commit_id)>"**_ - перемещает вас к указанному коммиту или ветке.

_**"cd <file_name>"**_ - указывает папку, в которой Git'у работать.

_**"cd.."**_ - выходит из папки, в которой вы находитесь(делает "шаг назад").

_**"git commit --all"**_ - добавляет все файлы в папке в коммит. 

"clear" - очищает терминал.

*Объёмные файлы(например, фото) в коммиты, как правило не вносят, а хранят отдельно. А для того, чтобы Git в команде "status" не указывал их, как неотслеживаемые, можно создать файл _**".gitignore"**_ и в него вносить названия файлов, которые не нужно отслеживать.


## Урок 2 - Работа с ветками

*Ветки можно использовать как черновики и отдельные рабочие пространства для каждого человека при работе в команде, компании. А затем "сливать" их в одно целое, единый проект.*

_**"git branch"**_ - показывает список имеющихся веток. Знак звёздочки (*) указывает, на какой ветке вы находитесь.

_**"git branch <branch_name>"**_ - создаёт новую ветку. 

_**"git checkout <branch_name>"**_ - позволяет перемещаться между ветками.

_**"git checkout -b <branch_name>"**_ - сочетает в себе команды **checkout & branch**. Создаёт новую ветку и сразу же перемещает вас в неё. 

_**"git merge <branch_name>"**_ - переносит данные из указанной ветки в ту, в которой вы находитесь.

_**"git branch -d <branch_name>"**_ - удаляет указанную ветку.

_**"git log --graph"**_ - показывает историю коммитов в виде древа с ветками. 

## Урок 3 - Удаленные репозитории.

### *Список команд для того, чтобы отправить локальный репозиторий на GitHub:*

1. _**git remote add origin <"link">**_ - указывает Git'у путь(ссылку) на удаленный репозиторий, связывает его с локальным. (Дословно, "добавить удаленый источник")
2. _**git branch -M <"master">**_ - назначает ветку (в данном случае, это ветка "master") главной. То есть по умолчанию, при использовании команды "git push", данные будут отправляться с этой ветки, если мы не указываем другую ветку.
3. _**git push -u origin <"master">**_ - отправляет данные из указанной ветки (в данном случае, ветки "master") в удалённый репозиторий на GitHub. (Дословно, "толкнуть данные в Hub")

### Другие команды:

_**"git clone <"link">"**_ - копирует репозиторий с GitHub. Используется, когда вы хотите взять чей-то репозиторий и внести в него изменения. 

_**"git pull"**_ - отправляет данные из GitHub в ваш локальный репозиторий. Используется, когда на GitHub в удаленный репозиторий внесли изменения(например, вы приняли **pull request**), и вы хотите перенести их на компьютер.

* _**pull request**_ - это запрос на внесение изменений со стороны. Когда кто-то берёт чужой репозиторий, вносит в него изменения и спрашивает владельца репозитория, хочет ли он внести их.
* Кнопка _**"FORK"**_ на GitHub используется для копирования чужого репозитория на свой аккаунт, чтобы работать с ним самостоятельно. 




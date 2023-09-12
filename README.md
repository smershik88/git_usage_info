# Использование системы Git

## Команды git

| Команда                        | Результат выполнения |
|--------------------------------|----------------------|
|`git init`| создает репозиторий в текущем каталоге|
|`git status`| выводит статус (состояние) репозитория в текущем каталоге|
|`git add`| подготовить файл к сохранению (коммиту)|
|`git add --all`| подготовить все файлы к сохранению (коммиту)|
|`git commit -m "text"`| сделать коммит с комментарием "text"|
|`git commit --amend --no-edit`| дополнить коммит новыми файлами (работает только с последним коммитом - HEAD), опция `--no-edit` указывает о том, что сообщение коммита менять не нужно|
|`git commit --amend -m "Новое сообщение"`| изменить сообщение коммита|
|`git log`| вывести историю коммитов|
|`git log --oneline`| вывести краткую историю коммитов|
|`git remote add <origin> <url>`| связать репозиторий с удаленным (\<origin\> - имя удаленного, \<url\> - url к удаленному репозиторию)|
|`git remote -v`| позволяет убедиться, что локальный и удаленный репозитории связаны (-v = --verbose)|
|`git push`| отправить изменения в удаленный репозиторий|
|`git push -u origin master`| использование вышеописанной команды в первый раз (-u связывает локальную ветку с одноименной удаленной, origin - имя удаленного репозитория, master - имя ветки)|

## Команды ssh

| Команда                                | Результат выполнения |
|----------------------------------------|----------------------|
|`ssh-keygen -t ed25519 -С "github_email"`| создает пару ssh - ключей в ~/.ssh (.pub - публичный, для шифрования; без .pub - приватный, для расшифровки)|
|`ssh -T git@github.com`| позволяет проверить ключи (в разделе `settings` на github заранее необходимо добавить свой публичный ключ - содержимое .pub файла в ~/.ssh)|

## Жизненный цикл файла в git

![Жизненный цикл файла](images/file_git_life_cycle.png)

# Подсказка по git

Инициализация папки как репозитория
```bash
$ cd ~/dev/first-project # перешли в нужную папку

$ git init # создали репозиторий
```
«Разгитить» папку, если что-то пошло не так, rm -rf .git
```bash
$ cd <папка с репозиторием> # перешли в папку

$ rm -rf .git # удалили подпапку .git
```
Проверить состояние репозитория — git status
```bash
$ git status
```
Подготовить файлы к сохранению — git add
```bash
$ touch todo.txt
$ touch readme.txt
# создали файлы todo.txt и readme.txt

$ git status # проверили статус

$ git add --all # подготовили к сохранению все файлы в репозитории
$ git status # проверили статус
```
или
```bash
$ git add todo.txt
$ git add readme.txt
$ git status 
```
или
```bash
$ git add . # добавить всю текущую папку
$ git status 
```
Выполнить коммит — git commit
```bash
$ git commit -m 'Мой первый коммит!'
```
Просмотреть историю коммитов — git log
```bash
$ git log
```
Проверка наличия SSH-ключа
```bash
$ cd ~ # перешли в домашнюю директорию

$ ls -la .ssh/ # вывели список созданных ключей
```

Инструкция по генерации SSH-ключа
```bash
$ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```
или
```bash
$ ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```

Привязать удалённый репозиторий к локальному — git remote add
```bash
$ cd ~/dev/first-project
$ git remote add origin git@github.com:%ИМЯ_АККАУНТА%/first-project.git
```
Убедиться, что репозитории связаны, — git remote -v
```bash
$ git remote -v
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (fetch)
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (push)
```

git push
```bash
$ git push -u origin main # Если команда приведёт к ошибке, попробуйте 
                          # заменить main на master.
```
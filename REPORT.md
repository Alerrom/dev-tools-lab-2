# Задача 1
`git instaweb` 

Или скачать расширение для VSCode, чтобы показать крысивый граф:)

# Задача 2
`git checkout ci`

`git rebase -i HEAD~2`

![Изображение 2.1](\docx\task-2-1.png)

![Изображение 2.2](\docx\task-2-2.png)

# Задача 3
`git reflog`

Ищем (ручкми) нужный коммит. Запоминаем первые 7 символов его хэша или копируем

`git checkout aca3abb`

`git branch old-master`

# Задача 4
`git blame prisma/seed.ts`

![Изображение 4](\docx\task-4-1.png)

# Задача 5
Ставим на компьютер Node js

`npm install --save-dev jest`

`git checkout master`

`git stash` (у меня откуда-то взялись изменения, которые мешали бинпоиску)

`git bisect start` (инициализаруем бинпоиск первого плохого коммита)
`git bisect bad`

`git bisect good 8673a612` (начинаем поиск)

`npm run test`

Последние 2 комманды выполняем до тех пор, пока нам не поступит сообщение о том, что поиск завершен.

![Изображение 5](\docx\task-5-1.png)

# Задача 6
`git filter-branch --tree-filter "rm -f .env" -- --all`

`echo .env >> .gitignore`

![Изображение 6.1](\docx\task-6-1.png)

![Изображение 6.2](\docx\task-6-2.png)

![Изображение 6.3](\docx\task-6-3.png)

# Задача 7
`git checkout feature`

`git filter-branch --env-filter "GIT_AUTHOR_NAME='Ershov Aleksandr Romanovich'; GIT_AUTHOR_EMAIL='alex2002andr@mail.ru'; GIT_COMMITTER_NAME='Ershov Aleksandr Romanovich'; GIT_COMMITTER_EMAIL='alex2002andr@mail.ru'" HEAD~3..HEAD`

![Изображение 7.1](\docx\task-7-1.png)

![Изображение 7.2](\docx\task-7-2.png)

# Задача 8
`git checkout master`

`git config rerere.enabled true`

`git merge feature`

Далее решаем конфликт (я это сделал через VSCode приняв новую старую версию)

`git add .`

`git commit --no-edit`

`git reset --hard HEAD~1`

`git merge feature`

Хоть при попытке `merge` мы увидим конфликт, можно заметить стручку "Resolved 'file-name' using previous resolution." Это значит, что все отработало нормально (конфликт починился без нашего внешнего вмешательства).

`git add .`

`git commit --no-edit`

![Изображение 8.1](\docx\task-8-1.png)

# Задача 9
`git fsck`

![Изображение 9.1](\docx\task-9-1.png)

# Задача 10
`git gc --prune=now --aggressive`

![Изображение 10.1](\docx\task-10-1.png)

![Изображение 10.2](\docx\task-10-2.png)

# Задача 11
`git remote add origin https://github.com/Alerrom/dev-tools-lab-2.git`

`git checkout master`

`git push -u origin master`

`git checkout feature`

`git push -u origin feature`

`git checkout old-master`

`git push -u origin old-master`

`git branch report`

`git checkoit report`

Далее создаю REPORT.md и \docx для храниения скриншотов. После чего приступаю к заполнению файлов.

Заливка по отдельным строчкам будет происходить через

`git add -p`

`e`

`git commit -m "*commit-message*"`

и так для каждого задания

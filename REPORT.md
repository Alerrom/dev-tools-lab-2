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


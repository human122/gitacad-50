## gitacad-50
Rep for training https://htmlacademy.ru/courses/50 with githab

## Об этом репозитории

Репозиторий замышлялся, чтобы тренироваться использовать систему контроля версий git и github, попутно проходя курсы htmlacademy.ru. Он состоит из коммитов, совпадающих с уроками htmlacademy.ru. Начинается все не с первого занятия первого курса, т.к. я додумался до такого использования только сейчас и git начал недавно изучать. Вы можете клонировать себе этот репозиторий и исследовать с помощью команд git или поменять поменять в нем что-то. Можно попробовать что-то улучшить в отдельных уроках или дополнить своими уроками для тренировки тех или иных навыков. Особое спасибо htmlacademy за такие замечательные уроки!

## Программы и команды

Операционная система Windows 7/8. В качестве текстового редактора использовался Sublime Text 2 и Notepad++ с отступами 2 пробела. Командная строка, git, Sublime использовались из набора OpenServer (тот, который рекомендован в интенсиве htmlacademy "Базовый PHP"). Git, как и много других полезных инструментов, встроен в OpenServer. Небольшая инструкция для начинающих:

Чтобы работать из командной строки (в данном случае Console Emulator) с git, нужно запустить "Open Server x86(64).exe", запустить сам сервер в системном трее, затем там же во вкладке "Дополнительно" запустить "Консоль", и уже там можно набрать git version и убедиться, что git работает. Команды, которые мне приходилось использовать, наполняя этот репозиторий:

cd - change directory (можно переходить сразу через несколько директорий)  
md - make directory (создать директорию, папку)  
touch <имя файла> - создать файл (в другой версии (не bash) аналогично работает команда "copy nul <имя файла>", либо сначала надо ввести "bash", чтобы запустился bash (для последней версии OpenServer))  
git help (или просто git, без help)  
git <команда> -help  
git init  
git status  
git add <имя файла>  
git add . (точка означает "добавить все файлы в репозитории")  
git commit -m "<текст комментария для коммита>"  
git commit -am "<текст комментария для коммита>" (если файлы новые создавали, то не добавятся)  
git branch  
git branch <имя ветки>  
git branch -b <имя ветки>  
git tag  
git tag <имя тэга>  
git tag -d <имя тэга>  
git checkout <тэг или hash коммита>  
git checkout -b <тэг или hash коммита>  
git diff <тэг1 или hash1> <тэг2 или hash2>  
git show  
gitk  
git log  
git log --max-count=4  
git remote -v  
git push `https://github.com/<ваше имя на гитхабе>/<имя вашего репозитория>`  
git push -u --tags origin master  
git push -u --tags origin <ветка>  
git push origin -d <тэг> (удалял тэг, который переименовал в локалке)  
git pull  
git fetch

Еще использовал алиасы как на сайте githowto. Очень удобно.

Теперь немного о настройке для Console Emulator и git, чтобы коммиты на русском отображались правильно. Помимо настроек user и email, которые запросит git в начале работы, для нормального отображения русского именно в этой консоли мне помогло добавление следующих строк в .gitconfig

```
[core]
    pager = cat|less -r
[i18n]
    commitencoding = utf-8
    logoutputencoding = utf-8
```

Что еще меня поначалу смущало в использовании СonEmu (Console Emulator), так это когда вводишь git log и он должен показать несколько страниц, он периодически останавливается и показывает двоеточие ":", нужно нажать "пробел", чтобы пролистать дальше, а когда высветится "END" нужно нажать "q" (т.е. quit).

## Обозначения для тэгов и коммитов

Комментарии к коммитам - это содержание тэга <title> из html файла. Тэги обозначают <номер курса>.<номер урока>. Таким образом вы сможете найти нужный урок на htmlacademy. Пример:

git checkout 50.7 означает, что вы переключились на коммит с тэгом 50.7, которому на htmlacademy соответствует урок https://htmlacademy.ru/courses/50/run/7

Только испытания я тэгировал как 50.9.test, т.е. добавлял еще слово "test". Все доступные тэги можно посмотреть командой git tag.

Кстати, в первый раз, когда пушил репозиторий, то тэги не отправил, оказалось, что надо прописывать в параметрах push еще и --tags.

## В процессе использовались

http://html-academy.ru/codeguide/html-css.html#css-order  
https://githowto.com/  
http://think-like-a-git.net/  
http://learngitbranching.js.org/  
https://habrahabr.ru/post/74839/  
https://habrahabr.ru/post/158639/ - сам не читал, но думаю, что в принципе кодировки не должны вызывать каких-то проблем, хоть я и сторонник писать коммиты на английском.  
http://ilfire.ru/kompyutery/shpargalka-po-sintaksisu-markdown-markdaun-so-vsemi-samymi-populyarnymi-tegami/  

## P.S.

Кстати, просто папки с версиями файлов у меня весят 72689 байт, а на диске занимают 241664 байта. Те же версии файлов в git весят 85172 байта, а на диске занимают 172032 байта, т.е. почти в полтора раза меньше. В этом, видимо, одна из фишек git, он хранит только изменения. Что означает вес (размер) файлов и разница в нем, я точно не знаю.

скриншоты:  
без git (просто папки) https://prnt.sc/ghbhzl  
с git https://prnt.sc/ghbhev

## Связанные репозитории

https://github.com/human122/gitacad-86  
https://github.com/human122/gitacad-130

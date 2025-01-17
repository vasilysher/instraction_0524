![logo](c2e07b2dfe7e27724dd3c36daed54591)

 # 1. Работа с Git hab
![leopard](leopard.jpeg)
! # Работа с Git hab
 
 ## 2. Проверка наличия установленного git
 В терминале выполнить команду 'git --version' 
Если git установлен то появится сообщение с информацией о версии программы. Инче будет сообщение об ошибке.

## 3. Установка git
загружаем последнюю версию git 

## 4. Настройка Git
'''
при первом использовании необходимо представится. Для это ввести две команды:
git config --global user.name «Ваше имя»
git config --global user.email ваша "почта@example.com"
''' piython

## 5. Начало работы с папкой репозитория

'добавляем новую папку/репозиторий где будем работать с файлами' Для этого набираем команду git init и enter.
Таким образом создали папку репозитория где будет хранится файл для работы.

## 6. Создаем файл
*создаем новый файл в папке репозитория, создается в проводнике. обязательно указать расширение файла* 
для добавления в отслеживание пишем команду git add и "название файла".

### 7. *Контроль изменений*
_добавление изменений в файле производится командой git add, затем git commit -m "название изменений"_
или можно набрать команду **git commit -am "название изменений"** - это соединение двух команд. При этом необходимо следить за правильностью написания команд, иначе выскочит в ошибку. Действия при ошибках расписаны ниже.
внимание: действия при ошибках и при не исполнении команд следующие: будет сообщение об ошибке или перенаправят в текстовую команду и в этом случае нужно:
- набираем i, затем внизу будет слово "вставка". 
- затем набираем "Esc".
- далее набираем ":wq" это команда записать и выход.
- выход в основной терминал.
не всегда сразу выходит)))

### 8. Работа с файлом
для работы с файлом применяются следующие команды:
1. **git log** - вывод всех ранее сделанных изменений commit
2. **git checkout "код коммита"**- переход от одного изменения к другому и дальнейшая работа в отдельной ветке.
3. **git checkout master** - возврат в основную ветку файла
4. **git diff** - показывает разницу между текущим и измененым файлом.
5. **git status** -  отслеживание изменений.

## 9. Работа в новых версиях файлов
1. создание **git branch** _имя_имя_ - новая ветка. Текущая ветка будет обозначена звездочкой **\*name_branch** и зеленым цветом.
2. работа в ветке с теме же командами что и ранее.
3. если необходимо объеденить с основной веткой то 
* _**git checkout master**_ выходим в основную ветку и затем
** _git merge** **(имя ветки которую хотим добавить)**_.
* смотрим что получилось и проверяем, что оствляем, а что нет. Изменения будут выделены цветом, и принимаем решения какую версию оставляем в __*чистовике*__.
4. **_git branch -d** **(имя ветки)**_- команда удаления ветки.
5. **_git branch -m_** - это команда на перименование существующей ветки.
далее нужно ввести новое имя ветки.
6. Создание ветки **git checkout -b** И имя новой ветки.
7. работа в новой ветке происходит по всем правилам, как и в основной ветке.
*Новая ветка необходима для проверки каких-либо ошибок или идей. Далее просто проводится сравнение или проверка получившися данных. Кроме этого в новой ветке возможно создание совсем нового продукта, на основе существующего.* 

## 10. Дополнительные команды
```
При работе в терминале часто бывает, что данных в терминале становится очень много и тогда делается команда **clear**.
Происходит очистка данных в терминале.
При наборе команд в терминале можно пользоватся стрелками "вверх" и "вниз" - происходит выбор и переключение между ранее набранными командами.
Т.к. файл с которым работают естественно есть много изменений и соответственно при вызове команды **git log** показывающей ранее сделаные изменения, в терминале могут быть "зависания" и не полный показ данных - в этом случае нажимаем __q__ и происходит возврат для набора команд.
**git commit -amend -am "наименование"** - команда позволяет исправлять ошибки в наименовании последнего коммита.
```

 ## 11. Визуализация данных.
 Команда __git log --graph__ - графически показывает как и какие "ветки" были сделаны, в виде полос сбоку терминала.
 Выход __q__. *Уточнение что при работе надо смотреть за регистром букв, а так же за дополнительными знаками препинания* 

 
## 12. Добавление файлов/рисунков.
При добавлении картинок и рисунков сначала находим нужный файл и добавляем в наш репозиторий.
Затем в тексте выбираем место куда нам необходимо вставить картинку и пишем следующий текст - ![текст описания](*вставляем отностительный путь из свойств картинки*). В результате картинка отображается. 

## 13. Добавление в игнорирование.
Т.к. картинки обчно не отсеживаются то нужно добавить их в игнорирование. 
Для что бы добавить какой-либой файл в игнорирование необходимо в репозитории проводника создать файл **.gitignore** командой **git add .gitignore** добавить в репозиторий и добавив в него ненужные нам файлы принято изменения ***__git commit -m__***.
Добавлять можно как само файлы через их наименование, так и блоки через расширения - "*.jpeg"  

## 14. Работа с документами.
Данная инструкция неполная и будет добавлятся далее.
Так же через сайт __github.com__ можно организовать работу распределнной команды по работе над каким-либо проектом.
На указанном выше сайте создается в ранее созданом аккаунте папка репозитория который возможно скачивать себе на локальное устройство и работать над своей частью. Затем заливать на общий ресурс и проводить слияние. 
Небольшой нюанс, при работе с ***github.com***, если на собственном устройстве установлено несколько браузеров, то вся загрузка/выгрузка файлов производится только через браузер который является основным.
Дополнения по командам для работы с **github.com** три основные команды:
***git pull*** - для загрузки данных с **github.com**, если проект есть на собственном устройстве, то сливает загружаемый проект с существующим.
***git push*** - для загрузки с локального устройства на удаленный репозиторий.
***git clone*** - загружает все с удаленного репозитория на локальное устройство, со слиянием всех веток - 
команда для удаления привязки к удаленному репозиторию - git remote remove origin.
при отправке данных с локальной машины необходимо выполнить следующие команды: **git remote add origin https://github.com/...**
и привязываем ветку к новому репозиторию __git push --set-upstream origin main__
Для обмена внутри **git hub** с известным участников используется команда **pull request** 

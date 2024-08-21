# Курс по Git
---
## _Все базовые команды для работы с Git_  
**pwd** – выводит путь к текущей директории  
**cd** – сменить директорию («~» - обозначение домашней директории)  
**ls** – отобразить содержимое директории   
**ls -a** отобразить скрытое содержимое дериктории  
**touch** – создать файл  
**mkdir** – создания директорий через терминал  
**cp** – копирование фалов из одного места в другое  
**mv** – перемещение файлов  
**cat** – прочитать содержимое текстового файла (txt)  
**rm** – удалить файл   
**rmdir** – удалить папку  
**rm -rf** - рекурсивно удаляет файлы и папки и избавляет от вопросов уточнения удаления  
**git version** – узнать версию Git  
**git config** -- global  
**git config** – list  
**git init** – создание Git-репозитория  
**git status** – текущее состояние репозитория  
**git add –all** подготавливать файлы к сохранению в репозитории (ключ –all означает, что все фалы будут сохранены)  
**git commit --m** – сделать коммит с выводом сообщения  
**git log** – посмотреть список коммитов  
**git log --oneline** – получить сокращенный лог 
**ssh-keygen -t ed25519 -C** "электронная почта, к которой привязан ваш аккаунт на GitHub" – генерация SSH пары  
**ssh-keygen -t rsa -b 4096 -C** "электронная почта, к которой привязан ваш аккаунт на GitHub" - генерация SSH пары (другой алгоритм)  
**git remote add** – привязать удаленный репозиторий к локальному  
**git remote -v** – проверка привязки удаленного репозитория к локальному  
**git push** – загрузить содержимое локального репозитория на удаленный  
## Вся необходимая информация [тут](https://practicum.yandex.ru/trainer/git-basics/lesson/cc37a4db-7f30-4210-94d2-f3044efecc41/)
---
## _Навигация по коммитам_
**Информация о коммите** — это набор данных: когда был сделан коммит, содержимое файлов в репозитории на момент коммита и ссылка на предыдущий, или родительский (англ. parent), коммит.  
Git хеширует (преобразует) информацию о коммите с помощью алгоритма _SHA-1_ (от англ. Secure Hash Algorithm — «безопасный алгоритм хеширования») и получает для каждого коммита свой уникальный хеш — результат хеширования. 
**Хеш** — основной идентификатор коммита и позволяет узнать его автора, дату и содержимое закоммиченных файлов.  
Файл _HEAD_ (англ. «голова», «головной») — один из служебных файлов папки .git. Он указывает на коммит, который сделан последним (то есть на самый новый).  
Внутри _HEAD_ — ссылка на служебный файл: refs/heads/master (или refs/heads/main в зависимости от названия ветки). Если заглянуть в этот файл, можно увидеть хеш последнего коммита.  
При работе с Git указатель HEAD используется довольно часто. Многие команды Git принимают в качестве параметра хеш коммита. Если нужно передать последний коммит, то вместо его хеша можно написать слово **HEAD** — Git поймёт, что вы имели в виду последний коммит. 
--- 
## _Статусы файлов в Git_
_untracked_ - статус файла, о существовании которого Git знает, но не следит за изменениями в нём.  
_tracked- — это противоположность _untracked_. Оно довольно широкое по смыслу: в него попадают файлы, которые уже были зафиксированы с помощью _git commit_, а также файлы, которые были добавлены в **staging area** командой _git add_. То есть все файлы, в которых Git так или иначе отслеживает изменения.
_modified_ - означает, что Git сравнил содержимое файла с последней сохранённой версией и нашёл отличия.  






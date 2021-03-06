- Перед любыми операциями с репозиториями у каждого пользователя должно быть настроено имя и адрес почты:
```bash
git config --global user.name "Firstname Lastnameov"
git config --global user.email f.lastnameov@analysiscenter.ru
```
Причем email **должен совпадать** с email'ом, который указан в вашем github-аккаунте (в нем может быть несколько email'ов). 

- В корневом каталоге каждого репозитория должен быть размещен файл README.md с кратким описанием проекта, структуры исходного кода, инструкцией по установке и ссылками на документацию.

- Все содержательные файлы рекомендуется размещать в подкаталогах, а в корневом хранить только описательные (README.md, INSTALL.md и т.п.), 
инсталляционные (setup.py, requirements.txt и т.п.), а также конфигурационные и make-файлы.

- Имена файлов должны содержать только латинские буквы. Пробелы в наименованиях файлов не допускаются.

- Коммиты в ветку `master` не допускаются. Она должна быть защищена от удаления и изменения истории 
(Settings - Branches - Protected branches).

- Изменения в исходном коде и файлах репозитория рекомендуется производить только в рамках задач (issues). 
Для каждого изменения исполнитель открывает отдельную ветку с наименованием вида <iTASK-ID>-<short branch name> (например, `i15-dataset` или `i22-HMM`).

- В рамках одной задачи можно создавать несколько веток в одном репозитории.

- Если у вас нет задачи, имеет смысл ее открыть и явным образом завести в issues.

- Коммиты в рабочие ветки рекомендуется делать регулярно, чтобы каждый коммит содержал не слишком объемные, 
но вместе с тем завершенные и независимые от всего остального изменения в репозитории 
(лучше закоммитить 3 измененных строки, чем сразу 300).

- Коммит должен содержать однострочный англоязычный комментарий (длиной 20-60 символов), 
отражающий содержание включенных в него изменений исходного кода и файлов.

- Более подробное описание изменений следует сохранять в файле HISTORY.md, размещенном в корневом каталоге репозитория.

- Выполнив задачу и завершив все изменения, исполнитель открывает pull request на слияние рабочей и продуктивной ветки (например, master).

- Перед слиянием рабочая ветка не должна отставать от продуктивной (что можно проверить с помощью `git status`). Для этого следует предварительно синхронизировать рабочую ветку (`git pull`).

- После слияния рабочая ветка удаляется.

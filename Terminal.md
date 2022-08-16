# Homework #1 
## Terminal 
1. Посмотреть где я			`pwd`
3. Создать папку			`mkdir foldername`
4. Зайти в папку			`cd foldername`
5. Создать 3 папки			`mkdir foldername1 foldername2 foldername3`
6. Зайти в любую папку			`cd foldername1`
7. Создать 5 файлов `(3 txt, 2 json)	touch 1_text_file.txt 2_text_file.txt 3_text_file.txt 1_json_file.json 2_json_file.json`
8. Создать 3 папки			`mkdir foldername1 foldername2 foldername3`
9. Вывести список содержимого папки	`ls -la`
10. Открыть любой txt файл		`vim 1_text_file.txt`
11. написать туда что-нибудь.		`[I] Insert text`
12. сохранить и выйти.		`[ESC] :wq`
13. Выйти из папки на уровень выше	`cd ..`
14. переместить любые 2 файла, которые вы создали, в любую другую папку.	`mv -t foldername1 1_json_file.json 1_text_file.txt`
15. скопировать любые 2 файла, которые вы создали, в любую другую папку.	`cp -t foldername2 2_json_file.json 2_text_file.txt`
16. Найти файл по имени								`find -L /c/Courses/Group_22/ -name "3_text_file.txt"`
17. просмотреть содержимое в реальном времени (команда grep)
```sh
grep -i insert foldername1/1_text_file.txt
```
```sh
tail -f foldername1/1_text_file.txt
```
18. вывести несколько первых строк из текстового файла				`head foldername1/1_text_file.txt`
19. вывести несколько последних строк из текстового файла			`tail foldername1/1_text_file.txt`
20. просмотреть содержимое длинного файла (команда less)			`less -F -E /c/Windows/setupact.log`
21. вывести дату и время
```sh
dt=$(date '+%d/%m/%Y %H:%M:%S')
echo "$dt"
```
***
* Отправить http запрос на сервер.
```sh
curl "http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000"
```
***
* Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

[Скрипт](https://github.com/Olgerd1323/QA_Courses_Group22/blob/Terminal/myscript.txt)

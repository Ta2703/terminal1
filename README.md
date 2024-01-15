Первое ДЗ 
Linux terminal (GitBash) commands

1) Посмотреть где я - pwd
2) Создать папку - mkdir QA
3) Зайти в папку - cd QA
4) Создать 3 папки - mkdir d1 d2 d3
5) Зайти в любоую папку - cd d1
6) Создать 5 файлов (3 txt, 2 json) - touch cats.txt cows.txt dogs.txt raccoon.json snake.json
7) Создать 3 папки - mkdir animals1 animals2 animals3 
8) Вывести список содержимого папки - ls -la
9) Открыть любой txt файл - cat > cats.txt
10) написать туда что-нибудь, любой текст. - 1.Yasha 2.Tosha 3.Tishka 
11) сохранить и выйти. -^C 
12) Выйти из папки на уровень выше - cd ..
—
13) переместить любые 2 файла, которые вы создали, в любую другую папку.  - mv d1/cats.txt d1/raccoon.json d2
14) скопировать любые 2 файла, которые вы создали, в любую другую папку. - cp d1/dogs.txt d1/snake.json d3
15) Найти файл по имени - find . -name cows.txt
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает. - tail -f d2/cats.txt | grep -i "Yasha" d2/cats.txt
17) вывести несколько первых строк из текстового файла - head -2 d2/cats.txt
18) вывести несколько последних строк из текстового файла - tail -2 d2/cats.txt
19) просмотреть содержимое длинного файла (команда less) изучите как она работает. - less d2/cats.txt (чтобы выйти  q)
20) вывести дату и время - date

    
=========

Задание *
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request - curl 'http://162.55.220.72:5006/terminal-hw-request’

 Вывод: 

``
{
  "Intro": "Hello!! This is your the first response from server", 
  "Tasks": {
    "Task_1": "Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)", 
    "result": [
      "Your_String", 
      "Your_number"
    ]
  }
}
`` 
curl 'http://162.55.220.72:5005/get_method?name=(Tamara)&age=(28)' 

Вывод: 

``
"(Tamara)", 
  "(28)"
``
   

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13



touch script.sh
vim script.sh

<code>
#!/bin/bash
mkdir d1 d2 d3
cd d1
touch cats.txt cows.txt dogs.txt raccoon.json snake.json
mkdir animals1 animals2 animals3 
 ls -la            
mv d1/cats.txt d1/raccoon.json d2   
</code>
Запустить - bash script.sh



Termial. HW_2
1. Сделать папку dir_1 - mkdir dir_1
2. Зайти в папку dir_1 -  cd dir_1
3. Создать папку inner_dir_1 - mkdir inner_dir_1
4. Посмотреть где ты находишься - pwd
5. Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt - touch tf_1.txt
6. Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками:
- the first 1
- the second 2
- the third 3
cat >> tf_2.txt -> Ctrl+C

7.Зайти в папку inner_dir_1 - cd inner_dir_1

8.Через cat сделать текстовый файл tf_3.txt c любыми строками cat>>tf_3.txt  -> Ctrl+C

 
 9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2” - cat >> tf_3.txt -> the second 2 -> Ctrl+C
 10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2” - cat >> tf_3.txt -> the sec 2 -> Ctrl+C
 11. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3” - cat >> tf_2.txt -> the sec 3 -> Ctrl+C
 12. Через cat добавить в текстовый файл tf_3.txt строку “the SeCoNd 2” - 	cat >> tf_3.txt -> the SeCoNd 2 ->Ctrl+C
 13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2” - cat >> tf_2.txt -> the seConD 2 -> Ctrl+C
 14. Сделать текстовый файл tf_4.txt в котором будет 15 строк. - Touch tf_4.txt -> vim tf_4.txt -> I -> esc -> :wq
 15. Сделать текстовый файл tF_5.txt в котором будет 13 строк. - Touch tF_5.txt -> vim tF_5.txt -> I -> esc -> :wq
 16. Вывести список всех файлов в папке. - ls -la
 17. Выйти из папки inner_dir_1 - cd ..
 18. Вывести содержимое файла tf_3.txt в терминал. - cat inner_dir_1/tf_3.txt
 19. Найти путь к файлу tf_4.txt -realpath $(find . -name tf_4.txt)
 20. Отчистить файл tf_4.txt от содержимого без удаления самого файла. - >inner_dir_1/tf_4.txt
 21. Найти путь к файлам у которых есть  “tf” в названии.  - realpath $(find . -name '*tf*')  
 22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре. - realpath $(find . -iname '*tf*') 
 23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке - grep sec *
 24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке - grep -i sec *
 25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке - grep -w sec *
 26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке - grep -w -i sec *
 27. Найти строки в файлах где есть комбинация букв “second” в текущей папке - grep second *
 28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке - grep -i second *
 29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем - grep -r second *
 30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке - grep -l second *
 31. Найти все строки во всех файлах где нет комбинации “second” - grep -r -v second *
 32. Найти только название и путь к файлам где нет комбинации “second” - grep -r -L second *
 33. Вывести в терминал 4 последних строк любого текстового файла - tail -n4 inner_dir_1/tf_3.txt
 34. Вывести в терминал 4 первые строки любого текстового файла. -  head -n4 tf_3.txt
 35. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым.  - mkdir inner_dir_2 | echo "some text" > tf_6.txt
 36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec” - grep -rl sec | xargs mv -t
 37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec” - grep -rl sec | xargs cp -t
 38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл. - grep -rh sec >> out.txt
 39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec” - grep -rl sec | xargs rm -rf
 40. Просто вывести в терминал строку “Good job!!” - echo 'Good job!!'


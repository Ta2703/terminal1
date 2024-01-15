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

## 🖥️ bash and git

During the functional software testing course, I learned basic bash and git skills. I completed the tasks listed below.

## Task 1 (bash)
```git
Открыть домашнюю директорию
pwd                                                         # Определить имя папки, в которой вы находитесь
mkdir test1                                                 # Создать внутри этой папки каталог  с именем test1
cd test1                                                    # Перейти в папку test1
touch file1.txt file2.txt file3.txt                         # Создать файл 1,2 и 3 внутри каталога test1
ls                                                          # Проверить содержимое каталога test1
cd ..                                                       # Перейти в домашнюю директорию
mkdir test2                                                 # Создать папку test2 внутри домашней директории
rmdir test2                                                 # Удалить папку test2
rm test1/file2.txt                                          # Удалить файл 2 из папки test1
mkdir test3                                                 # Создать папку в домашней директории test3 и 12 добавить в нее два файла
touch test3/file4.txt test3/file5.txt
rm -r test3                                                 # Удалить папку test3
mkdir test4                                                 # Создать папку test4 в домашней директории
mv test1/file1.txt test1/file3.txt test4                    # Переместить файлы 1 и 3 из папки test1 в папку test4
echo -e "line1\nline2\nline3" >> test4/file1.txt            # Добавить в файл 1 три строки со словами line
cat test4/file1.txt                                         # Посмотреть содержимое файла 1
echo -e "line4\nline5\nline6" >> test4/file3.txt            # Добавьте в файл 3 три строки со словами line
cat test4/file1.txt test4/file3.txt                         # Просмотрите содержимое двух файлов (1 и 3) сразу
nano test4/file1.txt                                        # Используя один из редакторов замените все строки в файле 1
*editing file1.txt*
cat test4/file1.txt
```

## Task 2 (bash)
```git
Зайти в домашнюю директорию
mkdir test3                                                 # Создать папку test 3
Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4
echo -e "row1\nrow2\nrow3\nrow4" >> test3/file4.txt
echo -e "row1\nrow2\nrow3\nrow4" >> test3/file5.txt
echo -e "row1\nrow2\nrow3\nrow4" >> test3/file6.txt
grep -i "row2" test3/file5.txt                              # Найдите строку row2 в файле 5
grep -Ri "row" test3                                        # Найдите строку row в папке test3
grep -c "row" test3/file6.txt                               # Посчитайте сколько строк с содержимым row в файле 6
find test3 -name "file5*"                                   # Найдите файл 5 внутри папки test3
find test3 -name "file5*" -delete                           # Используя команду find, удалите файл 5
echo "test" >> test3/file4.txt                              # Используя команду echo, добавьте слово test в файл 4
sed "s/test/fail/g" test3/file4.txt -i                      # Замените слово test в файле 4 на fail
echo test >> test3/file4.txt                                # Добавьте в файл 4 слово test так, чтобы сохранилось содержимое
ps aux                                                      # Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе
kill 666                                                    # Убейте процесс 666 в консоли
ping artsiomrusau.com                                       # Узнайте доступность ресурса artsiomrusau.com, используя ping
ping -c 5 artsiomrusau.com                                  # Отправьте 5 пакетов на сайт artsiomrusau.com
curl https://petstore.swagger.io/v2/pet/findByStatus?status=available
                                                            # Используя GET и команду curl, получите информацию о зарегистрированных питомцах на https://petstore.swagger.io/
curl -X POST https://petstore.swagger.io/v2/user -H 'Content-Type: application/json' --data '{"id": 1337, "username": "bruh", "firstName": "John", "lastName": "Isner", "email": "john@testmail.com", "password": "password", "phone": "79999999999", "userStatus": 1}'
                                                            # Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/
```

## Task 1 (git)
```git
Создать свой репозиторий в таким же именем, как и имя пользователя
git clone https://github.com/AndZhelBack/AndZhelBack        # Склонировать его на свой компьютер в отдельную папку
cd ..
git clone https://github.com/testrusau/testrusau            # Склонировать себе следующий репозиторий в отдельную папку https://github.com/testrusau/testrusau
Скопировать данные из склонированного репозитория и вставить их в ваш репозиторий из шага 2
Открыть файл README.md и поочередно заменить каждый блок на вашу информацию .
*editing of README.md via VS Code*
git add .
git commit -m "upd README"
git push
```

## Task 2 (git)
```git
Поочередно создайте репозитории для каждого выполненного задания по прошедшим модулям и загрузите туда ваши решения ДЗ.
Создать два локальных репозитория на компьютере + объявить их удаленно

git init api_testing
cd api_testing
git remote add origin https://github.com/AndZhelBack/api_testing.git
touch README.md
git add .
git commit -m "add README"
git push --set-upstream origin master

cd ..
git init web_testing
cd web_testing
git remote add origin https://github.com/AndZhelBack/web_testing.git
touch README.md
git add .
git commit -m "add README"
git push --set-upstream origin master
```

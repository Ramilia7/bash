# Команды Bash (MacOS)
## Работа с файлами и каталогами
<table border="1">
  
  </tr>
  <tr>
    <td>cd ~ /  cd $HOME</td>
    <td>открыть домашнюю директорию через терминал</td>
  </tr>
  <tr>
    <td>pwd</td>
    <td>определить имя папки, в которой вы находитесь</td>
  </tr>
  <tr>
    <td>mkdir test1 && ls</td>
    <td>создать внутри этой папки каталог с именем test1</td>
  </tr>
  <tr>
    <td>cd test1</td>
    <td>перейти в папку test1</td>
  </tr>
  <tr>
    <td>touch 1.txt 2.txt 3.txt</td>
    <td>cоздать файл 1,2 и 3 внутри каталога test1</td>
  </tr>
  <tr>
    <td>ls</td>
    <td>проверить содержимое каталога test1</td>
  </tr>
  <tr>
    <td>cd</td>
    <td>перейти в домашнюю директорию</td>
  </tr>
  <tr>
    <td>mkdir test2 && ls</td>
    <td>создать папку test2 внутри домашней директории</td>
  </tr>
  <tr>
    <td>rmdir test2 && ls</td>
    <td>удалить папку test2</td>
  </tr>
  <tr>
    <td>rm ~/test1/2.txt && cd test1 && ls</td>
    <td>удалить файл 2 из папки test1</td>
  </tr>
  <tr>
    <td>cd && mkdir test3 && touch test3/1.txt test3/2.txt && cd test3</td>
    <td>создать папку в домашней директории test3 и добавить в нее два файла</td>
  </tr>
  <tr>
    <td>cd && rm -r test3 && cd && ls</td>
    <td>удалить папку test3</td>
  </tr>
  <tr>
    <td>mkdir test4</td>
    <td>создать папку test4 в домашней директории</td>
  </tr>
  <tr>
    <td>cd && mv ~/test1/1.txt ~/test1/3.txt ~/test4/ && cd test4 && ls</td>
    <td>переместить файлы 1 и 3 из папки test1 в папку test4
</td>
  </tr>
  <tr>
    <td>echo -e "line\nline\nline" >> 1.txt</td>
    <td>добавить в файл 1 три строки со словами line</td>
  </tr>
  <tr>
    <td>cat 1.txt</td>
    <td>посмотреть содержимое файла 1</td>
  </tr>
  <tr>
    <td>echo -e "line\nline\nline" >> 3.txt</td>
    <td>добавьте в файл 3 три строки со словами line</td>
  </tr>
  <tr>
    <td>cat 1.txt 3.txt</td>
    <td>просмотрите содержимое двух файлов (1 и 3) сразу</td>
  </tr>
  <tr>
    <td>nano 1.txt замена вручную (Ctrl + X, затем Y, Enter для сохранения)</td>
    <td>используя один из редакторов замените все строки в файле 1</td>
  </tr>
</table>


## Редактирование файлов, мониторинг и завершение процессов, проверка доступности сайтов с помощью команды ping
<table border="1">
  
  </tr>
  <tr>
    <td>cd ~ /  cd $HOME</td>
    <td>зайти в домашнюю директорию через терминал </td>
  </tr>
   <tr>
    <td>mkdir test_3 && ls </td>
    <td>cоздать папку test 3</td>
  </tr>
   <tr>
    <td>echo -e "row1\nrow2\nrow3\nrow4" > ~/test_3/4.txt
<br>echo -e "row1\nrow2\nrow3\nrow4" > ~/test_3/5.txt
<br>echo -e "row1\nrow2\nrow3\nrow4" > ~/test_3/6.txt</td>
    <td>добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4 </td>
  </tr>
   <tr>
    <td>grep -n "row2" ~/test_3/5.txt </td>
    <td>найдите строку row2 в файле 5 </td>
  </tr>
   <tr>
    <td>grep -n "row" ~/test_3/* </td>
    <td>найдите строку row в папке test3 </td>
  </tr>
   <tr>
    <td>grep -c "row" ~/test_3/6.txt </td>
    <td>посчитайте сколько строк с содержимым row в файле 6</td>
  </tr>
   <tr>
    <td>find ~/test_3 -type f -name "5.txt" </td>
    <td>найдите файл 5 внутри папки test3 </td>
  </tr>
   <tr>
    <td>find ~/test_3 -type f -name "5.txt" -delete </td>
    <td>используя команду find, удалите файл 5 </td>
  </tr>
   <tr>
    <td>echo "test" > ~/test_3/4.txt </td>
    <td>используя команду echo, добавьте слово test в файл 4 (без сохранения содержимого)</td>
  </tr>
   <tr>
    <td>sed -i '' 's/test/fail/g' ~/test_3/4.txt </td>
    <td>замените слово test в файле 4 на fail</td>
  </tr>
   <tr>
    <td>echo "test" >> ~/test_3/4.txt </td>
    <td>добавьте в файл 4 слово test так, чтобы сохранилось содержимое</td>
  </tr>
   <tr>
    <td>ps aux </td>
    <td>просмотрите все процессы для юзеров не только в консоли, которые происходят в системе</td>
  </tr>
   <tr>
    <td>kill 666x </td>
    <td>убейте процесс 666 в консоли </td>
  </tr>
   <tr>
    <td>ping rusau.net (остановить выполнение ping Ctrl + C) </td>
    <td>узнайте доступность ресурса rusau.net, используя ping </td>
  </tr>
   <tr>
    <td>ping -c 5 rusau.net </td>
    <td>отправьте 5 пакетов на сайт rusau.net </td>
  </tr>
   <tr>
    <td>curl -X GET <br>"https://petstore.swagger.io/v2/pet/findByStatus?status=available,pending,sold" <br>-H "accept: application/json"</td>
    <td>Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/</td>
  </tr>
   <tr>
    <td>curl -X POST <br>"https://petstore.swagger.io/v2/user" \
-H "Content-Type: application/json" \
-d <br>'{
  <br>"id": 12345,
  <br>"username": "new_user",
  <br>"firstName": "John",
  <br>"lastName": "Doe",
  <br>"email": "johndoe@example.com",
 <br> "password": "securepassword",
  <br>"phone": "+1234567890",
  <br>"userStatus": 1
<br>}'</td>
    <td>Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/</td>
  </tr>
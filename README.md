# Домашние работы по обработке исключений (реализация на языке Python) площадка GeekBrains

<summary>Цели на репозиторий:</summary>
<p>

✔️ Выполнить домашнюю работу 1 семинара
  
✔️ Выполнить домашнюю работу 2 семинара

✔️ Выполнить домашнюю работу 3 семинара

</p>

<br>
<br>
↓ Домашние работы по семинарам с заданиями:

<details><summary><h4>Семинар 1. Обработка ошибок в программировании.</h4></summary>

✔️ Реализуйте 3 метода, чтобы в каждом из них получить разные исключения
Посмотрите на код, и подумайте сколько разных типов исключений вы тут сможете получить?

</details>
<details><summary><h4>Семинар 2. Исключения и их обработка.</h4></summary>

✔️ Реализуйте метод, который запрашивает у пользователя ввод дробного числа (типа float), и возвращает введенное значение. 
Ввод текста вместо числа не должно приводить к падению приложения, вместо этого, необходимо повторно запросить у пользователя ввод данных.

✔️ Если необходимо, исправьте данный код (задание 2 https://docs.google.com/document/d/17EaA1lDxzD5YigQ5OAal60fOFKVoCbEJqooB9XfhT7w/edit)

✔️ Дан следующий код, исправьте его там, где требуется (задание 3 https://docs.google.com/document/d/17EaA1lDxzD5YigQ5OAal60fOFKVoCbEJqooB9XfhT7w/edit)

✔️ Разработайте программу, которая выбросит Exception, когда пользователь вводит пустую строку. Пользователю должно показаться сообщение, что пустые строки вводить нельзя!!!

</details>
<details><summary><h4>Семинар 3. Продвинутая работа с исключениями.</h4></summary>

✔️ Напишите приложение, которое будет запрашивать у пользователя следующие данные в произвольном порядке, разделенные пробелом:
Фамилия Имя Отчество датарождения номертелефона пол

Форматы данных:

• фамилия, имя, отчество - строки

• датарождения - строка формата dd.mm.yyyy

• номертелефона - целое беззнаковое число без форматирования

• пол - символ латиницей f или m.

✔️ Приложение должно проверить введенные данные по количеству. Если количество не совпадает с требуемым, вернуть код ошибки, обработать его и показать пользователю сообщение, что он ввел меньше и больше данных, чем требуется.
<details><summary><h5>Подробности реализации</h5></summary>
Комментарий разработчика: данные полученные от пользователя, преобразуются в список, путем сплита входящих данных по разделителю "пробел", далее список проверяется на длину и если кол-во значений в нем, меньше 6, пользователь получит ошибку indexError, описанную в классе Error: 'IndexError: Получено некорректное кол-во данных!'. Проверка проходит внутри цикла WHILE, что позволит не закрыться программе в случае, получения ошибки, а предложит пользователю ввести данные снова.
</details>

✔️ Приложение должно попытаться распарсить полученные значения и выделить из них требуемые параметры. Если форматы данных не совпадают, нужно бросить исключение, соответствующее типу проблемы. Можно использовать встроенные типы java и создать свои. Исключение должно быть корректно обработано, пользователю выведено сообщение с информацией, что именно неверно.
<details><summary><h5>Подробности реализации</h5></summary>
Комментарий разработчика: данные парсим в самом начале, упаковываем их в список, далее проверяем каждый из параментов по заданному условию. Если какое либо из условий не совпадает с заявленным в ТЗ, выдаем пользователю ошибку и просим ввести данные снова. Исключения обрабатывает класс Error, включающий в себя, 6 видов ошибок: strError, indexError, dateError, numberError, genderError, writeReadError. Все ошибки содержат подсказки, о том, какого типа или формата должны быть данные, чтобы их можно было поправить.
</details>

✔️ Если всё введено и обработано верно, должен создаться файл с названием, равным фамилии, в него в одну строку должны записаться полученные данные, вида

<Фамилия><Имя><Отчество><датарождения> <номертелефона><пол>
<details><summary><h5>Подробности реализации</h5></summary>
Комментарий разработчика: если данные полученные от пользователя прошли все круги ада... то есть все этапы проверки, данные пишем в .txt файл, названием которому берем первый элемент полученных данных от пользователя, т.е. фамилию.
</details>


✔️ Однофамильцы должны записаться в один и тот же файл, в отдельные строки.
<details><summary><h5>Подробности реализации</h5></summary>
Комментарий разработчика: идентичные по названию файлы не перезаписываются, а данные в них не затираются, данные передаются в файл вместе с управляющим символом "\n", отвечающим за перенос строки, на новую.
</details>

✔️ Не забудьте закрыть соединение с файлом.

✔️ При возникновении проблемы с чтением-записью в файл, исключение должно быть корректно обработано, пользователь должен увидеть стектрейс ошибки.
<details><summary><h5>Подробности реализации</h5></summary>
Комментарий разработчика: для этой задачи, процесс записи обернут в try, except конструкцию, в случае непредвиденной ошибки, пользователь получит ошибку writeReadError: 'FileError: Непредвиденные проблемы с чтением-записью в файл. Обратитесь в тех. поддержку, по номеру: 88005553535, ведь лучше позвонить, чем у кого-то занимать!'
</details>

</details>


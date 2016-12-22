#ESM - Система распределения вычислительных заданий в Web. Руководство пользователя

##1. О программе
Программа предназначена для решения задач с применением вычислительной мощности машин клиентов, подключенных к сети

Авторы: студенты группы ЕТ-223 ЮУрГУ Челябинск
- Бобыкин Даниил [(hitroub)](https://github.com/hitroub)
- Гриценко Павел [(PaulSergeevich)](https://github.com/PaulSergeevich)
- Даутов Рустам [(FLPower793)](https://github.com/FLPower793)
- Каныбеков Ансар [(slooooowpanda)](https://github.com/slooooowpanda)
- Порватов Петр [(Bdish)](https://github.com/Bdish)

##2. Регистрация пользователей
1. На странице входа перейдите по ссылке "зарегистрироваться". Вы увидите страницу регистрации; 
2. Введите имя нового пользователя и пароль;
3. Нажмите кнопку "Create".

В случае, если вы попытаетесь зарегистрировать пользователя с одним и тем же именем дважды, вы увидите уведомление о том, что такой пользователь уже существует.


##3. Авторизация
На странице входа выполните следующие действия:

1. Введите имя пользователя и пароль;
2. Нажмите кнопку "Отправить".

В случае успешной авторизации вы перейдёте на главную страницу


##4. Главная страница
На главной странице расположены следующие ссылки:

1. Информация о приложении;
2. Контактная информация;
3. Главная страница;
4. Выход из учетной записи;
5. Отправка данных для решения задачи;
6. Отправка функции;
7. Просмотр результатов решения задач текущего пользователя;
8. Просмотр статуса решения задач.


##5. Отправка данных для решения задачи
Отправка данных для решения одной из задач, доступных на сервере производится следующим образом:

1. Выберите файл с расширением *.txt, содержащий данные задачи;
2. Выберите соответствующую задачу из списка;
3. Нажмите кнопку "Загрузить".

Для решения задачи экспоненциального сглаживания (ExpMov) содержимое файла для отправки может быть таким:
```
2
12
11
alpha 0.2
```
(Здесь 2 - количество данных; 12, 11 - собственно данные; alpha 0.2 - значение коэффициента alpha)

В случае успеха вы увидите сообщение о том, что файл загружен. Далее будет производится вычисление, по окончании которого вы увидите информационное окно. Для продолжения нажмите "ОК". Результат вычисления можно посмотреть на странице результатов.

##6. Страница результатов
Здесь отображается номер решенной задачи и соответствующий результат.
Статус решения задач можно посмотреть на странице статуса

##7. Отправка функций
Для отправки функции на сервер, необходимо создать файл "<Имя функции>.js" с исходным кодом функции javascript. Входные данные функции - массив данных для обработки и список параметров. Выходные данные - строка с ответом. 

##8. Системные требования
Для работы с приложением в качестве клиента необходим компьютер с веб-браузером, который поддерживает javascript
Для сервера?

##9. Надежность
Было проведено тестирование программного кода, в частности, были покрыты все модели, кроме метода Scheduler.signal(). Покрыты методы контроллера - Calculation, checkUser, Results, Status, resetTask, transferOut. Покрытие кода тестами составляет 38%. 

##10. Установка/удаление
###Установка
Для того чтобы установить данную программу на свой компьютер необходимо запустить файл “ComProj.exe”. Далее необходимо указать путь куда следует установить программу и нажать кнопку “Extract”. Необходимо дождаться окончания установки программы.

Перед запуском приложения необходимо проверить его работоспособность. Для этого следует запустить приложение и пройти по следующему адресу: [http://localhost:10802/Test/test](http://localhost:10802/Test/test). Появится информация о прохождении приложения определенных тестов. Если какой-либо тест не пройден, необходимо связаться с разработчиками для устранения данной проблемы.

###Удаление программы
Для того, чтобы удалить программу необходимо удалить папку ComProj.

##11. Масштабируемость
Текущая реализация подразумевает поддержку одного сервера. При необходимости, можно либо разместить на нескольких серверах по экземпляру приложения, либо модифицировать исходный код данного программного обеспечения для поддержки нескольких серверов.  

##12. Ограничения

##13. Поддержка браузеров

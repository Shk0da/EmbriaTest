**Задача 1**

Вам поступила задача:
Необходимо создать общую ленту новостей для пользователей с возможностью
оценки постов в ленте.
Лента должна иметь фильтр по категориям. Любой пользователь может
поставить &quot;лайк&quot; или отменить его. Необходимо предусмотреть возможность
просмотра списка всех оценивших пост пользователей. Ограничение на размер
хранения контента одного поста - 243 байта.
Предложите структуру базы данных MySQL, позволяющую реализовать данную
задачу. Напишите запросы для выборки и обновления контента. Обоснуйте выбор
индексов.

**Задача 2**

Имеется таблица пользователей:
```
 CREATE TABLE `users` (
    `id` int(11) NOT NULL AUTO_INCREMENT,
    `name` varchar(32) NOT NULL,
    `gender` tinyint(2) NOT NULL,
    `email` varchar(1024) NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB;
```


В таблице более 100 млн записей, и она находится под нагрузкой в production (идут
запросы на добавление / изменение / удаление).
В поле email может быть от одного до нескольких перечисленных через запятую
адресов. Может быть пусто.
Напишите скрипт, который выведет список представленных в таблице почтовых
доменов с количеством пользователей по каждому домену.

**Задача 3**

Дан текстовый файл размером 2ГБ. Напишите класс, реализующий
интерфейс SeekableIterator, для чтения данного файла.
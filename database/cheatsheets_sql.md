#### Создание базы данных

- Простое создание базы данных
```
CREATE DATABASE test;
```

- Создание базы данных с указанием кодировки по-умолчанию
```  
CREATE DATABASE test DEFAULT CHARACTER SET utf8;
```

- Создать базу данных, если таковая не существует. Если существует - не пытаться создавать
```   
CREATE DATABASE IF NOT EXISTS test;
```

#### Удаление/переименование бд
- Удаление базы данных
```
DROP DATABASE test;
```

- Удаление БД. Если БД не существует - не выдаст ошибку.
```  
DROP DATABASE IF EXISTS test;
```

- Переименование БД
```
RENAME DATABASE test TO production;
```

#### Создание таблицы

- Создание таблицы
```
CREATE TABLE `department` (
 `id` int(11),
 `name` varchar(255)
);
```

- Создание таблицы (более реальный пример)
```
CREATE TABLE `department` (
 `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
 `name` varchar(255) DEFAULT NULL,
 PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

`AUTO_INCREMENT` - автоматическая генерация данных
#### Удаление таблицы

- Удаление таблицы
```
DROP TABLE `name`;
```

- Удаление таблицы, если таковая существует. Если таблицы не существует - не будет выброшена ошибка
```
DROP TABLE IF EXISTS `name`;
```
- Посмотреть список таблиц
```
SHOW TABLES;
```

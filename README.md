# Домашнее задание к занятию "`Базы данных`" - `Репин Андрей`


---

### Задание 1
Опишите не менее семи таблиц, из которых состоит база данных:

какие данные хранятся в этих таблицах;
какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Получилось 6 таблиц. Мельчить далее не имеет смысла. Можно разбить таблицу АДРЕС на регионы и города. Но не имеет смысла, т.к. всего 3 филиала у фирмы.
###############################################################
Должность (
    идентификатор, первичный ключ, smallserial
    наименование должности varchar(50) 
)
###############################################################
Тип подразделения (
    идентификатор типа подразделения, первичный ключ, smallserial   
    наименование типа подразделения, varchar(30) 
)
###############################################################
Подразделение (
    идентификатор подразделения, первичный ключ, smallserial
    идентификатор типа подразделения, внешний ключ, smallint
    наименование подразделения varchar(100)
)
###############################################################
Адрес филиала (
    идентификатор адреса, первичный ключ, smallserial
    наименование адреса varchar(100)
)
###############################################################
Проекты (

    идентификатор проекта, первичный ключ, serial
    наименование проекта, varchar(100)

)
###############################################################
Сотрудники (
    идентификатор сотрудника, первичный ключ, serial
    фамилия varchar(30)
    имя varchar(30)
    отчество varchar(30)
    дата найма date
    оклад money
    идентификатор должности, внешний ключ, smallint
    идентификатор филиала, внешний ключ, smallint
    идентификатор структурного подразделения, внешний ключ, smallint 
)
# 12-01_databases
HW_12-01_Databases

# Домашнее задание к занятию 1 "Базы данных"

### Задание 1.
Опишите не менее 7 таблиц, из которых состоит БД:

- Какие данные хранятся в этих таблицах
- Какой тип данных у столбцов в этих таблицах, если данные хранятся в **PostgreSQL**

### Решение:

**Таблица 1** сотрудники
```
employee_id, primary key, smallserial
фамилия, varchar(20)
имя, varchar(10)
отчество, varchar(20)
дата_найма, date
оклад_id, foreign key, tinyint
структурное_подразделение_id, foreign key, tinyint
проект_id, foreign key, tinyint
```
**Таблица 2** оклады
```
оклад_id, primary key, tinyint
salary, primary key, numeric(6,2)
employee_id, foreign key, smallserial
```
**Таблица 3** тип_подразделения
```
тип_подразделения_id, primary key, tinyint
структурное_подразделение_id, foreign key, tinyint
```
**Таблица 4** структурное_подразделение
```
структурное_подразделение_id, primary key, tinyint
адрес_филиала_id, foreign key, tinyint 
тип_подразделения_id, foreign key, tinyint
```
**Таблица 5** адрес_филиала
```
адрес_филиала_id, primary key, tinyint
адрес_филиала, varchar(100)
город, foreign key, varchar(15)
```
**Таблица 6** город_филиала
```
город_филиала_id, primary key, tinyint
город, varchar(10)
```
**Таблица 7** проект
```
проект_id, primary key, tinyint
название_проекта, varchar(100)
```
---

# Диаграммы

## Диаграмма последовательности

```mermaid
sequenceDiagram
    actor User as Пользователь
    participant System as Система
    participant Model as ML-модель
    participant DataBase as База_данных

    User->>System: Отправить сообщение
    System->>Model: Передать текст
    Model->>DataBase: Запросить варианты записей, в зависимости от содержания сообщения
    DataBase->>Model: Вернуть доступные варианты записей
    Model-->>System: Вернуть доступные варианты записей
    System-->>User: Предложить доступные варианты записей
    User->>System: Выбрать запись из доступных
    System->>DataBase: Отправить запрос для внесения информации о записи в базу данных
    DataBase-->>System: Успешно выполненный запрос
    System-->>User: Сообщение об успешной записи
```

## Диаграмма классов

```mermaid
classDiagram

    class User {
        +int id
        +string name
    }

    class Appoinment{
        +int id
        +int id_user
        +int id_doctor
        +datetime time
        +int id_hospital
    }

    class Doctor {
        +int id
        +string name
        +int id_hospital
    }
    class Hospital {
        int id
        string address
    }

    User "1" <--> "*" Appoinment
    Doctor "1" <--> "*" Appoinment
    Appoinment "1" <--> "1" Hospital
    Doctor "1" <--> "1" Hospital
```
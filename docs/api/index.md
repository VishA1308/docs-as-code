# API

API предоставляет доступ к функциям ИИ-бота.

## Основные операции

- `POST /classification` — выполнить классификацию сообщения пользователя;
- `POST /users/{userId}/appointment` — записать к врачу пользователя по ID;
- `GET /users/{userId}/appointment` — получить все записи пользователя по ID;
- `DELETE /appointments/{appointmentId}` - удалить запись по ID.

## Спецификация

Полное описание API находится в файле `openapi.yaml`.

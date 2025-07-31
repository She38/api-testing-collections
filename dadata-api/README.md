# DaData API

Интеграция с API сервиса DaData — метод геолокации по координатам (/geolocate/address).

## 🔑 Авторизация

- Используется Bearer Token
- Токен вынесен в переменную {{api-token}}

## 🔧 Как использовать

1. Импортируй dadata-collection.json в Postman
2. Перейди в Environments и создай переменную:
   - api-token = Token your_token_here
3. Убедись, что выбран правильный environment при выполнении запроса

## 📨 Пример запроса

`json
{
  "lat": 55.878,
  "lon": 37.653
}

---

### README.md для VTB (vtb-api/README.md)

markdown
# VTB API — Создание заказа

Интеграция с тестовым окружением API банка ВТБ для создания платежного заказа.

## Авторизация

- Тип: Basic Auth
- Логин/пароль передаются через тело запроса
- Пароль вынесен в переменную {{password}}

## Как использовать

1. Импортировать vtb-collection.json в Postman
2. Задать переменную password в Environments
3. Убедиться, что выбран правильный environment при выполнении запроса

## Параметры запроса

| Поле        | Значение                              |
|-------------|----------------------------------------|
| userName    | test_daniel-api                       |
| password    | {{password}}                        |
| orderNumber | UUID заказа (генерируется динамически)|
| amount      | Сумма в копейках (например, 250000)   |
| returnUrl   | URL при успешной оплате               |
| failUrl     | URL при неуспешной оплате             |
| email       | Почта клиента                         |
| clientId    | Идентификатор клиента                 |
| description | Описание заказа                       |

## Результат

Ответ от API содержит orderId, formUrl, и другие поля, необходимые для редиректа на страницу оплаты.

## Безопасность

- Все чувствительные данные замаскированы переменными

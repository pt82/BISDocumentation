## create/order-to-delivery: Создание онлайн-заказа в Poster 

> Пример запроса на создание онлайн-заказа
```javascript
post(/create/order-to-delivery)
```
>Параметры запроса
```json
{
    "id":24,
    "phone": "+79237857776",
    "products": [
        {
            "product_id":9,
            "count": 1
        },
        {
        	"product_id":10,
            "count": 2
        }
    ]
}
```
### Аргументы
Свойство | Описание
-------- | --------
id | id салона (точки) (int)
phone| телефон клиета (string)
products | массив объектов товаров для заказа (array)
Массив `products` содержит объектs с такими свойствами:
Свойство | Описание
-------- | --------
product_id | id блюда (int)
count | количество (int)
> Пример ответа 
```json
{
 "success": true,
  "data": {
        "incoming_order_id": 12,
        "type": 1,
        "spot_id": 2,
        "status": 0,
        "client_id": 1,
        "client_address_id": 0,
        "table_id": null,
        "comment": null,
        "created_at": "2022-02-01 08:52:04",
        "updated_at": "2022-02-01 08:52:04",
        "transaction_id": null,
        "service_mode": 1,
        "delivery_price": null,
        "fiscal_spreading": 0,
        "fiscal_method": "",
        "promotion": null,
        "delivery_time": "0000-00-00 00:00:00",
        "payment_method_id": null,
        "first_name": null,
        "last_name": null,
        "phone": "79237857776",
        "email": null,
        "sex": null,
        "birthday": null,
        "address": null,
        "products": [
            {
                "io_product_id": 12,
                "product_id": 9,
                "modificator_id": 0,
                "incoming_order_id": 12,
                "count": "1.0000000",
                "price": 12000,
                "created_at": "2022-02-01 08:52:04"
            }
        ]
    }
}
```


Метод возврвщает список салонов

### Ответ

Свойство | Описание
-------- | --------
success | Объект с полем `success` может принимать true/false
data | Массив объектов `data` с данными о салоне
 
Массив `data` содержит объектs с такими свойствами
 
Свойство | Описание
-------- | --------
incoming_order_id |	Id онлайн-заказа
type | Тип заказа: 1 — онлайн-заказ, 2 — бронирование.
spot_id | Id салона (точки)
status | Статус заказа: 0 — новый, 1 — принят, 7 — отменён
client_id |	Id клиента
first_name |	Имя клиента
last_name |	Фамилия клиента
phone |	Телефон клиента
email |	Эл. почта клиента
sex |Пол клиента: 0 — не указан, 1 — мужской, 2 — женский
birthday | Дата рождения клиента, формат Y-m-d
client_address_id |	ID адреса клиента
address | Адрес клиента
comment |	Комментарий к онлайн-заказу
created_at |	Дата создания онлайн-заказа
updated_at | Дата изменения статуса онлайн-заказа
transaction_id |	Id связанного чека
fiscal_spreading |	Опциональный параметр. Признак, как отправлять товары на фискальный регистратор: 1 — отправлять только фискальные товары, 2 - отправлять все товары, 3 - не отправлять товары.
fiscal_method |	Опциональный параметр, метод оплаты на фискальном регистраторе: cash – наличными, card — картой. По умолчанию cash.
delivery_time |	Время доставки/самовывоза
products |	Список товаров (array)

Массив `products` содержит объектs с такими свойствами:
Свойство | Описание
-------- | --------
io_product_id |	Id товара в онлайн-заказе
product_id | Id товара
modificator_id | Id модификатора товара
incoming_order_id |	Id онлайн-заказа
count |	Количество товара в онлайн-заказе
created_at |Дата добавления товара в онлайн-заказ
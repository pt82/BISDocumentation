## dishes-to-delivery: Блюда

> Пример запроса на вывод блюд для доставки
```javascript
get(dishes-to-delivery)
```

>Параметры запроса
```json
{
    "department_id":24
}
```
### Аргументы
Свойство | Описание
-------- | --------
department_id| id салона (точки) (int)


> Пример ответа
```json
{
    "success": true,
    "data": {
        "schedules": [
            {
                "categoryIds": [
                    6,
                    5
                ]
            }
        ],
        "categories": [
            {
                "id": "6",
                "name": "Стейки",
                "images": [
                    {
                        "url": null,
                        "updatedAt": null
                    }
                ]
            },
            {
                "id": "5",
                "name": "Салаты",
                "images": [
                    {
                        "url": null,
                        "updatedAt": null
                    }
                ]
            }
        ],
        "products": [
            {
                "id": 1,
                "categoryId": "6",
                "name": "Гарнир: Морковь",
                "description": null,
                "price": 17000,
                "measure": null,
                "measureUnit": null,
                "images": [
                    {
                        "hash": "c4ee873a6942fe15b161e0716fe5a3b1",
                        "url": "https://avatarko.ru/img/kartinka/1/Jack_Vorobei.jpg"
                    }
                ]
            },
            {
                "id": 2,
                "categoryId": "6",
                "name": "Набор: Соль",
                "description": null,
                "price": 0,
                "measure": null,
                "measureUnit": null
            },
            {
                "id": 3,
                "categoryId": "5",
                "name": "Блюдо тест-1",
                "description": null,
                "price": 0,
                "measure": null,
                "measureUnit": null
            }
        ]
    }
}
```

Метод возврвщает список блюд салона (точки)

### Ответ

Свойство | Описание
-------- | --------
success | Объект с полем `success` может принимать true/false
data | Массив объектов `data` с данными о блюдах
 
Массив `data` содержит объектs с такими свойствами
 
Свойство | Описание
-------- | --------
schedules| масиив schedules содержит массив categoryIds, id категорий блюд
categories| масиив categories содержит категории блюд
products| масиив products содержит блюда

Массив `categories` содержит массив объектов с такими свойствами

Свойство | Описание
-------- | --------
id| id категории
id| наименование категории
images| массив изображений

Массив `products` содержит массив объектов с такими свойствами

Свойство | Описание
-------- | --------
id| id блюда
categoryId| id категории
name| название блюда
description | описание блюда
price | стоимость
measure| нетто
measureUnit| единица измерения
images | массив изображений
## departments: Список салонов

> Пример запроса на вывод салонов, достпных пользователю
```javascript
get(departments)
```

> Пример ответа 
```json
{
 "success": true,
 "data":[
	{
            "id": 8,
            "franchise_id": 4,
            "chain_id": 1,
            "department_id": "1b8e1451-ec5a-41cf-bd98-38913361e2cd",
            "manager_user_id": null,
            "yc_company_id": 215098,
            "department_name": "Ватутина, 33",
            "department_address": "Ватутина, 33",
            "timezone_offset": 12,
            "timezone_title": "Asia/Anadyr",
            "time_begin": null,
            "time_end": null,
            "created_at": "2021-09-16T12:34:05.000000Z",
            "updated_at": "2021-09-16T12:34:05.000000Z",
            "yc_name": "",
            "coordinates": {
                "lat": {
                    "min": "11",
                    "sec": "11",
                    "grad": "11"
                },
                "lon": {
                    "min": "22",
                    "sec": "22",
                    "grad": "22"
                }
            },
            "city": "Новосибирск",
            "deleted_at": null
        },
        {
            "id": 9,
            "franchise_id": 4,
            "chain_id": 1,
            "department_id": "559871ac-b9d1-4dd8-b58c-69e71e90c2cc",
            "manager_user_id": null,
            "yc_company_id": 282644,
            "department_name": "Дуси Ковальчук, 185",
            "department_address": "Дуси Ковальчук, 185",
            "timezone_offset": null,
            "timezone_title": null,
            "time_begin": null,
            "time_end": null,
            "created_at": null,
            "updated_at": null,
            "yc_name": "",
            "coordinates": null,
            "city": null,
            "deleted_at": null
        },
	]
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
id | id салона 
franchise_id |id франшизы
chain_id |id компании
manager_user_id | Менеджер ответсвенный за салон (таблица Users)
yc_company_id | id в интеграционной системе (например, Poster)  
department_name | Название салона
department_address | Адрес салона
timezone_offset | Временная зона
timezone_title | Название временной зоны
time_begin | График работы, начало
time_end | График работы, окончание
created_at | Дата создания 
updated_at | Дата обновления
updated_at | Дата обновления
yc_name | Имя в интеграционной системе
coordinates | Координаты

### Ответ

Функция возвращает Promise, который вернет объект со свойством `client` или ошибку. 

Свойство | Описание
-------- | --------
client | Объект типа [Client](/docs/v3/pos/types/client)
## persons| Список сотрудников

> Пример запроса на создание онлайн-заказа
```javascript
get(persons)
```

> Пример ответа
```json
{
 success| true
  data: [
            {
                "id": 23049,
                "person_id": "3d674ecb-65ab-490b-b5cf-9dcf7de67e7a",
                "person_ivideon_id": null,
                "face_gallery_id": null,
                "yc_staff_id": null,
                "department_id": "d508a1a6-40b8-4151-b0d7-69aef8708744",
                "department_name": "Чебуречная на Фрунзе"
                "chain_id": 60,
                "franchise_admin_id": null,
                "speciality_id": 3,
                "birth_date": 2000-01-01,
                "firstname": "Дарья",
                "lastname": "Иванова",
                "fatherland": "Леонидовна",
                "phone": "79011000000",
                "avatar": "https://bis.20x80.one/9f6c7ad7-545f-4b28-8666-294497b94716",
                "email": "dasha-demo@yandex.ru",
                "near_brday": null,
                "rating": null,
                "activity": null,
                "software": null,
                "period_haircut": null,
                "yc_id": null,
                "yc_name": null,
                "sex": null,
                "comment": null,
                "updated_at": "2022-01-13T03:42:07.000000Z",
                "created_at": "2022-01-10T07:02:46.000000Z",
                "invite_code": "ycmewq",
             },
	]
```


Метод возвращает список сотрудников

### Ответ

Свойство | Описание
-------- | --------
success | Объект с полем `success` может принимать true/false
data | Массив объектов `data` с данными о сотрудниках

Массив `data` содержит объекты с такими свойствами:

Свойство | Описание
-------- | --------
id| Id сотрудника
person_id|uid сотрудника
                person_ivideon_id|Id Ivideon (система распознования)
                face_gallery_id| Id группы распознования в Ivideon
                yc_staff_id| Id в интеграционной системе как сотрудника
                department_id| Id салона
                department_name| Название салона
                chain_id| id Компании
                franchise_admin_id| id франшизы
                speciality_id| id специальности
                birth_date| дата рождения
                firstname| Имя
                lastname| Фамилия
                fatherland| Отчество
                phone| телефон
                avatar| url аватар
                email| email
                sex| пол
                comment| коментарий
                updated_at| дата обновления
                created_at| дата создания
                invite_code| код для регистрации по ссылке

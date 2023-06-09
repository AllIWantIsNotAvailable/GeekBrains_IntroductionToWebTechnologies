# Задача №1:
> Проверить XML, правильно ли он составлен, не имеет ли он ошибок, если есть какие-либо недочеты, предоставьте правильный вариант в файле 1.xml

```xml
<req>
    <surname>Иванов</surname>
    <name>Иван</name>
    <patronymic>Иванович</patronymic>
    <birthdate>01.01.1990</birthdate>
    <birthplace>Москва</birthplace>
    <phone>8 926 766 48 48</phone>
</req
```

## Решение:
> - Отсутствует нотация документа xml.
> - Ошибка в закрывающем теге req.
> - Ошибкой не является, но в идеале добавить для группы тегов: surname, name, patronymic, birthdate, birthplace, phone родительский nod (узел), например user, так как в GET запросе могут быть переданы n записей пользователей.
> - Ошибкой не является, не очень очевидные имена узлов (patronymic).

### [Файл xml](https://github.com/AllIWantIsNotAvailable/GeekBrains_IntroductionToWebTechnologies/blob/main/seminars/Sem05_JSON_and_XML/HomeWork/1.xml):
```xml
<?xml version="1.0"?>
<req>
    <surname>Иванов</surname>
    <name>Иван</name>
    <patronymic>Иванович</patronymic>
    <birthdate>01.01.1990</birthdate>
    <birthplace>Москва</birthplace>
    <phone>8 926 766 48 48</phone>
</req>
```


# Задача №2:
> Проверить JSON, правильно ли он составлен, не имеет ли он ошибок, если есть какие-либо недочеты, предоставьте правильный вариант в файле 2.json:
```json
{
    "surname": "Иванов"
    "name": "Иван"
    "patronymic": "Иванович"
    "birthdate": "01.01.1990"
    "birthplace": "Москва"
    "phone": "8 926 766 48 48"
}
```

## Решение:
> - Отсутствуют символы разделителя пары ключ-значение объекта;
> - Ошибкой не является, но в идеале группу ключей-значений: surname, name, patronymic, birthdate, birthplace, phone; родительский объект, например object user, который в свою очередь будет являться элементом списка, так как в GET запросе могут быть переданы n записей пользователей.
> - Ошибкой не является, не очень очевидные имена узлов (patronymic).

### [Файл json](https://github.com/AllIWantIsNotAvailable/GeekBrains_IntroductionToWebTechnologies/blob/main/seminars/Sem05_JSON_and_XML/HomeWork/2.json):
```json
{
    "surname": "Иванов",
    "name": "Иван",
    "patronymic": "Иванович",
    "birthdate": "01.01.1990",
    "birthplace": "Москва",
    "phone": "8 926 766 48 48"
}
```

# Задача №3:
> Составить json по таблице, созданной при выполнении 4-го дз. (информация об одногруппниках с четырьмя полями: id, name, age, address.) Ответ представить в виде файла 3.json и прикрепить скрин, отображающий вид таблицы.

## Решение:

### [Таблица созданная в PostgreSQL для 3-го семинара](https://github.com/AllIWantIsNotAvailable/GeekBrains_IntroductionToWebTechnologies/blob/main/seminars/Sem05_JSON_and_XML/HomeWork/PostgreSQL%20table%20for%20seminar.csv):

| id | name      | age | address                                                             |
|----|-----------|-----|---------------------------------------------------------------------|
| 1  | Данила    | 25  | 501602, Кировская область, город Ногинск, проезд Славы, 53          |
| 2  | Макс      | 49  | 708223, Свердловская область, город Одинцово, пер. Ломоносова, 18   |
| 3  | Христофор | 52  | 549972, Иркутская область, город Можайск, пр. Космонавтов, 91       |
| 4  | Владимир  | 63  | 114433, Пензенская область, город Ступино, наб. Косиора, 35         |
| 5  | Виталий   | 20  | 141371, Белгородская область, город Видное, спуск Домодедовская, 52 |
| 6  | Виктория  | 38  | 191933, Воронежская область, город Наро-Фоминск, бульвар Чехова, 09 |
| 7  | Ксения    | 31  | 054875, Липецкая область, город Егорьевск, пл. Гоголя, 59           |
| 8  | Юлия      | 19  | 141499, Липецкая область, город Кашира, пл. Чехова, 35              |
| 9  | Кристина  | 38  | 568116, Тюменская область, город Ступино, пер. Сталина, 73          |


### [Файл json](https://github.com/AllIWantIsNotAvailable/GeekBrains_IntroductionToWebTechnologies/blob/main/seminars/Sem05_JSON_and_XML/HomeWork/3.json):
```json
{
	"students": [
					{
						"id": 1,
						"name": "Данила",
						"age": 25,
						"address": "501602, Кировская область, город Ногинск, проезд Славы, 53"
					},
					{
						"id": 2,
						"name": "Макс",
						"age": 49,
						"address": "708223, Свердловская область, город Одинцово, пер. Ломоносова, 18"
					},
					{
						"id": 3,
						"name": "Христофор",
						"age": 52,
						"address": "549972, Иркутская область, город Можайск, пр. Космонавтов, 91"
					},
					{
						"id": 4,
						"name": "Владимир",
						"age": 63,
						"address": "114433, Пензенская область, город Ступино, наб. Косиора, 35"
					},
					{
						"id": 5,
						"name": "Виталий",
						"age": 20,
						"address": "141371, Белгородская область, город Видное, спуск Домодедовская, 52"
					},
					{
						"id": 6,
						"name": "Виктория",
						"age": 38,
						"address": "191933, Воронежская область, город Наро-Фоминск, бульвар Чехова, 09"
					},
					{
						"id": 7,
						"name": "Ксения",
						"age": 31,
						"address": "054875, Липецкая область, город Егорьевск, пл. Гоголя, 59"
					},
					{
						"id": 8,
						"name": "Юлия",
						"age": 19,
						"address": "141499, Липецкая область, город Кашира, пл. Чехова, 35"
					},
					{
						"id": 9,
						"name": "Кристина",
						"age": 38,
						"address": "568116, Тюменская область, город Ступино, пер. Сталина, 73"
					}
				]
}
```
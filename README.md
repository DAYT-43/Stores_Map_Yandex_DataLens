# Stores_Map_Yandex_DataLens
# Аналитика в Yandex DataLens
  Проект для тренировки навыков визуализации и работы в DataLens, с пошаговым объяснением построения дашборда. 

## Цели по данному проектом:

1. Получить навыки работы с BI Инструментом Yandex Data Lens, для реализации визуализации данных по личному проекту “Участия и продажи тендерного отдела”

2. В рамках данного проекта, выявить в какой точке города Москвы требуется открыть новый филиал для магазина и сделал определенные выводы. 


Ссылка на мой [Дашборд Yandex DataLens](https://datalens.yandex.ru/cqp333qlbgzy3-dashbord-dz-netologiya?state=18dc6c9c214)

### Данный дашборд позволяет быстро оценить:

- Динамику продаж в целом и разбивке по магазинам
    - Продажи показывают уверенный рост в целом по городу. У всех магазинов в целом хороший рост, нет явных аутсайдеров. Открытие нового магазина может ускорить рост выручки
- Продажи в магазинах по продуктовым категориям
    - Лидеры по магазинам - «Бета» и «Дзета». Доли продаж каждой продуктовой категории во всех магазинах примерно одинаковы. С точки зрения продуктовых категорий лучше остальных «Техника для дома»
- Расположение магазинов, а также адреса доставок наших клиентов
    - В магазинах с локациями ближе к центру и ТТК выручка больше. Пустота с продажами в районе Раменок. Потенциальные локации - на юго-западе, ближе к центру в районе ТТК, районов Хамовники, Даниловский
    
![Untitled (14)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/22ef88cd-6dd7-4ea6-8d24-64009d604de8)


## Процесс создания дашборда

### Описываем датасет и логику работы с ним
![Untitled (15)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/53654ace-ce30-410f-adb9-81053eb8b4f0)

### Переносим таблицы
![Untitled (16)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/783aa733-e011-4d5a-b2ec-d6cfd7809425)

Тут важно указать правила агрегации (для каждого поля свой правильный формат)

Поле OrderId продублируем, чтобы сделать OrderCounts 

Создадим новое поле где посчитаем среднюю корзину (AverageOrder)

![Untitled (14)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/b818fc7c-c2f8-44fd-ab08-39e4952e73f3)


### Меняем тип там где должны быть геоданные на геоточку и там где районы ставим геополигон
![Untitled (17)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/b47b9db0-48d6-42d2-a25b-f5b1205c7eea)


### Создаем визуализацию
![Untitled (18)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/63f9ff4b-4e1d-4179-b4d1-0b408366ffc8)


### Создаем чарт, сохраняем
![Untitled (19)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/dd4f3eb6-77c8-4a78-9758-3db2022c2c3b)


Меняем Х на другой

меняем тип диаграммы и отображение по неделям 
![Untitled (20)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/b49cea10-b7f5-489c-acf1-71cb85e2d963)


Будет так , сохраняем 
![Untitled (21)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/29b867d9-15c5-4a1b-8ecb-dc5296467f84)


Заменим в цветах на ShopName  и увидим динамику разбивки по магазинам и изменим на диаграмму с областями
![Untitled (22)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/52465ae4-d9e4-4167-9e1d-a341ccfd7ead)

### Делаем карты

создаем первый слой

Увидим продажи по магазину
![Untitled (23)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/d2614893-07c0-4340-bb3d-44a310996a99)

Делаем второй слой с адресами клиентов, будет тепловая карта с адресами наших клиентов

переименуем слои , Доставки и Магазины(Слой1), сохраним чарт
![Untitled (24)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/0fb83019-a6a4-4ff3-bfe2-6d559ae8a57b)

### Работаем с дашбордом

Навигация - дашборд - создать дашборд
![Untitled (25)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/23c37fec-bbab-4ed3-a4a9-34e89fa2d4ff)

Добавляем первый чарт, нашу карту , потом остальные чарты
![Untitled (26)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/2255299b-21b9-4290-bd9c-bb4aeb748f3d)

настраиваем расположение 
![Untitled (27)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/805738d3-94e0-46ac-9e0f-6a598227f3c5)


Выбираем селектор, и поле к нему ShopName (Имя магазина)
![Untitled (28)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/fd2c9b5a-5e68-4296-b846-3fffc6fcba98)
![Untitled (29)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/c87be6b4-bebb-4678-ae72-911292313e04)

Аналогично добавляем селектор по времени заказа и ProductBrand
![Untitled (30)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/4e4ab6d4-7f6e-4a7d-acf4-437dd1996e78)


### FAQ по Data Lens
![Untitled (31)](https://github.com/DAYT-43/Stores_Map_Yandex_DataLens/assets/80617386/acfe73fb-5fce-4b05-a49e-f8e4b58b529e)

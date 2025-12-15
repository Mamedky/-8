**Отчет по Лабораторной работе 8. Диаграммы классов.**
-------------------------------------------------------
-------------------------------------------------------
Кинотеатр. Упрощенная диаграмма.
---------------------------------
Описание классов:

  
**Клиент** - посетитель кинотеатра. Клиент покупает и возвращает билеты. Каждый клиент может иметь несколько билетов.

**Фильм** - фильм, который показывают в кинотеатре. Фильм может быть показан на нескольких сеансах.

**Сеанс** - класс описывает конкретный показ фильма в определенное время. Сенс связан с одним фильмом и проводится в одном зале. Для одного сеанса может быть продано несколько билетов.

**Зал** - зал кинотеатра. Зал содержит набор мест и используется для проведения сеансов.

**Место** - отдельное место в зале. Место определяется номером и используется при приобритении билета.

**Билет** - билет на конкретный сеанс и место для клиента. 

Описание связей:

* Клиент - Билет
  
"Один ко многим". Один клиент может купить несколько билетов.
* Фильм - Сеанс
  
"Один ко многим". Один фильм может показываться на нескольких сеансах.
* Зал - Место
   
Композиция. Места есть только внутри конкретного зала (нет части без целого).
* Зал - Сеанс
   
"Один ко многим". В одном зале проходят разные сеансы.
* Сеанс - Билет
  
"Один ко многим". Для одного сеанса можно купить несколько билетов.
* Место - Билет
  
"Один ко многим". Одно место может быть связано с разными билетами на разные сеансы.

Ограничения:

* Билет действует только на один сеанс
* Билет привязан к одному месту
* Возврат билета возможен только до начала сеанса

Диаграмма:
-----
  
![](https://img.plantuml.biz/plantuml/png/VLJDQjjW4BmBz0wBBaq23irLfnpw1kqBc4P91Ou3jd8g1Vz0Iqd091GAfPT27q2uLgh6jleA-xrHP_PJPIbfWq58kpExi_Fjv-DnrXzbb-U3CCZIR928Vj9IS_tX9dXkyCj5xtMjkPkwgLQwb4Y_0BBLoisqG7pc9f7ikRd-1gTo7zqDabia5ljX40Ql1_tnMC1PWrNeritaRHY8f2VjcEQnlCn6wV2CkLwFJxrdKItHuLflW5nhuMPx-vPRudq2vlnnzbshxNSc0DZufjIbFq7EyORMxQQweXmRYWmEE6NnMD9XrgtwZOEZ-RIkkg8DYDn2Kg4RjuZbHJzBNgNdIPVu6Q1r8wM2lPp2edJWKQElo4E4LWyv_y0s7ZJ-Df6kk-uzFU_sUmRFUnniwHOmgEGduoq3ewC8KOcU7nuUH6qFOi4fLTWIMEkkp5pqXEu5-7vYSWz8FlBatLons5gjp8Wx-jyX_RSXTmsjo2p_DWDp1th0thaJsqcRk9sC9z1OGXlDTgR2ve7OtkQd6faljiNc2IKEBx94HkdPcqmkJbjmL6tUup3eKMMXlqpV4YLOaQScVcRTqhXwM8FJah8-FqHnVJpKTiRDnHQ76prlmNaVkFU5zzxVzNgo6aYJSMNuXq20_zpWUKSOPLOcp7tmQzpIfNaO9CCJuSoS_HWVzb_p1m00)


Частная клиника. Упрощенная диаграмма.
---------------------------------
Описание классов:

**Пациент** - пациент клиники. Имеет персональные данные и медицинскую карту. Он не взаимодействует с системой напрямую для записи на приём.

**Администратор** - сотрудник клиники, который выполняет запись и отмену записей пациентов.

**Врач** - медицинский работник. Врач заполняет медицинские карты пациентов и формирует планы лечения.

**Медицинская карта** - медицинский документ пациента. Медицинская карта принадлежит одному пациенту и содержит медицинские данные.

**План лечения** - класс описывает план лечения пациента. Одна медицинская карта может содержать несколько планов лечения.

**Запись на приём** - класс описывает запись пациента к врачу на конкретное время. Запись создаётся администратором по запросу пациента.

Описание связей:

* Пациент — Медицинская карта
  
Связь «один к одному». Каждый пациент имеет одну медицинскую карту.
* Медицинская карта — План лечения
  
Композиция. План лечения существует только в рамках медицинской карты.
* Врач — Медицинская карта

Связь «один ко многим». Один врач может заполнять медицинские карты нескольких пациентов.
* Пациент — Запись на приём
  
Связь «один ко многим». Пациент может иметь несколько записей на приём.
* Администратор — Запись на приём
 
Связь «один ко многим». Администратор оформляет записи пациентов.

Ограничения:  

* Запись на прием создается только администратором.Пациент не может создать запись самостоятельно.
* Запись возможна только на свободный слот
* Статус определяет состояние записи

Диаграмма:
-----

![](https://img.plantuml.biz/plantuml/png/bLLDRzD04BrRydzOcGDGb0YkEVN0F-3A9QfDQwbrKE9oGPKSWwXG8WKX9102gWgaNas8gSc7ynTc_n5lPkF4JXfIPCdsxio-UVDcnjxlXCrsU7foR5kX7nvxYhxJN4UKwxUKqWnNeWUAHfHHGhzWI6YAAr4qfWbiNTsbd8RAeIjPnSK9DcTOP7XB7DkohOFZPgUZw0BsDzW6kexLIzjITzHfnslxRaCz2Tj-S2XRz8C-qRVArlEZLk0rb1-4jdLMGdpFjFIvODMKspe8MrMqsYPQJO7ud5AXaWZNQqDC3yfkDTmUi0dEEToGa8vrdxw0_uW-uqY4zQjxznlgHSjtgyJUmMLgL61fX6OCQQC5rQPxuWSxcPOf08SnGE0hrXT0P26dDuSt73D9SOQ3OwxCqq2UO8qY6XhWbuDd2hGYeTv2PhQoIf6KUSPA8VPCzm3z0QkPUQzcCDs8csrpFwiqneHTG722YEVIVgZ6WgJl5WwKhDMHK-4YwEvcWJCXFXQfSZ02CpX6wmYHE6KDzRWPUXLQ3dqibDTzbWgjFozqTrRabbwCKbPZ94LFf4jnXDlB1DdANQBVHU5n-fA6Ue3YPxpa_RNvSHuviCZZ5lLkA9YuFAcE0RNx0EFkCVx3UdtFsLwZXXATHz94ltb6X6incGNB1SgjY9Pc3WeOmZVdRb1t56g9oFOU3V4EJBmFWBjzKFytHgvVypcWJGphSjW-YnAqGa-r_SEZKBMUxK2qBRJ0FnoCwjVSOqKsYedBb8ufLzZVaXcFV7rDK7YbFBuvIiZKL-ZyoQbamZR-5UJImhaUu9wQZmFbzKtUGq4oq9n3cIL6mIG6JFRxAPt4Nue_l3K1V2o8bwjfWT8Y0pTIkjIQ2HU4vD-JbaXJPbjUu2ek01TY7mly-Fu2)

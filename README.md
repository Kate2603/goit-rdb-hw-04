# goit-rdb-hw-04

1. 1. Створіть базу даних для керування бібліотекою книг згідно зі структурою, наведеною нижче. Використовуйте DDL-команди для створення необхідних таблиць та їх зв'язків.

Структура БД

a) Назва схеми — “LibraryManagement”

b) Таблиця "authors":

author_id (INT, автоматично зростаючий PRIMARY KEY)
author_name (VARCHAR)
c) Таблиця "genres":

genre_id (INT, автоматично зростаючий PRIMARY KEY)
genre_name (VARCHAR)
d) Таблиця "books":

book_id (INT, автоматично зростаючий PRIMARY KEY)
title (VARCHAR)
publication_year (YEAR)
author_id (INT, FOREIGN KEY зв'язок з "Authors")
genre_id (INT, FOREIGN KEY зв'язок з "Genres")
e) Таблиця "users":

user_id (INT, автоматично зростаючий PRIMARY KEY)
username (VARCHAR)
email (VARCHAR)
f) Таблиця "borrowed_books":

borrow_id (INT, автоматично зростаючий PRIMARY KEY)
book_id (INT, FOREIGN KEY зв'язок з "Books")
user_id (INT, FOREIGN KEY зв'язок з "Users")
borrow_date (DATE)
return_date (DATE)

Результат створення БД:

![alt text](<img/1 та 2/1.1.jpg>)

![alt text](<img/1 та 2/1.2.jpg>)

2. Заповніть таблиці простими видуманими тестовими даними. Достатньо одного-двох рядків у кожну таблицю.

Результат:

![alt text](<img/1 та 2/1.3.jpg>)

Заповнена БД:

Таблиця "authors"
![alt text](<img/1 та 2/1.4.jpg>)

Таблиця "books":
![alt text](<img/1 та 2/1.5.jpg>)

Таблиця "borrowed_books"
![alt text](<img/1 та 2/1.6.jpg>)

Таблиця "genres"
![alt text](<img/1 та 2/1.7.jpg>)

Таблиця "users"
![alt text](<img/1 та 2/1.8.jpg>)

3. Перейдіть до бази даних, з якою працювали у темі 3. Напишіть запит за допомогою операторів FROM та INNER JOIN, що об’єднує всі таблиці даних, які ми завантажили з файлів: order_details, orders, customers, products, categories, employees, shippers, suppliers. Для цього ви маєте знайти спільні ключі.

Перевірте правильність виконання запиту.

4. Виконайте запити, перелічені нижче.

Визначте, скільки рядків ви отримали (за допомогою оператора COUNT).
Змініть декілька операторів INNER на LEFT чи RIGHT. Визначте, що відбувається з кількістю рядків. Чому? Напишіть відповідь у текстовому файлі.
На основі запита з пункта 3 виконайте наступне: оберіть тільки ті рядки, де employee_id > 3 та ≤ 10.
Згрупуйте за іменем категорії, порахуйте кількість рядків у групі, середню кількість товару (кількість товару знаходиться в order_details.quantity)
Відфільтруйте рядки, де середня кількість товару більша за 21.
Відсортуйте рядки за спаданням кількості рядків.
Виведіть на екран (оберіть) чотири рядки з пропущеним першим рядком.

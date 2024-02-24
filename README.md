# Онлайн-гра: Адмін-панель для керування акаунтами

Цей проєкт представляє собою адмін-панель для зручного керування акаунтами у онлайн-грі. Для його використання слід виконати деякі кроки.

## Інструкції для запуску

1. **Зробіть fork репозиторію:** [https://github.com/pavlo-plynko/project-frontend.git](https://github.com/pavlo-plynko/project-frontend.git)

2. **Завантажте свою версію проєкту на комп'ютер.**

3. **Завантажте Tomcat версії 9:** [https://tomcat.apache.org/download-90.cgi](https://tomcat.apache.org/download-90.cgi)
   
   Важливо: Використовуйте версію 9 Tomcat, а не 10.

4. **Налаштуйте запуск програми через IntelliJ IDEA:**
   
   - Натисніть `Alt + Shift + F9`, оберіть `Edit Configurations…`.
   - Додайте нову конфігурацію `tom` (у рядок пошуку).
   - У полі "Server" вкажіть, куди завантажено і розпаковано Tomcat.
   - У вкладці "Deployment", оберіть `rpg:war exploded` у полі "Artifact".
   - У полі "Application context", залиште тільки `/` (слеш).
   - Натисніть `APPLY` та закрийте вікно налаштувань.

5. **Запустіть програму:** 

   - Натисніть `Alt + Shift + F9`, оберіть ім'я конфігурації та натисніть `Run`.

## Робота з UI

Розмітка та стилі розміщені у двох файлах:

- `<project_dir>/src/main/webapp/html/my.html` - розмітка та скрипти.
- `<project_dir>/src/main/webapp/css/my.css` - стилі.

### Таблиця облікових записів

На основі завдання додано таблицю з такими колонками:

1. #
2. Name
3. Title
4. Race
5. Profession
6. Level
7. Birthday
8. Banned

### Функції

1. **Отримання списку акаунтів:** Функція відправляє GET запит на URL "/rest/players" та відображає результат у таблиці.

2. **Пейджинг:** Додана секція з кнопками пейджингу та випадаючим списком для вибору кількості акаунтів на сторінці.

3. **Видалення акаунту:** Додана функція для видалення акаунту, яка відправляє DELETE запит на сервер на URL "/rest/players/{id}".

4. **Редагування акаунту:** Додана функція для редагування акаунту. При натисканні на кнопку "Edit", можливість редагування полів з подальшим збереженням змін на сервері.

5. **Створення нового акаунту:** Додано можливість створення нового акаунту через введення даних у відповідних полях та відправлення POST запиту на URL "/rest/players".

### Інші покращення

- Додано горизонтальну лінію та текст, що надає можливість створення нового облікового запису.
- Додані блоки тексту та поля для введення параметрів облікового запису для створення нового акаунту.

### Завдання зроблено!

Тепер ви можете користуватися цією адмін-панеллю для керування акаунтами у онлайн-грі. Насолоджуйтесь та розробляйте додатковий функціонал за необхідністю!
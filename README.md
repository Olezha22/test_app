# Test App

Test App це міні додаток на flutter який працює на IOS та Android.

## Перший екран - Секундомір

- Пульсуюча кнопка з іконкою play яка пульсує доти доки не запущено секундомір
- Зверху над кнопкою розташований секундомір який відображає інформацію в форматі години:хвилини:секунди
- коли секундомір починає працювати тобто є хоча б одна секунда на ньому відображається під кнопкою play кнопка з текстом "Скинути"
- Логіка і state management реалізована за допомогою Cubit

## Другий екран - Локація

- Ми отримуємо поточну Ip адресу користувача
- Ip адресу показуємо на карті
- Під картою з нашої API відображаємо всі дані з анімацією
- Під даними є кнопка "Оновити" яка обновляє а точніше отримує Ip адресу якщо вона така сама то відображаємо старі дані якщо ні відображаємо дані з нової Ip адреси
- Також оновлювати можна за допомогою жесту pull-to-fresh
- Якщо вибиває помилку читання з API наприклад немає інтернет з'єднання то дані беруться з нашого кешу тобто кожен раз коли ми оновлюємо і отримуємо дані з API наш кеш оновлюється за допомогою SharedPreferences якщо дані в кеші не знайдено то користувачу показуємо екран помилки
- Для управління станом використовував Bloc

## Третій екран - Операції

- Є три активні кнопки, коли ми натискаємо на них виконується тільки ця операція що пристосована для цієї кнопки і одразу міняємо колір іконки активної кнопки
- Для кнопки "Оцініть додаток" ми викликаємо метод який викликає алерт щоб поставити додатку оцінку - кількість зірок
- Для кнопки "Поділитися" ми викликаємо метод який може поширити текст який я передав в програмі відповідно до вибраної мови
- Для кнопки "Зв'язатися з нами" ми викликаємо метод який відкриває браузер і відкриває силку на тестове завдання

## Додатково

- Додано три локалізації: укр, англ, нім.
  1. Ми можемо вибрати на якій мові відображати додаток в нашому AppBar
  2. Це реалізовано через Cubit
- Також є Tab bar який відображає наші 3 екрани

==============================
Лазаренко Андрій Ростиславович
==============================


#. Локальні та віддалені репозиторії Git. Наведіть команду для відправки локальних комітів з гілки dev до віддаленого репозиторію.

   - Локальний репозиторій - це репозиторій, що вже лежить на ПК.
     Віддалений репозиторій - це репозиторій, що існує десь у мережі, його можна клонувати на свою машину щоб він став локальним(git clone).
     git push dev після чого обираємо гілку звідки відправляти, а потім гілку куди віправляти.
     
#. Як підтягнути зміни, що відбулись у віддаленому upstream-репозиторії (гілка master) до локального репозиторію? Наведіть команду.

   - git pull origin master
   
#. Прокоментуйте (за допомогою коментарів Make) Makefile що використовується для збірки модулів ядра в курсі.
   Що відбувається в кожній строчці?
#. Що таке QEMU? Для чого він використовується? Що дає KVM в QEMU?

   - QEMU - це програма, що дозволяє проводити емуляцію різних процесорів або навіть певної периферії.
     KVM дозволяє працювати із певними програмами на віртуальній ОС, але він огороджує від цих програм фізичні апаратні ресурси. Тобто він працює як певне сполучення між хостом
     та гостем. На мою думку це надає достатній захист.
   
#. Яким чином модуль ядра отримує параметри? Наведіть код для двох параметрів (count - integer та path - строка),
   значення яких за замовчуванням 69 та "ctl:data" відповідно. Якою командою переглянути параметри модуля ядра?
#. Якщо роздрукувати поточне значення jiffies до запуску тасклета та всередині тасклета, то
   чому ці два виводимих значення можуть відрізнятися на 0, 1 чи 2? Поясніть для кожного випадку.

   - Якщо ядро не заняте виконанням якоїсь дії, то затримка виконання тсклета буде 0. Коли ж ядро зайняте певним процесом. то затримка виконання буде вже 1 такт.
   
#. Які обмеження має алокація фізичної (kmalloc) та віртуальної (vmalloc) пам'яті? Які їх переваги та недоліки?

   - Функція vmalloc використовується для роботи із віртуальною пам'яттю. Вона дає неперервну область пам'яті. Об'єм пам'яті не обмежений.
     Функція kmalloc використовується для роботи із фізичною пам'яттю. Вона має обмеження на розмір запрошеної пам'яті. Цей розмір складає 128 КБ.
     vmalloc працює повільніше за kmalloc
     
#. Що таке callback-функції та для чого використовуються? Наведіть приклад використання container_of у callback-функції

   - Сallback-функція це фукція, що виконується після завершення виконання певної дії. 
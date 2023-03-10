# LeetCode Problems

In this lab work, our task was to solve three problems from LeetCode or Codewars. We have choosen such problems:
- Add Two Numbers
- Letter Combinations of a Phone Number
- Two Sum

Detailed information about these problems you can find in subdirectories.

## Answers to control questions: 
1. **Чи є різниця між виконанням JavaScript в браузері та в середовищі Node.js?**

Так, є різниця між виконанням JavaScript в браузері та в середовищі Node.js.

Браузери і Node.js засновані на різних двигунах JavaScript. Браузери використовують двигун V8, який розробляється Google і використовується в Chrome, а Node.js використовує двигун V8 разом з іншими компонентами для побудови серверних додатків.

Крім того, в середовищі Node.js доступні модулі, які не підтримуються в браузерах, такі як модулі для роботи з файловою системою і мережею. Також у Node.js використовується інший API для взаємодії з середовищем, наприклад, модуль process, який дозволяє отримувати інформацію про середовище виконання і налаштування додатку.

Крім цього, у браузері JavaScript може взаємодіяти з DOM (Document Object Model), що дозволяє динамічно змінювати вміст сторінки. У Node.js немає такої можливості, оскільки він призначений для виконання серверних додатків і не має доступу до DOM.

Отже, хоча використання JavaScript в браузері та в середовищі Node.js базується на одній мові програмування, існують певні різниці у функціональності та доступних API.

2. **Основні типи в JavaScript**

- **Примітивні типи даних:**
- ```number```: числовий тип даних, який включає цілі числа та числа з плаваючою крапкою.
- ```string```: рядковий тип даних, який включає послідовності символів.
- ```boolean```: булевий тип даних, який може бути або true (істина), або false (хиба).
- ```null```: тип даних, що представляє порожнечу.
- ```undefined```: тип даних, який показує, що змінна не має значення.
- ```symbol```: тип даних, що використовується для створення унікальних ідентифікаторів.
- **Об'єктні типи даних:**
- ```object```: об'єктний тип даних, який представляє складний тип даних, що може містити значення різних типів даних та методи.
- **Спеціальні типи даних** 
- ```NaN```: тип даних, який використовується для позначення помилки, яка виникає при спробі виконати математичну операцію, яка не може бути виконана.
- ```Infinity``` та ```-Infinity```: тип даних, який використовується для позначення додатного та від'ємного нескінченності.

3. **Як працює замикання в JavaScript?**

Замикання (closure) - це один з ключових механізмів JavaScript, який дозволяє функціям запам'ятовувати значення змінних, що знаходяться в зовнішньому контексті виклику функції. Замикання дають можливість створювати функції, які можуть зберігати свій внутрішній стан і поводитися як об'єкти з функціональними можливостями.

Коли функція створюється в JavaScript, вона отримує доступ до змінних, які знаходяться в тому ж самому контексті, де і створена ця функція. Якщо функція зберігає посилання на ці змінні і повертається з контексту, в якому ці змінні знаходяться, то вони все ще доступні для функції.

4. **Назвіть основні стандартні бібліотеки Node.Js**

<img src="/Lab1/img/data-types.jpg" alt="Libs" width="750" />

5. **Які є способи імпортувати модулі в Node.js?**

В Node.js для імпортування модулів використовуються ключові слова require та import.
Використання ключового слова require
require є вбудованим ключовим словом Node.js, яке дозволяє імпортувати модулі з інших файлів. Щоб імпортувати модуль, використовується наступний синтаксис:  const moduleName = require('module-name');

Використання ключового слова import
import є стандартним ключовим словом JavaScript ES6, яке дозволяє імпортувати модулі з інших файлів. Щоб імпортувати модуль, використовується наступний синтаксис: import moduleName from 'module-name';

Проте варто зазначити, що ключове слово import не є повністю підтримуваним в Node.js до сих пір і він не підтримує деякі сучасні функції JavaScript, які підтримуються у браузерах. Однак, ви можете використовувати import у Node.js, якщо ви встановите додатковий пакет, який підтримує його (наприклад, @babel/plugin-transform-modules-commonjs).

6. **Як повʼязані Google Chrome, Chromium та Node.js?**

Google Chrome, Chromium та Node.js мають спільність в тому, що вони використовують двигун V8 для виконання JavaScript-коду, але вони призначені для різних цілей та мають різні функціональні можливості.

7. **Як можна дозволити імпортувати змінні з поточного модуля у Node.js?**

У Node.js, щоб дозволити імпортувати змінні з поточного модуля, потрібно використовувати об'єкт exports або module.exports.

Наприклад, якщо ви хочете дозволити імпортувати змінну myVariable з поточного модуля, ви можете додати такий код у кінці модуля:

```node
exports.myVariable = myVariable;
```

або

```node
module.exports = { myVariable };
```

У першому випадку ми додаємо myVariable до об'єкта exports, а в другому ми повністю замінюємо module.exports на об'єкт з myVariable.

Після цього імпортувати змінну можна у іншому модулі за допомогою команди require:

```node
const { myVariable } = require('./myModule');
```

Цей підхід дозволяє ділити код на окремі модулі та експортувати змінні з них, що дозволяє зберігати код чистим та організованим.

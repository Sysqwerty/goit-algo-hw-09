# goit-algo-hw-09

[Тема 9. Жадібні алгоритми та динамічне програмування](https://www.edu.goit.global/uk/learn/13571785/19646173/19658335/training?blockId=21205235)

# Аналізуючи результати виконання, можна зробити наступні спостереження:

<h2>Час виконання:</h2>

- Час виконання жадібного алгоритму значно менший, ніж у випадку алгоритму динамічного програмування.

<h2>Продуктивність при великих сумах:</h2>

- Жадібний алгоритм показує добрі результати для невеликих та середніх значень сум (10, 58, 75, 113), але для
  великих сум (наприклад, 9999, 15768, 23374, 55755, 91232) він може втрачати оптимальність і видає необов'язково
  оптимальні результати.
- Алгоритм динамічного програмування показує стабільні та оптимальні результати навіть при великих сумах.
  Його ефективність на високому рівні.

<h2>Висновок:</h2>

- Жадібний алгоритм для швидкості: використання жадібного алгоритму може бути обґрунтованим, якщо важливо мінімізувати
  час виконання та ресурси, і не
  критично враховувати оптимальність рішення у всіх випадках.

- Динамічне програмування для великих сум: алгоритм динамічного програмування виявляється більш ефективним
  при роботі з великими сумами. Він забезпечує оптимальні результати та продовжує виявлятися ефективним, що може бути
  критично в сценаріях, де важлива точність рішення.

| Amount | Greedy Algorithm Time | Greedy Algorithm Result                  | Dynamic Programming Algorithm Time | Dynamic Programming Algorithm Result     |
|--------|-----------------------|------------------------------------------|------------------------------------|------------------------------------------|
| 10     | 8e-05                 | {10: 1}                                  | 0.00075                            | {10: 1}                                  |
| 58     | 0.00012               | {50: 1, 5: 1, 2: 1, 1: 1}                | 0.00479                            | {1: 1, 2: 1, 5: 1, 50: 1}                |
| 75     | 9e-05                 | {50: 1, 25: 1}                           | 0.00587                            | {25: 1, 50: 1}                           |
| 113    | 0.00011               | {50: 2, 10: 1, 2: 1, 1: 1}               | 0.00918                            | {1: 1, 2: 1, 10: 1, 50: 2}               |
| 500    | 0.0001                | {50: 10}                                 | 0.04979                            | {50: 10}                                 |
| 1000   | 8e-05                 | {50: 20}                                 | 0.1131                             | {50: 20}                                 |
| 1013   | 0.00012               | {50: 20, 10: 1, 2: 1, 1: 1}              | 0.11333                            | {1: 1, 2: 1, 10: 1, 50: 20}              |
| 1127   | 0.0001                | {50: 22, 25: 1, 2: 1}                    | 0.12389                            | {2: 1, 25: 1, 50: 22}                    |
| 2893   | 0.00014               | {50: 57, 25: 1, 10: 1, 5: 1, 2: 1, 1: 1} | 0.34641                            | {1: 1, 2: 1, 5: 1, 10: 1, 25: 1, 50: 57} |
| 9999   | 0.0001                | {50: 199, 25: 1, 10: 2, 2: 2}            | 1.22066                            | {2: 2, 10: 2, 25: 1, 50: 199}            |
| 15768  | 0.00013               | {50: 315, 10: 1, 5: 1, 2: 1, 1: 1}       | 1.90247                            | {1: 1, 2: 1, 5: 1, 10: 1, 50: 315}       |
| 23374  | 0.00011               | {50: 467, 10: 2, 2: 2}                   | 2.89026                            | {2: 2, 10: 2, 50: 467}                   |
| 55755  | 9e-05                 | {50: 1115, 5: 1}                         | 7.23779                            | {5: 1, 50: 1115}                         |
| 91232  | 0.00011               | {50: 1824, 25: 1, 5: 1, 2: 1}            | 13.51482                           | {2: 1, 5: 1, 25: 1, 50: 1824}            |

Обираючи між алгоритмами, слід враховувати конкретні вимоги вашої задачі: чи пріоритет має оптимальність рішення чи
швидкість виконання.
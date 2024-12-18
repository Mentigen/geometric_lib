# Unit тесты с проверкой некорректных данных

## Результаты тестов для некорректных данных

| Тестируемая функция                          | Входные данные              | Описание ситуации         | Ожидаемый результат          | Фактический результат | Дата       | Вердикт |
|----------------------------------------------|-----------------------------|---------------------------|------------------------------|-----------------------|------------|---------|
| `rectangle.area`                             | `(10, 0)`                   | Корректные данные         | `0`                          | `0`                   | 2024-10-16 | ОК      |
| `rectangle.area`                             | `(-10, 10)`                 | Отрицательная сторона     | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `rectangle.area`                             | `("a", 5)`                  | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `rectangle.area`                             | `(1e10, 1e10)`              | Очень большие числа       | `1e20`                       | `1e20`                | 2024-10-16 | ОК      |
| `rectangle.perimeter`                        | `(10, 10)`                  | Корректные данные         | `40`                         | `40`                  | 2024-10-16 | ОК      |
| `rectangle.perimeter`                        | `(10, -10)`                 | Отрицательная сторона     | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `rectangle.perimeter`                        | `(10, "width")`             | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `rectangle.perimeter`                        | `(1e10, 1e10)`              | Очень большие числа       | `4e10`                       | `4e10`                | 2024-10-16 | ОК      |
| `square.area`                                | `(10)`                      | Корректные данные         | `100`                        | `100`                 | 2024-10-16 | ОК      |
| `square.area`                                | `(-10)`                     | Отрицательная сторона     | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `square.area`                                | `("side")`                  | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `square.area`                                | `(1e10)`                    | Очень большое число       | `1e20`                       | `1e20`                | 2024-10-16 | ОК      |
| `square.perimeter`                           | `(10)`                      | Корректные данные         | `40`                         | `40`                  | 2024-10-16 | ОК      |
| `square.perimeter`                           | `(-10)`                     | Отрицательная сторона     | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `square.perimeter`                           | `("side")`                  | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `square.perimeter`                           | `(1e10)`                    | Очень большое число       | `4e10`                       | `4e10`                | 2024-10-16 | ОК      |
| `triangle.area`                              | `(10, 5)`                   | Корректные данные         | `25`                         | `25`                  | 2024-10-16 | ОК      |
| `triangle.area`                              | `(-10, 5)`                  | Отрицательное основание   | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `triangle.area`                              | `("a", 5)`                  | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `triangle.area`                              | `(1e10, 1e10)`              | Очень большие числа       | `5e19`                       | `5e19`                | 2024-10-16 | ОК      |
| `triangle.perimeter`                         | `(3, 4, 5)`                 | Корректные данные         | `12`                         | `12`                  | 2024-10-16 | ОК      |
| `triangle.perimeter`                         | `(3, -4, 5)`                | Отрицательная сторона     | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `triangle.perimeter`                         | `(3, 4, "side")`            | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `triangle.perimeter`                         | `(1e10, 1e10, 1e10)`        | Очень большие числа       | `3e10`                       | `3e10`                | 2024-10-16 | ОК      |
| `circle.area`                                | `(7)`                       | Корректные данные         | `153.94`                     | `153.94`              | 2024-10-16 | ОК      |
| `circle.area`                                | `(-7)`                      | Отрицательный радиус      | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `circle.area`                                | `("radius")`                | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `circle.area`                                | `(1e10)`                    | Очень большое число       | `3.141592653589793e20`       | `3.141592653589793e20` | 2024-10-16 | ОК      |
| `circle.perimeter`                           | `(7)`                       | Корректные данные         | `43.98`                      | `43.98`               | 2024-10-16 | ОК      |
| `circle.perimeter`                           | `(-7)`                      | Отрицательный радиус      | `ValueError`                 | `ValueError`          | 2024-10-16 | ОК      |
| `circle.perimeter`                           | `("radius")`                | Строка вместо числа       | `TypeError`                  | `TypeError`           | 2024-10-16 | ОК      |
| `circle.perimeter`                           | `(1e10)`                    | Очень большое число       | `6.283185307179586e10`       | `6.283185307179586e10` | 2024-10-16 | ОК      |

---

## Заключение
Тесты успешно проверили основные и граничные случаи для всех функций, включая некорректные значения: отрицательные числа, неподходящие типы данных и очень большие числа. Функции реагируют на них в соответствии с ожидаемыми результатами.

# Транспортная задача

Данный проект представляет собой решение транспортной задачи с использованием метода северо-западного угла для начального распределения ресурсов. Код на Python выполняет следующие функции:

- Инициализация транспортного плана с помощью метода северо-западного угла.
- Вычисление общего стоимости перевозки на основе полученного транспортного плана.

## Описание функций

### `north_west_corner_method(cost_matrix, supply, demand)`

Эта функция инициализирует транспортный план по методу северо-западного угла.

**Параметры:**
- `cost_matrix` (numpy.ndarray): матрица издержек, где каждая ячейка содержит стоимость перевозки от источника к пункту назначения.
- `supply` (numpy.ndarray): массив, содержащий величину предложения от каждого источника.
- `demand` (numpy.ndarray): массив, содержащий величину спроса для каждого пункта назначения.

**Возвращает:**
- `transport_plan` (numpy.ndarray): матрица, содержащая количество ресурсов, которые следует перевезти от источников к пунктам назначения.

### `calculate_total_cost(transport_plan, cost_matrix)`

Эта функция вычисляет общую стоимость перевозки по данному транспортному плану.

**Параметры:**
- `transport_plan` (numpy.ndarray): матрица, полученная из функции `north_west_corner_method`, содержащая распределение ресурсов.
- `cost_matrix` (numpy.ndarray): матрица издержек.

**Возвращает:**
- `total_cost` (float): общая стоимость перевозки.

## Установка и использование

1. Убедитесь, что у вас установлен Python и библиотека NumPy.
pip install numpy


2. Скопируйте код в файл (например, `transportation_problem.py`).

3. Импортируйте функции в своём скрипте и задайте необходимые параметры:

   import numpy as np
   from transportation_problem import north_west_corner_method, calculate_total_cost

   # Пример выходных данных
   cost_matrix = np.array([[8, 6, 10], [9, 12, 13], [14, 9, 15]])
   supply = np.array([50, 60, 70])
   demand = np.array([40, 80, 60])

   transport_plan = north_west_corner_method(cost_matrix, supply, demand)
   total_cost = calculate_total_cost(transport_plan, cost_matrix)

   print("Транспортный план:\n", transport_plan)
   print("Общая стоимость перевозки:", total_cost)
Пример
Предположим, у нас есть 3 источника и 3 пункта назначения:
cost_matrix = np.array([[8, 6, 10],
                         [9, 12, 13],
                         [14, 9, 15]])

supply = np.array([50, 60, 70])
demand = np.array([40, 80, 60])

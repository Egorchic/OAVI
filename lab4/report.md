# Лабораторная работа №4. Выделение контуров на изображении

**Вариант:** 8  
**Метод:** Оператор Прюитта 3×3

---

## Используемые методы

### Преобразование в полутон
Исходные цветные изображения переводятся в полутоновые по формуле взвешенного усреднения:

$$Y = 0.299 \cdot R + 0.587 \cdot G + 0.114 \cdot B$$

### Оператор Прюитта 3×3
Ядра для вычисления горизонтальной и вертикальной составляющих градиента:

$$G_x = \begin{bmatrix}
1 & 0 & -1 \\
1 & 0 & -1 \\
1 & 0 & -1
\end{bmatrix}, \quad
G_y = \begin{bmatrix}
1 & 1 & 1 \\
0 & 0 & 0 \\
-1 & -1 & -1
\end{bmatrix}$$

Модуль градиента вычисляется как сумма модулей:

$$|G| = |G_x| + |G_y|$$

### Нормализация
Каждая градиентная матрица линейно растягивается в диапазон [0, 255] для визуализации.

### Бинаризация
Для выделения контуров применяется пороговая обработка: пиксели со значением выше порога становятся белыми, остальные – чёрными. Для каждого изображения приведены результаты бинаризации при порогах 10, 20, 30, 40, 50, 60, 70.

---

## Результаты

### 1. Исходные и полутоновые изображения

| № | Исходное (цветное) | Полутоновое |
|---|--------------------|-------------|
| **text1** | ![text1](imgs/text1_original.png) | ![text1_gray](imgs/text1_gray.png) |
| **text2** | ![text2](imgs/text2_original.png) | ![text2_gray](imgs/text2_gray.png) |
| **text3** | ![text3](imgs/text3_original.png) | ![text3_gray](imgs/text3_gray.png) |
| **text4** | ![text4](imgs/text4_original.png) | ![text4_gray](imgs/text4_gray.png) |
| **text5** | ![text5](imgs/text5_original.png) | ![text5_gray](imgs/text5_gray.png) |

---

### 2. Градиентные матрицы \(G_x\), \(G_y\) и модуль градиента \(G\) (нормализованные)

#### text1
| \(G_x\) | \(G_y\) | \(G\) |
|---------|---------|-------|
| ![text1_Gx](imgs/text1_Gx.png) | ![text1_Gy](imgs/text1_Gy.png) | ![text1_G](imgs/text1_G.png) |

#### text2
| \(G_x\) | \(G_y\) | \(G\) |
|---------|---------|-------|
| ![text2_Gx](imgs/text2_Gx.png) | ![text2_Gy](imgs/text2_Gy.png) | ![text2_G](imgs/text2_G.png) |

#### text3
| \(G_x\) | \(G_y\) | \(G\) |
|---------|---------|-------|
| ![text3_Gx](imgs/text3_Gx.png) | ![text3_Gy](imgs/text3_Gy.png) | ![text3_G](imgs/text3_G.png) |

#### text4
| \(G_x\) | \(G_y\) | \(G\) |
|---------|---------|-------|
| ![text4_Gx](imgs/text4_Gx.png) | ![text4_Gy](imgs/text4_Gy.png) | ![text4_G](imgs/text4_G.png) |

#### text5
| \(G_x\) | \(G_y\) | \(G\) |
|---------|---------|-------|
| ![text5_Gx](imgs/text5_Gx.png) | ![text5_Gy](imgs/text5_Gy.png) | ![text5_G](imgs/text5_G.png) |

---

### 3. Бинаризация модуля градиента \(G\) (различные пороги)

Для каждого изображения показаны результаты бинаризации при порогах 10, 20, 30, 40, 50, 60 и 70.

#### text1

| T=10 | T=20 |
|------|------|
| ![text1_binary_T10](imgs/text1_binary_T10.png) | ![text1_binary_T20](imgs/text1_binary_T20.png) |

| T=30 | T=40 |
|------|------|
| ![text1_binary_T30](imgs/text1_binary_T30.png) | ![text1_binary_T40](imgs/text1_binary_T40.png) |

| T=50 | T=60 |
|------|------|
| ![text1_binary_T50](imgs/text1_binary_T50.png) | ![text1_binary_T60](imgs/text1_binary_T60.png) |

| T=70 |
|------|
| ![text1_binary_T70](imgs/text1_binary_T70.png) |

Итог:

#### text2

| T=10 | T=20 |
|------|------|
| ![text2_binary_T10](imgs/text2_binary_T10.png) | ![text2_binary_T20](imgs/text2_binary_T20.png) |

| T=30 | T=40 |
|------|------|
| ![text2_binary_T30](imgs/text2_binary_T30.png) | ![text2_binary_T40](imgs/text2_binary_T40.png) |

| T=50 | T=60 |
|------|------|
| ![text2_binary_T50](imgs/text2_binary_T50.png) | ![text2_binary_T60](imgs/text2_binary_T60.png) |

| T=70 |
|------|
| ![text2_binary_T70](imgs/text2_binary_T70.png) |

Итог:

#### text3

| T=10 | T=20 |
|------|------|
| ![text3_binary_T10](imgs/text3_binary_T10.png) | ![text3_binary_T20](imgs/text3_binary_T20.png) |

| T=30 | T=40 |
|------|------|
| ![text3_binary_T30](imgs/text3_binary_T30.png) | ![text3_binary_T40](imgs/text3_binary_T40.png) |

| T=50 | T=60 |
|------|------|
| ![text3_binary_T50](imgs/text3_binary_T50.png) | ![text3_binary_T60](imgs/text3_binary_T60.png) |

| T=70 |
|------|
| ![text3_binary_T70](imgs/text3_binary_T70.png) |

Итог:

#### text4

| T=10 | T=20 |
|------|------|
| ![text4_binary_T10](imgs/text4_binary_T10.png) | ![text4_binary_T20](imgs/text4_binary_T20.png) |

| T=30 | T=40 |
|------|------|
| ![text4_binary_T30](imgs/text4_binary_T30.png) | ![text4_binary_T40](imgs/text4_binary_T40.png) |

| T=50 | T=60 |
|------|------|
| ![text4_binary_T50](imgs/text4_binary_T50.png) | ![text4_binary_T60](imgs/text4_binary_T60.png) |

| T=70 |
|------|
| ![text4_binary_T70](imgs/text4_binary_T70.png) |

Итог:

#### text5

| T=10 | T=20 |
|------|------|
| ![text5_binary_T10](imgs/text5_binary_T10.png) | ![text5_binary_T20](imgs/text5_binary_T20.png) |

| T=30 | T=40 |
|------|------|
| ![text5_binary_T30](imgs/text5_binary_T30.png) | ![text5_binary_T40](imgs/text5_binary_T40.png) |

| T=50 | T=60 |
|------|------|
| ![text5_binary_T50](imgs/text5_binary_T50.png) | ![text5_binary_T60](imgs/text5_binary_T60.png) |

| T=70 |
|------|
| ![text5_binary_T70](imgs/text5_binary_T70.png) |

Итог:

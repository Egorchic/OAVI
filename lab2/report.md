# Лабораторная работа №2
## Обесцвечивание и бинаризация растровых изображений

**Вариант:** 8  

---

## Результаты обработки

### 1. Сравнение исходных цветных и полутоновых изображений

Для каждого примера слева показано исходное цветное изображение, справа – полученное полутоновое.

Для каждого исходного цветного изображения выполнялось взвешенное усреднение каналов:

$$Y = 0.299 \cdot R + 0.587 \cdot G + 0.114 \cdot B$$

| **Мультфильм** | |
|:---:|:---:|
| ![cartoon](imgs/cartoon.png) | ![cartoon_gray](imgs/cartoon_gray.png) |

| **Рентгеновский снимок** | |
|:---:|:---:|
| ![xray](imgs/xray.png) | ![xray_gray](imgs/xray_gray.png) |

| **Контурная карта** | |
|:---:|:---:|
| ![map](imgs/map.png) | ![map_gray](imgs/map_gray.png) |

| **Текст (равномерный фон)** | |
|:---:|:---:|
| ![text1](imgs/text1.png) | ![text1_gray](imgs/text1_gray.png) |

| **Текст с неравномерной засветкой** | |
|:---:|:---:|
| ![text2](imgs/text2.png) | ![text2_gray](imgs/text2_gray.png) |

| **Дополнительный пример текста** | |
|:---:|:---:|
| ![text3](imgs/text3.png) | ![text3_gray](imgs/text3_gray.png) |

---

### 2. Сравнение полутоновых и бинаризованных (метод WAN) изображений

Для каждого примера слева приведено полутоновое изображение, справа – результат адаптивной бинаризации методом WAN.

Порог вычисляется по формуле:

$$T_{Singh} = m(x,y) \left( 1 - k \left( \frac{s(x,y)}{1-\delta} - 1 \right) \right)$$

| **Мультфильм** | |
|:---:|:---:|
| ![cartoon_gray](imgs/cartoon_gray.png) | ![cartoon_wan](imgs/cartoon_wan.png) |

| **Рентгеновский снимок** | |
|:---:|:---:|
| ![xray_gray](imgs/xray_gray.png) | ![xray_wan](imgs/xray_wan.png) |

| **Контурная карта** | |
|:---:|:---:|
| ![map_gray](imgs/map_gray.png) | ![map_wan](imgs/map_wan.png) |

| **Текст (равномерный фон)** | |
|:---:|:---:|
| ![text1_gray](imgs/text1_gray.png) | ![text1_wan](imgs/text1_wan.png) |

| **Текст с неравномерной засветкой** | |
|:---:|:---:|
| ![text2_gray](imgs/text2_gray.png) | ![text2_wan](imgs/text2_wan.png) |

| **Дополнительный пример текста** | |
|:---:|:---:|
| ![text3_gray](imgs/text3_gray.png) | ![text3_wan](imgs/text3_wan.png) |


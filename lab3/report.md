# Лабораторная работа №3
## Фильтрация изображений (ранговая фильтрация)


**Вариант:** 8  


---

Фильтрация полутоновых изображений с окном 3×3 и рангом 7/9.

$$ \text{Mask} =
\begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix} $$

### Используемые методы
- **Полутоновое преобразование**: взвешенное усреднение каналов RGB по формуле  
  \( Y = 0.299 R + 0.587 G + 0.114 B \).
- **Ранговая фильтрация**: для каждого пикселя из окна 3×3 выбирается элемент с заданным порядковым номером (рангом). В работе использован ранг 7 (седьмой по величине из 9 значений). Края изображения дополняются отражением.
- **Разностное изображение**: модуль разности между исходным полутоном и отфильтрованным изображением. Для улучшения видимости слабых изменений применяется умножение на 10 с клиппингом до 255.

---

## 1. Исходные цветные и полутоновые изображения

| **text1** | **text1_gray** |
|:---:|:---:|
| ![text1](imgs/text1.png) | ![text1_gray](imgs/text1_gray.png) |

| **text2** | **text2_gray** |
|:---:|:---:|
| ![text2](imgs/text2.png) | ![text2_gray](imgs/text2_gray.png) |

| **text3** | **text3_gray** |
|:---:|:---:|
| ![text3](imgs/text3.png) | ![text3_gray](imgs/text3_gray.png) |

| **text4** | **text4_gray** |
|:---:|:---:|
| ![text4](imgs/text4.png) | ![text4_gray](imgs/text4_gray.png) |

| **text5** | **text5_gray** |
|:---:|:---:|
| ![text5](imgs/text5.png) | ![text5_gray](imgs/text5_gray.png) |

---

## 2. Полутоновые и отфильтрованные (ранг 7/9, окно 3×3)

| **text1_gray** | **text1_filtered** |
|:---:|:---:|
| ![text1_gray](imgs/text1_gray.png) | ![text1_filtered](imgs/text1_filtered.png) |

| **text2_gray** | **text2_filtered** |
|:---:|:---:|
| ![text2_gray](imgs/text2_gray.png) | ![text2_filtered](imgs/text2_filtered.png) |

| **text3_gray** | **text3_filtered** |
|:---:|:---:|
| ![text3_gray](imgs/text3_gray.png) | ![text3_filtered](imgs/text3_filtered.png) |

| **text4_gray** | **text4_filtered** |
|:---:|:---:|
| ![text4_gray](imgs/text4_gray.png) | ![text4_filtered](imgs/text4_filtered.png) |

| **text5_gray** | **text5_filtered** |
|:---:|:---:|
| ![text5_gray](imgs/text5_gray.png) | ![text5_filtered](imgs/text5_filtered.png) |

---

## 3. Разностные изображения (модуль разности) и их контрастированные версии (×10)

| **text1_diff** | **text1_diff_x10** |
|:---:|:---:|
| ![text1_diff](imgs/text1_diff.png) | ![text1_diff_x10](imgs/text1_diff_x10.png) |

| **text2_diff** | **text2_diff_x10** |
|:---:|:---:|
| ![text2_diff](imgs/text2_diff.png) | ![text2_diff_x10](imgs/text2_diff_x10.png) |

| **text3_diff** | **text3_diff_x10** |
|:---:|:---:|
| ![text3_diff](imgs/text3_diff.png) | ![text3_diff_x10](imgs/text3_diff_x10.png) |

| **text4_diff** | **text4_diff_x10** |
|:---:|:---:|
| ![text4_diff](imgs/text4_diff.png) | ![text4_diff_x10](imgs/text4_diff_x10.png) |

| **text5_diff** | **text5_diff_x10** |
|:---:|:---:|
| ![text5_diff](imgs/text5_diff.png) | ![text5_diff_x10](imgs/text5_diff_x10.png) |
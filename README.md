# INFORME SOBRE LA INTERPOLACIÓN DE NEWTON Y LAGRANGE PARA LA ESTIMACIÓN DE POBLACIÓN

## 1. Introducción

La interpolación es una técnica fundamental en el análisis de datos que permite estimar valores intermedios a partir de un conjunto discreto de datos conocidos. En el contexto del crecimiento poblacional, es esencial para proyectar cifras futuras basadas en datos históricos. Este informe se centra en la estimación de la población para el año 2024 utilizando dos métodos de interpolación: **Interpolación de Newton** e **Interpolación de Lagrange**. Ambos métodos son herramientas matemáticas útiles para realizar predicciones y extrapolaciones.

## 2. Objetivo General

Estimar la población para el año 2024 utilizando los métodos de interpolación de Newton e interpolación de Lagrange basados en los datos históricos de población entre los años 1882 y 2012.

## 3. Objetivos Específicos

- Aplicar el método de interpolación de **Lagrange** para obtener una estimación de la población en el año 2024.
- Aplicar el método de interpolación de **Newton** para estimar la población para el mismo año.
- Comparar las estimaciones obtenidas con el valor real de la población en 2024.
- Calcular el error absoluto y relativo con respecto a la población conocida en 2024.

---

## 4. Marco Teórico

### 4.1 Interpolación

La interpolación es un método utilizado para estimar valores intermedios en un conjunto de datos discretos. Se construye un polinomio que pasa por los puntos conocidos, permitiendo predecir valores en otros puntos. Los métodos más comunes son la **Interpolación de Newton** y la **Interpolación de Lagrange**.

### 4.2 Interpolación de Newton

El polinomio de interpolación de Newton se basa en las **diferencias divididas**, que se utilizan para construir un polinomio que pasa por todos los puntos de datos conocidos. El polinomio se expresa como:


![alt tag](https://github.com/javihen/PoblacionDeBolivia/blob/main/img/1.png)

### 4.3 Interpolación de Lagrange

El método de interpolación de Lagrange utiliza una combinación de polinomios basados en todos los puntos de datos. El polinomio de Lagrange es:

![alt tag](https://github.com/javihen/PoblacionDeBolivia/blob/main/img/2.png)

donde cada \(L_i(x)\) es un polinomio que depende de los puntos conocidos.

---

## 5. Aplicación

### 5.1 Datos Proporcionados

Los datos de población entre 1882 y 2012 son:

| Año (\(x_i\)) | Población (\(y_i\)) |
|---|---|
| 1882 | 1,172,156 |
| 1900 | 1,766,451 |
| 1950 | 2,704,165 |
| 1976 | 4,613,419 |
| 1992 | 6,420,792 |
| 2001 | 8,274,325 |
| 2012 | 10,059,856 |

### 5.2 Interpolación de Lagrange

**Cálculo:**

Utilizando la fórmula de Lagrange, el polinomio de interpolación se expresa como:

![alt tag](https://github.com/javihen/PoblacionDeBolivia/blob/main/img/2.png)

Los términos \(L_i(x)\) se calculan para \(i = 0, 1, \dots, 6\), y finalmente se evalúa en \(x = 2024\). 

**Resultado:**

La estimación de la población para el año **2024** utilizando el método de Lagrange es:

![alt tag](https://github.com/javihen/PoblacionDeBolivia/blob/main/img/2.png)
---

### 5.3 Interpolación de Newton

**Cálculo:**

Para calcular el polinomio de Newton, primero se determinan las diferencias divididas. La fórmula de las diferencias divididas se usa para obtener el polinomio de interpolación:

\[
P(x) = f[x_0] + f[x_0, x_1](x - x_0) + f[x_0, x_1, x_2](x - x_0)(x - x_1) + \dots
\]

Evaluando en \(x = 2024\) se obtiene:

![alt tag](https://github.com/javihen/PoblacionDeBolivia/blob/main/img/3.png)

---

### 5.4 Cálculo del Error

Se nos dio el valor real de la población en 2024 como **11,312,320 habitantes**. Para calcular el error entre la estimación y el valor real:

- **Error Absoluto:**

![alt tag](https://github.com/javihen/PoblacionDeBolivia/blob/main/img/4.png)

- **Error Relativo:**

![alt tag](https://github.com/javihen/PoblacionDeBolivia/blob/main/img/5.png)

---

## 6. Conclusiones

1. **Estimaciones Equivalentes**: Tanto la **Interpolación de Newton** como la **Interpolación de Lagrange** produjeron la misma estimación de población para 2024, que fue **6,108,122 habitantes**.

2. **Precisión y Limitaciones**: Ambas estimaciones subestiman la población real en un **45.99%**, lo que sugiere que los métodos de interpolación polinómica pueden no capturar adecuadamente la dinámica del crecimiento poblacional a largo plazo.

3. **Uso de Métodos Alternativos**: La interpolación es útil para estimar valores intermedios, pero su efectividad puede disminuir al extrapolar, sugiriendo que se podrían considerar métodos adicionales, como modelos de regresión, para obtener estimaciones más precisas.

4. **Relevancia en la Toma de Decisiones**: Estos métodos son fundamentales en diversas áreas, como la demografía, economía y ciencias aplicadas, donde las proyecciones precisas son cruciales para la planificación y toma de decisiones.

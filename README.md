# Análisis de Datos con NumPy y Pandas en Python

¡Hola a todos! 👋 Bienvenidos a este espacio donde exploraremos el fascinante mundo del análisis de datos. Si estás buscando sumergirte en este campo o simplemente quieres potenciar tus habilidades, has llegado al lugar correcto. Hoy hablaremos de tres herramientas esenciales en Python que todo analista de datos debe dominar: **Pandas, NumPy y Matplotlib**. 

### ¿Por qué son importantes estas herramientas?

En la era digital, las empresas generan enormes volúmenes de datos cada día. Ya sea para mejorar recomendaciones de contenido, analizar patrones de visualización o optimizar estrategias, procesar y entender esta información es clave. Aquí es donde entran en juego nuestras poderosas aliadas: **Pandas, NumPy y Matplotlib**.

---

### 🔢 NumPy: La base de todo

**NumPy** es una librería fundamental para el manejo de operaciones matemáticas y estadísticas en grandes conjuntos de datos. Si trabajas con datos a gran escala, NumPy te ofrece:

- **Velocidad y eficiencia**: Sus operaciones vectorizadas son mucho más rápidas que las listas tradicionales de Python.
- **Manejo de arrays multidimensionales**: Ideal para manipular y transformar datos complejos de manera sencilla.

---

### 🐼 Pandas: Manipulación de datos con estilo

**Pandas**, construida sobre NumPy, simplifica el trabajo con datos tabulares (como hojas de cálculo o bases de datos). Entre sus ventajas destacan:

- **Manipulación intuitiva**: Filtrado, agrupación y pivotación de datos con pocas líneas de código.
- **Análisis profundo**: Sus estructuras de datos, como los `DataFrames`, permiten explorar y entender la información para tomar decisiones basadas en hechos.

Dominar Pandas no solo optimiza tu flujo de trabajo, sino que también abre puertas en áreas como *business intelligence*, *machine learning* y *ciencia de datos*.

---

### 📊 Matplotlib: Visualización efectiva

Una vez procesados y analizados los datos, es crucial comunicar los resultados de manera clara y atractiva. **Matplotlib** es la librería por excelencia para crear visualizaciones profesionales:

- **Gráficos personalizables**: Desde simples líneas hasta complejos gráficos de dispersión.
- **Integración con Pandas y NumPy**: Genera visualizaciones directamente desde tus DataFrames o arrays.

---

### 🚀 Proyecto práctico: Análisis de ventas online

A lo largo de este blog (y futuras entradas), desarrollaremos un proyecto realista: analizaremos información de ventas de una tienda online. Este ejercicio te permitirá:

- Manipular y limpiar grandes conjuntos de datos.
- Realizar análisis estadísticos detallados.
- Automatizar tareas repetitivas.
- Visualizar resultados de manera impactante.

¡Perfecto para agregar a tu portafolio profesional!

---

### ⚙️ Configuración inicial

Para seguir el curso, puedes usar entornos como **Google Colab** o **Visual Studio Code**. Primero, instala las librerías:

```python
# Instalación de las librerías
!pip install numpy pandas matplotlib
```

Luego, impórtalas en tu código:

```python
# Importación estándar
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```
---

# Manipulación de Dimensiones en Arrays NumPy

Hoy vamos a profundizar en uno de los conceptos más fundamentales para cualquier científico de datos: **la manipulación de dimensiones en arrays NumPy**.

## ¿Por qué son cruciales las dimensiones en el análisis de datos?

Las dimensiones en NumPy transforman completamente cómo trabajamos con información. Dominar este concepto nos permite abordar problemas complejos con mayor eficiencia y precisión, desde simples análisis estadísticos hasta proyectos avanzados de machine learning.

### 🔢 Empezando por lo básico: El escalar

Un escalar en NumPy es nuestro punto de partida: un valor único representado como dimensión cero. Imagina que queremos registrar la temperatura de un día específico:

```python
import numpy as np

temperatura_dia = np.array(42)
print(f"Temperatura: {temperatura_dia}°")
print(f"Tipo de dato: {type(temperatura_dia)}")
```

### 📈 Avanzando a una dimensión: Los vectores

Cuando necesitamos analizar datos a lo largo del tiempo, como las temperaturas de toda una semana, utilizamos vectores (arrays unidimensionales):

```python
temperaturas_semana = np.array([30, 29, 42, 35, 33, 36, 42])
print("Temperatura por día de la semana:")
print(temperaturas_semana)
```

### 🧮 Trabajando con dos dimensiones: Matrices

Las matrices nos permiten organizar datos en filas y columnas, perfectas para representar información tabular:

```python
# Matriz de ventas mensuales por producto
ventas_trimestrales = np.array([
    [150, 200, 175],  # Producto A
    [300, 250, 275],  # Producto B
    [100, 150, 125]   # Producto C
])

print("Ventas trimestrales por producto:")
print(ventas_trimestrales)
```

### 🎯 Explorando múltiples dimensiones: Tensores

Para datos más complejos, como imágenes con canales de color, utilizamos tensores:

```python
# Tensor representando una pequeña imagen RGB (2x2 píxeles)
imagen_miniatura = np.array([
    [[255, 0, 0], [0, 255, 0]],    # Rojos y verdes
    [[0, 0, 255], [255, 255, 255]] # Azules y blanco
])

print("Tensor de imagen RGB:")
print(imagen_miniatura)
```

## 🛠️ Creación avanzada de arrays en NumPy

NumPy ofrece múltiples formas de crear arrays adaptados a necesidades específicas:

```python
# Crear un rango de valores
secuencia = np.arange(15)
print(f"Secuencia: {secuencia}")

# Matriz identidad
matriz_identidad = np.eye(4)
print("Matriz identidad 4x4:")
print(matriz_identidad)

# Matriz diagonal
diagonal_especial = np.diag([1, 2, 3, 4])
print("Matriz diagonal:")
print(diagonal_especial)

# Valores aleatorios
numeros_aleatorios = np.random.rand(3, 2)
print("Matriz 3x2 con valores aleatorios:")
print(numeros_aleatorios)
```

## 💡 Aplicaciones prácticas en ciencia de datos

Estas estructuras dimensionales son fundamentales para:

- **Procesamiento de imágenes**: Los tensores manejan dimensiones de altura, ancho y canales de color
- **Series temporales**: Los vectores son ideales para datos secuenciales
- **Análisis tabular**: Las matrices representan perfectamente hojas de cálculo
- **Aprendizaje profundo**: Los tensores de alta dimensión son el corazón de las redes neuronales


**Recuerda**: La práctica hace al maestro. Te recomiendo experimentar con estos ejemplos y familiarizarte con las diferentes formas de crear y manipular arrays NumPy.


---

# Creación y Manipulación de Arrays en NumPy
En nuestra entrega anterior exploramos las dimensiones en NumPy, desde escalares hasta tensores. Hoy profundizaremos en los métodos de creación de arrays y el manejo de tipos de datos, aspectos fundamentales para un análisis de datos eficiente.

## 🛠️ Métodos de Creación de Arrays

### 1. Desde Estructuras de Python
La forma más directa de crear arrays es a partir de listas existentes:

```python
import numpy as np

# Array unidimensional desde lista simple
array_1d = np.array([1, 2, 3, 4, 5])
print("Array 1D:", array_1d)

# Array bidimensional desde lista de listas
array_2d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print("\nArray 2D:")
print(array_2d)
```

### 2. Funciones Predefinidas para Creación Rápida
NumPy ofrece funciones especializadas para crear arrays con patrones específicos:

```python
# Array de ceros
zeros = np.zeros((3, 3))
print("Matriz de ceros 3x3:")
print(zeros)

# Array de unos
ones = np.ones((2, 4))
print("\nMatriz de unos 2x4:")
print(ones)

# Secuencia con paso definido
rango = np.arange(0, 20, 5)  # Inicio, fin, paso
print("\nSecuencia con paso 5:", rango)

# Valores equidistantes
lineal = np.linspace(0, 1, 5)  # Inicio, fin, número de elementos
print("\n5 valores entre 0 y 1:", lineal)
```

## 📊 Especificación de Tipos de Datos

El control de tipos de datos es crucial para optimizar memoria y precisión en cálculos numéricos:

```python
# Diferentes tipos de datos
enteros_32 = np.array([1, 2, 3], dtype='int32')
flotantes_32 = np.array([1.5, 2.8, 3.1], dtype='float32')
booleanos = np.array([True, False, True], dtype='bool')
complejos = np.array([1+2j, 3+4j], dtype='complex64')
texto = np.array(['python', 'numpy', 'data'], dtype='str')

print("Enteros 32-bit:", enteros_32.dtype)
print("Flotantes 32-bit:", flotantes_32.dtype)
print("Booleanos:", booleanos.dtype)
print("Complejos:", complejos.dtype)
print("Texto:", texto.dtype)
```

## ⚠️ Manejo de Valores NaN

Los valores NaN (Not a Number) son esenciales para trabajar con datos faltantes o indefinidos:

```python
# Array con valores NaN
datos_con_nan = np.array([3.2, 5.1, np.nan, 8.7, np.nan, 10.2])
print("Array original:", datos_con_nan)

# Detección de valores NaN
mask_nan = np.isnan(datos_con_nan)
print("Posiciones con NaN:", mask_nan)

# Filtrando valores NaN
datos_limpios = datos_con_nan[~mask_nan]
print("Datos limpios:", datos_limpios)
```

## 💡 Aplicaciones Prácticas

Estas técnicas de creación y manipulación de arrays son fundamentales para:

- **Preprocesamiento de datos**: Limpieza y transformación inicial
- **Optimización de memoria**: Elección adecuada de tipos de datos
- **Manejo de datos faltantes**: Identificación y tratamiento de valores NaN
- **Preparación para machine learning**: Creación de datasets estructurados

## 🔄 Conversión entre Tipos de Datos

```python
# Conversión entre tipos
enteros = np.array([1, 2, 3, 4])
flotantes = enteros.astype('float64')
print("Enteros:", enteros.dtype)
print("Convertido a flotantes:", flotantes.dtype)
```


**Tip profesional**: Siempre verifica el tipo de datos de tus arrays con `.dtype` para asegurar la precisión en tus cálculos.


---

cc

# 4. Álgebra Lineal Aplicada con NumPy

En entradas anteriores exploramos la creación y manipulación de arrays en NumPy. Hoy daremos un paso crucial: **el álgebra lineal aplicada**, una herramienta fundamental para cualquier científico de datos que quiera llevar sus análisis al siguiente nivel.

## 🧮 ¿Por qué el Álgebra Lineal es Esencial?

El álgebra lineal es el lenguaje matemático detrás de:
- **Machine learning**: Redes neuronales y algoritmos de optimización
- **Procesamiento de imágenes**: Transformaciones y filtros
- **Análisis de datos**: Regresiones y descomposiciones
- **Gráficos por computadora**: Rotaciones y escalamientos 3D

## 🔢 Operaciones Fundamentales con NumPy

### Suma de Matrices

La suma se realiza elemento por elemento:

$$
A = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix}, \quad
B = \begin{pmatrix}
5 & 6 \\
7 & 8 \\
\end{pmatrix}
$$

$$
A + B = \begin{pmatrix}
1+5 & 2+6 \\
3+7 & 4+8 \\
\end{pmatrix} = \begin{pmatrix}
6 & 8 \\
10 & 12 \\
\end{pmatrix}
$$

```python
import numpy as np

A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

suma = A + B
print("Suma de matrices:\n", suma)
```

### Multiplicación de Matrices: Entendiendo la Diferencia

#### Producto Hadamard (Elemento por Elemento)

$$
A \odot B = \begin{pmatrix}
1×5 & 2×6 \\
3×7 & 4×8 \\
\end{pmatrix} = \begin{pmatrix}
5 & 12 \\
21 & 32 \\
\end{pmatrix}
$$

```python
# Producto Hadamard (elemento por elemento)
hadamard = A * B
print("Producto Hadamard:\n", hadamard)
```

#### Producto Matricial Tradicional

$$
A \cdot B = \begin{pmatrix}
1×5 + 2×7 & 1×6 + 2×8 \\
3×5 + 4×7 & 3×6 + 4×8 \\
\end{pmatrix} = \begin{pmatrix}
19 & 22 \\
43 & 50 \\
\end{pmatrix}
$$

```python
# Producto matricial tradicional
matricial = A @ B  # Equivalente a np.dot(A, B)
print("Producto matricial:\n", matricial)
```

### Transposición de Matrices

Intercambio de filas por columnas:

$$
A^T = \begin{pmatrix}
1 & 3 \\
2 & 4 \\
\end{pmatrix}
$$

```python
A_transpuesta = A.T
print("Transpuesta de A:\n", A_transpuesta)
```

## 🎯 Operaciones Avanzadas para Ciencia de Datos

### Determinante de una Matriz

El determinante proporciona información sobre la transformación lineal:

$$
det(A) = (1×4) - (2×3) = 4 - 6 = -2
$$

```python
determinante = np.linalg.det(A)
print(f"Determinante de A: {determinante:.2f}")
```

### Matriz Inversa

La matriz inversa $A^{-1}$ satisface $A \cdot A^{-1} = I$, donde $I$ es la matriz identidad:

$$
A^{-1} = \frac{1}{det(A)} \cdot \begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix} = \frac{1}{-2} \cdot \begin{pmatrix}
4 & -2 \\
-3 & 1 \\
\end{pmatrix} = \begin{pmatrix}
-2 & 1 \\
1.5 & -0.5 \\
\end{pmatrix}
$$

```python
inversa = np.linalg.inv(A)
print("Inversa de A:\n", inversa)

# Verificación: A * A⁻¹ debería ser la identidad
identidad = A @ inversa
print("Verificación (A * A⁻¹):\n", identidad.round(2))
```

### Valores y Vectores Propios

Fundamentales para reducción de dimensionalidad (PCA) y análisis de sistemas:

$$
A \cdot \vec{v} = \lambda \cdot \vec{v}
$$

Donde $\lambda$ son los valores propios y $\vec{v}$ los vectores propios.

```python
valores, vectores = np.linalg.eig(A)
print("Valores propios:\n", valores)
print("Vectores propios:\n", vectores)
```

## 🧩 Resolución de Sistemas de Ecuaciones

Para resolver sistemas de la forma $AX = B$:

```python
# Sistema: 1x + 2y = 5, 3x + 4y = 6
A = np.array([[1, 2], [3, 4]])
B = np.array([5, 6])

solucion = np.linalg.solve(A, B)
print(f"Solución del sistema: x = {solucion[0]:.2f}, y = {solucion[1]:.2f}")
```

## 💡 Aplicaciones Prácticas en Data Science

1. **Regresión lineal**: Resolución de sistemas para encontrar coeficientes óptimos
2. **Análisis de componentes principales (PCA)**: Descomposición en valores propios
3. **Procesamiento de imágenes**: Transformaciones afines usando matrices
4. **Recomendaciones**: Descomposición SVD para sistemas de recomendación

```python
# Ejemplo: Regresión lineal múltiple
# X @ coeficientes = y
X = np.array([[1, 2], [1, 3], [1, 4]])  # Con columna de unos para intercepto
y = np.array([3, 5, 7])

coeficientes = np.linalg.inv(X.T @ X) @ X.T @ y
print("Coeficientes de regresión:", coeficientes)
```


**Recuerda**: La práctica constante es clave. Te recomiendo experimentar con estas operaciones usando datasets reales para solidificar tu comprensión.
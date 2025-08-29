# Álgebra Lineal Aplicada con NumPy

El álgebra lineal es una rama fundamental de las matemáticas que se centra en el estudio de los vectores, las matrices y las transformaciones lineales. NumPy proporciona herramientas para resolver sistemas de ecuaciones lineales, realizar transformaciones geométricas y modelar problemas en diversas áreas de la ciencia y la ingeniería. Su aplicación es tan amplia que se encuentra en el corazón de múltiples disciplinas científicas y tecnológicas, facilitando desde la simulación de fenómenos físicos hasta la optimización de sistemas complejos.

Los vectores y las matrices, los bloques de construcción del álgebra lineal, nos permiten representar y manipular datos de manera eficiente, un vector puede representar una lista de valores que podrían ser coordenadas espaciales, mientras que una matriz puede representar una transformación que afecta a estos vectores. Las operaciones básicas del álgebra lineal, como la suma, la multiplicación y la transposición de matrices, forman la base de muchas técnicas avanzadas en la física, la ingeniería, la economía y la informática.

Conceptos básicos de álgebra lineal

- Vectores: Son objetos que tienen magnitud y dirección. Se pueden representar como una lista de números, que son las coordenadas del vector.
- Matrices: Son arreglos bidimensionales de números que representan transformaciones lineales. Una matriz puede transformar un vector en otro vector.
- Transformaciones Lineales: Son funciones que toman vectores como entrada y producen otros vectores como salida, respetando las operaciones de suma y multiplicación por un escalar.
- Espacios Vectoriales: Conjuntos de vectores que pueden sumarse entre sí y multiplicarse por escalares, siguiendo ciertas reglas.


Ejemplos aplicativos

- Gráficos por Computadora: Las transformaciones lineales se utilizan para rotar, escalar y traducir objetos en la pantalla.
- Procesamiento de Imágenes: Las matrices de convolución (kernels) se usan para aplicar filtros a las imágenes, mejorando su calidad o destacando características específicas.
- Aprendizaje Automático: Los algoritmos de regresión lineal, redes neuronales y otros modelos dependen en gran medida de las operaciones matriciales.


Operaciones principales en álgebra lineal
Vamos a ver algunas de las operaciones más comunes en álgebra lineal utilizando matrices.

Suma de matrices

La suma de matrices se realiza elemento por elemento. Por ejemplo, si tenemos dos matrices A y B:

**Matriz A:**
$$
A = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix}
$$

**Matriz B:**
$$
B = \begin{pmatrix}
5 & 6 \\
7 & 8 \\
\end{pmatrix}
$$

**Suma de matrices (A + B):**
$$
A + B = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix} + \begin{pmatrix}
5 & 6 \\
7 & 8 \\
\end{pmatrix} = \begin{pmatrix}
1+5 & 2+6 \\
3+7 & 4+8 \\
\end{pmatrix} = \begin{pmatrix}
6 & 8 \\
10 & 12 \\
\end{pmatrix}
$$


Código en NumPy para la suma de matrices:

```python
import numpy as np

A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

suma = A + B
print("Suma de matrices:\n", suma)
```

Multiplicación de matrices

La multiplicación de matrices combina filas de una matriz con columnas de otra. Por ejemplo, si tenemos las mismas matrices A y B:

**Producto elemento por elemento (A ⊙ B):**
$$
A \odot B = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix} \odot \begin{pmatrix}
5 & 6 \\
7 & 8 \\
\end{pmatrix} = \begin{pmatrix}
1×5 & 2×6 \\
3×7 & 4×8 \\
\end{pmatrix} = \begin{pmatrix}
5 & 12 \\
21 & 32 \\
\end{pmatrix}
$$

*Nota: El símbolo ⊙ representa el producto Hadamard (elemento por elemento), diferente al producto matricial tradicional.*


### Explicación de la Notación del Producto Hadamard (⊙)

#### Diferencia entre Producto Hadamard y Producto Matricial Tradicional

##### Producto Matricial Tradicional (1·3 o 1×3)
El símbolo `·` o `×` se reserva tradicionalmente para el **producto matricial** (también llamado producto punto en contextos específicos), que sigue reglas específicas:

$$
A \cdot B = \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix} \cdot \begin{pmatrix}
e & f \\
g & h \\
\end{pmatrix} = \begin{pmatrix}
ae + bg & af + bh \\
ce + dg & cf + dh \\
\end{pmatrix}
$$

### Producto Hadamard (⊙)
El símbolo `⊙` se utiliza específicamente para el **producto elemento por elemento** (también conocido como producto Hadamard), donde:

$$
A \odot B = \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix} \odot \begin{pmatrix}
e & f \\
g & h \\
\end{pmatrix} = \begin{pmatrix}
a \times e & b \times f \\
c \times g & d \times h \\
\end{pmatrix}
$$

## ¿Por qué no usar el mismo símbolo?

1. **Operaciones diferentes**: Son operaciones matemáticamente distintas con reglas y aplicaciones diferentes.

2. **Propiedades diferentes**:
   - El producto matricial no es conmutativo: A·B ≠ B·A
   - El producto Hadamard sí es conmutativo: A⊙B = B⊙A

3. **Contextos de uso distintos**:
   - El producto matricial se usa en transformaciones lineales
   - El producto Hadamard se usa en procesamiento de señales y álgebra de matrices elemento-wise

## En programación (NumPy)
```python
# Producto Hadamard (elemento por elemento)
A * B

# Producto matricial tradicional
A @ B  # o np.dot(A, B)
```

La notación matemática diferenciada ayuda a evitar confusiones entre estas dos operaciones fundamentalmente distintas.

Código en NumPy para la multiplicación de matrices:

```python
producto = np.dot(A, B)
print("Producto de matrices:\n", producto)
```

Transposición de Matrices

La transposición de una matriz intercambia sus filas y columnas. Por ejemplo, la transposición de la matriz A es:

**Matriz Original A**
$$
A = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix}
$$

**Transposición de Matriz (Aᵀ)**



$$
A^T = \begin{pmatrix}
1 & 3 \\
2 & 4 \\
\end{pmatrix}
$$

**En código NumPy:**
```python
import numpy as np

A = np.array([[1, 2], [3, 4]])
A_transpuesta = A.T
print("A transpuesta:\n", A_transpuesta)
```

Determinante de una matriz

El determinante es un valor único que puede calcularse a partir de una matriz cuadrada. Por ejemplo, el determinante de la matriz AAA es:


**Determinante**
$$
A = \begin{pmatrix}
1&2 \\
2&4 \\
\end{pmatrix}
$$

El determinante de A, denotado como det(A),se calcula como:

$$
det(A)=(1·4)-(2·3)= 4-6=-2
$$


Código en NumPy para el determinante de una matriz:

```python
determinante = np.linalg.det(A)
print("Determinante de A:", determinante)
```

Más operaciones de álgebra lineal con NumPy

NumPy ofrece una variedad de funciones que facilitan el trabajo con álgebra lineal. Aquí hay algunas más:

**Inversa de una matriz**

La matriz inversa de A:

La matriz inversa de A es una matriz A^-1 tal que A·A^-1=I, donde I es la matriz identidad  

```python
inversa = np.linalg.inv(A)
print("Inversa de A:\n", inversa)
```

Valores y vectores propios

Los valores propios y los vectores propios son fundamentales en muchas aplicaciones, como en la compresión de datos y el análisis de sistemas dinámicos.

```python
valores_propios, vectores_propios = np.linalg.eig(A)
print("Valores propios de A:\n", valores_propios)
print("Vectores propios de A:\n", vectores_propios)
```

Resolución de sistemas de ecuaciones lineales

Para resolver un sistema de ecuaciones lineales AX=BAX = BAX=B:

```python
B = np.array([1, 2])
X = np.linalg.solve(A, B)
print("Solución del sistema AX = B:\n", X)
```

NumPy es una herramienta poderosa para manejar cálculos numéricos y operaciones de álgebra lineal en Python. Su eficiencia y facilidad de uso la convierten en una biblioteca indispensable para científicos de datos, ingenieros y desarrolladores. Desde la creación de arrays hasta la manipulación de imágenes, NumPy abre un mundo de posibilidades en diversas aplicaciones del mundo real.
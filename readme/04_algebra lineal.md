# Álgebra Lineal Aplicada con NumPy: Potenciando tu Análisis de Datos

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
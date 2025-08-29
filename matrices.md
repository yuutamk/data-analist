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

## Operaciones entre Matrices

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

---

# Transposición de Matriz

## Matriz Original A
$$
A = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix}
$$

## Transposición de Matriz (Aᵀ)
La matriz transpuesta se obtiene intercambiando filas por columnas:

$$
A^T = \begin{pmatrix}
1 & 3 \\
2 & 4 \\
\end{pmatrix}
$$

### Explicación:
- La primera fila de A (1, 2) se convierte en la primera columna de Aᵀ
- La segunda fila de A (3, 4) se convierte en la segunda columna de Aᵀ

**En código NumPy:**
```python
import numpy as np

A = np.array([[1, 2], [3, 4]])
A_transpuesta = A.T
print("A transpuesta:\n", A_transpuesta)
```

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


La matriz inversa de A es una matriz A^-1 tal que A·A^-1=I, donde I es la matriz identidad 

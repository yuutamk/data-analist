# Manipulación de Arrays NumPy 

Métodos de creación de Arrays de NumPy
NumPy proporciona diversas maneras de crear arrays, facilitando la realización de cálculos numéricos y análisis de datos de manera eficiente en Python.

1. Creación de Arrays a partir de Listas
Podemos crear un array a partir de una lista o una lista de listas:

import numpy as np

# Array unidimensional
array_1d = np.array([1, 2, 3, 4])

# Array bidimensional
array_2d = np.array([[1, 2, 3], [4, 5, 6]])
2. Creación de Arrays con Funciones Predefinidas
NumPy proporciona funciones predefinidas para crear arrays de manera más rápida y conveniente:

np.zeros(): Crea un array lleno de ceros.


zeros_array = np.zeros((3, 3))

np.ones(): Crea un array lleno de unos.


ones_array = np.ones((2, 4))

np.arange(): Crea un array con una secuencia de números.

range_array = np.arange(0, 10, 2)  # [0, 2, 4, 6, 8]

np.linspace(): Crea un array con números igualmente espaciados.

linspace_array = np.linspace(0, 1, 5)  # [0., 0.25, 0.5, 0.75, 1.]

3. Especificando Tipos de Datos (Datatypes)
Al crear un array, podemos especificar el tipo de datos que contendrá utilizando el parámetro dtype. Esta especificación es crucial para la eficiencia y precisión en cálculos numéricos. Aquí se detallan algunos de los tipos de datos más comunes:

int32: Entero de 32 bits.
float32: Número de punto flotante de 32 bits.
float64: Número de punto flotante de 64 bits (por defecto para números flotantes en NumPy).
bool: Valores booleanos (True o False).
complex64: Número complejo de 64 bits.
complex128: Número complejo de 128 bits.
str: Cadenas de texto.
Podemos especificar estos tipos de datos al crear el array utilizando el parámetro dtype:

pythonCopiar código
# Array de enteros
int_array = np.array([1, 2, 3], dtype='int32')

# Array de flotantes
float_array = np.array([1.0, 2.0, 3.0], dtype='float32')

# Array de booleanos
bool_array = np.array([True, False, True], dtype='bool')

# Array de números complejos
complex_array = np.array([1+2j, 3+4j], dtype='complex64')

# Array de cadenas de texto
str_array = np.array(['a', 'b', 'c'], dtype='str')

Algunos de estos tipos también pueden ser especificados con abreviaturas en el parámetro dtype. Por ejemplo, 'd' es equivalente a float64, que es el tipo de datos de punto flotante de 64 bits en NumPy:

# Creando un array con dtype 'd' (equivalente a float64)
array_float64 = np.array([1, 2, 3], dtype='d')
print(array_float64)

4. NaN (Not a Number)
NaN es un valor especial utilizado para representar datos que no son números, especialmente en el contexto de operaciones matemáticas que no tienen un resultado definido. Por ejemplo, la división de cero por cero (0/0) o la raíz cuadrada de un número negativo.

nan_array = np.array([1, 2, np.nan, 4])
print(nan_array)

El valor NaN es muy útil para manejar datos faltantes o resultados indefinidos en cálculos numéricos.
# Creación y Manipulación de Arrays en NumPy: Guía Práctica

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
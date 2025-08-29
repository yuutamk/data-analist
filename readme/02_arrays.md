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

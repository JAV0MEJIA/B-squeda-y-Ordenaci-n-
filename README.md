# B-squeda-y-Ordenaci-n-
Búsqueda y Ordenación en Arreglos Multidimensionales

# ordenacion de arreglo dimencional
def bubble_sort(row):
    n = len(row)
    for i in range(n):
        # Últimos i elementos ya están en su lugar correcto
        for j in range(0, n-i-1):
            # Intercambiar si el elemento encontrado es mayor que el siguiente elemento
            if row[j] > row[j+1]:
                row[j], row[j+1] = row[j+1], row[j]

def ordenar_fila_matriz(matriz, indice_fila):
    # Copiar la fila específica para no modificar la matriz original
    fila = matriz[indice_fila].copy()
    bubble_sort(fila)
    matriz_ordenada = matriz.copy()
    matriz_ordenada[indice_fila] = fila
    return matriz_ordenada

def imprimir_matriz(matriz):
    for fila in matriz:
        print(fila)

# Matriz original de ejemplo 3x3
matriz = [
    [3, 1, 8],
    [5, 2, 7],
    [4, 9, 6]
]

# Mostrar la matriz original
print("Matriz original:")
imprimir_matriz(matriz)

# Ordenar la fila 1 (índice 0 en Python) utilizando bubble sort
indice_fila_a_ordenar = 1
matriz_ordenada = ordenar_fila_matriz(matriz, indice_fila_a_ordenar)

# Mostrar la matriz con la fila ordenada
print("\nMatriz con la fila", indice_fila_a_ordenar, "ordenada:")
imprimir_matriz(matriz_ordenada)

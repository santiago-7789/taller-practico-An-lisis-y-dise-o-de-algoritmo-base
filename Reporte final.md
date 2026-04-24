# Reporte Final - Taller de Algoritmos

## Resumen Ejecutivo
En la clase y en este taller aprendimos conceptos fundamentales como son la búsqueda binaria y lineal, generalmente la búsqueda binaria es la mejor opción en la mayoria de casos cuando hay muchos elementos, así automatizando el tiempo de una manera más eficiente, tambien de las colas FIFO, siendo muy importante para sistemas de impresoras, pools de conexiones, simulación de eventos, etc.

## Actividad 1: Búsqueda Binaria
- Funcionamiento: La búsqueda binaria es fundamental para reducir la cantidad de operaciones, con solamente pocas comparaciones, siendo algo más eficiente para el sistema con la reducción de comparaciones.
- Complejidad: O(log n)
- Test Cases
test case 1: ![alt text](<Captura de pantalla 2026-04-23 132859.png>)
test case 2: ![alt text](<Captura de pantalla 2026-04-23 132939.png>)

## Actividad 2: Análisis con Flowgorithm


- **Diagrama:**
  Se implementó un algoritmo de **búsqueda lineal** en Flowgorithm con la siguiente estructura:
  
  **1. Declaración de variables:**
     - `Entero n, meta, i` → Variables para el tamaño, valor a buscar e índice
     - `Booleano encontrado` → Bandera de control (true/false)
     - `Entero Matriz array[5]` → Array de 5 posiciones
  
  **2. Inicialización:**
     - `meta = 3` (valor a buscar)
     - `n = 5` (tamaño del array)
     - `i = 0` (índice inicial)
     - `encontrado = false` (inicialmente no se ha encontrado)
     - Array: `[1, 2, 3, 4, 5]`
  
  **3. Lógica del algoritmo:**
     - **Bucle While:** Condición `i < n AND encontrado == false`
     - **Decisión:** Verifica si `array[i] == meta`
       - **Verdadero:** 
         - Muestra: "Registro encontrado en posición: " + i
         - Establece: `encontrado = true`
       - **Falso:** 
         - Incrementa: `i = i + 1`
     - El bucle se repite hasta encontrar el elemento o recorrer todo el array
  
  **4. Resultado de ejecución:**
     - Buscó el valor `3`
     - Lo encontró en la **posición 2** (array[2] = 3)
     - Iteraciones realizadas: 3 (posiciones 0, 1, 2)

- **Complejidad:** O(n) - En el peor caso requiere recorrer todos los elementos











- Complejidad: O(n)

## Actividad 3: Colas FIFO
- Operaciones

Enqueue (opción 1 - Agregar): Permite ingresar una nueva solicitud al final de la cola

dequeue (opción 2 - Atender): Atiende y elimina la primera solicitud de la cola 

Ver estado (opción 3 - Consultar): Muestra todas las solicitudes actualmente en la cola del orden de atención


 
- Validación FIFO: 
| Paso | Operación | Entrada | Cola Resultante | Tamaño | Verificación |
|------|-----------|---------|-----------------|--------|--------------|
| 1 | Enqueue | depósito | (depósito) | 1 | primer elemento ingresado |
| 2 | Enqueue | Retiro | (depósito, Retiro) | 2 | Segundo elemento |
| 3 | Enqueue | Transferencia | (depósito, Retiro, Transferencia) | 3 | Tercer elemento |
| 4 | Dequeue | - | (Retiro, Transferencia) | 2 | Salió depósito (FIFO) |
| 5 | Dequeue | - | (Transferencia) | 1 | Salió Retiro |
| 6 | Dequeue | - | () | 0 | Salió Transferencia (Cola vacía) |




pruebas: ![alt text](<Captura de pantalla 2026-04-23 135845.png>)
![alt text](<Captura de pantalla 2026-04-23 135956.png>)
![alt text](<Captura de pantalla 2026-04-23 140053.png>)
![alt text](<Captura de pantalla 2026-04-23 140138.png>)
![alt text](<Captura de pantalla 2026-04-23 140152.png>)
![alt text](<Captura de pantalla 2026-04-23 140221.png>)







## Actividad 4: Comparativa
- Resultados:

Tabla comparativa 


| Elemento | posición | Lineal(comp.) | Binaria(comp.) | Mejora |
|----------|----------|---------------|----------------|--------|
| 1002 | 0 | 1 | 3 | sin mejora |
| 3311 | 4 | 5 | 3 | 40% menos |
| 5020 | 6 | 7 | 3 | 57% menos |
| 6081 | 7 | 8 | 4 | 50% menos |
| 9999 | N/A | 8 | 4 | 50% menos |


pruebas:

1002: 

Binaria:![alt text](<Captura de pantalla 2026-04-23 141616.png>)

Lineal: ![alt text](<Captura de pantalla 2026-04-23 141634.png>)


3311: 

Binaria: ![alt text](<Captura de pantalla 2026-04-23 142102.png>)

Lineal: ![alt text](<Captura de pantalla 2026-04-23 142127.png>)


5020: 

Binaria: ![alt text](<Captura de pantalla 2026-04-23 142341.png>)

Lineal: ![alt text](<Captura de pantalla 2026-04-23 142354.png>)

6081:


Binaria: ![alt text](<Captura de pantalla 2026-04-23 142552.png>)

Lineal: ![alt text](<Captura de pantalla 2026-04-23 142611.png>)



9999: 


Binaria: ![alt text](<Captura de pantalla 2026-04-23 142919.png>)

Lineal: ![alt text](<Captura de pantalla 2026-04-23 142944.png>)



Analisis matemático

para n = 8 elementos

Búsqueda Lineal (peor caso): 8 comparaciones
Búsqueda Binaria (peor caso): ⌈log₂(8)⌉ = 3 comparaciones


Para n = 1,000 elementos:

Búsqueda Lineal (peor caso): 1,000 comparaciones
Búsqueda Binaria (peor caso): ⌈log₂(1000)⌉ = 10 comparaciones
Mejora: 99%



- Recomendaciones

- Usar búsqueda lineal para datasets pequeños (<100 elementos)
- Usar búsqueda binaria para datasets grandes (<1,000 elementos)


## Conclusiones y Aprendizajes

Para la complejidad algoritmica no es solamente teoria, impacta en el rendimiento de los algoritmos. La diferencia entre 0(n) y 0(log n) es crítico, con muchos elementos la búsqueda binaria es mucho más eficiente que la lineal y toma menos operaciones, pero para un algoritmo con pocos elementos la lineal es más simple y eficiente en algunos casos

Para la estructura de datos las colas FIFO son fundamentales en sistemas reales ( bancos, impresoras, redes, etc .) donde el orden de llegada determina el orden de atención.

Por último, los diagramas de flujo nos permiten visualizar el comportamiento del algoritmo y contar iteraciones manualmente, siendo una base fundamental e importante para empezar a programar.


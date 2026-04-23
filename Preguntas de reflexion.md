Respuestas preguntas de reflexión
Nivel 1: comprensión
1 . ¿Cuál es la diferencia fundamental entre búsqueda lineal y binaria?

R// La diferencia es que la búsqueda lineal se encarga de comparar cada elemento con el valor ingresado por el usuario, mientras la binaria separa por grupos, dividiendo el espacio de busqueda a la mitad con cada iteración, descartando la mitad que no contiene el elemento.

2.¿Por qué un vector debe estar ordenado para usar búsqueda binaria?

R// Un vector debe estar ordenado para usar búsqueda binaria porque este algoritmo funciona descartando la mitad del espacio de búsqueda en cada iteración. Para saber qué mitad descartar, compara el elemento del medio con el valor buscado. Si el vector está ordenado, puede determinar con certeza si el elemento está en la mitad izquierda o derecha. Sin ordenaimento, no podria saber qué mitad descartar, haciendo imposible el funcionamiento óptimo de este algoritmo.

3.¿Qué significa FIFO y cómo lo experimentas en tu vida cotidiana?

R// FIFO significa "First in, First Out" (Primero en entrar, Primero en salir), es una estructura de datos donde el primer elemento que llega es el primero en ser atendido y los elementos se agregan al final y se eliminan del inicio.

En mi vida cotidiana se experimenta cuando hay fila para pagar algo en un supermercado o en una tienda, el primero que llega es atendido y el que va llegando va atrás en la cola y así sucesivamente.

Nivel 2: Aplicación

4 .Si tuvieras una base de datos de 1 millón de registros, ¿cuál algoritmo recomendarías? ¿Por qué?

R// Recomendaria búsqueda binaria si los datos estan ordenados, con la búsqueda lineal requiere hasta 1 millon de comparaciones en el peor de los casos, con búsqueda binaria solamente rquiere 20 comparaciones log2(1,000,000)=20
Siendo una diferencia abismal, siendo la búsqueda binaria una opción mas eficiente en este caso.

5 .Diseña un escenario donde una cola FIFO sería inapropiada. ¿Qué estructura usarías?

R// Un escenario inapropiado para la cola FIFO seria la sala de mergencias de un hospital, ya que, por ejemplo, si llega alguien con dolor de cabeza primero y luego llega alguien con un problemas respiratorios, se atenderia primero al del dolor de cabeza, lo cual seria inapropiado y pondria en riesgo una vida, siendo peligroso.

La estructura que se usaria seria una cola de prioridad, donde cada paciente recibe una prioridad según la gravedad de su codición. EL paciente con problema respiratorio tendria una prioridad alta y seria atendido primero, sin importar el orden de llegada.

6 .¿Puede fallar la búsqueda binaria en algún caso? Describe.

R// Si, como se mencionó anteriormente si el  vector no está ordenado, la búsqueda binaria puede fallar, descartando incorrectamente la mitad que contiene el elemento, llevando a un resultado erróneo.

Nivel 3: Síntesis

7. Compara el costo de ordenamiento + búsqueda binaria vs búsqueda lineal directa:


a. Dataset pequeño (n=100):
- Ordenar + Binaria: 100 × log₂(100) ≈ 700 operaciones + 7 búsquedas = ~707
- Lineal: 100 operaciones
- Conclusión: Búsqueda lineal es más eficiente (100 < 707)

b. Dataset mediano (n=100,000):
- Ordenar + Binaria: 100,000 × log₂(100,000) ≈ 1,700,000 + 17 = ~1,700,017
- Lineal: 100,000 operaciones
- Conclusión: Depende del número de búsquedas

c. Dataset grande (n=1,000,000):
- Ordenar + Binaria: 1,000,000 × log₂(1,000,000) ≈ 20,000,000 + 20 = ~20,000,020
- Lineal: 1,000,000 operaciones
- Conclusión:
  * 1 búsqueda → Lineal (1,000,000 ops)
  * 20+ búsquedas → Ordenar + Binaria (mucho más eficiente)

8. Propón un algoritmo híbrido que combine búsqueda lineal y binaria:

Algoritmo Híbrido Propuesto: "Búsqueda Adaptativa Lineal-Binaria"

Descripción:
Este algoritmo decide dinámicamente qué técnica usar según el tamaño del dataset y la posición del elemento:

Pseudocódigo:
1. Si n < 50 entonces
2.     Usar búsqueda lineal (más simple para pocos datos)
3. Sino
4.     Si los primeros 10 elementos contienen el valor entonces
5.         Usar búsqueda lineal (elemento cercano al inicio)
6.     Sino
7.         Usar búsqueda binaria (elemento en el resto del vector)
8.     FinSi
9. FinSi


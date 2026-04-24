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
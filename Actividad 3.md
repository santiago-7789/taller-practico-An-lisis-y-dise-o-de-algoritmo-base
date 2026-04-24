Operaciones
Enqueue(opción 1): Agrega una solicitud al final de la cola, aumentando el tamaño y la cola
Dequeue(opcion 2): Atiende la primera solicitud, eliminadola y avanzando en la cola
Ver estado: Muestra todas las solicitudes en orden de atención en la cola




TABLA DE VALIDACION FIFO-ACTIVIDAD 3

| Paso | Operación | Entrada | Cola Resultante | Tamaño | Verificación |
|------|-----------|---------|-----------------|--------|--------------|
| 1 | Enqueue | depósito | (depósito) | 1 | primer elemento ingresado |
| 2 | Enqueue | Retiro | (depósito, Retiro) | 2 | Segundo elemento |
| 3 | Enqueue | Transferencia | (depósito, Retiro, Transferencia) | 3 | Tercer elemento |
| 4 | Dequeue | - | (Retiro, Transferencia) | 2 | Salió depósito (FIFO) |
| 5 | Dequeue | - | (Transferencia) | 1 | Salió Retiro |
| 6 | Dequeue | - | () | 0 | Salió Transferencia (Cola vacía) |







Pruebas: 
![alt text](<Captura de pantalla 2026-04-23 135845.png>)
![alt text](<Captura de pantalla 2026-04-23 135956.png>)
![alt text](<Captura de pantalla 2026-04-23 140053.png>)
![alt text](<Captura de pantalla 2026-04-23 140138.png>)
![alt text](<Captura de pantalla 2026-04-23 140152.png>)
![alt text](<Captura de pantalla 2026-04-23 140221.png>)
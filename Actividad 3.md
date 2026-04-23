Operaciones
Enqueue(opción 1): Agrega una solicitud al final de la cola, aumentando el tamaño y la cola
Dequeue(opcion 2): Atiende la primera solicitud, eliminadola y avanzando en la cola
Ver estado: Muestra todas las solicitudes en orden de atención en la cola




TABLA DE VALIDACION FIFO-ACTIVIDAD 3




Paso      operación        Entrada       cola resultante         tamaño       verificación
 
1         Enqueue          déposito      (déposito)                 1           primer elemento ingresado        
2         Enqueue          Retiro         (depósito,retiro)         2               Segundo elemento
3         Enqueue          Transferencia  (depósito,reti,trans)     3               Tercer elemento
4         Dequeue          ---------      (reti,trans)              2               Salió depósito
5         Dequeue          ---------     (transferencia)            1               Salió retiro 
6         Dequeue          ---------     ---------------            0           Salió transferencia
7         Ver estado       ---------     ---------------            0            La cola está vacia



Pruebas: 
![alt text](<Captura de pantalla 2026-04-23 135845.png>)
![alt text](<Captura de pantalla 2026-04-23 135956.png>)
![alt text](<Captura de pantalla 2026-04-23 140053.png>)
![alt text](<Captura de pantalla 2026-04-23 140138.png>)
![alt text](<Captura de pantalla 2026-04-23 140152.png>)
![alt text](<Captura de pantalla 2026-04-23 140221.png>)
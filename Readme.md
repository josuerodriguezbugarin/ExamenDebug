# Examen de Depuración en PyCharm

---

## **Instrucciones:**

1. Realiza un fork de este repositorio y clónalo.
1. Las respuestas a las preguntas realízalas en este Readme
2. Cada pregunta vale un punto

### Apartado 1

- Coloca un punto de interrupción **normal** en la línea donde se inicializa la lista de la serie: `serie = [0, 1]`. 
- ![punto.png](imagenes/punto.png)
- Inicia el modo *Debug*.
- ![debug.png](imagenes/debug.png)

**Pregunta**

1. Si la función es llamada con `n=10`, ¿cuál es el valor de la variable `n` que se visualiza en la ventana de variables del debugger justo antes de que se ejecute la línea `serie = [0, 1]`?
Justo antes de que se ejecute la línea serie = [0, 1], el debugger muestra que la variable n tiene el valor 10, porque la función se ha llamado como funcion_bucle(10).
![n10.png](imagenes/n10.png)
---

### Apartado 2
![stepout.png](imagenes/stepout.png)

-  Asegúrate de que la llamada a la función es `print(funcion_bucle(10))`.
- ![aa.png](imagenes/aa.png)
-  Inicia el modo *Debug* y avanza hasta que la ejecución se detenga en la línea `siguiente_numero = calcular_siguiente(serie)`.
- ![step over.png](imagenes/step%20over.png)
-  Utiliza la opción de depuración adecuada para **entrar dentro** de la función `calcular_siguiente`.
- hago un step into
![aux.png](imagenes/aux.png)
**Preguntas**

1. Justo cuando el debugger se detiene dentro de la función `calcular_siguiente` por **primera vez**, ¿cuál es el valor que tiene la variable local `aux` *después* de que se ejecute la línea `aux = serie[-1] + serie[-2]`?
**(Indica el valor numérico exacto de la variable `aux` en ese momento y el nombre de la herramienta de *debugging* que utilizaste para entrar en la función).**
El valor de aux es 1, porque serie[-1] = 1 y serie[-2] = 0, así que 1 + 0 = 1.

La herramienta del debugger que utilicé para entrar en la función fue Step Into.
2. Si estuvieras dentro de la función `calcular_siguiente` y quisieras salir rápidamente sin ejecutar el resto de las líneas, volviendo al punto de llamada en `funcion_bucle`, ¿qué función del debugger deberías usar?
Tengo que usar step out.
3. ¿Qué diferencia fundamental existe entre usar *Step Over* y *Step Into* en la línea `siguiente_numero = calcular_siguiente(serie)`?
Step Into entra dentro de la función calcular_siguiente y permite depurar su código línea a línea.
Step Over ejecuta la función completa sin entrar en ella y continúa en la siguiente línea del programa.
---

### Apartado 3

-  Cambia la llamada a la función para que el número de elementos sea mayor: `print(funcion_bucle(1000))`.
- ![1000.png](imagenes/1000.png)
-  Establece un **Breakpoint Condicional** para que la ejecución se detenga solo cuando `siguiente_numero` sea **mayor que 20000**.
![punto2.png](imagenes/punto2.png)
**Pregunta**

1. Cuando el *Breakpoint Condicional* se activa por **primera vez** (la primera vez que `siguiente_numero` es mayor que 20000), ¿qué longitud tiene `serie`?
![importante.png](imagenes/importante.png)

---

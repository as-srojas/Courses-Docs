
# Tipos de Controladores en JMeter

JMeter proporciona varios tipos de controladores que controlan el flujo de ejecución del plan de pruebas. Estos se pueden clasificar en **Controladores Lógicos** y **Muestreadores (Samplers)**.

## 1. **Controlador Simple**

Este controlador simplemente agrupa otros elementos bajo él, organizándolos sin afectar su ejecución.

## 2. **Controlador de Bucle (Loop)**

El Controlador de Bucle ejecuta sus hijos (peticiones) un número especificado de veces o indefinidamente.

- **Configuración**: Especifica cuántas veces ejecutar los elementos hijos.

## 3. **Controlador de Una Sola Vez**

Este controlador asegura que sus elementos hijos se ejecuten solo una vez durante la prueba. Es útil para operaciones como iniciar sesión, donde solo deseas realizar una tarea una vez por usuario.

## 4. **Controlador de Intercalado (Interleave)**

Este controlador ejecuta uno de sus elementos hijos durante cada iteración de su padre. Alterna entre las peticiones, intercalándolas.

## 5. **Controlador Aleatorio**

El Controlador Aleatorio selecciona uno de sus elementos hijos para ejecutarse de manera aleatoria en cada iteración.

## 6. **Controlador de Orden Aleatorio**

Este controlador aleatoriza el orden de ejecución de sus elementos hijos, pero asegura que cada hijo se ejecute una vez por iteración.

## 7. **Controlador de Rendimiento (Throughput)**

El Controlador de Rendimiento te permite controlar con qué frecuencia se ejecutan sus elementos hijos. Puedes establecer un porcentaje o un número absoluto de ejecuciones.

- **Ejecución por Porcentaje**: Solo un porcentaje de las iteraciones incluirá los elementos hijos.
- **Ejecuciones Totales**: Puedes establecer un número fijo de veces que los elementos hijos deben ejecutarse.

## 8. **Controlador If**

El Controlador If ejecuta sus elementos hijos en función del resultado de una condición que defines. Es similar a una instrucción if en programación.

- **Condición**: Puedes usar una variable de JMeter, una función o una expresión para evaluarla.

## 9. **Controlador While**

El Controlador While ejecuta sus elementos hijos repetidamente hasta que una condición se vuelva falsa. La condición se reevalúa antes de cada iteración.

- **Condición**: Al igual que el Controlador If, utiliza expresiones o funciones para determinar si seguir ejecutando.

## 10. **Controlador Switch**

El Controlador Switch ejecuta uno de sus elementos hijos según el valor de una variable o función de JMeter. Es similar a una instrucción switch-case en lenguajes de programación.

## 11. **Controlador ForEach**

Este controlador itera sobre un conjunto de valores relacionados, como los valores de un archivo CSV, y pasa cada valor a sus elementos hijos.

- **Configuración**: Debes definir la variable que almacenará cada valor a medida que avanza el bucle.

## 12. **Controlador de Módulo (Module)**

El Controlador de Módulo te permite reutilizar fragmentos de un plan de prueba haciendo referencia a ellos desde otras partes del plan.

## 13. **Controlador Include**

El Controlador Include inserta fragmentos de un plan de prueba externo en el plan principal. Esto es útil para reutilizar funcionalidades comunes.

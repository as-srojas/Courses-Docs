# TEST CASES
- Entradas
- Pre condiciones
- Post Condiciones
- Salidas

## Técnicas

- Tablas de Partición Equivalente (Equivalent Class Partitioning):

    Esta técnica se utiliza para reducir el número de casos de prueba necesarios para cubrir diferentes situaciones en un rango de entrada. Se divide el conjunto de datos de entrada en clases equivalentes o particiones basadas en propiedades similares. Luego, se seleccionan casos de prueba de cada partición para asegurar una buena cobertura sin necesidad de probar cada valor individual. Esto ayuda a optimizar la cobertura de pruebas mientras se minimiza la duplicación.

- Valores al Límite (Boundary Values):

    Esta técnica se enfoca en probar los valores límite de un rango de entrada. Los errores tienden a ocurrir con mayor frecuencia en los límites de los rangos, por lo que probar valores justo dentro y justo fuera de esos límites es esencial. Por ejemplo, si una función acepta valores entre 1 y 100, se probarían casos en 0, 1, 2, 99, 100 y 101 para asegurarse de que la función se comporte correctamente en los bordes.

- Gráficas de Causa/Efecto (Cause/Effect Graphs):

    También conocidas como gráficos de Ishikawa o diagramas de espina de pescado, estas gráficas ayudan a identificar las posibles causas de un problema y cómo se relacionan entre sí. En el contexto de pruebas, se utilizan para identificar combinaciones específicas de factores que pueden llevar a situaciones de prueba. Esto ayuda a planificar y priorizar los casos de prueba según las interacciones entre los factores.

- Tabla de Decisión Binaria (Binary Decision Tables):

    Estas tablas se utilizan para manejar combinaciones complejas de condiciones y acciones. Son especialmente útiles en sistemas que toman decisiones basadas en múltiples factores. Cada combinación de condiciones y acciones se representa en la tabla, lo que facilita la identificación y diseño de casos de prueba exhaustivos para cada escenario posible.

- Tablas de Decisión Multiple (Multiple Decision Tables):

    Las Tablas de Decisión Múltiple son una extensión de las Tablas de Decisión Binaria. Estas tablas son particularmente útiles cuando se manejan múltiples condiciones y acciones interconectadas en un sistema. En lugar de simplemente evaluar una combinación de condiciones, las Tablas de Decisión Múltiple permiten capturar múltiples condiciones y acciones complejas. Esto es especialmente útil cuando hay dependencias entre diferentes decisiones y se necesita una representación más detallada para la lógica de decisión.

- Pruebas de Transición de Estado (State Transition Test):

1. Diagramas de Transición de Estados

2. Tablas de Transición de Estados

    Las Pruebas de Transición de Estado se utilizan para probar sistemas que tienen estados y transiciones entre esos estados. Estos sistemas se conocen como sistemas de estado finito o máquinas de estado. La idea es diseñar casos de prueba que cubran diferentes transiciones entre los estados y verifiquen el comportamiento del sistema en función de esas transiciones. Esto es particularmente relevante en software que cambia de estado, como aplicaciones interactivas, controladores o sistemas embebidos.

- UI Testing

1. Prueba el estado inicial de cada ventana y menú del sistema

    1.1. Posición del cursor en cada ventana.

    1.2. Habilitar/Deshabilitar estados de control y opciones del menú.

2. Prueba todos los cambios que habilitan e inhabilitan el estado.

3. prueba la secuencia del Tab en cada ventana

4. Prueba la nevegación en toda la aplicación mientras distintos  tipos de ventana están abiertos.

5. Testeo de internacionalización y localización.

6. Prueba para Undo, Redo, drag y drop, navegación BACKWARDs.

7. Prueba todas las líneas del diagrama de navegación.

8. Técnica: Usa una matriz o diagrama de navegación de UI para representar el flujo entre diferentes ventanas y opciones del menú.
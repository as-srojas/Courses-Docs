# Testing Types: Load, Stress, and Endurance

## Load Test

- **Definición**: Evalúa el rendimiento del sistema bajo una carga esperada de usuarios o transacciones.
- **Objetivo**: Verificar que el sistema funcione correctamente bajo condiciones normales de uso.
- **Uso común**:
  - Probar el número máximo de usuarios concurrentes que puede manejar sin errores.
  - Asegurarse de que el tiempo de respuesta y el comportamiento del sistema se mantengan estables bajo cargas predecibles.
- **Resultados esperados**: Buen desempeño bajo condiciones de carga planificada y predefinida.

## Stress Test

- **Definición**: Evalúa el comportamiento del sistema cuando se le somete a una carga que excede la capacidad esperada.
- **Objetivo**: Identificar los puntos de falla, cuellos de botella y la capacidad máxima del sistema.
- **Uso común**:
  - Poner al sistema bajo una carga extrema o inesperada (más usuarios o transacciones de las que puede soportar).
  - Descubrir el comportamiento del sistema bajo condiciones anormales.
- **Resultados esperados**: Detección de fallos, comportamiento bajo carga extrema y la capacidad de recuperación tras una falla.

## Endurance Test

- **Definición**: Evalúa cómo el sistema maneja cargas sostenidas durante largos períodos de tiempo.
- **Objetivo**: Verificar la estabilidad del sistema durante un uso prolongado y asegurarse de que no haya problemas como fugas de memoria o degradación de rendimiento con el tiempo.
- **Uso común**:
  - Simular el uso continuo del sistema durante horas o días.
  - Detectar degradación de rendimiento a largo plazo o fallos que se manifiestan tras un uso prolongado.
- **Resultados esperados**: Estabilidad del sistema y rendimiento constante durante toda la prueba.

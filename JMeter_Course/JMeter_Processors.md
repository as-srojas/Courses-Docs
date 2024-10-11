# Tipos de Pre Processors y Post Processors en JMeter

## Introducción

En JMeter, los Pre Processors y Post Processors son elementos clave que permiten modificar y manipular las solicitudes y las respuestas en los tests de carga y rendimiento. Estos componentes ayudan a preparar las pruebas o a procesar los resultados de manera dinámica. A continuación, exploraremos los principales tipos de Pre Processors y Post Processors en JMeter.

## Pre Processors

Los **Pre Processors** en JMeter se ejecutan antes de que se realice una solicitud, permitiendo modificar o preparar las variables y los datos que se van a enviar. Algunos de los Pre Processors más comunes son:

### 1. **HTTP URL Re-writing Modifier**

Este Pre Processor se utiliza para modificar la URL en las solicitudes HTTP. Es útil para agregar información de sesión en las URLs o para manejar cambios en la estructura de las URLs en las pruebas de rendimiento.

### 2. **User Parameters**

Permite definir parámetros de usuario que se pueden utilizar en diferentes hilos de prueba. Es útil cuando es necesario asignar valores específicos a diferentes usuarios o iteraciones durante la ejecución de la prueba.

### 3. **Regular Expression Extractor**

Este Pre Processor extrae valores específicos de la respuesta de una solicitud anterior utilizando expresiones regulares. Luego, esos valores pueden ser utilizados en solicitudes posteriores.

### 4. **BeanShell PreProcessor**

Permite ejecutar código escrito en BeanShell (un lenguaje similar a Java) antes de que se realice una solicitud. Ofrece una gran flexibilidad, ya que se puede manipular el comportamiento de las pruebas mediante scripting.

### 5. **JSR223 PreProcessor**

Similar al BeanShell PreProcessor, este permite ejecutar código en lenguajes compatibles con JSR223 (como Groovy o JavaScript). Se utiliza para realizar operaciones personalizadas antes de que se envíen las solicitudes.

## Post Processors

Los **Post Processors** se ejecutan después de que se realice una solicitud, y se utilizan para manipular o extraer información de las respuestas recibidas. Algunos de los Post Processors más utilizados son:

### 1. **Regular Expression Extractor**

Se utiliza para extraer valores específicos de la respuesta de una solicitud utilizando expresiones regulares. Este Post Processor es esencial para manejar dinámicamente los datos recibidos y pasarlos a futuras solicitudes.

### 2. **JSON Extractor**

Permite extraer valores de respuestas JSON. Es muy útil para procesar respuestas en formato JSON, ya que facilita la extracción de datos específicos sin necesidad de escribir expresiones regulares complejas.

### 3. **XPath Extractor**

Este Post Processor extrae datos de respuestas en formato XML utilizando expresiones XPath. Es útil cuando se trabaja con servicios que devuelven respuestas en XML.

### 4. **CSS/JQuery Extractor**

Permite extraer datos de respuestas HTML utilizando selectores CSS o JQuery. Este Post Processor es muy útil cuando se necesitan extraer datos de una página web para utilizarlos en futuras solicitudes.

### 5. **Debug PostProcessor**

Este Post Processor permite depurar la información relacionada con las variables y respuestas de las solicitudes. Es útil para obtener detalles adicionales sobre el flujo de ejecución de las pruebas.

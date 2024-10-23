
# Fundamentos del Lenguaje de Programación Ruby

Ruby es un lenguaje de programación interpretado, orientado a objetos y de propósito general, conocido por su simplicidad y flexibilidad. Fue creado por Yukihiro Matsumoto en 1995 y ha ganado popularidad debido a su sintaxis legible y a la comunidad detrás de Rails, un marco de desarrollo web.

## Características principales

1. **Orientado a Objetos**: Todo en Ruby es un objeto, incluyendo números y cadenas.
2. **Sintaxis sencilla y legible**: La sintaxis de Ruby es similar al inglés, lo que facilita su aprendizaje.
3. **Interactividad**: Ruby permite el uso de IRB (Interactive Ruby), que proporciona una consola para ejecutar código Ruby en tiempo real.
4. **Flexible**: Ruby no fuerza paradigmas de programación específicos, como otros lenguajes.
5. **Dinámico**: Ruby utiliza tipado dinámico, lo que significa que no es necesario declarar el tipo de una variable.

## Sintaxis básica

### Variables

No es necesario declarar el tipo de una variable en Ruby.

```ruby
nombre = "Ana"
edad = 25
```

### Estructuras de control

#### Condicionales

```ruby
if edad >= 18
  puts "Eres mayor de edad."
else
  puts "Eres menor de edad."
end
```

#### Bucles

```ruby
for i in 1..5
  puts i
end
```

O con un bucle `while`:

```ruby
i = 0
while i < 5
  puts i
  i += 1
end
```

### Métodos

Los métodos en Ruby se definen con la palabra clave `def`:

```ruby
def saludo(nombre)
  puts "Hola, #{nombre}!"
end

saludo("Ana")
```

### Arreglos

Los arreglos en Ruby pueden almacenar múltiples valores.

```ruby
nombres = ["Ana", "Juan", "Pedro"]
nombres.each do |nombre|
  puts nombre
end
```

## Tipos de Datos

1. **Números**: Tanto enteros como decimales (flotantes) son soportados.
2. **Cadenas**: Manipulación de texto.
3. **Símbolos**: Son inmutables y generalmente usados como identificadores.
4. **Booleanos**: `true` y `false`.
5. **Arreglos y Hashes**: Estructuras para almacenar colecciones de datos.

## Manejo de excepciones

```ruby
begin
  # Código propenso a error
  resultado = 10 / 0
rescue ZeroDivisionError
  puts "No se puede dividir por cero."
end
```

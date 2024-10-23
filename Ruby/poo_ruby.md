# Clases y Objetos en Ruby

Una clase es una plantilla para crear objetos (instancias). En Ruby, una clase se define con la palabra clave `class`.

```ruby
class Persona
  def initialize(nombre, edad)
    @nombre = nombre
    @edad = edad
  end

  def presentarse
    puts "Hola, me llamo #{@nombre} y tengo #{@edad} años."
  end
end

# Crear una instancia de la clase Persona
persona1 = Persona.new("Ana", 25)
persona1.presentarse
```

## Atributos de instancia

En Ruby, las variables de instancia se definen con el prefijo `@`. Estos valores son específicos para cada instancia de la clase.

### Métodos de acceso

Ruby permite la creación de métodos para acceder y modificar los atributos de instancia mediante `attr_accessor`, `attr_reader`, y `attr_writer`.

```ruby
class Persona
  attr_accessor :nombre, :edad
end

persona1.nombre = "Juan"
puts persona1.nombre  # Juan
```

## Herencia

Ruby permite la herencia mediante el uso del símbolo `<`, que indica que una clase hereda de otra.

```ruby
class Empleado < Persona
  def initialize(nombre, edad, puesto)
    super(nombre, edad)  # Llamar al constructor de la clase padre
    @puesto = puesto
  end

  def presentarse
    super  # Llamar al método de la clase padre
    puts "Y soy un #{@puesto}."
  end
end

empleado1 = Empleado.new("Ana", 25, "Ingeniera")
empleado1.presentarse
```

## Polimorfismo

El polimorfismo en Ruby se logra al permitir que diferentes clases respondan a los mismos métodos de diferentes maneras.

```ruby
class Gato
  def hablar
    puts "Miau!"
  end
end

class Perro
  def hablar
    puts "Guau!"
  end
end

animales = [Gato.new, Perro.new]
animales.each { |animal| animal.hablar }
```

## Módulos

Los módulos son una forma de compartir métodos entre clases. Se utilizan para evitar la herencia múltiple.

```ruby
module Caminante
  def caminar
    puts "Estoy caminando."
  end
end

class Persona
  include Caminante
end

persona = Persona.new
persona.caminar
```

# Dart Cheat-Sheet


Dart es un lenguaje de programación desarrollado por Google, utilizado para crear aplicaciones web, móviles y de servidor. 

Esta una cheat-sheet de Dart de referencia rápida:

**1.  Comentarios**

```dart
// Comentario de una línea
/* Comentario
   de varias líneas */` 
```

**2.  Variables y Tipos de Datos**


```dart
// Declaración de variables
var variable;
int entero = 42;
double decimal = 3.14;
String texto = 'Hola, Dart';
bool verdaderoFalso = true;
List<int> lista = [1, 2, 3];

// Map: Representa una colección de pares clave-valor.
Map<String, int> mapa = {'uno': 1, 'dos': 2, 'tres': 3};

// Num: Es una clase de la que heredan `int` y `double`. Se puede utilizar // para representar cualquier tipo de número.
num numero = 3.14;

// dynamic: Representa cualquier tipo de dato. 
// Si no se especifica el tipo de variable, Dart asume que es de tipo 
// `dynamic`. Sin embargo, es recomendable ser explícito con los 
// tipos de datos.
dynamic variable = 'Texto';
variable = 5;

// Constantes y finales
const pi = 3.141592;

// final: Indica que una variable solo puede ser asignada una vez
// y no se puede cambiar después de su asignación. 
// Dart también infiere automáticamente el tipo de dato.
final fechaActual = DateTime.now();
```

**3.  Estructuras de control**

```dart 
// If-Else
if (condicion) {
  // Código si es verdadero
} else {
  // Código si es falso
}

// Switch
switch (variable) {
  case valor1:
    // Código si es valor1
    break;
  case valor2:
    // Código si es valor2
    break;
  default:
    // Código si no coincide con ningún caso
}

// For loop
for (int i = 0; i < 10; i++) {
  // Código a ejecutar
}

// While loop
while (condicion) {
  // Código a ejecutar
}

// Do-While loop
do {
  // Código a ejecutar
} while (condicion);
```

**4.  Colecciones**

```dart
// Listas
List<int> numeros = [1, 2, 3, 4, 5];
List<String> palabras = ['uno', 'dos', 'tres'];

// Mapas
Map<String, int> mapa = {'clave1': 1, 'clave2': 2, 'clave3': 3};

// Conjuntos
Set<String> conjunto = {'valor1', 'valor2', 'valor3'};
```

**5.  Funciones**

```dart
// Función simple
void saludo() {
  print('Hola, Dart');
}

// Función con parámetros y retorno
int suma(int a, int b) {
  return a + b;
}

// Función de flecha
bool esPar(int numero) => numero % 2 == 0;
```

**6.  Clases y Objetos**


```dart
class Persona {
  String nombre;
  int edad;

  // Constructor
  Persona(this.nombre, this.edad);

  // Método
  void presentarse() {
    print('Hola, mi nombre es $nombre y tengo $edad años');
  }
}

void main() {
  // Instanciar un objeto
  var persona = Persona('Juan', 30);
  persona.presentarse();
} 
```

**7.  Herencia y Polimorfismo**



```dart
class Empleado extends Persona {
  String puesto;

  // Constructor
  Empleado(String nombre, int edad, this.puesto) : super(nombre, edad);

  // Sobreescribir método
  @override
  void presentarse() {
    print('Hola, mi nombre es $nombre, tengo $edad años y trabajo como $puesto');
  }
}
```

**8.  Mixins**
Los mixins son una forma de reutilizar el código de una clase en múltiples jerarquías de herencia. 
En lugar de extender de una clase base, un mixin te permite "mezclar" el código de una o más clases en tu clase actual. 
Esto proporciona una alternativa flexible a la herencia única, lo que permite que las clases hereden comportamientos y propiedades de múltiples fuentes.

Un mixin se define usando la palabra clave mixin en lugar de class. Los mixins pueden implementar otros mixins o interfaces, pero no pueden tener constructores. 
Para usar un mixin en una clase, usa la palabra clave with seguida del nombre del mixin.


```
mixin Saludable {
  void mantenerseSaludable() {
    print('Realizar ejercicio y mantener una dieta balanceada');
  }
}

class Atleta extends Persona with Saludable {
  // ...Código de la clase...
}
```

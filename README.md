# Extendiendo-clases

Extendiendo Clases:

En TypeScript, puedes crear una nueva clase que herede propiedades y métodos de una clase existente utilizando la palabra clave `extends`. Esto te permite extender la funcionalidad de una clase base y reutilizar código.

Aquí tienes un ejemplo de cómo extender una clase en TypeScript:

```typescript
class Animal {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  speak() {
    console.log("The animal makes a sound.");
  }
}

class Dog extends Animal {
  breed: string;

  constructor(name: string, breed: string) {
    super(name);
    this.breed = breed;
  }

  speak() {
    console.log("The dog barks.");
  }
}

const myDog = new Dog("Max", "Labrador");
console.log(myDog.name); // Max
console.log(myDog.breed); // Labrador
myDog.speak(); // The dog barks.
```

En este ejemplo, hemos creado una clase `Animal` con una propiedad `name` y un método `speak`. Luego, creamos una clase `Dog` que extiende la clase `Animal`. La clase `Dog` agrega una propiedad `breed` y redefine el método `speak` para que el perro ladre en lugar de hacer el sonido genérico del animal.

2. Creando Clases Abstractas:
En TypeScript, una clase abstracta es una clase que no se puede instanciar directamente, pero puede ser utilizada como clase base para otras clases. Una clase abstracta puede contener métodos abstractos, que son métodos que no tienen implementación en la clase abstracta pero deben ser implementados en las clases derivadas.

Aquí tienes un ejemplo de cómo crear una clase abstracta en TypeScript:

```typescript
abstract class Shape {
  abstract getArea(): number;
}

class Square extends Shape {
  sideLength: number;

  constructor(sideLength: number) {
    super();
    this.sideLength = sideLength;
  }

  getArea(): number {
    return this.sideLength ** 2;
  }
}

const mySquare = new Square(5);
console.log(mySquare.getArea()); // 25
```

En este ejemplo, hemos creado una clase abstracta `Shape` con un método abstracto `getArea`. Luego, creamos una clase `Square` que extiende la clase `Shape` y proporciona una implementación para el método `getArea`. La clase `Square` se puede instanciar y llamar al método `getArea` para calcular el área del cuadrado.

Las clases abstractas son útiles cuando deseas definir una estructura común y asegurarte de que las clases derivadas implementen ciertos métodos o comportamientos.

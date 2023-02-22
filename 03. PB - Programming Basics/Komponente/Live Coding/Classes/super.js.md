`super` in einer JavaScript-Klasse bezieht sich auf die übergeordnete Klasse, die mit dem `extends`-Schlüsselwort erweitert wurde. Es ermöglicht den Zugriff auf die Methoden und Eigenschaften der übergeordneten Klasse.

Hier ist ein Beispiel, das `super` verwendet, um die Methode der übergeordneten Klasse aufzurufen:

```JS
class Animal {
  constructor(name) {
    this.name = name;
  }

  sayHello() {
    return `Hello, I'm ${this.name}`;
  }
}

class Dog extends Animal {
    constructor(name, breed) {
        super(name);
        this.breed = breed;
    }

    sayHelloExtended() {
        return `${super.sayHello()}, I'm a ${this.breed}.`;
    }

    bark() {
        return `Woof! Woof!`;
    }
}

const myDog = new Dog("Rufus", "Golden Retriever");

console.log(myDog.sayHello());
console.log(myDog.sayHelloExtended());
console.log(myDog.bark());
```

In diesem Beispiel erweitert die `Dog`-Klasse die `Animal`-Klasse. Wenn wir eine Instanz der `Dog`-Klasse erstellen, wird zuerst der Konstruktor der übergeordneten Klasse aufgerufen (`super(name)`), um den Namen des Tieres zu setzen. Anschließend wird dann der Konstruktor der `Dog`-Klasse aufgerufen, um die Rasse zu setzen.

In der `sayHelloExtended`-Methode der `Dog`-Klasse wird `super.sayHello()` aufgerufen, um die gleichnamige Methode der `Animal`-Klasse aufzurufen und dann den Rückgabewert anzupassen, um auch die Rasse des Hundes anzugeben.

Darüber hinaus haben wir die Methode `bark` hinzugefügt, welche nur einer Instanz aus der Klasse `Dog` zur Verfügung steht.

Hier ist ein weiteres Beispiel in dem wir eine Unter-Klasse `Cat` aus der Klasse `Animal` erstellen:

```JS
class Cat extends Animal {
    constructor(name, breed) {
        super(name);
        this.breed = breed;
    }

    meow() {
        return `Meow! Gib mir Essen mein Sklave!`;
    }

    getBreed() {
        return this.breed;
    }
}

const simba = new Cat("Simba", "Mainecoon");

console.log(simba.meow());
console.log(simba.getBreed());
console.log(simba.sayHello());
```

Dieser Code definiert eine `Cat` Klasse, die von der `Animal` Klasse erbt und hat einen Konstruktor, der den Namen und die Rasse der Katze als Parameter erhält. Die Methoden `meow()` und `getBreed()` geben eine Zeichenkette mit dem Klang, den Katzen normalerweise machen, und die Rasse der Katze zurück, die im Konstruktor festgelegt wurde. Die Variable `simba` wird erstellt, indem ein neues `Cat`-Objekt mit den Werten `Simba` als Name und `Mainecoon` als Rasse erstellt wird. Dann wird `meow()` und `getBreed()` aufgerufen, um die entsprechenden Informationen auszugeben. Der letzte Aufruf `console.log(simba.sayHello());` wird fehlschlagen, da die Methode `sayHello()` nicht in der Klasse definiert wurde.


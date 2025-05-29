# **NLG - Developer Applicatie**

---

### :pushpin: Voor wie: Onervaren developers

Hey,

Leuk dat je interesse hebt in developen bij NLG! :computer: Hier krijg je een korte opdracht om mee te beginnen. Je hoeft nog niks te kunnen — we leggen alles stap voor stap uit. Ik verwacht screenshots in mijn DM over een week! :smile:

Veel plezier! :muscle:

– Rebecca // Ragbecca
- Marten // Marten_mrfcyt

_En onthoud: fouten maken hoort erbij!_ :sunglasses:

---

## :white_check_mark: Opdracht 1: Hello World

1. **Download IntelliJ IDEA (Community Edition)**
:point_right: [Download hier](https://www.jetbrains.com/idea/download/?section=windows)

2. **Maak een Java-project aan**
:point_right: [Volg deze stappen](https://www.jetbrains.com/help/idea/creating-and-running-your-first-java-application.html#get-started)

> Zet "Add Sample Code" **uit** tijdens het maken!

3. **Zorg dat je een JDK installeert** als je dat nog niet hebt.

---

### :brain: Uitleg over Java

**Wat is een class?**
> Een class is een soort container voor code. Bijvoorbeeld: `FruitTypes` kan een class zijn waarin je fruitsoorten opslaat.

**Wat is de `main`-methode?**
> De motor van je programma. Alles start vanuit hier.

```java
public class HelloWorld {
    public static void main(String[] args) {
        HelloWorld plugin = new HelloWorld();
    }
}
```

**Wat betekent alles in `public static void main(String[] args)`?**

- `public` = iedereen mag deze functie gebruiken
- `static` = je hoeft geen object aan te maken om het te gebruiken
- `void` = het geeft niks terug
- `main` = de naam van de methode
- `String[] args` = een array van strings (gegevenslijstje)

**Voorbeeld array:**

```java
public class HelloWorld {
    public static void main(String[] args) {
        String[] fruits = {"banana", "orange", "lemon"};
        System.out.println(fruits[0]); // banana
    }
}
```

### :sparkles: Jouw opdracht:
- Maak een grote `String[]` array (geen fruit)
- Print de eerste waarde
- Print de laatste waarde (zonder expliciet indexnummer)
- Kies een thema

---

## :rocket: Opdracht 2 (niet verplicht)

Je leert nu extra over objecten, functies, beveiliging, arrays en nog veel meer!

### :sponge: Limitatie van Arrays

Arrays kunnen niet groter worden:

```java
public static void main(String[] args) {
    String[] fruits = {"banana", "orange", "apple"};
    fruits[0] = "pear";
    System.out.println(fruits[0]); // pear
    // fruits[3] = "kiwi"; // ERROR: Index out of bounds!
}
```

### :electric_plug: Wat is een package?
> Een soort gereedschapskist voor Java. Sommige dingen zoals `String` hoef je niet te importeren, andere wel.

**Een compiler zet je code om naar iets wat de computer snapt.**

### :bricks: Interface + Implementatie

```java
interface Fruit {
    String name = "Fruit";
    void showName();
}

class Apple implements Fruit {
    @Override
    public void showName() {
        System.out.println(name);
    }
}
```

:arrow_right: Met `@Override` pas je een methode aan.  
:arrow_right: `implements` geeft aan dat je een interface gebruikt.

---

## :books: Wat is een `List`?

Een List is als een array, maar dan flexibel.

```java
import java.util.List;
import java.util.ArrayList;

public class HelloWorld {
    public static void main(String[] args) {
        List<String> lijst = new ArrayList<>();
        lijst.add("hallo");
        lijst.remove(0);
    }
}
```

:arrow_right: `new` betekent dat je een nieuw object maakt en geheugen reserveert  
:arrow_right: `<String>` geeft aan wat voor type data de lijst bevat

> Alternatief:
```java
List<String> lijst = List.of("hallo", "wereld");
```
Let op: deze is niet aanpasbaar!

### :blue_book: Meer info:
:point_right: [ArrayList JavaDoc](https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html)

---

### :sparkles: Opdracht 2 Taken:

- Leg uit wat een `int` is
- Noem andere datatypes
- Maak een lijst (zelfde thema als opdracht 1)
- Print eerste en laatste waarde van de lijst
- Maak de lijst leeg, print de lengte (moet 0 zijn)
